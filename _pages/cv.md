---
layout: page
permalink: /cv/
title: CV
nav: true
nav_order: 4
---

<p class="cv-download">
  <a class="btn" href="{{ '/assets/pdf/cv_english.pdf' | relative_url }}" target="_blank" rel="noopener"
    ><i class="fa-solid fa-file-pdf"></i> Download PDF</a
  >
</p>

<!-- Pages are drawn with PDF.js so the CV shows even when the browser is set to download PDFs. -->
<div id="cv-pdf" class="cv-pdf" data-src="{{ '/assets/pdf/cv_english.pdf' | relative_url }}"></div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js"></script>
<script>
  (function () {
    var container = document.getElementById("cv-pdf");
    pdfjsLib.GlobalWorkerOptions.workerSrc = "https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.worker.min.js";

    function render(pdf) {
      container.innerHTML = "";
      var scale = Math.min(window.devicePixelRatio || 1, 2) * 2;
      var chain = Promise.resolve();
      for (var n = 1; n <= pdf.numPages; n++) {
        chain = chain.then(
          (function (pageNumber) {
            return function () {
              return pdf.getPage(pageNumber).then(function (page) {
                var viewport = page.getViewport({ scale: scale });
                var canvas = document.createElement("canvas");
                canvas.className = "cv-pdf-page";
                canvas.width = viewport.width;
                canvas.height = viewport.height;
                container.appendChild(canvas);
                return page.render({ canvasContext: canvas.getContext("2d"), viewport: viewport }).promise;
              });
            };
          })(n),
        );
      }
    }

    pdfjsLib
      .getDocument(container.dataset.src)
      .promise.then(render)
      .catch(function () {
        container.textContent = "The CV could not be displayed here. Use the Download PDF button above.";
      });
  })();
</script>

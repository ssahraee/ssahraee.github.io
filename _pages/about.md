---
layout: about
title: about
permalink: /
subtitle: PhD student in cryptography at <a href='https://www.lirmm.fr/'>LIRMM</a>, Montpellier.

profile:
  align: left
  more_info: >
    <p>LIRMM</p>
    <p>Montpellier, France</p>
    <p>sara.sahraee [at] lirmm [dot] fr</p>

selected_papers: false # set to true to list papers marked as "selected={true}"
social: false # set to true once you add links in _data/socials.yml

announcements:
  enabled: false # includes a list of news items

latest_posts:
  enabled: false
---

## Bio

I am a PhD student in cryptography at the Laboratoire d'Informatique, de Robotique et de Microélectronique de Montpellier ([LIRMM](https://www.lirmm.fr/)), supervised by Loïc Masure.

Before my PhD, I completed a Master's degree in Cryptology and Cybersecurity at the University of Bordeaux, during which I spent four months as a cryptography research intern at [PQShield](https://pqshield.com/), supervised by Thomas Espitau. I also hold a BSc in Mathematics with French from the University of Manchester.

## Research

My PhD thesis is titled _Security Proofs of Masking against Side-Channel Attacks in the Noisy Leakage Model_.

My research focuses on security proofs for masking. In particular, I work on:

- the noisy-leakage, random-probing and _t_-probing models
- tight reductions between these models
- composition of masked gadgets

<!-- Temporary font picker: remove once a font pairing is chosen. -->
<div id="font-picker" style="position: fixed; bottom: 4.5rem; left: 1rem; z-index: 1000; padding: 0.6rem 0.8rem; border-radius: 0.75rem; background: var(--global-card-bg-color); border: 1px solid var(--global-divider-color); box-shadow: 0 6px 20px rgba(0, 0, 0, 0.12); font-size: 0.85rem;">
  <label for="font-select" style="display: block; margin-bottom: 0.3rem; font-weight: 600;">Try a font pairing</label>
  <select id="font-select" style="padding: 0.2rem 0.4rem; border-radius: 0.4rem;">
    <option value='"Fraunces", Georgia, serif|"Nunito Sans", sans-serif'>1. Fraunces + Nunito Sans</option>
    <option value='"Lora", Georgia, serif|"Source Sans 3", sans-serif'>2. Lora + Source Sans 3</option>
    <option value='"Cormorant Garamond", Georgia, serif|"Lato", sans-serif'>3. Cormorant Garamond + Lato</option>
    <option value='"DM Serif Display", Georgia, serif|"DM Sans", sans-serif'>4. DM Serif Display + DM Sans</option>
    <option value='"Libre Baskerville", Georgia, serif|"Karla", sans-serif'>5. Libre Baskerville + Karla</option>
    <option value='"Nunito", sans-serif|"Nunito", sans-serif'>6. Nunito (rounded, all text)</option>
    <option value='"Lora", Georgia, serif|"Lora", Georgia, serif'>7. Lora (serif, all text)</option>
  </select>
</div>
<script>
  (function () {
    var select = document.getElementById("font-select");
    function apply(value) {
      var parts = value.split("|");
      document.documentElement.style.setProperty("--font-heading", parts[0]);
      document.documentElement.style.setProperty("--font-body", parts[1]);
    }
    select.addEventListener("change", function () {
      apply(select.value);
    });
  })();
</script>

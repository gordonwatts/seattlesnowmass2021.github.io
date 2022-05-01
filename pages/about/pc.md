---
permalink: /about/pc/
title: Program Committee
---

# Program Committee

<br/>
Please feel free to contact anyone you would like to discuss the program.
<br/>

<div class="container-fluid">
  <div class="row" style="display: flex; flex-wrap: wrap">
  {% for member in site.data.orgs.pc.personnel  %}
       {% assign person = site.data.people[member] %}
       {% include standard_person_card.md %}
  {% endfor %}
  </div>
</div>
<br/>

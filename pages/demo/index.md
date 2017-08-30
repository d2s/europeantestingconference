---
permalink: /demo/
year: demo
layout: index-2018
---

{% capture sections_path %}{{ page.permalink }}sections/{% endcapture %}

{% for page in site.pages %}
{% if page.path contains sections_path %}
<section id="etc_2018_{{ page.about }}"  class="b-section b-section_{{ page.section_type }}">
  <h3 class="b-section__title">{{ page.title }}</h3>
  <div class="b-{{ page.type }}">
       {{ page.content | markdownify }}
  </div>
</section>
{% endif %}
{% endfor %}
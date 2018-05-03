---
permalink: /2019/
year: 2019
layout: index-2019
---

{% capture sections_path %}{{ page.permalink }}sections/{% endcapture %}

{% for page in site.pages %}
{% if page.path contains sections_path %}
<section id="etc_2019_{{ page.about }}"  class="b-section b-section_{{ page.section_type }}">
    {% if page.title %}
    <h3 class="b-section__title">{{ page.title }}</h3>
    {% endif %} 
  <div class="b-{{ page.type }}">
       {{ page.content | markdownify }}
  </div>
</section>
{% endif %}
{% endfor %}
---
subtitle: No homepage, yet.
date: 2018-08-22 12:24:50
layout: layouts/page.njk
is_index: true
---

{% render '@vf-intro', {"vf_intro_phase": "alpha", "vf_intro_heading": siteConfig.siteInformation.title,
  "vf_intro_lede": siteConfig.siteInformation.short_description,
  "vf_intro_text": [
    "You can use this configuration add and create VF components and component libraries."
  ]
} %}



<section class="vf-intro | embl-grid embl-grid--has-centered-content">
<div>
  <!-- empty -->
</div>
<div class="vf-content">

## What you get

- a highly componentised structure for your design system and documentation
- a documentation site powered by the [Eleventy](https://www.11ty.io) static site generator and [Fractal component library](https://fractal.build/)
- access to the [Visual Framework](https://visual-framework.github.io/vf-welcome/) component system
- a [/components]({{'/components' | url}}) url to document and demonstrate all components available

</div>
</section>

<section class="embl-grid embl-grid--has-centered-content">
  <div></div>
  <div class="vf-content">
    {# show all pages classes as sections #}
    {%- for section in collections.sections  %}
      {% if section.data.is_index ==  true %}
        {% set absolutePostUrl %}{{ metadata.id }}{{ section.url }}{% endset %}

## [{{ section.data.title }}]({{ absolutePostUrl | url }})

{{ section.data.subtitle }}

      {% endif %}
    {%- endfor %}
  </div>
</section>

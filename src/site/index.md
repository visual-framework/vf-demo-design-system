---
subtitle: No homepage, yet.
date: 2018-08-22 12:24:50
layout: layouts/base.njk
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
- a documentation site powered by the [Eleventy](https://www.11ty.io) static site generator
- access to the Visual Framework component system
- a [/components]({{'/components' | url}}) url to document and demonstrate all components available

## Adding components

After adding a component, rerun `gulp dev` to ensure it's fully detected by the environment.

### Installation from npm

To add a component from `vf-core` (or other sources) you can use Yarn:

- installation: `yarn add @visual-framework/vf-logo`
- updating: `yarn upgrade-interactive --latest`

### Manual installation for customisation

1. Download a pattern
2. Copy it to `./src/components/vf-component-name`

### Add your own local component

You can add a custom VF-compatible component to `./src/components` and use it in
your site.

- `gulp vf-component`

You'll find a `vf-sample` component there, we've used it below:

<pre><code>{%- verbatim %}Code: {% render "@vf-sample", {text: "with some text"} %}{% endverbatim %}

Returns: {% render "@vf-sample", {text: "with some text"}, false, { escape: false, beautify: true, highlight: true } %}
</code></pre>

</div>
</section>

---
title: Spacing
section: styles
tags: posts
layout: layouts/post.njk
---

<style>
.swatches {
    grid-row-gap: 32px;
}
.swatch {
  border: 2px solid #333;
}
.swatch__details {
  padding: 16px;
}
.spacing__example {
  border-bottom: 2px solid #333;
  background-color: #f3f3f3;
  display: flex;
  width: 100%;
  height: 200px;
  justify-content: center;
  align-items: center;
}
</style>
<main class="swatches | vf-grid vf-grid__col-4">
{% for item in styles.spacing.properties %}

<article class="swatch">
  <div class="spacing__example">
    <item class="spacing" style="height: {{ item.value }}; width: {{ item.value }}; background: #009f4d;"></item>
  </div>
  <section class="swatch__details">
  <h3 class="swatch__colour-name">{{ item.meta.friendlyName }}</h3>
  <p class="swatch__colour-hex"><span class="swatch__meta">Value: </span>{{ item.value }}</p>
  {% if item.meta.sassVariable %}
  <p class="swatch__sass-variable"><span class="swatch__meta">Sass Variable: </span>{{ item.meta.sassVariable }}</p>
  {% endif %}
  {% if item.meta.CSSCustomProperty %}
  <p class="swatch__css-property"><span class="swatch__meta">CSS: </span>{{ item.meta.CSSCustomProperty }}</p>
  {% endif %}
  {% if item.meta.comment %}
  <h4 class="swatch__notes">notes:</h4>
  <p class="swatch__comment">{{ item.meta.comment }}</p>
  {% endif %}
  </section>
</article>

{% else %}

<p>bugger</p>

{% endfor %}
</main>

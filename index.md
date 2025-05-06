---
layout: default
---

<div class="home">
  <head>
      <title>{{ site.title }}</title>
  </head>
  {%- if site.apps.size > 0 -%}
  <ul class="post-list">
      {% for app in site.apps  %}
      <li>
          <a class="black-link post-link-layout" href="{{ app.url | relative_url }}">
            {{ app.title | escape }}
          </a>
      </li>
      {% endfor %}
  </ul>
  {%- endif -%}
</div>

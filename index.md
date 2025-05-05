---
layout: default
---

<div class="home">
  <head>
      <title>{{ site.title }}</title>
  </head>
  {%- if site.articles.size > 0 -%}
  <ul class="post-list">
      {% for article in site.articles  %}
      <li>
          <a class="black-link post-link-layout" href="{{ article.url | relative_url }}">
            {{ article.title | escape }}
          </a>
      </li>
      {% endfor %}
  </ul>
  {%- endif -%}
</div>

---
layout: default
---

<article class="app-content-container" itemscope itemtype="https://schema.org/ItemList">
    <head>
        <title>{{ site.title }}</title>
    </head>
    {%- if site.apps.size > 0 -%}
    <div class="apps-list">
        <ul >
            {% for app in site.apps %}
                {% if jekyll.environment == "development" or app.app != "test" %}
                <li>
                    <a class="black-link" href="{{ app.url | relative_url }}">
                        {%- include app_brand.html logo=app.logo title=app.title -%}
                    </a>
                </li>
                {% endif %}
            {% endfor %}
        </ul>
    </div>
    {%- endif -%}
</article>
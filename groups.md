---
layout: default
---

{%- assign page_paths = site.pages | map: "path" -%}

<header class="post-header">
Groups
</header>

<div class="post-content">
    <ul>
    {%- for path in page_paths -%}
        {%- assign my_page = site.pages | where: "path", path | first -%}
        {%- if my_page.title and my_page.path contains 'groups' -%}
        <li><a class="page-link" href="{{ my_page.url | relative_url }}">{{ my_page.title | escape }}</a></li>
        {%- endif -%}
    {%- endfor -%}
    </ul>
</div>

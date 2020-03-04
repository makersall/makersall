---
layout: default
title:  Drafts
permalink: /drafts/
---
<h1> Drafts</h1>

<p> Here's a list of the files in the pages/drafts folder:</p>

<div class="post-content">
  {%- for draft in site.pages -%} 
    {% if draft.path contains 'pages/drafts' %}
      <p><a href="{{ draft.url | relative_url }}"> {{ draft.title | escape }} </a><br/>({{ draft.path}})</p>
    {% endif %}
  {%- endfor -%}
 </div> 


---
layout: default
title:  Blog
permalink: /blog/
---

<article class="post">

  <header class="post-header">
    <h1 class="post-title">{{ page.title | escape }}</h1>
  </header>
  {%- if page.image -%}
  <div class="main-image">
    <img src="{{'/assets/images/' | append:  page.image | relative_url }} ">
    {%- if page.image-citation -%}
      <div class="main-image-citation">{{ page.image-citation }} </div>
    {%- endif -%}

  </div>  
  {%- endif -%}

  <div class="post-content">

    {%- for post in site.posts -%}
      <h3> <a class="post-link" href="{{ post.url | relative_url }}"> {{ post.title | escape }} </a> </h3>
      <div class="content"> {{ post.content }} </div>
      {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
      <span class="post-meta">{{ post.date | date: date_format }} - {{ post.author }}</span>
    {%- endfor -%}

    <p> </p>
    <hr/>
    <p> </p>


    <p> For archived blog posts, please visit the  <a href="https://makersall.wordpress.com/">old Makers All site</a></p>

    <p class="feed-subscribe">
      <a href="{{ 'feed.xml' | relative_url }}">
        <svg class="svg-icon orange"><use xlink:href="{{ 'assets/minima-social-icons.svg#rss' | relative_url }}"></use></svg><span>Subscribe</span>
      </a>
    </p>

 </div>

</article>

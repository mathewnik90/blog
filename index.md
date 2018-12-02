---
layout: default
title: home
---

## Latest blog
<div class="blog-index">  
  {% assign post = site.posts.first %}
  {% assign content = post.content %}
  {% include post_detail.html %}
</div>

### Recent posts
{% for post in site.posts offset:1 limit:2 %}
<div class="recent">
    <a href="{{ site.baseurl }}{{ post.url }}">
                    <div class="rel">
                        <div class="post-title">{{ post.title }}</div>
                        <span class="post-excerpt">{{ post.excerpt }}</span>
                        <span class="post-date">{{post.date | date: "%B %-d, %Y"}}</span>
                    </div>
    </a>
</div>  
{% endfor %}
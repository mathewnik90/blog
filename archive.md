---
layout: default
title: Archive
---

# All posts

<section class="archive-posts">

   {% for post in site.posts %}
       {% assign currentDate = post.date | date: "%Y" %}
       {% if currentDate != prevDate %}
           {% unless forloop.first %}</ul>{% endunless %}
           <h2>{{ currentDate }}</h2>
           <ul>
           {% assign prevDate = currentDate %}
       {% endif %}
       <li class="archive-urls">
        <a href="{{ post.url }}"><span>{{ post.date | date: "%B %-d, %Y" }}</span> - {{ post.title }}</a> 

        {% if post.tags %}
        {% assign sorted_tags = post.tags | sort %}
        {% for tag in sorted_tags %}
        <span class="tag">{{tag}}</span>
        {% endfor %}
        {% endif %}

       </li>

       {% if forloop.last %}</ul>{% endif %}
   {% endfor %}

</section>


---
layout: page
title: Programming Notes
tagline: Supporting tagline
---
{% include JB/setup %}


## About
--

    blog_func = lambda thoughts: markdown(thoughts)
    map(blog_func, ['java', 'python', 'objective-c'])

###文章列表
--
<ul >
    {% for post in site.posts limit 4 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
        {{ post.content | strip_html | truncatewords:75}}<br>
            <a href="{{ post.url }}">Read more...</a><br><br>
    {% endfor %}
</ul>

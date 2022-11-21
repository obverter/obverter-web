---
layout: page
author: Ben Tyler Elliott
title: Topics
---

<!-- @format -->

<h1 class="content-listing-header sans">Topics</h1>

{% for tag in site.tags %} {% if tag[0] != "index" %}

<h3 class="topic" id="{{ tag[0] }}">{{ tag[0] }} ¬</h3>
<div class="topic-list">
    <ul>
{% for post in tag[1] %}
        <small>
            <a href="{{ post.url }}">{{ post.title }}</a>
            <br/>
            <small>{{ post.date | date: '%b %w, %Y'}}</small>
            <br></small>
{% endfor %}
        </ul>
    </div>
{% endif %} {% endfor %}

---
layout: page
title: Blog
permalink: /blog/
---
<h1>Categories</h1>

{% for category in site.categories %}<a href="{{base_url}}/categories/{{ category | first}}/">{{ category | first }}</a>{% unless forloop.last %}, {% endunless %}{% endfor %}

<h1>Tags</h1>
<div class="tagcloud">
{% for tag in site.tags %}

    <li style="font-size: {{ tag | last | size | times: 100 | divided_by: site.tags.size| plus: 70 }}%">
        <a href="{{base_url}}/tags/{{ tag | first }}/">
            {{ tag | first }}
        </a>

    </li>
{% endfor %}
</div>
  <article class="post-content">
    <h1>Posts</h1>
    <ul class="post-list">
      {% for post in site.posts %}
        <li>
          {% include post_title.html %}
        </li>
      {% endfor %}
    </ul>

  </article>
<p class="rss-subscribe">subscribe <a href="http://feeds.feedburner.com/Geoexamples">via RSS</a></p>

---
title: "Blog posts"
permalink: /blogposts/
header:
  image: "images/singapore_banner.jpg"
---
<!---
{% include group-by-array collection=site.posts field="tags" %}
{% for category in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ category | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}

-->
Tags:
{% assign sorted_tags = (site.tags | sort:0) %}

{% for tag in sorted_tags %} {% assign t = tag | first %} {% assign posts = tag | last %}
{{ t }} ({{ posts.size }})
{% endfor %}
{% for tag in sorted_tags %} {% assign t = tag | first %} {% assign posts = tag | last %}

Below is the list of blog posts I've written, separated by categories.
{% for category in site.categories %}
  <h2 name="{{ category | first }}">{{ category | first }}</h2>
    {% for posts in category %}
      {% for post in posts %}
        {% include archive-single.html %}
      {% endfor %}
    {% endfor %}
{% endfor %}

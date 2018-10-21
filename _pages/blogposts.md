---
title: "Blog posts"
permalink: /blogposts/
header:
  image: "images/singapore_banner.jpg"
---

Below is the list of blog posts I've written, separated by categories.

{% include group-by-array collection=site.posts field="tags" %}

<!---
{% for category in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ category | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}

-->

{% for category in site.categories %}
  <h2 name="{{ category | first }}">{{ category | first }}</h2>
    <ul>
    {% for posts in category %}
      {% for post in posts %}
        {% include archive-single.html %}
      {% endfor %}
    {% endfor %}
    </ul>
{% endfor %}

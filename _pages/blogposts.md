---
title: "Blog posts"
permalink: /blogposts/
layout: tags
excerpt: "Collection of the posts I've written"
header:
  overlay_image: "images/Singapore_banner2.jpg"
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "Taken in 2017"

---
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

<!---
Below is the list of blog posts I've written, separated by categories.
{% for category in site.categories %}
  <h2 name="{{ category | first }}">{{ category | first }}</h2>
    {% for posts in category %}
      {% for post in posts %}
        {% include archive-single.html %}
      {% endfor %}
    {% endfor %}
{% endfor %}
--->

---
permalink: /press/
title: Seattle Snowmass Community Summer Study Press 
hero_image: /assets/images/uw-fountain.jpg
hide_hero: false
---
If you are a member of the press and are planning on attending, please [get in touch for registration](mailto:snowmass-loc2022@uw.edu)!

Articles in reverse publication order:

{% assign sorted_articles = site.data.press | sort: "date" %}
{% for article in sorted_articles reversed %}
*  <a href="{{ article.link }}">{{ article.title }}</a> - {{ article.publication }} ({{ article.date }})
{% endfor %}

---
layout: default
title: "Pramod's corner of the web"
---

## Welcome!

Hi there, welcome to this page!

- Blog (archived): [pramod493.wordpress.com](https://pramod493.wordpress.com)
- LinkedIn: [linkedin.com/in/pramodkr](https://www.linkedin.com/in/pramodkr/)

---

## Posts

{% if site.posts.size > 0 %}
| Title | Date |
|-------|------|
{% for post in site.posts %}| [{{ post.title }}]({{ post.url | relative_url }}) | {{ post.date | date: "%B %d, %Y" }} |
{% endfor %}
{% else %}
*No posts yet.*
{% endif %}

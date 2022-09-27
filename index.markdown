---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---


# List of post by Tags
{% for category in site.categories %}
  <h2>{{ category[0] }}</h2>
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

<hr>

# Port Scanning Steps
{% for post in site.posts %}
{% for step in post.steps%}
{% for tag in step.tags%}
{% if tag == "Port scanning" %}
{{ tag }} - {{ step.name }} - <a href="{{ post.url }}">{{ post.title }}</a>
{% endif %}
{% endfor %}
{% endfor %}
{% endfor %}

<hr>

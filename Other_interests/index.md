---
title: Other interests
---

# {{ page.title }}
	
{% for post in site.tags.OSTATNE %}
* {{ post.date | date_to_string }} - [{{ post.title }}]( {{ post.url }} ) 

	{{ post.excerpt | remove: '<p>' | remove: '</p>' }}
{% endfor %}


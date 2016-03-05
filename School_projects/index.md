---
maintitle: School projects
title1: Web publications
title2: Database systems
---

# {{ page.maintitle }}
	
## {{ page.title1 }}
{% for post in site.posts%}
{% if post.category == 'WP' and post.tag == 'SCHOOL' %}
* {{ post.date | date_to_string }} - [{{ post.title }}]( {{ post.url }} ) 

	{{ post.excerpt | remove: '<p>' | remove: '</p>' }}
{% endif %}
{% endfor %}


## {{ page.title2 }}
{% for post in site.posts %}
{% if post.category == 'DS' and post.tag == 'SCHOOL' %}
* {{ post.date | date_to_string }} - [{{ post.title }}]( {{ post.url }} ) 

	{{ post.excerpt | remove: '<p>' | remove: '</p>' }}
{% endif %}
{% endfor %}




---
maintitle: School projects
title1: 6.semester
title2: 4.semester
---

# {{ page.maintitle }}
	
## {{ page.title1 }}
{% for post in site.posts%}
{% if post.category == '6.semester' and post.tag == 'SCHOOL' %}
* {{ post.date | date_to_string }} - [{{ post.title }}]( {{ post.url }} ) 

	{{ post.excerpt | remove: '<p>' | remove: '</p>' }}
{% endif %}
{% endfor %}


## {{ page.title2 }}
{% for post in site.posts %}
{% if post.category == '4.semester' and post.tag == 'SCHOOL' %}
* {{ post.date | date_to_string }} - [{{ post.title }}]( {{ post.url }} ) 

	{{ post.excerpt | remove: '<p>' | remove: '</p>' }}
{% endif %}
{% endfor %}




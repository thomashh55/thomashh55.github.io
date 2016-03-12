---
title: School projects
semester6: 6.semester
semester4: 4.semester
---

# {{ page.title }}

*FIIT - faculty of informatics and information technologies*

**Projects are devided into subjects of different semesters:**
	
## {{ page.semester6 }}
{% for post in site.posts%}
{% if post.category == '6.semester' and post.tag == 'SCHOOL' %}
* {{ post.date | date_to_string }} - [{{ post.title }}]( {{ post.url }} ) 

	{{ post.excerpt | remove: '<p>' | remove: '</p>' }}
{% endif %}
{% endfor %}


## {{ page.semester4 }}
{% for post in site.posts %}
{% if post.category == '4.semester' and post.tag == 'SCHOOL' %}
* {{ post.date | date_to_string }} - [{{ post.title }}]( {{ post.url }} ) 

	{{ post.excerpt | remove: '<p>' | remove: '</p>' }}
{% endif %}
{% endfor %}




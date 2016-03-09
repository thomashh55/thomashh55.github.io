---
title: "Web publication"
tag: "SCHOOL"
category: "6.semester"
date: 2016-02-02
---

<img src="{{ site.url }}/Downloads/Obr2.jpg" alt="objdiagram">

Subject oriented towards XML,XSLT,.. languages and publication of documents on the internet.

<!--excerpt--> 

{% for assignment in site.web_publication %}

{% assign assignm = site.data.web_publicationDATA[assignment.title] %}  

* **{{ assignment.date | date_to_string }} - [{{ assignment.title }}]( {{ assignment.url }} )** 

	**Main theme**: *{{ assignm.main_theme }}*, **Hours spent:** *{{ assignm.hours_spent }}*, **Points count:** *{{ assignm.points_count }}* 

	Excerpt:

	{{ assignment.excerpt | remove: '<p>' | remove: '</p>' }}

	<br/>

{% endfor %}

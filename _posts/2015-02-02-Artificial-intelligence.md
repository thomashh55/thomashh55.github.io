---
title: "Artificial intelligence"
tag: "SCHOOL"
category: "4.semester"
date: 2015-02-02
description: "Subject of 4. semester in FIIT concerning implementation of AI algorithms"
---

<img src="{{ site.url }}/Downloads/Obr3.jpg" alt="objdiagram">

Oriented towards such AI algorithms like production system, evolutionary algorithms, search of possible solutions etc.

<!--excerpt--> 

*Consists of 4 assignments:*


{% for assignment in site.artificial_intelligence %}

{% assign assignm = site.data.artificial_intelligenceDATA[assignment.title] %}  

* **{{ assignment.date | date_to_string }} - [{{ assignment.title }}]( {{ assignment.url }} )** 

	**Main theme**: *{{ assignm.main_theme }}*, **Hours spent:** *{{ assignm.hours_spent }}*, **Points count:** *{{ assignm.points_count }}* 

	Excerpt:

	{{ assignment.excerpt | remove: '<p>' | remove: '</p>' }}

	<br/>

{% endfor %}

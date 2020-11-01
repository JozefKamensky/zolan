---
layout: default
title: Projects
permalink: /projects/
---
<div class="container">
	<div class="row">
		<div class="col col-12">
            {% for project in site.projects %}
                {% include article-content.html content=project %}
            {% endfor %}
		</div>
	</div>
</div>
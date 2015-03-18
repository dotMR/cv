---
permalink: /plain/
---
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
</head>

#{{ site.data.resume.name }}
{{ site.data.resume.address }} \\
{{ site.data.resume.email }} \\
{{ site.data.resume.phone }}

* * *

###SUMMARY
{{ site.data.resume.summary }}

* * *

###EXPERIENCE
{% for pos in site.data.resume.positions %}
**{{ pos.company }}**\\
**{{ pos.role }}**\\
{{ pos.location }}\\
{{ pos.timeframe }}

{% if pos.description %}{{ pos.description }}{% endif %}

{% if pos.highlights %}
{% for highlight in pos.highlights %}
- {{ highlight.description}}
{% endfor %}
{% endif %}

{% for detail in pos.detail %}
**{{ detail.title }}**
: {{ detail.description }}
{% endfor %}

{% endfor %}

* * *

###PROJECT SUMMARIES

{% for prj in site.data.resume.projects %}
**{{ prj.title }}**\\
{% if prj.link %}{{ prj.link}}{% endif %}\\
{{ prj.timeframe }}

{{ prj.description }}

{% for detail in prj.detail %}
**{{ detail.title }}**
: {{ detail.description }}
{% endfor %}

{% endfor %}

* * *

###EDUCATION
{% for edu in site.data.resume.education %}
**{{ edu.school }}**\\
{{ edu.location }}\\
{{ edu.program }}\\
{{ edu.timeframe }}

{{ edu.description }}
{% endfor %}
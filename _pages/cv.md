---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}
{% assign cv = site.data.cv %}

{% if cv.basics.summary %}
Summary
======
{{ cv.basics.summary }}
{% endif %}

{% if cv.basics.email or cv.basics.phone or cv.basics.website or cv.basics.profiles %}
Contact
======
{% if cv.basics.location.city %}* {{ cv.basics.location.city }}{% if cv.basics.location.countryCode %}, {{ cv.basics.location.countryCode }}{% endif %}{% endif %}
{% if cv.basics.email %}* [{{ cv.basics.email }}](mailto:{{ cv.basics.email }}){% endif %}
{% if cv.basics.phone %}* {{ cv.basics.phone }}{% endif %}
{% if cv.basics.website %}* [{{ cv.basics.website }}]({{ cv.basics.website }}){% endif %}
{% for profile in cv.basics.profiles %}
* {{ profile.network }}: [{{ profile.username }}]({{ profile.url }})
{% endfor %}
{% endif %}

{% if cv.work %}
Work Experience
======
{% for job in cv.work %}
* **{{ job.position }}**, {% if job.url %}[{{ job.name }}]({{ job.url }}){% else %}{{ job.name }}{% endif %}, {{ job.startDate | date: "%b %Y" }} - {% if job.endDate and job.endDate != "" %}{{ job.endDate | date: "%b %Y" }}{% else %}Present{% endif %}
  {% if job.summary %}* {{ job.summary }}{% endif %}
  {% for item in job.highlights %}
  * {{ item }}
  {% endfor %}
{% endfor %}
{% endif %}

{% if cv.education %}
Education
======
{% for item in cv.education %}
* **{{ item.studyType }}{% if item.area %}, {{ item.area }}{% endif %}**, {{ item.institution }}, {{ item.startDate | date: "%b %Y" }} - {% if item.endDate and item.endDate != "" %}{{ item.endDate | date: "%b %Y" }}{% else %}Present{% endif %}
  {% if item.gpa %}* Grade: {{ item.gpa }}{% endif %}
  {% for course in item.courses %}
  * {{ course }}
  {% endfor %}
{% endfor %}
{% endif %}

{% if cv.skills %}
Skills
======
{% for skill in cv.skills %}
* **{{ skill.name }}:** {{ skill.keywords | join: ", " }}
{% endfor %}
{% endif %}

{% if cv.languages %}
Languages
======
{% for item in cv.languages %}
* **{{ item.language }}:** {{ item.fluency }}
{% endfor %}
{% endif %}

{% if cv.publications %}
Selected Publications
======
{% for item in cv.publications %}
* {% if item.website %}[{{ item.name }}]({{ item.website }}){% else %}{{ item.name }}{% endif %}. {{ item.publisher }}{% if item.releaseDate %}, {{ item.releaseDate | date: "%Y" }}{% endif %}.
{% endfor %}
{% endif %}

{% if cv.portfolio %}
Selected Projects
======
{% for item in cv.portfolio %}
* **{% if item.url %}[{{ item.name }}]({{ item.url }}){% else %}{{ item.name }}{% endif %}:** {{ item.description }}
{% endfor %}
{% endif %}

{% if cv.interests %}
Interests
======
{% for item in cv.interests %}
* **{{ item.name }}:** {{ item.keywords | join: ", " }}
{% endfor %}
{% endif %}

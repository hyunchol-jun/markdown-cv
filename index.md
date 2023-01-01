---
layout: cv
title: Hyunchol_Jun_Resume
---

{% include_relative cv_header.md %}

---

<!-- I am a passionate web developer who graduated recently from a Web Dev bootcamp with a background in Electrical Engineering and Aircraft Maintenance.  -->
<!-- I have been coding as a hobby since University, where I self-taught and created Android apps.  -->
<!-- At my previous position at Oracle, I acquired a good understanding of databases and a DBA certificate (OCP 10g.) -->

## Technical Skills

{% for group in site.data.cv.skills %}
{{ group.category }}
:
{% for value in group.values -%}
{{ value }}{% unless forloop.last %}, {% endunless -%}
{% endfor %}
{% endfor %}

## Personal Projects

{% for project in site.data.cv.personalProjects %}

### {{ project.name }} - [{{ project.url }}]({{ project.url }})

{{ project.description }}

#### Highlights

{% for highlight in project.highlights %}

{{highlight.title}}
: {{highlight.content}}

{% endfor %}

#### Tech Stack

{% for tech in project.techStack %}{{ tech }}{% unless forloop.last %}, {% endunless %}{% endfor %}

{% endfor %}

<!-- #### Project Links  -->
<!---->
<!-- Front-End repository -->
<!-- : [https://github.com/hyunchol-jun/better-eat-client](https://github.com/hyunchol-jun/better-eat-client) -->
<!---->
<!-- Back-End repository -->
<!-- : [https://github.com/hyunchol-jun/better-eat-server](https://github.com/hyunchol-jun/better-eat-server) -->
<!---->

## Education

{% for education in site.data.cv.educations -%}

### {{ education.degree }}

**{{ education.school }}**
`{{ education.endDate }}`
_{{ education.location }}_
{% for description in education.descriptions -%}

- {{ description }}
  {% endfor %}

{% endfor %}

## Experiences

{% for experience in site.data.cv.experiences -%}

### {{ experience.role }}

**{{ experience.company }}**
`{{ experience.startDate }} - {{ experience.endDate }}`
_{{ experience.location }}_

{% for description in experience.descriptions -%}

- {{ description }}
  {% endfor %}

{% endfor %}

## Certifications

{% for certification in site.data.cv.certifications -%}
**{{ certification.name }}**
`{{ certification.date }}`

{% endfor %}

<!-- ### Footer

Last updated: May 2013 -->

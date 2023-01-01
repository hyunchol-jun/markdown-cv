---
layout: cv
title: Hyunchol_Jun_Resume
---

<div class="first-col" markdown="1">
{% include_relative cv_header.md %}

## Technical Skills

{% for group in site.data.cv.skills %}
{{ group.category }}
: {% for value in group.values -%}{{ value }}{% unless forloop.last %}, {% endunless -%}{% endfor %}
{% endfor %}

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

</div>

<div class="second-col" markdown="1">
## Personal Projects

{% for project in site.data.cv.personalProjects %}

### {{ project.name }} - [{{ project.url }}]({{ project.url }})

{{ project.description }}

#### Tech Stack

{% for tech in project.techStack %}{{ tech }}{% unless forloop.last %}, {% endunless %}{% endfor %}

#### Highlights

{% for highlight in project.highlights %}

{{highlight.title}}
: {{highlight.content}}

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

</div>

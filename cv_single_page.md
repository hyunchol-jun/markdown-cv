---
layout: cv
title: Hyunchol_Jun_Resume
---

{% include_relative cv_header.md %}

## Technical Skills
{% for group in site.data.cv.skills %}
{{ group.category }}
: 
    {% for value in group.values -%} 
        {{ value }}{% unless forloop.last %}, {% endunless -%}
    {% endfor %}
{% endfor %}

## Personal Projects

### BetterEat - [https://better-eat.hyuncholjun.com](http://better-eat.hyuncholjun.com)
BetterEat is a full-stack web application that helps users to search for & store recipes based on their food preferences. It also manages inventory & grocery lists in a smart way.

#### Highlights
Search For/Store Recipes
: Makes external API calls to get recipes data, and stores in database table connecting to user with Many-To-Many relationship.

Grocery List
: Saves grocery items to the user in the database. Also checks for duplicate entries utilizing 'Unique Constraint'.

React Features
: Utilizes various React Hooks to make the application performant, including useRef, useMemo, useContext and useReducer.

Server Structure
: Implements MVC design pattern in the Express.js server to increase scalability.

#### Tech Stack
React, React-router, Sass, Express, MySQL, Knex.js, JWT, Netlify, Heroku

## Education

{% for education in site.data.cv.educations -%}
### {{ education.degree }}
**{{ education.school }}**
`{{ education.endDate }}`
*{{ education.location }}*
{% for description in education.descriptions -%}
- {{ description }}
{% endfor %}
{% endfor %}

## Experiences

{% for experience in site.data.cv.experiences -%}
### {{ experience.role }}
**{{ experience.company }}**
`{{ experience.startDate }} - {{ experience.endDate }}`
*{{ experience.location }}*
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

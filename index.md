---
layout: cv
title: Hyunchol_Jun_Resume
---

{% include_relative cv_header.md %}

As a recent Web Development bootcamp graduate with a background in Electrical Engineering and Aircraft Maintenance, I am passionate about making a positive difference in the world through programming.

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
BetterEat is a full-stack web application that helps users to search & store recipes based on their food preferences and manage inventory & grocery lists.

#### Highlights
Search Recipes
: Makes external API calls to get recipe data through the back-end server to protect the API key in the server's environment variable.

Store Recipes
: Stores recipe data to the corresponding user in the database using a Many-to-Many relationship.

Grocery List
: Saves grocery items to the user in the database. Also checks for duplicate entries utilizing MySQL's unique constraint feature.

React Features
: Utilizes various React Hooks to make the application performant, including useRef, useMemo, useContext, useReducer.

Server Structure
: Implements the MVC design pattern in the Express.js server to increase readability and to make future changes easy.

Authentication
: Implements login with JWT and only stores a salted hash of the password to the database using the Bcrypt library to keep the passwords secure.

#### Tech Stack
React, React-router, Sass, Express, MySQL, Knex.js, JWT, Netlify, Heroku

#### Project Links 

Front-End repository
: [https://github.com/hyunchol-jun/better-eat-client](https://github.com/hyunchol-jun/better-eat-client)

Back-End repository
: [https://github.com/hyunchol-jun/better-eat-server](https://github.com/hyunchol-jun/better-eat-server)


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

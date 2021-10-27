---
layout: workshop      # DON'T CHANGE THIS.
# More detailed instructions (including how to fill these variables for an
# online workshop) are available at
# https://carpentries.github.io/workshop-template/customization/index.html
venue: "Online"        # brief name of the institution that hosts the workshop without address (e.g., "Euphoric State University")
address: "Online"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria"), videoconferencing URL, or 'online'
country: "gb"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes) for the institution that hosts the workshop
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) for the
latitude: "53.46674756854867"        # decimal latitude of workshop venue (use https://www.latlong.net/)
longitude: "-2.2337120440390756"       # decimal longitude of the workshop venue (use https://www.latlong.net)
humandate: "06 - 10 December 2021"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "9:30 - 13:00"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
timezone: "GMT (UTC + 0)"
startdate: 2021-12-06      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2021-12-10        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Steve Crouch", "James Graham", "Aleksandra Nenadic"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["Gareth Francis", "David Young", "James Perry"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["a.nenadic@manchester.ac.uk", "s.crouch@software.ac.uk", "t.sloan@epcc.ed.ac.uk"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:  "" # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document (e.g., https://pad.carpentries.org/2015-01-01-euphoria)
eventbrite: "199677680317"           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

{% comment %} See instructions in the comments below for how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
HEADER

Edit the values in the block above to be appropriate for your workshop.
If the value is not 'true', 'false', 'null', or a number, please use
double quotation marks around the value, unless specified otherwise.
And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}


{% comment %}
Check DC curriculum
{% endcomment %}

{% if site.carpentry == "dc" %}
{% unless site.curriculum == "dc-ecology" or site.curriculum == "dc-genomics" or site.curriculum == "dc-socsci" or site.curriculum == "dc-geospatial" %}
<div class="alert alert-warning">
It looks like you are setting up a website for a Data Carpentry curriculum but you haven't specified the curriculum type in the <code>_config.yml</code> file (current value in <code>_config.yml</code>: "<strong>{{ site.curriculum }}</strong>", possible values: <code>dc-ecology</code>, <code>dc-genomics</code>, <code>dc-socsci</code>, or <code>dc-geospatial</code>). After editing this file, you need to run <code>make serve</code> again to see the changes reflected.
</div>
{% endunless %}
{% endif %}

{% comment %}
Check SWC curriculum
{% endcomment %}

{% if site.carpentry == "swc" %}
{% unless site.curriculum == "swc-inflammation" or site.curriculum == "swc-gapminder" %}
<div class="alert alert-warning">
It looks like you are setting up a website for a Software Carpentry curriculum but you haven't specified the curriculum type in the <code>_config.yml</code> file (current value in <code>_config.yml</code>: "<strong>{{ site.curriculum }}</strong>", possible values: <code>swc-inflammation</code>, or <code>swc-gapminder</code>). After editing this file, you need to run <code>make serve</code> again to see the changes reflected.
</div>
{% endunless %}
{% endif %}

{% comment %}
<h2 id="general">General Information</h2>

{% if site.carpentry == "swc" %}
{% include swc/intro.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}
{% endcomment %}

This is a pilot workshop for the Intermediate Python Software Skills course developed by the [Software Sustainability Institute](https://software.ac.uk) and delivered to the members of the [LSST:UK community](https://www.lsst.ac.uk/). The workshop will be led by instructors but will be largely in self-learning format - this means particiants will go though the materials on their own or in groups aided by insturctors and a group of helpers.
  
<h3 id="audience">Audience</h3>
This course is aimed at teaching a core set of established intermediate-level best practice Python software development skills for working as part of a team in a research environment. A typical learner for this course may be someone who is working in academic research and who has gained basic software development skills and has been applying those skills actively for half a year or more. Now their software development-related projects are becoming larger and are involving more stakeholders so they now they need additional software engineering skills to help them design more robust software code, automate the process of testing and verifying its correctness and support collaborations with others.

<h3 id="where">When & Where</h3>
The workshop will run online over 5 half-days, from {{page.humandate}}, {{page.humantime}}, using Zoom. The Zoom link to use for this event will be shared via email to registered participants.

<h3>Registration</h3>
Registration will be announced soon.

<h3>Requirements</h3>
Participants must have a laptop/PC with a Mac, Linux, or Windows operating system and a few [software tools](https://softwaresaved.github.io/python-intermediate-development/setup.html) installed ahead of the workshop.

<h3>Code of Conduct</h3>

All participants (including instructors, helpers and observers) are required to abide by The Carpentries <a href="{{
site.swc_site }}/conduct/">Code of Conduct</a>.

<h3 id="contact">Contact</h3>
<p>
Please email
{% if page.email %}
  {% for contact in page.email %}
    {% if forloop.last and page.email.size > 1 %}
      or
    {% else %}
      {% unless forloop.first %}
      ,
      {% endunless %}
    {% endif %}
    <a href='mailto:{{contact}}'>{{contact}}</a>
  {% endfor %}
{% else %}
  to-be-announced
{% endif %}
for more information.
</p>

<hr/>

<h3 id="schedule">Materials & Schedule</h3>
The [material to be covered at the workshop](https://softwaresaved.github.io/python-intermediate-development/index.html) is available online but is still in development and thus may change. 

Provisional schedule is shown below - be aware that there might be slight shift between the actual material covered on each day as you will be asked to finish all tasks from 
the previous day before moving forward.

<div class="row">
<!--  <div style="padding-left: 15px;">Before the workshop: please fill in the <a href="{{ site.pre_survey }}{{ site.github.project_title }}">pre-workshop survey</a></div>-->
  {% assign startdate = {{page.startdate}} | date: '%s' %}
  {% assign day1 =  startdate | date_to_long_string %}
  {% assign day2 =  startdate | plus: 86400 | date_to_long_string %}
  {% assign day3 =  startdate | plus: 86400 | plus: 86400 | date_to_long_string %}
  {% assign day4 =  startdate | plus: 86400 | plus: 86400 | plus: 86400 | date_to_long_string %}
  {% assign day5 =  startdate | plus: 86400*4 | date_to_long_string %}

  <div style="padding-left: 15px;">
    <h4>Day 1, {{day1}}, {{page.humantime}} {{page.timezone}}</h4>
    <p><a href="https://softwaresaved.github.io/python-intermediate-development/01-section1-intro/index.html" target="_blank">Environment For Collaborative Code Development</a></p>

    <h4>Day 2, {{day2}}, {{page.humantime}} {{page.timezone}}</h4>
    <p><a href="https://softwaresaved.github.io/python-intermediate-development/11-section2-intro/index.html" target="_blank">Ensuring Correctness of Software at Scale</a></p>
    
    <h4>Day 3, {{day3}}, {{page.humantime}} {{page.timezone}}</h4>
    <p><a href="https://softwaresaved.github.io/python-intermediate-development/21-section3-intro/index.html">Software Architecture and Design</a></p>
    
    <h4>Day 4, {{day4}}, {{page.humantime}} {{page.timezone}}</h4>
    <p><a href="https://softwaresaved.github.io/python-intermediate-development/31-section4-intro/index.html" target="_blank">Developing Software In a Team and Releasing It</a></p>
    
    <h4>Day 5, {{day5}}, {{page.humantime}} {{page.timezone}}</h4>
    <p><a href="https://softwaresaved.github.io/python-intermediate-development/40-wrap-up/index.html" target="_blank">Finishing off tasks from previous days, Q & A, workshop wrap up</a></p>
  </div>
</div>





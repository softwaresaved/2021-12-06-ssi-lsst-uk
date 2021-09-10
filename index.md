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
instructor: ["Aleksandra Nenadic", "Steve Crouch", "James Graham"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: [""]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["a.nenadic@manchester.ac.uk", "s.crouch@software.ac.uk", "t.sloan@epcc.ed.ac.uk"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:  "" # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document (e.g., https://pad.carpentries.org/2015-01-01-euphoria)
eventbrite: ""           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
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

This is a pilot workshop for the Intermediate Python Software Skills course developed by the [Software Sustainability Institute](https://software.ac.uk) and delivered to the members of the [LSST:UK community](https://www.lsst.ac.uk/).
  
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

{% comment %}
Collaborative Notes

If you want to use an Etherpad, go to

https://pad.carpentries.org/YYYY-MM-DD-site

where 'YYYY-MM-DD-site' is the identifier for your workshop,
e.g., '2015-06-10-esu'.

Note we also have a CodiMD (the open-source version of HackMD)
available at https://codimd.carpentries.org
{% endcomment %}
{% if page.collaborative_notes %}

{% comment %}
<h2 id="collaborative_notes">Collaborative Notes</h2>

<p>
We will use this <a href="{{ page.collaborative_notes }}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code during the workshop.
</p>
<hr/>
{% endif %}


{% comment %}
SURVEYS - DO NOT EDIT SURVEY LINKS
{% endcomment %}
<h2 id="surveys">Surveys</h2>
<p>Please be sure to complete these surveys before and after the workshop.</p>
<p><a href="{{ site.pre_survey }}{{ site.github.project_title }}">Pre-workshop survey</a></p>
<p><a href="{{ site.post_survey }}{{ site.github.project_title }}">Post-workshop survey</a></p>
{% comment %}

<hr/>


{% comment %}
SCHEDULE

Show the workshop's schedule.  Edit the items and times in the table
to match your plans.  You may also want to change 'Day 1' and 'Day
2' to be actual dates or days of the week.
{% endcomment %}
<h3 id="schedule">Schedule & Materials</h3>

<div class="row">
<!--  <div style="padding-left: 15px;">Before the workshop: please fill in the <a href="{{ site.pre_survey }}{{ site.github.project_title }}">pre-workshop survey</a></div>-->
  {% assign startdate = {{page.startdate}} | date: '%s' %}
  {% assign day1 =  startdate | date_to_long_string %}
  {% assign day2 =  startdate | plus: 86400 | date_to_long_string %}
  {% assign day3 =  startdate | plus: 86400 | plus: 86400 | date_to_long_string %}
  {% assign day4 =  startdate | plus: 86400 | plus: 86400 | plus: 86400 | date_to_long_string %}

  <div class="col-md-6">
    <h3>Day 1, {{day1}}, {{page.humantime}} {{page.timezone}}</h3>
    <table class="table table-striped">
      <tr> <td><a href="https://swcarpentry.github.io/shell-novice" target="_blank">Automating Tasks with shell</a></td> </tr>
    </table>
  </div>
  <div class="col-md-6">
    <h3>Day 2, {{day2}}, {{page.humantime}} {{page.timezone}}</h3>
    <table class="table table-striped">
      <tr> <td><a href="http://swcarpentry.github.io/python-novice-gapminder/" target="_blank">Building Programs with Python - Part 1</a></td> </tr>
    </table>
  </div>
</div>
<div class="row">
    <div class="col-md-6">
    <h3>Day 3, {{day3}}, {{page.humantime}} {{page.timezone}}</h3>
    <table class="table table-striped">
      <tr> <td><a href="http://swcarpentry.github.io/python-novice-gapminder/" target="_blank">Building Programs with Python - Part 2</a></td> </tr>
    </table>
  </div>
  <div class="col-md-6">
      <h3>Day 4, {{day4}}, {{page.humantime}} {{page.timezone}}</h3>
      <table class="table table-striped">
        <tr> <td><a href="http://swcarpentry.github.io/git-novice" target="_blank">Version Control with Git</a></td> </tr>
      </table>
  </div>
</div>

<hr/>

{% comment %}
SYLLABUS

Show what topics will be covered.

1. If your workshop is R rather than Python, remove the comment
around that section and put a comment around the Python section.
2. Some workshops will delete SQL.
3. Please make sure the list of topics is synchronized with what you
intend to teach.
4. You may need to move the div's with class="col-md-6" around inside
the div's with class="row" to balance the multi-column layout.

This is one of the places where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}
{% comment %}
<h2 id="syllabus">Syllabus</h2>

{% if site.carpentry == "swc" %}
{% include swc/syllabus.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/syllabus.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/syllabus.html %}
{% endif %}

<hr/>

<h2 id="setup">Setup</h2>
<h3>Installation instructions</h3>
<p>
  To participate in this workshop,
  you will need to install <strong>all of the software described below before coming to the workshop</strong>. We will run a pre-workshop installation session to help everyone set up and make sure they have the required software installed.
</p>

{% if site.carpentry == "swc" %}
{% include swc/setup.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/setup.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/setup.html %}
{% endif %}

<p>
  We maintain a list of common issues that occur during installation as a reference for instructors
  that may be useful on the
  <a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Configuration Problems and Solutions wiki page</a>.
</p>
{% endcomment %}

{% comment %}
These are the installation instructions for the tools used
during the workshop.
{% endcomment %}



---
layout: workshop      # DON'T CHANGE THIS.
carpentry: ""    # what kind of Carpentry (must be either "lc" or "dc" or "swc")
venue: "Basic Image Analysis with Python"
address: "Breezeway Bioinformatics Training Room 1540, Building 1, Unit 5, 600 Main Street, Bar Harbor, Maine"
country: "us"
language: "en"
latlng: "44.365646, -68.197153"
humandate: "Mar 28-29, 2019"
humantime: "1:30pm - 4:30pm Thu; 9:00 am - 4:30 pm Fri"
startdate: 2019-03-28
enddate: 2019-03-29
instructor: [""]
helper: [""]
email: ["susan.mcclatchy@jax.org"]
collaborative_notes: https://pad.carpentries.org/2019-03-28-image-analysis-bh
eventbrite: 57836189600
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
EVENTBRITE

This block includes the Eventbrite registration widget if
'eventbrite' has been set in the header.  You can delete it if you
are not using Eventbrite, or leave it in, since it will not be
displayed if the 'eventbrite' field in the header is not set.
{% endcomment %}
{% if page.eventbrite %}
<iframe
src="https://www.eventbrite.com/tickets-external?eid={{page.eventbrite}}&ref=etckt"
frameborder="0"
width="100%"
height="280px"
scrolling="auto">
</iframe>
{% endif %}


<h2 id="general">General Information</h2>

{% comment %}
INTRODUCTION

Edit the general explanatory paragraph below if you want to change
the pitch.
{% endcomment %}
{% if page.carpentry == "swc" %}
{% include sc/intro.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}

{% comment %}
AUDIENCE

Explain who your audience is.  (In particular, tell readers if the
workshop is only open to people from a particular institution.
{% endcomment %}
{% if page.carpentry == "swc" %}
{% include sc/who.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/who.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/who.html %}
{% endif %}

{% comment %}
LOCATION

This block displays the address and links to maps showing directions
if the latitude and longitude of the workshop have been set.  You
can use https://itouchmap.com/latlong.html to find the lat/long of an
address.
{% endcomment %}
{% if page.latlng %}
<p id="where">
<strong>Where:</strong>
{{page.address}}.
Get directions with
<a href="//www.openstreetmap.org/?mlat={{page.latlng | replace:',','&mlon='}}&zoom=16">OpenStreetMap</a>
or
<a href="//maps.google.com/maps?q={{page.latlng}}">Google Maps</a>.
</p>
{% endif %}

{% comment %}
DATE

This block displays the date and links to Google Calendar.
{% endcomment %}
{% if page.humandate %}
<p id="when">
<strong>When:</strong>
{{page.humandate}}.
{% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
SPECIAL REQUIREMENTS

Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
<strong>Requirements:</strong> Participants must bring a laptop with a
Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.). They should have a few specific software packages installed (listed
<a href="#setup">below</a>). They are also required to abide by
{% if page.carpentry == "swc" %}
Software Carpentry's
{% elsif page.carpentry == "dc" %}
Data Carpentry's
{% elsif page.carpentry == "lc" %}
Library Carpentry's
{% endif %}
<a href="{{site.swc_site}}/conduct.html">Code of Conduct</a>.
</p>

{% comment %}
ACCESSIBILITY

Modify the block below if there are any barriers to accessibility or
special instructions.
{% endcomment %}
<p id="accessibility">
<strong>Accessibility:</strong> We are committed to making this workshop
accessible to everybody.
The workshop organizers have checked that:
</p>
<ul>
<li>The room is wheelchair / scooter accessible.</li>
<li>Accessible restrooms are available.</li>
</ul>
<p>
Materials will be provided in advance of the workshop and
large-print handouts are available if needed by notifying the
organizers in advance.  If we can help making learning easier for
you (e.g. sign-language interpreters, lactation facilities) please
get in touch (using contact details below) and we will
attempt to provide them.
</p>

{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
<strong>Contact</strong>:
Please email
{% if page.email %}
{% for email in page.email %}
{% if forloop.last and page.email.size > 1 %}
or
{% else %}
{% unless forloop.first %}
,
{% endunless %}
{% endif %}
<a href='mailto:{{email}}'>{{email}}</a>
{% endfor %}
{% else %}
to-be-announced
{% endif %}
for more information.
</p>

<hr/>



{% comment %}
SCHEDULE

Show the workshop's schedule.  Edit the items and times in the table
to match your plans.  You may also want to change 'Day 1' and 'Day
2' to be actual dates or days of the week.
{% endcomment %}
<h2 id="schedule">Schedule</h2>

<div class="row">
<div class="col-md-6">
<h3>Thursday, March 28</h3>
<table class="table table-striped">
<tr> <td>Before</td>  <td><a href="https://www.surveymonkey.com/r/image-analysis">Pre-workshop survey</a></td> </tr>
<tr> <td>13:30</td>  <td>Workshop overview</td> </tr>
<tr> <td>13:45</td>  <td><a href="https://github.com/TheJacksonLaboratory/PythonImagingBasic/blob/master/lessons/0-Background_and_Setup.ipynb">Background and setup</a></td> </tr>
<tr> <td>14:00</td>  <td>Images are arrays</td> </tr>
<tr> <td>15:00</td>  <td>Coffee</td> </tr>
<tr> <td>15:15</td>  <td>Images are arrays (continued)</td> </tr>
<tr> <td>16:15</td>  <td>Wrap-up</td> </tr>
<tr> <td>16:30</td>  <td>End</td> </tr>
</table>
</div>
<div class="col-md-6">
<h3>Friday, March 29</h3>
<table class="table table-striped">
<tr> <td>09:00</td>  <td>Image I / O</td> </tr>
<tr> <td>10:30</td>  <td>Coffee</td> </tr>
<tr> <td>10:45</td>  <td>Filters and convolutions</td> </tr>
<tr> <td>12:30</td>  <td>Lunch</td> </tr>
<tr> <td>13:30</td>  <td>Morphology</td> </tr>
<tr> <td>15:00</td>  <td>Coffee</td> </tr>
<tr> <td>16:15</td>  <td><a href="https://www.surveymonkey.com/r/post-image-analysis">Post-workshop survey</a></td> </tr>
<tr> <td>16:30</td>  <td>End</td> </tr>
</table>
</div>
</div>


{% comment %}
Collaborative Notes

If you want to use an Etherpad, go to

http://pad.software-carpentry.org/YYYY-MM-DD-site

where 'YYYY-MM-DD-site' is the identifier for your workshop,
e.g., '2015-06-10-esu'.
{% endcomment %}
{% if page.collaborative_notes %}
<p id="collaborative_notes">
We will use this <a href="{{page.collaborative_notes}}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
{% endif %}

<hr/>


{% comment %}
SETUP

Delete irrelevant sections from the setup instructions.  Each
section is inside a 'div' without any classes to make the beginning
and end easier to find.

This is the other place where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}

<h2 id="setup">Setup</h2>

<p>
To participate in a
{% if page.carpentry == "swc" %}
Software Carpentry
{% elsif page.carpentry == "dc" %}
Data Carpentry
{% elsif page.carpentry == "lc" %}
Library Carpentry
{% endif %}
workshop,
you will need access to the software described below.
In addition, you will need an up-to-date web browser.
</p>
<p>
We maintain a list of common issues that occur during installation as a reference for instructors
that may be useful on the
<a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Configuration Problems and Solutions wiki page</a>.
</p>

<div id="python"> {% comment %} Start of 'Python' section. Remove the third paragraph if
the workshop will teach Python using something other than
the Jupyter notebook.
Details at https://jupyter-notebook.readthedocs.io/en/stable/notebook.html#browser-compatibility {% endcomment %}
<h3>Python</h3>

<p>
<a href="https://python.org">Python</a> is a popular language for
research computing, and great for general-purpose programming as
well.  Installing all of its research packages individually can be
a bit difficult, so we recommend
<a href="https://www.anaconda.com/distribution/">Anaconda</a>,
an all-in-one installer.
</p>
<p>
Regardless of how you choose to install it,
<strong>please make sure you install Python version 3.x</strong>
(e.g., 3.6 is fine).
</p>
<p>
We will teach Python using the <a href="https://jupyter.org/">Jupyter notebook</a>,
a programming environment that runs in a web browser. For this to work you will need a reasonably
up-to-date browser. The current versions of the Chrome, Safari and
Firefox browsers are all
<a href="https://jupyter-notebook.readthedocs.io/en/stable/notebook.html#browser-compatibility">supported</a>
(some older browsers, including Internet Explorer version 9
and below, are not).
</p>

<div class="row">
<div class="col-md-4">
<h4 id="python-windows">Windows</h4>
<a href="https://www.youtube.com/watch?v=xxQ0mzZ8UvA">Video Tutorial</a>
<ol>
<li>Open <a href="https://www.anaconda.com/download/#windows">https://www.anaconda.com/download/#windows</a> with your web browser.</li>
<li>Download the Python 3 installer for Windows.</li>
<li>Install Python 3 using all of the defaults for installation <em>except</em> make sure to check <strong>Add Anaconda to my PATH environment variable</strong>.</li>
</ol>
</div>
<div class="col-md-4">
<h4 id="python-macosx">macOS</h4>
<a href="https://www.youtube.com/watch?v=TcSAln46u9U">Video Tutorial</a>
<ol>
<li>Open <a href="https://www.anaconda.com/download/#macos">https://www.anaconda.com/download/#macos</a> with your web browser.</li>
<li>Download the Python 3 installer for OS X.</li>
<li>Install Python 3 using all of the defaults for installation.</li>
</ol>
</div>
<div class="col-md-4">
<h4 id="python-linux">Linux</h4>
<ol>
<li>Open <a href="https://www.anaconda.com/download/#linux">https://www.anaconda.com/download/#linux</a> with your web browser.</li>
<li>Download the Python 3 installer for Linux.<br>
(The installation requires using the shell. If you aren't
comfortable doing the installation yourself
stop here and request help at the workshop.)
</li>
<li>
Open a terminal window.
</li>
<li>
Type <pre>bash Anaconda3-</pre> and then press
<kbd>Tab</kbd>. The name of the file you just downloaded should
appear. If it does not, navigate to the folder where you
downloaded the file, for example with:
<pre>cd Downloads</pre>
Then, try again.
</li>
<li>
Press <kbd>Return</kbd>. You will follow the text-only prompts. To move through
the text, press <kbd>Spacebar</kbd>. Type <code>yes</code> and
press enter to approve the license. Press enter to approve the
default location for the files. Type <code>yes</code> and
press enter to prepend Anaconda to your <code>PATH</code>
(this makes the Anaconda distribution the default Python).
</li>
<li>
Close the terminal window.
</li>
</ol>
</div>
</div>
{% comment %}
<p>
Once you are done installing the software listed above,
please go to <a href="setup/index.html">this page</a>,
which has instructions on how to test that everything was installed correctly.
</p>
{% endcomment %}
</div> {% comment %} End of 'Python' section. {% endcomment %}
<div id="git"> {% comment %} Start of 'Git' section. {% endcomment %}
<h3>Git</h3>
<p>
Git is a version control system that lets you track who made changes
to what when and has options for easily updating a shared or public
version of your code
on <a href="https://github.com/">github.com</a>. You will need a
<a href="https://help.github.com/articles/supported-browsers/">supported
web browser</a>.
</p>
<p>
You will need an account at <a href="https://github.com/">github.com</a>. Basic GitHub accounts are free. We encourage
you to create a GitHub account if you don't have one already.
Please consider what personal information you'd like to reveal. For
example, you may want to review these
<a href="https://help.github.com/articles/keeping-your-email-address-private/">instructions
for keeping your email address private</a> provided at GitHub.
</p>

<div class="row">
<div class="col-md-4">
<h4 id="git-windows">Windows</h4>
You will first need to install <a href="https://git-scm.com/download/win">git</a>.
</div>
<div class="col-md-4">
<h4 id="git-macosx">macOS</h4>
<a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">Video Tutorial</a>
<p>
<strong>For OS X 10.9 and higher</strong>, install Git for Mac
by downloading and running the most recent "mavericks" installer from
<a href="http://sourceforge.net/projects/git-osx-installer/files/">this list</a>.
Because this installer is not signed by the developer, you may have to
right click (control click) on the .pkg file, click Open, and click
Open on the pop up window.
After installing Git, there will not be anything in your <code>/Applications</code> folder,
as Git is a command line program.
<strong>For older versions of OS X (10.5-10.8)</strong> use the
most recent available installer labelled "snow-leopard"
<a href="http://sourceforge.net/projects/git-osx-installer/files/">available here</a>.
</p>
</div>
<div class="col-md-4">
<h4 id="git-linux">Linux</h4>
<p>
If Git is not already available on your machine you can try to
install it via your distro's package manager. For Debian/Ubuntu run
<code>sudo apt-get install git</code> and for Fedora run
<code>sudo dnf install git</code>.
</p>
</div>
</div>
</div> {% comment %} End of 'Git' section. {% endcomment %}


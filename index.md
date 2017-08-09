---
layout: default
---

# [](#header-1)Welcome, I'm James!

<center>
  <img HEIGTH="320" WIDTH="240" src="assets/images/IMG_3118-1.JPG" class="img-responsive img-circle" alt="Oops!">
</center>

I'm a recent graduate of the University of Kansas with a Ph. D. in physics.
My dissertation research involved the statistical analysis of terabyte-sized
data sets resulting from ultrarelativistic heavy-ion collisions recorded by the
[CMS detector](http://cms.web.cern.ch/news/what-cms) at the
[CERN LHC](https://home.cern/topics/large-hadron-collider).
You can find more information on my dissertation
[here](https://cds.cern.ch/record/2275797).

My resume can be found 
[here]({{ site.url }}/assets/files/JamesRCastle_ResumeAugust2017.pdf) 
and you can learn more about me professionally at my 
[LinkedIn profile](https://www.linkedin.com/in/jrcastle90).

## [](#header-2)Interests
- Big Data and high-performance computing technologies
- Automation through Unix/Linux shell and/or python scripting
- Experimental study of ultrarelativistic heavy-ion collisions
- Nuclear medicine
- Statistical analyses including:
  - Machine learning
  - Unfolding/deconvolution
  - Hypothesis testing
  - Monte-Carlo simulation
  - Linear regression
  - Multivariate analysis

## [](#header-2)Projects
{% for post in site.posts %}
  <li><span>{{ post.date | date_to_string }}</span> » <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></li>
{% endfor %}
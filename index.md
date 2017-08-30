---
layout: default
---

# [](#header-1)Welcome, I'm James!

<center>
  <img HEIGTH="320" WIDTH="240" src="assets/images/IMG_3118-1.JPG" class="img-responsive img-circle" alt="Oops!">
</center>

My first passion in life was music.  For most of my young adult life, 
I aspired to be a jazz musician making a living by playing my saxophone. 
That dream followed me up until my senior year of high school when I 
discovered physics. While a majority of people would say they hated their physics 
courses in high school and college, I loved mine. I saw every homework 
and exam problem as a puzzle waiting to be solved, where each new	
challenge was met with excitement. I enjoyed physics so	much that I decided 
to pursue a Ph.D. in it at the University of Kansas. My dissertation research 
involved the statistical analysis of terabyte-sized data sets resulting from 
ultrarelativistic heavy-ion collisions recorded by the 
[CMS detector](http://cms.web.cern.ch/news/what-cms) at the 
[CERN LHC](https://home.cern/topics/large-hadron-collider). 
I successfully defended my dissertation in July 2017. 
You can find more information on my dissertation 
[here](https://cds.cern.ch/record/2275797) and learn more about me 
professionally via [LinkedIn](https://www.linkedin.com/in/jrcastle90).

I am currently seeking to utilize and expand the skills I have gained as a 
researcher at CERN by pursuing a career in data science. As an experimental 
physicist, I have extensive experience in the fields of physics, statistics, 
computer science, data science, and mathematics. In addition, my experience 
as a Ph.D. candidate has allowed me to develop skills in all phases of project 
management (design, execution, and defending), problem solving, critical 
thinking, and time management. 

## [](#header-2)Interests
- Big Data and high-performance computing technologies
- Automation through Unix/Linux shell and/or python scripting
- Experimental study of ultrarelativistic heavy-ion collisions
- Nuclear medicine
- Machine learning:
  - Supervised learning
  - Regularized linear regression
  - Regularized logistic regression
  - Neural networks
  - Unsupervised learning
- Statistical analyses including:
  - Unfolding/deconvolution
  - Hypothesis testing
  - Monte-Carlo simulation
  - Linear regression
  - Multivariate analysis

## [](#header-2)Projects
{% for post in site.posts %}
  <li><span>{{ post.date | date_to_string }}</span> » <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></li>
{% endfor %}
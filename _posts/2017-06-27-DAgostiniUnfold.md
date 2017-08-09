---
layout: post
title: "D'Agostini Unfolder"
use_math: true
---

Unfolding is a standard statistical technique that is used in a wide variety 
of fields from high energy physics to medical imaging.
Most commonly, unfolding is used to remove detector resolution 
effects from measurements. Detector resolution can be understood with the 
following example. Within a PET scan, tomographic images (_e.g._, Fig. 1) 
of the body are obtained by measuring back-to-back photons that are emitted 
from positrons and electrons annihilating. There are two key ingredients in 
this type of measurement that affect the quality of the reconstructed image: 
the uncertainty on the position and time of the measured photons. We will 
focus on the position measurement for this example. Now, the detector that 
is used to measure the photons has a finite granularity and there is a 
nonzero probability that the position of the photon will be recorded as 
somewhere other than where it truly was. This, in turn, will cause the 
reconstructed image of the body to blur. This blur is the detector 
resolution effect. 

<center>
  <img HEIGTH="501" WIDTH="566" src="{{ site.url }}/assets/images/PET-image.jpg" class="img-responsive img-circle" alt="Oops!">
  <br> Figure 1: Example of a PET scan of the human brain
</center>

Apart from improving the detector itself, this resolution can be partially 
removed using unfolding. The premise of this technique assumes that the 
``true'' image, which can be represented by a probability distribution $p(T)$, 
is the convolution of the measured distribution $p(O)$ and a response function 
$p(O|T)$. The response function is a conditional probability that measures the 
probability that a photon from the previous example was measured in one position, 
while its true position was elsewhere. Since the detector granularity is finite, 
it is more common to work with binned data and the unfolding problem can be expressed as 

<center> $p(O_i) = p(O_i|T_j) \ast p(T_j)$, </center>

where the observed and true images are represented with vectors and the response 
function is now a response matrix. This particular setup is the classic $\mathbf{A}x=b$ 
problem in linear algebra, where we want to invert the response matrix and apply it 
to the observed image to get back the true image. However, the response matrix very 
often is ill-conditioned and cannot be inverted. This is where unfolding comes in. 
There are several "flavors" of unfolding on the market, all of which have the same 
goal to create a pseudo-inverse of the response matrix and use that to obtain the true 
image. 

The key statistical tool used in my research as a graduate student was unfolding. In 
particular, I used the D'Agostini iterative flavor of unfolding, which is described 
in Ref. [1]. In order to fully understand the inner workings of this method for 
unfolding I wrote my own D'Agostini unfolder class in C++, which can be found
[here](https://github.com/jrcastle/DAgostiniUnfold). 
This class relies heavily on libraries from the ROOT software framework [2] and 
cannot be run without it. Building this class was solely for educational purposes to 
become an expert on the technique. However I did use it to produce some of the key 
results for my dissertation as well as scientific publications.

[1] G. D’Agostini, Nucl. Instrum. Meth. A **362,** 487 (1995).  
[2] R. Brun and F. Rademakers, _New computing techniques in physics research V. Proceedings, 5th International Workshop, AIHENP ’96, Lausanne, Switzerland, September 2-6, 1996,_ Nucl. Instrum. Meth. A **389,** 81 (1997).


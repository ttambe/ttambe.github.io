---
layout: page
title: Number Systems
description: 
img: assets/img/number_systems.jpg
importance: 1
category: " "
related_publications: 
---

As the demand for both greater arithmetic density and computational accuracy grows, number systems will play an increasingly pivotal role in the design of next-generation computing platforms. There are vast opportunities to explore the algorithm-architecture co-design of novel number systems that provide greater amortization of the PPA costs that scale with arithmetic density, and most importantly, without compromising on computational accuracy. Below is a short summary of my relevant work on this topic so far.

<hr style="border:0.75px solid gray">

Emerging AI models exhibit a parameter distribution spread that far exceeds the dynamic range of commonly-used low-precision data types. Realizing the need for adaptive tensor scaling, we proposed the best paper award-winning number system called [__AdaptivFloat__](http://127.0.0.1:4000/assets/pdf/Tambe_dac_2020_paper.pdf), which informs a generalized floating-point based mathematical blueprint for adaptive and resilient DNN quantization, and that can be easily applied on neural models of various categories (CNN, RNN, Transformers), and parameter statistics. 

In essence, AdaptivFloat introduces in its exponent field an exponent bias that is computed from the maximum absolute value in a given tensor. This allows the datatype to dynamically shift, at a layer, channel, or vector granularity -- its representation range in order to cater to the most impactful parameters in a DNN's weight, activation, or gradient tensor. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/adaptivfloat_conversion.jpg" title="adaptivfloat mechanism" class="img-fluid rounded z-depth-1" %}
        <p class="caption">AdaptivFloat quantization scheme based on exponential bias shift from maximum absolute tensor value.</p>
    </div>
</div>

To facilitate the exploration of newer number formats in the context of deep learning and other emerging applications, we developed and [open-sourced](https://github.com/ma3mool/goldeneye) [__GoldenEye__](https://ma3mool.github.io/files/22-DSN-goldeneye.pdf), a number format simulator that enables the selection of configurable number systems as a first-order parameter when evaluating their impact on DNN classification accuracy. 

We further demonstrated how the number system and the underlying hardware can be optimally co-designed for [reconfigurable architectures](https://dl.acm.org/doi/10.1145/3524059.3532359), and for domain-specific applications such as [robotics](https://ras.papercept.net/conferences/conferences/IROS23/program/IROS23_ContentListWeb_2.html). 

---
layout: page
title: Domain-Specific Architectures
description: 
img: assets/img/domain_hw_arch.jpg
importance: 2
category: " "
related_publications: 
---

The slowdown of transistor scaling coupled with the surging democratization of AI has spurred the rise of application-driven architectures to continue delivering gains in performance and energy efficiency. My PhD work has developed domain-specific hardware architectures for natural language processing (NLP) and AI training workloads as summarized below.


<hr style="border:0.75px solid gray">

1) [EdgeBERT](https://dl.acm.org/doi/abs/10.1145/3466752.3480095) is an algorithm-hardware co-design framework multi-task NLP inference. The EdgeBERT accelerator tailors its latency and energy consumption via entropy-based early exit and dynamic voltage-frequency scaling (DVFS). Computation and memory footprint overheads are further alleviated by employing a calibrated combination of adaptive attention span, selective network pruning, and floating-point quantization. EdgeBERT source code is open-sourced [here](https://github.com/harvard-acc/EdgeBERT).

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/edgebert_accel.jpg" title="EdgeBERT Accelerator" class="img-fluid rounded z-depth-1 mx-auto d-block" width="750" height="550" %}
        <p class="caption">The EdgeBERT hardware accelerator system highlighting its processing and special function units. A fast-switching LDO and fast-locking ADPLL are also integrated for latency-driven DVFS. </p>
    </div>
</div>
<hr style="border:0.75px solid gray">

2) [CAMEL](https://arxiv.org/pdf/2305.03148.pdf) is a model-architecture co-design framework for on-device machine learning training using embedded DRAMs. The specialized accelertor consists of a systolic array core and a hybrid eDRAM-SRAM memory subsystem as illustrated below. The reconfigurable systolic array core utilizes block floating-point (BFP) -based processing elements.

<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.html path="assets/img/camel_accel.jpg" title="CAMEL Accelerator" class="img-fluid rounded z-depth-1" %}
        <p class="caption">CAMEL ML training accelerator. </p>
    </div>
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.html path="assets/img/camel_pe.jpg" title="CAMEL PE" class="img-fluid rounded z-depth-1" %}
        <p class="caption">Block floating-point -based processing element.</p>
    </div>
 </div>
 <hr style="border:0.75px solid gray">

 3) [FlexASR](https://ieeexplore.ieee.org/document/9791855) is a hardware accelerator with [AdaptivFloat](https://arxiv.org/abs/1909.13271)-based processing elements, optimized for attention-based recurrent neural networks used in speech and machine translation AI workloads. FlexASR is open-sourced [here](https://github.com/harvard-acc/FlexASR/).

 <div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.html path="assets/img/flexasr_top.jpg" title="FlexASR Top-Level" class="img-fluid rounded z-depth-1" %}
        <p class="caption">Top-level FlexASR accelerator.</p>
    </div>
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.html path="assets/img/flexasr_pe.jpg" title="FlexASR PE" class="img-fluid rounded z-depth-1" %}
        <p class="caption">AdaptivFloat-based processing element.</p>
    </div>
 </div>
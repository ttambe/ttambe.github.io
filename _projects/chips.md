---
layout: page
title: Chips
description:
img: assets/img/ml_chip.jpg
#redirect: https://unsplash.com
importance: 3
category: " "
---

A pinnacle of my research efforts is to turn architectural proof-of-concepts into physical realizations via ASIC tapeouts in order to demonstrate the real impact of co-optimizing different optimization vectors across the software-architecture-silicon stack. Here are some of these highlights:

<hr style="border:0.75px solid gray">


1) A 12nm Sparse Transformer Processor (STP) that efficiently accelerates transformer workloads by tailoring its latency and energy expenditures according to the complexity of the input query it processes. Key contributions of this work are as follows: (1) A specialized datapath for entropy-based early exit assessment reduces BERT latency by up to 6.13x, e.g., inferences terminate early at an average early exit layer of 3.90 (out of 12) for the SST-2 NLP benchmark; (2) A mixed-precision (MP) FP4/FP8 MAC supports per-vector exponent biases during 4-bit floating point (FP4) computations, allowing the processor to double its throughput while reducing its energy consumption and maintaining high inference accuracy, depending on the entropy; and (3) A fine-grained sentence-level power management scheme opportunistically scales the accelerator’s supply voltage and clock frequency while meeting an application’s end-to-end latency target. Together, the proposed STP achieves a peak efficiency of 65mJ/inf, a 7.14x energy improvement, on average, over conventional BERT inference without the key innovations. [Publication](https://ieeexplore.ieee.org/document/10067817).

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/edgebert_chip.jpg" title="edgebert chip" class="img-fluid rounded z-depth-1 mx-auto d-block" width="550" height="550" %}
    </div>
</div>


<hr style="border:0.75px solid gray">


2) A 16nm system-on-chip for noise-robust speech recognition and NLP featuring hardware acceleration of sequence-to-sequence attention-based DNNs with AdaptivFloat-based processing elements, and unsupervised Bayesian-based speech denoising. The test chip executes a full speech-enhancing ASR pipeline while consuming 2.24mJ of energy per frame and 18ms end-to-end latency -- enabling real-time throughput. [Publication](https://ieeexplore.ieee.org/document/9791855).

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/flexasr_pipeline.jpg" title="sm6 flexasr pipeline" class="img-fluid rounded z-depth-1 mx-auto d-block" %}
    </div>
</div>


<hr style="border:0.75px solid gray">


3) A 16nm programmable accelerator (PGMA) for unsupervised probabilistic machine perception tasks that performs Bayesian inference on probabilistic models mapped onto a 2D Markov Random Field, using MCMC. Exploiting two degrees of parallelism, it performs Gibbs sampling inference at up to 1380x faster with 1965x less energy than an Arm CortexA53 on the same SoC, and 1.5x faster with 6.3x less energy than an embedded FPGA in the same technology. [Publication](https://ieeexplore.ieee.org/document/9162784).

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/pgma.jpg" title="pgma" class="img-fluid rounded z-depth-1 mx-auto d-block" width="300" height="300" %}
    </div>
</div>

<p> <br> </p>
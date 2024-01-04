---
title: "A power calculator for imbalanced experiments"
categories:
  - Blog
tags:
  - e-commerce
  - Experimentation
  - Causal Inference
header:
  teaser: /assets/images/off-balance.jpg
---

In a previous [post](https://ggiannarakis.github.io/blog/rdd/), we delved into the intriguing world of imbalanced experiments, 
and pushed the boundaries to the extreme by entirely omitting a control group.
Now, let's bring things back to a more common scenario, where a smaller control group is actually included in the experiment,
alongside a (much) bigger treatment group. In this context, a first experimental design consideration revolves 
around the implications of this group imbalance on statistical power.

It's a well-known fact that, given a fixed total sample size, **an equal split between control and treatment 
groups maximizes power[^1]**. However, what happens when we deviate from this balance,
say by opting for a 9:1 split? We know that some power is sacrificed, but quantifying this loss becomes crucial.
The question becomes: **How much power are we really losing?**

While power calculators for balanced experiments abound online, 
such as [Evan Miller's Sample Size Calculator](https://www.evanmiller.org/ab-testing/sample-size.html)
or the one from [booking.com](https://bookingcom.github.io/powercalculator/),
finding a calculator tailored for imbalanced scenarios proved to be a challenge. 
This led me to embark on a project of my own, leveraging the power of **Streamlit, Python, and R**.

The [**power calculator for imbalanced experiments**](https://ggiannarakis-imbalanced-power-calc-main-k5d1d9.streamlit.app/)
was designed to answer the critical question:
**What is the statistical power of my experiment when I intentionally introduce an imbalance in group sizes?**
Whether you're considering a 9:1 split or exploring other imbalanced configurations, 
this tool empowers you to make informed decisions about the trade-off between group sizes and statistical power.

You can **try it for yourself** by visiting the [public web app](https://ggiannarakis-imbalanced-power-calc-main-k5d1d9.streamlit.app/)
deployed on Streamlit Community Cloud. For more info, take a look at 
the [Portfolio project](https://ggiannarakis.github.io/portfolio/0.imbalanced/).
[Code](https://github.com/ggiannarakis/imbalanced-power-calc) is also on Github.

[^1]: [https://alexdeng.github.io/causal/abstats.html#statistical-power](https://alexdeng.github.io/causal/abstats.html#statistical-power)
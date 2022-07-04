---
title: "Causal machine learning for sustainable decision-making in agriculture"
categories:
  - Blog
tags:
  - Agriculture
  - Causal Inference
  - Machine Learning
header:
  teaser: /assets/images/germination.jpg
gallery:
  - url: /assets/images/new-cap.png
    image_path: assets/images/new-cap.png
---

There are big changes coming for agriculture in Europe. The Common Agricultural Policy (CAP)
that applies to all member-states was recently revamped, and its new measures come into force
in 2023, to last until 2027.

This comes at a time of soaring inflation and increased food crisis hazard, not to mention
growing demand for agricultural products and complications from extreme climatic events.

To what concerns the policy measures, the EU seems to have learned from past mistakes
and is now adopting smarter options. This is what the new CAP promises:

{% include gallery caption="The official website of the new CAP stresses
the need for targeted support to farmers and for measures that are adapted to local conditions. " %}

This is to be contrasted with past measures that were applied horizontally, and frequently fell short.
footnote here

### What can AI bring to the table?

From the AI perspective, the new CAP has a **Personalization** issue to solve. 
It is unrealistic to expect that the same policy measure, e.g. farmers having to diversify
the crops they grow, will work equally well over agricultural areas that differ along multiple
dimensions. It is clear that decision-making on policy measures should be local,
taking into account the relevant specificities, ideally on a parcel-level.

This is where **causal inference** and **machine learning**, coupled with the right data, can help.

### Enter CATEs

For a farmer, to implement a policy measure is to **intervene** on land. In return, the intervention
is done to achieve a certain sustainable goal, such as to increase
the sequestration of soil organic carbon and thus mitigate climate change. In other words,
interventions are done in order to get a desired result, by driving (causing) an **outcome**
metric of interest. Of course, the particular characteristics of each piece of land such 
as climate, soil, land use will influence the effect magnitude. 

In the Potential Outcomes terminology, we want to learn the following function from data:

$$ \theta (x) = E[Y(1) - Y(0) | X = x] $$

where $$Y(1) \equiv Y(T=1)$$ and $$Y(0) \equiv Y(T=0)$$ are the potential value of the outcome
metric $$Y$$ if an intervention is carried out in a unit $$(T=1)$$ or not $$(T=0)$$.
The expectation is taken over all units, and it is conditional on $$X$$, essentially a feature
vector containing all relevant characteristics of the unit. This is what is known as
a Conditional Average Treatment Effect (CATE).

### Outlook

If we can learn this from data sufficiently well, we have at our disposal a truly powerful
data-driven tool for decision-making: having a good estimate of the effect of alternative
CAP policy measures for a particular parcel, we may simply assign the most-effective intervention
and call it a day.

This is a hard but very important problem to solve, and CATEs are being studied in
various fields, such as personalized medicine, ad targeting and others.

At the National Observatory of Athens, we are leveraging big Earth Observation data
to obtain the information needed for such a problem. Satellite images, weather models, land use,
and other high-resolution geospatial data are used, paired with Computer Vision and ML methods
to extract information from them and feed our analysis. Expect Updates!
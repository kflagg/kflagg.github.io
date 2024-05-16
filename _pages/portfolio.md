---
title: "Portfolio"
permalink: "/portfolio/"
toc: true
---


## Data Consulting


### Analysis of an Electric Fence Permeability Experiment

- Client: Brittani Johnson
- Project Type: [MS thesis](https://scholarworks.montana.edu/handle/1/14687)
- Capacity: graduate assistant consultant at [MSU SCRS](https://www.montana.edu/statisticalconsulting)

#### Project Summary

The client, a master's student in the Department of Animal and Range Sciences
at Montana State University, had conducted an experiment regarding selective
permeability of electric fences to grizzly bears. The objective was to assess
which of two fence designs was better at preventing passage when powered on,
while also not impeding the natural movements of bears throughout their habitat
when powered off. Triangular enclosures of either fence design were set up at
locations around the Blackfoot Valley in western Montana. Bait was placed at
the center of each enclosure. The fences were alternately powered on and off for
several days at a time while trail cameras filmed interactions between grizzly
bears and the fences.

#### Services Provided

- Provided recommendations on model/method selection.
    - The initial recommendation was to use generalized estimating equations
      to implement logistic regression to estimate the probability of bear
      passage, but this was not possible because of small success counts
      at some locations.
    - Several nonparametric hypothesis tests for multidimensional contingency
      tables were used instead.
- Carried out the analysis in R.
- Computed binomial confidence intervals and generated plots summarizing the
  data.


### Analysis of an Advance Directives Completion Intervention

- Client: Christine Fanelli
- Project Type: [DNP capstone project](https://scholarworks.montana.edu/handle/1/12777)
- Capacity: graduate assistant consultant at [MSU SCRS](https://www.montana.edu/statisticalconsulting)

#### Project Summary

The client, a doctor of nursing practice student in the College of Nursing at
Montana State University, had conducted a survey about knowledge of advance
directives among patients aged 65 and older at a family practice clinic in rural
southwestern Montana. The client also implemented an intervention where those
patients were provided with educational materials about advance directives
during their clinic visits. The survey was conducted both before and during the
intervention period, and the objective was to assess if the intervention was
associated with greater rates of patients having advance directives.

#### Services Provided

- Provided recommendations on model/method selection. A logistic regression
  GLM was used.
- Carried out analysis in R.
- Generated plots summarizing the data.
- Recommended wording to explain the statistical methods and results.


### Analysis of a Mental Health Stigma Survey

- Client: Sarah Keller
- Project Type: [internal report](https://scholarworks.montana.edu/handle/1/14927)
  upon which the client based several talks and posters
- Capacity: graduate assistant consultant at [MSU SCRS](https://www.montana.edu/statisticalconsulting)

#### Project Summary

The client, a professor in the Department of Communication and Theatre at
Montana State University, Billings, had conducted an experiment to assess if
an online video-based intervention could reduce stigma around discussing
suicide and mental health among college students at a university in Montana.
Participants were assigned to one of two treatment groups or to a control
group, and completed a questionnaire before viewing a video and then again two
weeks later. The videos viewed by the treatment groups were based upon an
acclaimed theatre program in which local high school and college students
discussed their experiences with depression and suicidal ideation, and the
questionnaire included the Self-Stigma of Seeking Help survey instrument.

#### Services Provided

- Provided recommendations on model/method selection. A linear regression
  model was used.
- Conducted psychometric evaluation of the survey instrument.
- Carried out analysis in R.
- Generated plots summarizing the data.
- Recommended wording to explain the statistical methods and results.


### Analysis of Food Security Survey Data

- Client: Erin Smith
- Project Type: [peer-reviewed research paper](https://doi.org/10.5304/jafscd.2019.09B.011)
- Capacity: graduate assistant consultant at [MSU SCRS](https://www.montana.edu/statisticalconsulting)

#### Project Summary

The client, a master's student in the Department of Health and Human Development
at Montana State University, had conducted a survey where residents of the
Flathead Indian Reservation in western Montana provided interviews and responded
to a questionnaire regarding their food security, their use of wild foods, and
their identities as Native Americans. The objective was to assess the impact of
hunting and gathering on both food security and cultural identity in the context
of climate change affective food availability.

#### Services Provided

- Provided guidance on model/method selection and implementation in JMP.
- Recommended wording to explain the statistical methods and results.
- Copyedited the manuscript.


## Personal Projects


### Trend and Correlation Analysis of Several ETFs

![Log-scale plot of daily values of several index funds and ETFs. UVXY
and SQQQ generally decay over time and FXAIX is very stable. The others move
up and down together. The values are normalized to be 100% at the end of
March 2024.]({{ site.url }}{{ site.baseurl }}/assets/etf/alllog.png)

I conducted this analysis for a
[blog post]({{ site.url }}{{ site.baseurl }}/etf/). The objective was to take
an interesting topic (exchange-traded funds with surprisingly consistent
pricing behavior) and illustrate what a data analysis looks like when it avoids
scope creep and unnecessary complexity. The post follows the process of making
some initial observations, developing hypotheses, obtaining relevant data,
and drawing insights from straightforward visuals and summary tables. Although
the analysis proved inconclusive regarding the initial hypotheses, and I
thought of many new questions for further analysis along the way, I made a point
of sticking to the original purpose and scope.


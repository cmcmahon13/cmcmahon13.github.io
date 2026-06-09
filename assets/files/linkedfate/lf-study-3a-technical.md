---
title: "Linked Fate Study 3a: Technical Appendix"
author: "Casey McMahon"
date: "2026-05-27"
output:
  html_document:
    toc: true
    toc_float:
      collapsed: false
      smooth_scroll: true
    code_folding: hide
    keep_md: true
---

# Study 3a: Black and White Women Workshop Experiment

This technical appendix documents the Study 3a analyses for the linked fate workshop experiment. The study tested whether participants responded differently to gender-equality workshop advertisements depending on the racial composition of the panelists. The main outcomes were linked fate, self-applicability, and inclusion.





## Overview

Study 3a tested whether Black women and White women responded differently to a gender-equality workshop advertisement depending on whether the panel featured mostly Black women or mostly White women. The primary outcomes were self-applicability, inclusion, and linked fate with the featured group.

## Sample and data checks

The visible sample table focuses on participant race because this study intentionally sampled women. I kept the gender check hidden in the source code as a data-cleaning check.



<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Participant race</caption>
 <thead>
  <tr>
   <th> Participant group </th>
   <th> N </th>
   <th> Percent </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Black women </td>
   <td> 201 </td>
   <td> 42.8% </td>
  </tr>
  <tr>
   <td> White women </td>
   <td> 269 </td>
   <td> 57.2% </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Participant age</caption>
 <thead>
  <tr>
   <th> N </th>
   <th> M </th>
   <th> SD </th>
   <th> Min </th>
   <th> Max </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> 470 </td>
   <td> 43.39 </td>
   <td> 13.42 </td>
   <td> 18.00 </td>
   <td> 77.00 </td>
  </tr>
</tbody>
</table>

## Measures and scale construction

Participants responded to all items on 1–7 agreement scales. Higher scores indicate greater self-applicability, greater inclusion, and stronger linked fate.

<div class="measure-card">
  <h3>Self-applicability</h3>
  <ul>
    <li>I feel this workshop was intended for people like me.</li>
    <li>I believe that the workshop organizers were thinking of the experiences of people like me when they created this event.</li>
    <li>This workshop has the experiences of people like me in mind.</li>
  </ul>
</div>

<div class="measure-card">
  <h3>Inclusion</h3>
  <ul>
    <li>I would feel like I did not belong in this workshop. <em>Reverse-coded</em></li>
    <li>I would fit in the general environment of this workshop.</li>
    <li>I would fit in well with the other women at this workshop.</li>
    <li>I would feel out of place at this workshop. <em>Reverse-coded</em></li>
  </ul>
</div>

<div class="measure-card">
  <h3>Linked fate</h3>
  <ul>
    <li>In the workplace, I deal with similar issues as [target group].</li>
    <li>Workplace issues that affect me also affect [target group].</li>
    <li>Efforts to advance [target group] in the workplace will also help people like me to advance.</li>
    <li>Career progress for [target group] will also mean career progress for people like me.</li>
  </ul>
</div>


``` r
# Reverse-coded inclusion items
data <- data %>%
  dplyr::mutate(
    ex_1_r = 8 - ex_1,
    ex_4_r = 8 - ex_4
  ) %>%
  dplyr::mutate(
    sa_mean = rowMeans(
      dplyr::pick(sa_1, sa_2, sa_3),
      na.rm = TRUE
    ),
    in_mean = rowMeans(
      dplyr::pick(ex_1_r, ex_2, ex_3, ex_4_r),
      na.rm = TRUE
    ),
    lf_mean = rowMeans(
      dplyr::pick(lfsb_1, lfsb_2, lfsb_3, lfsb_4),
      na.rm = TRUE
    )
  )

scale_items <- list(
  "Linked fate" = c("lfsb_1", "lfsb_2", "lfsb_3", "lfsb_4"),
  "Self-applicability" = c("sa_1", "sa_2", "sa_3"),
  "Inclusion" = c("ex_1_r", "ex_2", "ex_3", "ex_4_r")
)

scale_vars <- c("lf_mean", "sa_mean", "in_mean")
scale_labels <- c(
  "lf_mean" = "Linked fate",
  "sa_mean" = "Self-applicability",
  "in_mean" = "Inclusion"
)
```

The reliability table reports Cronbach's alpha for each scale. The correlations provide a quick check on how strongly the three outcomes are related.

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Scale reliability</caption>
 <thead>
  <tr>
   <th> Scale </th>
   <th> Cronbach's alpha </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Linked fate </td>
   <td> 0.90 </td>
  </tr>
  <tr>
   <td> Self-applicability </td>
   <td> 0.97 </td>
  </tr>
  <tr>
   <td> Inclusion </td>
   <td> 0.95 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Scale descriptive statistics</caption>
 <thead>
  <tr>
   <th> Scale </th>
   <th> N </th>
   <th> M </th>
   <th> SD </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Linked fate </td>
   <td> 470 </td>
   <td> 4.96 </td>
   <td> 1.54 </td>
  </tr>
  <tr>
   <td> Self-applicability </td>
   <td> 470 </td>
   <td> 5.31 </td>
   <td> 1.46 </td>
  </tr>
  <tr>
   <td> Inclusion </td>
   <td> 470 </td>
   <td> 5.32 </td>
   <td> 1.44 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Scale correlations</caption>
 <thead>
  <tr>
   <th> Scale </th>
   <th> Linked fate </th>
   <th> Self-applicability </th>
   <th> Inclusion </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Linked fate </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
  </tr>
  <tr>
   <td> Self-applicability </td>
   <td> 0.48 </td>
   <td>  </td>
   <td>  </td>
  </tr>
  <tr>
   <td> Inclusion </td>
   <td> 0.36 </td>
   <td> 0.71 </td>
   <td>  </td>
  </tr>
</tbody>
</table>

## Primary ANOVAs

The primary analyses test whether each outcome differed by panel composition, participant race, and their interaction. The interaction term is the most important test because it indicates whether Black women and White women responded differently to the majority-Black versus majority-White workshop panels.


``` r
data <- data %>%
  dplyr::mutate(
    prace_name = factor(prace_name),
    webad_race = factor(webad_race)
  )

sa_aov <- aov(sa_mean ~ webad_race * prace_name, data = data)
in_aov <- aov(in_mean ~ webad_race * prace_name, data = data)
lf_aov <- aov(lf_mean ~ webad_race * prace_name, data = data)
```

### Linked fate

This model tests whether participants felt more linked fate with panels that featured their own racial group than with panels featuring the other group.

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Linked fate ANOVA results</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Effect </th>
   <th style="text-align:center;"> df </th>
   <th style="text-align:center;"> F </th>
   <th style="text-align:center;"> p </th>
   <th style="text-align:center;"> η<sub>p</sub>² </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Workshop composition </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 21.95 </td>
   <td style="text-align:center;"> &lt; .001 </td>
   <td style="text-align:center;"> 0.04 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Participant race </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 8.12 </td>
   <td style="text-align:center;"> 0.005 </td>
   <td style="text-align:center;"> 0.02 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Workshop composition × participant race </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 231.79 </td>
   <td style="text-align:center;"> &lt; .001 </td>
   <td style="text-align:center;"> 0.33 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Linked fate means by participant race and panel composition</caption>
 <thead>
  <tr>
   <th> Participant race </th>
   <th> Panel composition </th>
   <th> N </th>
   <th> M </th>
   <th> SD </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Black women </td>
   <td> Majority Black women panel </td>
   <td> 105 </td>
   <td> 6.00 </td>
   <td> 0.89 </td>
  </tr>
  <tr>
   <td> Black women </td>
   <td> Majority White women panel </td>
   <td> 96 </td>
   <td> 3.44 </td>
   <td> 1.50 </td>
  </tr>
  <tr>
   <td> White women </td>
   <td> Majority Black women panel </td>
   <td> 135 </td>
   <td> 4.62 </td>
   <td> 1.38 </td>
  </tr>
  <tr>
   <td> White women </td>
   <td> Majority White women panel </td>
   <td> 134 </td>
   <td> 5.58 </td>
   <td> 1.12 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Linked fate Tukey-adjusted post hoc comparisons</caption>
 <thead>
  <tr>
   <th> Contrast </th>
   <th> b </th>
   <th> SE </th>
   <th> df </th>
   <th> t </th>
   <th> p </th>
   <th> d </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Black women majority Black women panel - White women majority Black women panel </td>
   <td> 1.38 </td>
   <td> 0.16 </td>
   <td> 466.0 </td>
   <td> 8.58 </td>
   <td> &lt; .001 </td>
   <td> 1.12 </td>
  </tr>
  <tr>
   <td> Black women majority Black women panel - Black women majority White women panel </td>
   <td> 2.56 </td>
   <td> 0.18 </td>
   <td> 466.0 </td>
   <td> 14.62 </td>
   <td> &lt; .001 </td>
   <td> 2.06 </td>
  </tr>
  <tr>
   <td> Black women majority Black women panel - White women majority White women panel </td>
   <td> 0.42 </td>
   <td> 0.16 </td>
   <td> 466.0 </td>
   <td> 2.61 </td>
   <td> 0.046 </td>
   <td> 0.34 </td>
  </tr>
  <tr>
   <td> White women majority Black women panel - Black women majority White women panel </td>
   <td> 1.18 </td>
   <td> 0.17 </td>
   <td> 466.0 </td>
   <td> 7.11 </td>
   <td> &lt; .001 </td>
   <td> 0.95 </td>
  </tr>
  <tr>
   <td> White women majority Black women panel - White women majority White women panel </td>
   <td> -0.96 </td>
   <td> 0.15 </td>
   <td> 466.0 </td>
   <td> -6.36 </td>
   <td> &lt; .001 </td>
   <td> -0.78 </td>
  </tr>
  <tr>
   <td> Black women majority White women panel - White women majority White women panel </td>
   <td> -2.14 </td>
   <td> 0.17 </td>
   <td> 466.0 </td>
   <td> -12.90 </td>
   <td> &lt; .001 </td>
   <td> -1.72 </td>
  </tr>
</tbody>
</table>

### Self-applicability

This model tests whether the workshop felt more applicable to participants when the panel featured mostly women from their own racial group.

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Self-applicability ANOVA results</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Effect </th>
   <th style="text-align:center;"> df </th>
   <th style="text-align:center;"> F </th>
   <th style="text-align:center;"> p </th>
   <th style="text-align:center;"> η<sub>p</sub>² </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Workshop composition </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 4.36 </td>
   <td style="text-align:center;"> 0.037 </td>
   <td style="text-align:center;"> 0.01 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Participant race </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 10.18 </td>
   <td style="text-align:center;"> 0.002 </td>
   <td style="text-align:center;"> 0.02 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Workshop composition × participant race </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 8.76 </td>
   <td style="text-align:center;"> 0.003 </td>
   <td style="text-align:center;"> 0.02 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Self-applicability means by participant race and panel composition</caption>
 <thead>
  <tr>
   <th> Participant race </th>
   <th> Panel composition </th>
   <th> N </th>
   <th> M </th>
   <th> SD </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Black women </td>
   <td> Majority Black women panel </td>
   <td> 105 </td>
   <td> 5.90 </td>
   <td> 1.09 </td>
  </tr>
  <tr>
   <td> Black women </td>
   <td> Majority White women panel </td>
   <td> 96 </td>
   <td> 5.18 </td>
   <td> 1.41 </td>
  </tr>
  <tr>
   <td> White women </td>
   <td> Majority Black women panel </td>
   <td> 135 </td>
   <td> 5.09 </td>
   <td> 1.49 </td>
  </tr>
  <tr>
   <td> White women </td>
   <td> Majority White women panel </td>
   <td> 134 </td>
   <td> 5.16 </td>
   <td> 1.59 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Self-applicability Tukey-adjusted post hoc comparisons</caption>
 <thead>
  <tr>
   <th> Contrast </th>
   <th> b </th>
   <th> SE </th>
   <th> df </th>
   <th> t </th>
   <th> p </th>
   <th> d </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Black women majority Black women panel - White women majority Black women panel </td>
   <td> 0.81 </td>
   <td> 0.19 </td>
   <td> 466.0 </td>
   <td> 4.35 </td>
   <td> &lt; .001 </td>
   <td> 0.57 </td>
  </tr>
  <tr>
   <td> Black women majority Black women panel - Black women majority White women panel </td>
   <td> 0.72 </td>
   <td> 0.20 </td>
   <td> 466.0 </td>
   <td> 3.56 </td>
   <td> 0.002 </td>
   <td> 0.50 </td>
  </tr>
  <tr>
   <td> Black women majority Black women panel - White women majority White women panel </td>
   <td> 0.74 </td>
   <td> 0.19 </td>
   <td> 466.0 </td>
   <td> 3.97 </td>
   <td> &lt; .001 </td>
   <td> 0.52 </td>
  </tr>
  <tr>
   <td> White women majority Black women panel - Black women majority White women panel </td>
   <td> -0.09 </td>
   <td> 0.19 </td>
   <td> 466.0 </td>
   <td> -0.47 </td>
   <td> 0.965 </td>
   <td> -0.06 </td>
  </tr>
  <tr>
   <td> White women majority Black women panel - White women majority White women panel </td>
   <td> -0.07 </td>
   <td> 0.17 </td>
   <td> 466.0 </td>
   <td> -0.40 </td>
   <td> 0.978 </td>
   <td> -0.05 </td>
  </tr>
  <tr>
   <td> Black women majority White women panel - White women majority White women panel </td>
   <td> 0.02 </td>
   <td> 0.19 </td>
   <td> 466.0 </td>
   <td> 0.10 </td>
   <td> 1.000 </td>
   <td> 0.01 </td>
  </tr>
</tbody>
</table>

### Inclusion

This model tests whether the workshop environment felt more inclusive when the panel featured mostly women from the participant's own racial group.

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Inclusion ANOVA results</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Effect </th>
   <th style="text-align:center;"> df </th>
   <th style="text-align:center;"> F </th>
   <th style="text-align:center;"> p </th>
   <th style="text-align:center;"> η<sub>p</sub>² </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Workshop composition </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 6.39 </td>
   <td style="text-align:center;"> 0.012 </td>
   <td style="text-align:center;"> 0.01 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Participant race </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 17.90 </td>
   <td style="text-align:center;"> &lt; .001 </td>
   <td style="text-align:center;"> 0.04 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Workshop composition × participant race </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 3.88 </td>
   <td style="text-align:center;"> 0.049 </td>
   <td style="text-align:center;"> 0.01 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Inclusion means by participant race and panel composition</caption>
 <thead>
  <tr>
   <th> Participant race </th>
   <th> Panel composition </th>
   <th> N </th>
   <th> M </th>
   <th> SD </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Black women </td>
   <td> Majority Black women panel </td>
   <td> 105 </td>
   <td> 5.94 </td>
   <td> 0.95 </td>
  </tr>
  <tr>
   <td> Black women </td>
   <td> Majority White women panel </td>
   <td> 96 </td>
   <td> 5.32 </td>
   <td> 1.38 </td>
  </tr>
  <tr>
   <td> White women </td>
   <td> Majority Black women panel </td>
   <td> 135 </td>
   <td> 5.13 </td>
   <td> 1.52 </td>
  </tr>
  <tr>
   <td> White women </td>
   <td> Majority White women panel </td>
   <td> 134 </td>
   <td> 5.03 </td>
   <td> 1.59 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Inclusion Tukey-adjusted post hoc comparisons</caption>
 <thead>
  <tr>
   <th> Contrast </th>
   <th> b </th>
   <th> SE </th>
   <th> df </th>
   <th> t </th>
   <th> p </th>
   <th> d </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Black women majority Black women panel - White women majority Black women panel </td>
   <td> 0.81 </td>
   <td> 0.18 </td>
   <td> 466.0 </td>
   <td> 4.41 </td>
   <td> &lt; .001 </td>
   <td> 0.57 </td>
  </tr>
  <tr>
   <td> Black women majority Black women panel - Black women majority White women panel </td>
   <td> 0.61 </td>
   <td> 0.20 </td>
   <td> 466.0 </td>
   <td> 3.09 </td>
   <td> 0.012 </td>
   <td> 0.44 </td>
  </tr>
  <tr>
   <td> Black women majority Black women panel - White women majority White women panel </td>
   <td> 0.90 </td>
   <td> 0.18 </td>
   <td> 466.0 </td>
   <td> 4.92 </td>
   <td> &lt; .001 </td>
   <td> 0.64 </td>
  </tr>
  <tr>
   <td> White women majority Black women panel - Black women majority White women panel </td>
   <td> -0.19 </td>
   <td> 0.19 </td>
   <td> 466.0 </td>
   <td> -1.03 </td>
   <td> 0.732 </td>
   <td> -0.14 </td>
  </tr>
  <tr>
   <td> White women majority Black women panel - White women majority White women panel </td>
   <td> 0.10 </td>
   <td> 0.17 </td>
   <td> 466.0 </td>
   <td> 0.56 </td>
   <td> 0.944 </td>
   <td> 0.07 </td>
  </tr>
  <tr>
   <td> Black women majority White women panel - White women majority White women panel </td>
   <td> 0.29 </td>
   <td> 0.19 </td>
   <td> 466.0 </td>
   <td> 1.54 </td>
   <td> 0.415 </td>
   <td> 0.21 </td>
  </tr>
</tbody>
</table>

Together, these analyses test whether representation in the workshop advertisement shaped linked fate, self-applicability, and inclusion differently for Black women and White women.

## Mediation models

The mediation model tests whether linked fate explains why cross-race workshop panels were evaluated differently by Black women and White women. The analysis uses only the cross-race workshop conditions: White women viewing the majority-Black panel and Black women viewing the majority-White panel. Participant race is coded 0 = White women and 1 = Black women, so negative indirect effects indicate pathways that help explain lower self-applicability or inclusion among Black women relative to White women in the cross-race conditions.


``` r
data <- data %>%
  dplyr::mutate(
    prace_process = dplyr::case_when(
      race == 1 ~ 1,
      race == 4 ~ 0,
      TRUE ~ NA_real_
    ),
    targ_gp_process = dplyr::case_when(
      webad_race == "majority black" ~ 1,
      webad_race == "majority white" ~ 0,
      TRUE ~ NA_real_
    ),
    comparison = dplyr::case_when(
      prace_process == 0 & targ_gp_process == 0 ~ "ww_ww",
      prace_process == 0 & targ_gp_process == 1 ~ "ww_focal",
      prace_process == 1 & targ_gp_process == 0 ~ "focal_ww",
      prace_process == 1 & targ_gp_process == 1 ~ "focal_focal",
      TRUE ~ NA_character_
    )
  )

data_sub <- data %>%
  dplyr::filter(comparison %in% c("ww_focal", "focal_ww"))

sa_mediation_results <- run_simple_mediation(
  data = data_sub,
  x = "prace_process",
  m = "lf_mean",
  y = "sa_mean",
  x_label = "Participant race",
  m_label = "linked fate",
  y_label = "Self-applicability",
  boot = 10000,
  seed = 654321
)

in_mediation_results <- run_simple_mediation(
  data = data_sub,
  x = "prace_process",
  m = "lf_mean",
  y = "in_mean",
  x_label = "Participant race",
  m_label = "linked fate",
  y_label = "Inclusion",
  boot = 10000,
  seed = 654321
)
```

### Self-applicability mediation

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Self-applicability mediation effects</caption>
 <thead>
  <tr>
   <th style="text-align:center;"> Effect </th>
   <th style="text-align:center;"> Description </th>
   <th style="text-align:center;"> Estimate </th>
   <th style="text-align:center;"> SE </th>
   <th style="text-align:center;"> 95% CI </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> a path </td>
   <td style="text-align:center;"> Participant race → linked fate </td>
   <td style="text-align:center;"> -1.18 </td>
   <td style="text-align:center;"> 0.19 </td>
   <td style="text-align:center;"> [-1.55, -0.79] </td>
  </tr>
  <tr>
   <td style="text-align:center;"> b path </td>
   <td style="text-align:center;"> linked fate → Self-applicability </td>
   <td style="text-align:center;"> 0.46 </td>
   <td style="text-align:center;"> 0.06 </td>
   <td style="text-align:center;"> [0.32, 0.59] </td>
  </tr>
  <tr>
   <td style="text-align:center;"> Total effect </td>
   <td style="text-align:center;"> Participant race → Self-applicability </td>
   <td style="text-align:center;"> 0.09 </td>
   <td style="text-align:center;"> 0.19 </td>
   <td style="text-align:center;"> [-0.29, 0.46] </td>
  </tr>
  <tr>
   <td style="text-align:center;"> Direct effect </td>
   <td style="text-align:center;"> Participant race → Self-applicability adjusting for linked fate </td>
   <td style="text-align:center;"> 0.63 </td>
   <td style="text-align:center;"> 0.19 </td>
   <td style="text-align:center;"> [0.26, 0.99] </td>
  </tr>
  <tr>
   <td style="text-align:center;"> Indirect effect </td>
   <td style="text-align:center;"> Participant race → linked fate → Self-applicability </td>
   <td style="text-align:center;"> -0.54 </td>
   <td style="text-align:center;"> 0.11 </td>
   <td style="text-align:center;"> [-0.78, -0.33] </td>
  </tr>
</tbody>
</table>

### Inclusion mediation

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Inclusion mediation effects</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Effect </th>
   <th style="text-align:left;"> Description </th>
   <th style="text-align:center;"> Estimate </th>
   <th style="text-align:center;"> SE </th>
   <th style="text-align:center;"> 95% CI </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> a path </td>
   <td style="text-align:left;"> Participant race → linked fate </td>
   <td style="text-align:center;"> -1.18 </td>
   <td style="text-align:center;"> 0.19 </td>
   <td style="text-align:center;"> [-1.55, -0.79] </td>
  </tr>
  <tr>
   <td style="text-align:left;"> b path </td>
   <td style="text-align:left;"> linked fate → Inclusion </td>
   <td style="text-align:center;"> 0.33 </td>
   <td style="text-align:center;"> 0.06 </td>
   <td style="text-align:center;"> [0.18, 0.48] </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Total effect </td>
   <td style="text-align:left;"> Participant race → Inclusion </td>
   <td style="text-align:center;"> 0.19 </td>
   <td style="text-align:center;"> 0.20 </td>
   <td style="text-align:center;"> [-0.19, 0.58] </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Direct effect </td>
   <td style="text-align:left;"> Participant race → Inclusion adjusting for linked fate </td>
   <td style="text-align:center;"> 0.59 </td>
   <td style="text-align:center;"> 0.20 </td>
   <td style="text-align:center;"> [0.18, 0.98] </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Indirect effect </td>
   <td style="text-align:left;"> Participant race → linked fate → Inclusion </td>
   <td style="text-align:center;"> -0.39 </td>
   <td style="text-align:center;"> 0.10 </td>
   <td style="text-align:center;"> [-0.60, -0.20] </td>
  </tr>
</tbody>
</table>

The mediation tables show whether linked fate statistically accounts for differences in self-applicability and inclusion in the cross-race workshop conditions. Significant indirect effects indicate that lower linked fate helps explain why the same gender-equality workshop may feel less applicable or inclusive for Black women when the panel primarily features the other racial group.

---
title: "Linked Fate Study 3b: Technical Appendix"
author: "Casey McMahon"
date: "2026-05-14"
output:
  html_document:
    toc: true
    toc_float:
      collapsed: false
      smooth_scroll: true
    code_folding: hide
    keep_md: true
---

# Study 3b: Latina and White Women Workshop Experiment

This technical appendix documents the Study 3b analyses for the linked fate workshop experiment. The study tested whether participants responded differently to gender-equality workshop advertisements depending on the racial composition of the panelists. The main outcomes were linked fate, self-applicability, and inclusion.





## Overview

Study 3b tested whether Latina women and White women responded differently to a gender-equality workshop advertisement depending on whether the panel featured mostly Latina women or mostly White women. The primary outcomes were self-applicability, inclusion, and linked fate with the featured group.

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
   <td> Latina women </td>
   <td> 292 </td>
   <td> 46.7% </td>
  </tr>
  <tr>
   <td> White women </td>
   <td> 333 </td>
   <td> 53.3% </td>
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
   <td> 623 </td>
   <td> 38.14 </td>
   <td> 12.66 </td>
   <td> 18.00 </td>
   <td> 95.00 </td>
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
    ex_1_r = dplyr::case_when(
      ex_1 == 1 ~ 7,
      ex_1 == 2 ~ 6,
      ex_1 == 3 ~ 5,
      ex_1 == 4 ~ 4,
      ex_1 == 5 ~ 3,
      ex_1 == 6 ~ 2,
      ex_1 == 7 ~ 1,
      TRUE ~ NA_real_
    ),
    ex_4_r = dplyr::case_when(
      ex_4 == 1 ~ 7,
      ex_4 == 2 ~ 6,
      ex_4 == 3 ~ 5,
      ex_4 == 4 ~ 4,
      ex_4 == 5 ~ 3,
      ex_4 == 6 ~ 2,
      ex_4 == 7 ~ 1,
      TRUE ~ NA_real_
    ),
    sa_mean = furniture::rowmeans(dplyr::select(., sa_1, sa_2, sa_3)),
    in_mean = furniture::rowmeans(dplyr::select(., ex_1_r, ex_2, ex_3, ex_4_r)),
    lf_mean = furniture::rowmeans(dplyr::select(., lfsb_1, lfsb_2, lfsb_3, lfsb_4))
  )

scale_items <- list(
  "Self-applicability" = c("sa_1", "sa_2", "sa_3"),
  "Inclusion" = c("ex_1_r", "ex_2", "ex_3", "ex_4_r"),
  "Linked fate" = c("lfsb_1", "lfsb_2", "lfsb_3", "lfsb_4")
)

scale_vars <- c("sa_mean", "in_mean", "lf_mean")
scale_labels <- c(
  "sa_mean" = "Self-applicability",
  "in_mean" = "Inclusion",
  "lf_mean" = "Linked fate"
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
   <td> Self-applicability </td>
   <td> 0.96 </td>
  </tr>
  <tr>
   <td> Inclusion </td>
   <td> 0.93 </td>
  </tr>
  <tr>
   <td> Linked fate </td>
   <td> 0.89 </td>
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
   <td> Inclusion </td>
   <td> 625 </td>
   <td> 83.95 </td>
   <td> 40.20 </td>
  </tr>
  <tr>
   <td> Linked fate </td>
   <td> 625 </td>
   <td> 5.00 </td>
   <td> 1.31 </td>
  </tr>
  <tr>
   <td> Self-applicability </td>
   <td> 625 </td>
   <td> 5.16 </td>
   <td> 1.41 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Scale correlations</caption>
 <thead>
  <tr>
   <th> Scale </th>
   <th> Self-applicability </th>
   <th> Inclusion </th>
   <th> Linked fate </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Self-applicability </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
  </tr>
  <tr>
   <td> Inclusion </td>
   <td> 0.12 </td>
   <td>  </td>
   <td>  </td>
  </tr>
  <tr>
   <td> Linked fate </td>
   <td> 0.54 </td>
   <td> 0.04 </td>
   <td>  </td>
  </tr>
</tbody>
</table>

## Primary ANOVAs

The primary analyses test whether each outcome differed by panel composition, participant race, and their interaction. The interaction term is the most important test because it indicates whether Latina women and White women responded differently to the majority-Latina versus majority-White workshop panels.


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
   <th> Effect </th>
   <th> df </th>
   <th> F </th>
   <th> p </th>
   <th> η<sub>p</sub>² </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> webad_race </td>
   <td> 1 </td>
   <td> 15.71 </td>
   <td> 
   </td>
<td> 0.02 </td>
  </tr>
  <tr>
   <td> prace_name </td>
   <td> 1 </td>
   <td> 1.34 </td>
   <td> 0.248 </td>
   <td> 0.00 </td>
  </tr>
  <tr>
   <td> webad_race × prace_name </td>
   <td> 1 </td>
   <td> 161.08 </td>
   <td> 
   </td>
<td> 0.21 </td>
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
   <td> Latina women </td>
   <td> Majority Latina women panel </td>
   <td> 144 </td>
   <td> 5.88 </td>
   <td> 0.94 </td>
  </tr>
  <tr>
   <td> Latina women </td>
   <td> Majority White women panel </td>
   <td> 148 </td>
   <td> 4.26 </td>
   <td> 1.28 </td>
  </tr>
  <tr>
   <td> White women </td>
   <td> Majority Latina women panel </td>
   <td> 164 </td>
   <td> 4.58 </td>
   <td> 1.25 </td>
  </tr>
  <tr>
   <td> White women </td>
   <td> Majority White women panel </td>
   <td> 169 </td>
   <td> 5.31 </td>
   <td> 1.14 </td>
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
   <td> Latina women majority Latina women panel - White women majority Latina women panel </td>
   <td> 1.31 </td>
   <td> 0.13 </td>
   <td> 621.0 </td>
   <td> 9.85 </td>
   <td> 
   </td>
<td> 1.12 </td>
  </tr>
  <tr>
   <td> Latina women majority Latina women panel - Latina women majority White women panel </td>
   <td> 1.63 </td>
   <td> 0.14 </td>
   <td> 621.0 </td>
   <td> 11.97 </td>
   <td> 
   </td>
<td> 1.40 </td>
  </tr>
  <tr>
   <td> Latina women majority Latina women panel - White women majority White women panel </td>
   <td> 0.57 </td>
   <td> 0.13 </td>
   <td> 621.0 </td>
   <td> 4.33 </td>
   <td> 
   </td>
<td> 0.49 </td>
  </tr>
  <tr>
   <td> White women majority Latina women panel - Latina women majority White women panel </td>
   <td> 0.32 </td>
   <td> 0.13 </td>
   <td> 621.0 </td>
   <td> 2.44 </td>
   <td> 0.071 </td>
   <td> 0.28 </td>
  </tr>
  <tr>
   <td> White women majority Latina women panel - White women majority White women panel </td>
   <td> -0.74 </td>
   <td> 0.13 </td>
   <td> 621.0 </td>
   <td> -5.78 </td>
   <td> 
   </td>
<td> -0.63 </td>
  </tr>
  <tr>
   <td> Latina women majority White women panel - White women majority White women panel </td>
   <td> -1.06 </td>
   <td> 0.13 </td>
   <td> 621.0 </td>
   <td> -8.09 </td>
   <td> 
   </td>
<td> -0.91 </td>
  </tr>
</tbody>
</table>

### Self-applicability

This model tests whether the workshop felt more applicable to participants when the panel featured mostly women from their own racial group.

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Self-applicability ANOVA results</caption>
 <thead>
  <tr>
   <th> Effect </th>
   <th> df </th>
   <th> F </th>
   <th> p </th>
   <th> η<sub>p</sub>² </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> webad_race </td>
   <td> 1 </td>
   <td> 8.91 </td>
   <td> 0.003 </td>
   <td> 0.01 </td>
  </tr>
  <tr>
   <td> prace_name </td>
   <td> 1 </td>
   <td> 12.08 </td>
   <td> 
   </td>
<td> 0.02 </td>
  </tr>
  <tr>
   <td> webad_race × prace_name </td>
   <td> 1 </td>
   <td> 20.44 </td>
   <td> 
   </td>
<td> 0.03 </td>
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
   <td> Latina women </td>
   <td> Majority Latina women panel </td>
   <td> 144 </td>
   <td> 5.80 </td>
   <td> 1.00 </td>
  </tr>
  <tr>
   <td> Latina women </td>
   <td> Majority White women panel </td>
   <td> 148 </td>
   <td> 4.95 </td>
   <td> 1.48 </td>
  </tr>
  <tr>
   <td> White women </td>
   <td> Majority Latina women panel </td>
   <td> 164 </td>
   <td> 4.92 </td>
   <td> 1.39 </td>
  </tr>
  <tr>
   <td> White women </td>
   <td> Majority White women panel </td>
   <td> 169 </td>
   <td> 5.05 </td>
   <td> 1.50 </td>
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
   <td> Latina women majority Latina women panel - White women majority Latina women panel </td>
   <td> 0.88 </td>
   <td> 0.16 </td>
   <td> 621.0 </td>
   <td> 5.66 </td>
   <td> 
   </td>
<td> 0.65 </td>
  </tr>
  <tr>
   <td> Latina women majority Latina women panel - Latina women majority White women panel </td>
   <td> 0.85 </td>
   <td> 0.16 </td>
   <td> 621.0 </td>
   <td> 5.34 </td>
   <td> 
   </td>
<td> 0.62 </td>
  </tr>
  <tr>
   <td> Latina women majority Latina women panel - White women majority White women panel </td>
   <td> 0.75 </td>
   <td> 0.15 </td>
   <td> 621.0 </td>
   <td> 4.82 </td>
   <td> 
   </td>
<td> 0.55 </td>
  </tr>
  <tr>
   <td> White women majority Latina women panel - Latina women majority White women panel </td>
   <td> -0.03 </td>
   <td> 0.15 </td>
   <td> 621.0 </td>
   <td> -0.19 </td>
   <td> 0.998 </td>
   <td> -0.02 </td>
  </tr>
  <tr>
   <td> White women majority Latina women panel - White women majority White women panel </td>
   <td> -0.14 </td>
   <td> 0.15 </td>
   <td> 621.0 </td>
   <td> -0.91 </td>
   <td> 0.798 </td>
   <td> -0.10 </td>
  </tr>
  <tr>
   <td> Latina women majority White women panel - White women majority White women panel </td>
   <td> -0.11 </td>
   <td> 0.15 </td>
   <td> 621.0 </td>
   <td> -0.70 </td>
   <td> 0.898 </td>
   <td> -0.08 </td>
  </tr>
</tbody>
</table>

### Inclusion

This model tests whether the workshop environment felt more inclusive when the panel featured mostly women from the participant's own racial group.

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Inclusion ANOVA results</caption>
 <thead>
  <tr>
   <th> Effect </th>
   <th> df </th>
   <th> F </th>
   <th> p </th>
   <th> η<sub>p</sub>² </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> webad_race </td>
   <td> 1 </td>
   <td> 0.25 </td>
   <td> 0.618 </td>
   <td> 0.00 </td>
  </tr>
  <tr>
   <td> prace_name </td>
   <td> 1 </td>
   <td> 656.92 </td>
   <td> 
   </td>
<td> 0.51 </td>
  </tr>
  <tr>
   <td> webad_race × prace_name </td>
   <td> 1 </td>
   <td> 0.01 </td>
   <td> 0.925 </td>
   <td> 0.00 </td>
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
   <td> Latina women </td>
   <td> Majority Latina women panel </td>
   <td> 144 </td>
   <td> 114.00 </td>
   <td> 29.43 </td>
  </tr>
  <tr>
   <td> Latina women </td>
   <td> Majority White women panel </td>
   <td> 148 </td>
   <td> 115.38 </td>
   <td> 28.00 </td>
  </tr>
  <tr>
   <td> White women </td>
   <td> Majority Latina women panel </td>
   <td> 164 </td>
   <td> 56.50 </td>
   <td> 27.15 </td>
  </tr>
  <tr>
   <td> White women </td>
   <td> Majority White women panel </td>
   <td> 169 </td>
   <td> 57.46 </td>
   <td> 27.88 </td>
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
   <td> Latina women majority Latina women panel - White women majority Latina women panel </td>
   <td> 57.50 </td>
   <td> 3.21 </td>
   <td> 621.0 </td>
   <td> 17.93 </td>
   <td> 
   </td>
<td> 2.05 </td>
  </tr>
  <tr>
   <td> Latina women majority Latina women panel - Latina women majority White women panel </td>
   <td> -1.39 </td>
   <td> 3.29 </td>
   <td> 621.0 </td>
   <td> -0.42 </td>
   <td> 0.975 </td>
   <td> -0.05 </td>
  </tr>
  <tr>
   <td> Latina women majority Latina women panel - White women majority White women panel </td>
   <td> 56.54 </td>
   <td> 3.19 </td>
   <td> 621.0 </td>
   <td> 17.75 </td>
   <td> 
   </td>
<td> 2.01 </td>
  </tr>
  <tr>
   <td> White women majority Latina women panel - Latina women majority White women panel </td>
   <td> -58.88 </td>
   <td> 3.18 </td>
   <td> 621.0 </td>
   <td> -18.49 </td>
   <td> 
   </td>
<td> -2.10 </td>
  </tr>
  <tr>
   <td> White women majority Latina women panel - White women majority White women panel </td>
   <td> -0.96 </td>
   <td> 3.08 </td>
   <td> 621.0 </td>
   <td> -0.31 </td>
   <td> 0.989 </td>
   <td> -0.03 </td>
  </tr>
  <tr>
   <td> Latina women majority White women panel - White women majority White women panel </td>
   <td> 57.92 </td>
   <td> 3.16 </td>
   <td> 621.0 </td>
   <td> 18.32 </td>
   <td> 
   </td>
<td> 2.06 </td>
  </tr>
</tbody>
</table>

Together, these analyses test whether representation in the workshop advertisement shaped linked fate, self-applicability, and inclusion differently for Latina women and White women.

## Mediation models

The mediation model tests whether linked fate explains why cross-race workshop panels were evaluated differently by Latina women and White women. The analysis uses only the cross-race workshop conditions: White women viewing the majority-Latina panel and Latina women viewing the majority-White panel. Participant race is coded 0 = White women and 1 = Latina women, so negative indirect effects indicate pathways that help explain lower self-applicability or inclusion among Latina women relative to White women in the cross-race conditions.


``` r
data <- data %>%
  dplyr::mutate(
    prace_process = dplyr::case_when(
      race_2 == 2 ~ 1,
      race_2 == 4 ~ 0,
      TRUE ~ NA_real_
    ),
    targ_gp_process = dplyr::case_when(
      webad_race == "majority latina" ~ 1,
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
  boot = 10000,
  seed = 654321
)

in_mediation_results <- run_simple_mediation(
  data = data_sub,
  x = "prace_process",
  m = "lf_mean",
  y = "in_mean",
  boot = 10000,
  seed = 654321
)
```

### Self-applicability mediation

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Self-applicability mediation paths and indirect effect</caption>
 <thead>
  <tr>
   <th> Path </th>
   <th> Estimate </th>
   <th> SE </th>
   <th> 95% CI </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> a path: participant race → linked fate </td>
   <td> -0.32 </td>
   <td> 0.14 </td>
   <td>  </td>
  </tr>
  <tr>
   <td> b path: linked fate → sa_mean </td>
   <td> 0.46 </td>
   <td> 0.06 </td>
   <td>  </td>
  </tr>
  <tr>
   <td> Indirect effect: participant race → linked fate → sa_mean </td>
   <td> -0.15 </td>
   <td> 0.07 </td>
   <td> [-0.30, -0.02] </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Self-applicability total, direct, and indirect effects</caption>
 <thead>
  <tr>
   <th> Effect </th>
   <th> Estimate </th>
   <th> SE </th>
   <th> 95% CI </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Total effect </td>
   <td> 0.03 </td>
   <td> 0.16 </td>
   <td> [-0.30, 0.34] </td>
  </tr>
  <tr>
   <td> Direct effect </td>
   <td> 0.18 </td>
   <td> 0.15 </td>
   <td> [-0.12, 0.47] </td>
  </tr>
  <tr>
   <td> Indirect effect </td>
   <td> -0.15 </td>
   <td> 0.07 </td>
   <td> [-0.30, -0.02] </td>
  </tr>
</tbody>
</table>

### Inclusion mediation

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Inclusion mediation paths and indirect effect</caption>
 <thead>
  <tr>
   <th> Path </th>
   <th> Estimate </th>
   <th> SE </th>
   <th> 95% CI </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> a path: participant race → linked fate </td>
   <td> -0.32 </td>
   <td> 0.14 </td>
   <td>  </td>
  </tr>
  <tr>
   <td> b path: linked fate → in_mean </td>
   <td> 1.59 </td>
   <td> 1.24 </td>
   <td>  </td>
  </tr>
  <tr>
   <td> Indirect effect: participant race → linked fate → in_mean </td>
   <td> -0.51 </td>
   <td> 0.53 </td>
   <td> [-1.78, 0.29] </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Inclusion total, direct, and indirect effects</caption>
 <thead>
  <tr>
   <th> Effect </th>
   <th> Estimate </th>
   <th> SE </th>
   <th> 95% CI </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Total effect </td>
   <td> 58.88 </td>
   <td> 3.12 </td>
   <td> [52.59, 65.00] </td>
  </tr>
  <tr>
   <td> Direct effect </td>
   <td> 59.39 </td>
   <td> 3.15 </td>
   <td> [53.27, 65.47] </td>
  </tr>
  <tr>
   <td> Indirect effect </td>
   <td> -0.51 </td>
   <td> 0.53 </td>
   <td> [-1.78, 0.29] </td>
  </tr>
</tbody>
</table>

The mediation tables show whether linked fate statistically accounts for differences in self-applicability and inclusion in the cross-race workshop conditions. Significant indirect effects indicate that lower linked fate helps explain why the same gender-equality workshop may feel less applicable or inclusive when the panel primarily features the other racial group.

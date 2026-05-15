---
title: "Linked Fate Study 2a: Technical Appendix"
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

# Study 2a: Black Women and White Women

This technical appendix documents the Study 2a analyses for the linked fate project. The study examines whether Black women and White women differ in perceived linked fate and whether those differences are explained by perceived relational orientation and workplace treatment by people high in power and status.






## Sample characteristics

This section verifies the analytic sample and summarizes participant demographics.

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
   <td> 203 </td>
   <td> 49.51 </td>
  </tr>
  <tr>
   <td> White women </td>
   <td> 207 </td>
   <td> 50.49 </td>
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
   <td> 410 </td>
   <td> 43.69 </td>
   <td> 13.81 </td>
   <td> 19 </td>
   <td> 79 </td>
  </tr>
</tbody>
</table>

## Measurement check: exploratory factor analysis

The exploratory factor analysis checks whether the mediator items cluster in ways that are consistent with the planned scale construction. This section is used as a measurement check before creating composite scores for the main analyses.

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Factor-analysis diagnostics</caption>
 <thead>
  <tr>
   <th> Diagnostic </th>
   <th> Value </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> KMO overall MSA </td>
   <td> 0.851 </td>
  </tr>
  <tr>
   <td> Bartlett's test χ² </td>
   <td> 9525.66 </td>
  </tr>
  <tr>
   <td> Bartlett's test p </td>
   <td> &lt; .001 </td>
  </tr>
  <tr>
   <td> Correlation matrix determinant </td>
   <td> 4.24e-11 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>First 10 eigenvalues</caption>
 <thead>
  <tr>
   <th> Factor </th>
   <th> Eigenvalue </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> 1 </td>
   <td> 7.17 </td>
  </tr>
  <tr>
   <td> 2 </td>
   <td> 4.66 </td>
  </tr>
  <tr>
   <td> 3 </td>
   <td> 3.77 </td>
  </tr>
  <tr>
   <td> 4 </td>
   <td> 1.83 </td>
  </tr>
  <tr>
   <td> 5 </td>
   <td> 1.58 </td>
  </tr>
  <tr>
   <td> 6 </td>
   <td> 1.22 </td>
  </tr>
  <tr>
   <td> 7 </td>
   <td> 1.13 </td>
  </tr>
  <tr>
   <td> 8 </td>
   <td> 0.92 </td>
  </tr>
  <tr>
   <td> 9 </td>
   <td> 0.67 </td>
  </tr>
  <tr>
   <td> 10 </td>
   <td> 0.57 </td>
  </tr>
</tbody>
</table>

<details>
<summary><strong>Show exploratory factor solution tables</strong></summary>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Five-factor solution</caption>
 <thead>
  <tr>
   <th> Item </th>
   <th> ML3 </th>
   <th> ML1 </th>
   <th> ML2 </th>
   <th> ML5 </th>
   <th> ML4 </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> sup_wb_1 </td>
   <td> -0.82 </td>
   <td> 0.05 </td>
   <td> 0.02 </td>
   <td> -0.02 </td>
   <td> 0.08 </td>
  </tr>
  <tr>
   <td> sup_wb_2 </td>
   <td> 0.87 </td>
   <td> 0.02 </td>
   <td> -0.01 </td>
   <td> 0.05 </td>
   <td> -0.05 </td>
  </tr>
  <tr>
   <td> sup_wb_3 </td>
   <td> 0.78 </td>
   <td> -0.08 </td>
   <td> 0.09 </td>
   <td> 0.04 </td>
   <td> 0.03 </td>
  </tr>
  <tr>
   <td> sup_wb_4 </td>
   <td> 1.00 </td>
   <td> 0.11 </td>
   <td> -0.01 </td>
   <td> -0.02 </td>
   <td> -0.06 </td>
  </tr>
  <tr>
   <td> sup_bw_1 </td>
   <td> -0.09 </td>
   <td> 0.20 </td>
   <td> -0.07 </td>
   <td> -0.68 </td>
   <td> 0.09 </td>
  </tr>
  <tr>
   <td> sup_bw_2 </td>
   <td> 0.30 </td>
   <td> -0.08 </td>
   <td> 0.07 </td>
   <td> 0.59 </td>
   <td> -0.07 </td>
  </tr>
  <tr>
   <td> sup_bw_3 </td>
   <td> -0.28 </td>
   <td> -0.16 </td>
   <td> 0.07 </td>
   <td> 0.84 </td>
   <td> 0.05 </td>
  </tr>
  <tr>
   <td> sup_bw_4 </td>
   <td> 0.06 </td>
   <td> 0.00 </td>
   <td> 0.01 </td>
   <td> 0.83 </td>
   <td> -0.06 </td>
  </tr>
  <tr>
   <td> comp_bw_1 </td>
   <td> -0.04 </td>
   <td> 0.06 </td>
   <td> -0.01 </td>
   <td> 0.55 </td>
   <td> 0.01 </td>
  </tr>
  <tr>
   <td> comp_bw_2 </td>
   <td> -0.07 </td>
   <td> -0.10 </td>
   <td> 0.18 </td>
   <td> -0.51 </td>
   <td> -0.04 </td>
  </tr>
  <tr>
   <td> comp_bw_3 </td>
   <td> -0.12 </td>
   <td> 0.03 </td>
   <td> -0.14 </td>
   <td> 0.62 </td>
   <td> 0.10 </td>
  </tr>
  <tr>
   <td> comp_bw_4 </td>
   <td> -0.12 </td>
   <td> -0.03 </td>
   <td> -0.01 </td>
   <td> -0.08 </td>
   <td> 0.04 </td>
  </tr>
  <tr>
   <td> comp_wb_1 </td>
   <td> 0.47 </td>
   <td> -0.05 </td>
   <td> 0.18 </td>
   <td> 0.06 </td>
   <td> 0.10 </td>
  </tr>
  <tr>
   <td> comp_wb_2 </td>
   <td> -0.71 </td>
   <td> 0.00 </td>
   <td> 0.06 </td>
   <td> 0.10 </td>
   <td> -0.11 </td>
  </tr>
  <tr>
   <td> comp_wb_3 </td>
   <td> 0.68 </td>
   <td> 0.02 </td>
   <td> 0.01 </td>
   <td> -0.05 </td>
   <td> 0.18 </td>
  </tr>
  <tr>
   <td> comp_wb_4 </td>
   <td> -0.29 </td>
   <td> 0.05 </td>
   <td> 0.07 </td>
   <td> 0.11 </td>
   <td> -0.02 </td>
  </tr>
  <tr>
   <td> bm_bw_e_1 </td>
   <td> 0.05 </td>
   <td> 0.20 </td>
   <td> -0.06 </td>
   <td> 0.15 </td>
   <td> 0.29 </td>
  </tr>
  <tr>
   <td> bm_bw_e_2 </td>
   <td> -0.04 </td>
   <td> 0.34 </td>
   <td> -0.07 </td>
   <td> 0.05 </td>
   <td> 0.23 </td>
  </tr>
  <tr>
   <td> bm_ww_e_1 </td>
   <td> 0.10 </td>
   <td> -0.14 </td>
   <td> 0.09 </td>
   <td> -0.01 </td>
   <td> 0.80 </td>
  </tr>
  <tr>
   <td> bm_ww_e_2 </td>
   <td> 0.04 </td>
   <td> -0.17 </td>
   <td> 0.19 </td>
   <td> -0.08 </td>
   <td> 0.88 </td>
  </tr>
  <tr>
   <td> bm_bw_b_1 </td>
   <td> -0.12 </td>
   <td> 0.83 </td>
   <td> 0.21 </td>
   <td> 0.00 </td>
   <td> -0.07 </td>
  </tr>
  <tr>
   <td> bm_bw_b_2 </td>
   <td> -0.07 </td>
   <td> 0.87 </td>
   <td> 0.18 </td>
   <td> -0.03 </td>
   <td> -0.10 </td>
  </tr>
  <tr>
   <td> bm_bw_b_3 </td>
   <td> 0.04 </td>
   <td> 1.03 </td>
   <td> -0.01 </td>
   <td> -0.11 </td>
   <td> -0.12 </td>
  </tr>
  <tr>
   <td> bm_bw_b_4 </td>
   <td> 0.08 </td>
   <td> 1.04 </td>
   <td> -0.06 </td>
   <td> -0.12 </td>
   <td> -0.13 </td>
  </tr>
  <tr>
   <td> bm_ww_b_1 </td>
   <td> 0.03 </td>
   <td> 0.09 </td>
   <td> 0.94 </td>
   <td> -0.04 </td>
   <td> 0.02 </td>
  </tr>
  <tr>
   <td> bm_ww_b_2 </td>
   <td> -0.02 </td>
   <td> 0.08 </td>
   <td> 0.96 </td>
   <td> 0.00 </td>
   <td> 0.03 </td>
  </tr>
  <tr>
   <td> bm_ww_b_3 </td>
   <td> 0.00 </td>
   <td> 0.03 </td>
   <td> 0.89 </td>
   <td> -0.05 </td>
   <td> 0.11 </td>
  </tr>
  <tr>
   <td> bm_ww_b_4 </td>
   <td> 0.00 </td>
   <td> 0.03 </td>
   <td> 0.89 </td>
   <td> -0.02 </td>
   <td> 0.10 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Six-factor solution</caption>
 <thead>
  <tr>
   <th> Item </th>
   <th> ML3 </th>
   <th> ML1 </th>
   <th> ML2 </th>
   <th> ML6 </th>
   <th> ML5 </th>
   <th> ML4 </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> sup_wb_1 </td>
   <td> -0.85 </td>
   <td> 0.02 </td>
   <td> 0.07 </td>
   <td> 0.00 </td>
   <td> 0.07 </td>
   <td> -0.06 </td>
  </tr>
  <tr>
   <td> sup_wb_2 </td>
   <td> 0.88 </td>
   <td> 0.03 </td>
   <td> -0.03 </td>
   <td> 0.04 </td>
   <td> -0.05 </td>
   <td> 0.01 </td>
  </tr>
  <tr>
   <td> sup_wb_3 </td>
   <td> 0.80 </td>
   <td> -0.06 </td>
   <td> 0.06 </td>
   <td> 0.02 </td>
   <td> 0.03 </td>
   <td> 0.02 </td>
  </tr>
  <tr>
   <td> sup_wb_4 </td>
   <td> 1.01 </td>
   <td> 0.12 </td>
   <td> -0.02 </td>
   <td> -0.02 </td>
   <td> -0.06 </td>
   <td> 0.01 </td>
  </tr>
  <tr>
   <td> sup_bw_1 </td>
   <td> -0.11 </td>
   <td> 0.18 </td>
   <td> -0.01 </td>
   <td> -0.66 </td>
   <td> 0.07 </td>
   <td> -0.07 </td>
  </tr>
  <tr>
   <td> sup_bw_2 </td>
   <td> 0.30 </td>
   <td> -0.07 </td>
   <td> 0.07 </td>
   <td> 0.59 </td>
   <td> -0.07 </td>
   <td> -0.02 </td>
  </tr>
  <tr>
   <td> sup_bw_3 </td>
   <td> -0.26 </td>
   <td> -0.13 </td>
   <td> 0.03 </td>
   <td> 0.81 </td>
   <td> 0.06 </td>
   <td> 0.05 </td>
  </tr>
  <tr>
   <td> sup_bw_4 </td>
   <td> 0.06 </td>
   <td> 0.00 </td>
   <td> 0.01 </td>
   <td> 0.83 </td>
   <td> -0.07 </td>
   <td> 0.00 </td>
  </tr>
  <tr>
   <td> comp_bw_1 </td>
   <td> -0.05 </td>
   <td> 0.06 </td>
   <td> 0.01 </td>
   <td> 0.56 </td>
   <td> 0.01 </td>
   <td> -0.01 </td>
  </tr>
  <tr>
   <td> comp_bw_2 </td>
   <td> -0.03 </td>
   <td> -0.07 </td>
   <td> 0.11 </td>
   <td> -0.54 </td>
   <td> -0.03 </td>
   <td> 0.09 </td>
  </tr>
  <tr>
   <td> comp_bw_3 </td>
   <td> -0.15 </td>
   <td> 0.02 </td>
   <td> -0.09 </td>
   <td> 0.65 </td>
   <td> 0.09 </td>
   <td> -0.07 </td>
  </tr>
  <tr>
   <td> comp_bw_4 </td>
   <td> -0.11 </td>
   <td> -0.02 </td>
   <td> -0.02 </td>
   <td> -0.09 </td>
   <td> 0.04 </td>
   <td> 0.00 </td>
  </tr>
  <tr>
   <td> comp_wb_1 </td>
   <td> 0.48 </td>
   <td> -0.03 </td>
   <td> 0.15 </td>
   <td> 0.05 </td>
   <td> 0.10 </td>
   <td> 0.05 </td>
  </tr>
  <tr>
   <td> comp_wb_2 </td>
   <td> -0.69 </td>
   <td> 0.01 </td>
   <td> 0.03 </td>
   <td> 0.08 </td>
   <td> -0.10 </td>
   <td> 0.07 </td>
  </tr>
  <tr>
   <td> comp_wb_3 </td>
   <td> 0.69 </td>
   <td> 0.02 </td>
   <td> -0.01 </td>
   <td> -0.05 </td>
   <td> 0.18 </td>
   <td> 0.01 </td>
  </tr>
  <tr>
   <td> comp_wb_4 </td>
   <td> -0.28 </td>
   <td> 0.06 </td>
   <td> 0.05 </td>
   <td> 0.10 </td>
   <td> -0.01 </td>
   <td> 0.04 </td>
  </tr>
  <tr>
   <td> bm_bw_e_1 </td>
   <td> 0.06 </td>
   <td> 0.22 </td>
   <td> -0.10 </td>
   <td> 0.13 </td>
   <td> 0.30 </td>
   <td> 0.08 </td>
  </tr>
  <tr>
   <td> bm_bw_e_2 </td>
   <td> -0.05 </td>
   <td> 0.33 </td>
   <td> -0.02 </td>
   <td> 0.07 </td>
   <td> 0.21 </td>
   <td> -0.04 </td>
  </tr>
  <tr>
   <td> bm_ww_e_1 </td>
   <td> 0.10 </td>
   <td> -0.16 </td>
   <td> 0.11 </td>
   <td> 0.00 </td>
   <td> 0.78 </td>
   <td> -0.09 </td>
  </tr>
  <tr>
   <td> bm_ww_e_2 </td>
   <td> 0.06 </td>
   <td> -0.15 </td>
   <td> 0.12 </td>
   <td> -0.10 </td>
   <td> 0.90 </td>
   <td> 0.05 </td>
  </tr>
  <tr>
   <td> bm_bw_b_1 </td>
   <td> -0.04 </td>
   <td> 0.95 </td>
   <td> 0.00 </td>
   <td> -0.07 </td>
   <td> -0.02 </td>
   <td> 0.49 </td>
  </tr>
  <tr>
   <td> bm_bw_b_2 </td>
   <td> 0.01 </td>
   <td> 0.99 </td>
   <td> -0.02 </td>
   <td> -0.10 </td>
   <td> -0.05 </td>
   <td> 0.46 </td>
  </tr>
  <tr>
   <td> bm_bw_b_3 </td>
   <td> -0.01 </td>
   <td> 1.02 </td>
   <td> 0.14 </td>
   <td> -0.06 </td>
   <td> -0.17 </td>
   <td> -0.10 </td>
  </tr>
  <tr>
   <td> bm_bw_b_4 </td>
   <td> 0.02 </td>
   <td> 0.99 </td>
   <td> 0.07 </td>
   <td> -0.06 </td>
   <td> -0.17 </td>
   <td> -0.05 </td>
  </tr>
  <tr>
   <td> bm_ww_b_1 </td>
   <td> 0.02 </td>
   <td> 0.09 </td>
   <td> 0.93 </td>
   <td> -0.04 </td>
   <td> 0.01 </td>
   <td> 0.03 </td>
  </tr>
  <tr>
   <td> bm_ww_b_2 </td>
   <td> -0.03 </td>
   <td> 0.07 </td>
   <td> 0.97 </td>
   <td> 0.00 </td>
   <td> 0.01 </td>
   <td> 0.01 </td>
  </tr>
  <tr>
   <td> bm_ww_b_3 </td>
   <td> -0.03 </td>
   <td> 0.00 </td>
   <td> 0.95 </td>
   <td> -0.02 </td>
   <td> 0.09 </td>
   <td> -0.07 </td>
  </tr>
  <tr>
   <td> bm_ww_b_4 </td>
   <td> -0.02 </td>
   <td> 0.01 </td>
   <td> 0.91 </td>
   <td> -0.01 </td>
   <td> 0.09 </td>
   <td> -0.02 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Seven-factor solution</caption>
 <thead>
  <tr>
   <th> Item </th>
   <th> ML4 </th>
   <th> ML3 </th>
   <th> ML2 </th>
   <th> ML7 </th>
   <th> ML6 </th>
   <th> ML1 </th>
   <th> ML5 </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> sup_wb_1 </td>
   <td> -0.85 </td>
   <td> 0.06 </td>
   <td> 0.02 </td>
   <td> 0.02 </td>
   <td> 0.07 </td>
   <td> 0.03 </td>
   <td> -0.06 </td>
  </tr>
  <tr>
   <td> sup_wb_2 </td>
   <td> 0.88 </td>
   <td> -0.03 </td>
   <td> 0.03 </td>
   <td> 0.03 </td>
   <td> -0.04 </td>
   <td> -0.01 </td>
   <td> 0.00 </td>
  </tr>
  <tr>
   <td> sup_wb_3 </td>
   <td> 0.80 </td>
   <td> 0.06 </td>
   <td> -0.05 </td>
   <td> 0.02 </td>
   <td> 0.03 </td>
   <td> -0.04 </td>
   <td> 0.03 </td>
  </tr>
  <tr>
   <td> sup_wb_4 </td>
   <td> 1.01 </td>
   <td> -0.02 </td>
   <td> 0.10 </td>
   <td> -0.03 </td>
   <td> -0.05 </td>
   <td> 0.02 </td>
   <td> -0.01 </td>
  </tr>
  <tr>
   <td> sup_bw_1 </td>
   <td> -0.12 </td>
   <td> -0.02 </td>
   <td> 0.15 </td>
   <td> -0.62 </td>
   <td> 0.09 </td>
   <td> 0.01 </td>
   <td> -0.10 </td>
  </tr>
  <tr>
   <td> sup_bw_2 </td>
   <td> 0.31 </td>
   <td> 0.08 </td>
   <td> -0.09 </td>
   <td> 0.56 </td>
   <td> -0.08 </td>
   <td> 0.04 </td>
   <td> 0.00 </td>
  </tr>
  <tr>
   <td> sup_bw_3 </td>
   <td> -0.24 </td>
   <td> 0.01 </td>
   <td> -0.07 </td>
   <td> 0.82 </td>
   <td> 0.08 </td>
   <td> -0.05 </td>
   <td> 0.08 </td>
  </tr>
  <tr>
   <td> sup_bw_4 </td>
   <td> 0.06 </td>
   <td> 0.01 </td>
   <td> 0.00 </td>
   <td> 0.81 </td>
   <td> -0.05 </td>
   <td> 0.01 </td>
   <td> 0.00 </td>
  </tr>
  <tr>
   <td> comp_bw_1 </td>
   <td> -0.05 </td>
   <td> -0.01 </td>
   <td> 0.07 </td>
   <td> 0.56 </td>
   <td> 0.03 </td>
   <td> -0.01 </td>
   <td> -0.02 </td>
  </tr>
  <tr>
   <td> comp_bw_2 </td>
   <td> -0.03 </td>
   <td> 0.12 </td>
   <td> -0.07 </td>
   <td> -0.55 </td>
   <td> -0.05 </td>
   <td> -0.04 </td>
   <td> 0.10 </td>
  </tr>
  <tr>
   <td> comp_bw_3 </td>
   <td> -0.14 </td>
   <td> -0.11 </td>
   <td> 0.03 </td>
   <td> 0.66 </td>
   <td> 0.11 </td>
   <td> 0.02 </td>
   <td> -0.07 </td>
  </tr>
  <tr>
   <td> comp_bw_4 </td>
   <td> -0.11 </td>
   <td> -0.02 </td>
   <td> -0.02 </td>
   <td> -0.08 </td>
   <td> 0.04 </td>
   <td> -0.01 </td>
   <td> 0.01 </td>
  </tr>
  <tr>
   <td> comp_wb_1 </td>
   <td> 0.49 </td>
   <td> 0.13 </td>
   <td> 0.00 </td>
   <td> 0.05 </td>
   <td> 0.11 </td>
   <td> -0.05 </td>
   <td> 0.05 </td>
  </tr>
  <tr>
   <td> comp_wb_2 </td>
   <td> -0.70 </td>
   <td> 0.05 </td>
   <td> -0.01 </td>
   <td> 0.05 </td>
   <td> -0.13 </td>
   <td> 0.07 </td>
   <td> 0.07 </td>
  </tr>
  <tr>
   <td> comp_wb_3 </td>
   <td> 0.69 </td>
   <td> -0.03 </td>
   <td> 0.05 </td>
   <td> -0.04 </td>
   <td> 0.18 </td>
   <td> 0.01 </td>
   <td> 0.01 </td>
  </tr>
  <tr>
   <td> comp_wb_4 </td>
   <td> -0.28 </td>
   <td> 0.05 </td>
   <td> 0.07 </td>
   <td> 0.11 </td>
   <td> 0.00 </td>
   <td> -0.04 </td>
   <td> 0.02 </td>
  </tr>
  <tr>
   <td> bm_bw_e_1 </td>
   <td> 0.04 </td>
   <td> -0.05 </td>
   <td> 0.04 </td>
   <td> 0.07 </td>
   <td> 0.10 </td>
   <td> 0.66 </td>
   <td> 0.07 </td>
  </tr>
  <tr>
   <td> bm_bw_e_2 </td>
   <td> -0.12 </td>
   <td> 0.10 </td>
   <td> -0.03 </td>
   <td> -0.05 </td>
   <td> -0.08 </td>
   <td> 1.02 </td>
   <td> -0.07 </td>
  </tr>
  <tr>
   <td> bm_ww_e_1 </td>
   <td> 0.11 </td>
   <td> 0.04 </td>
   <td> -0.03 </td>
   <td> 0.11 </td>
   <td> 0.82 </td>
   <td> -0.04 </td>
   <td> -0.06 </td>
  </tr>
  <tr>
   <td> bm_ww_e_2 </td>
   <td> 0.08 </td>
   <td> 0.06 </td>
   <td> -0.02 </td>
   <td> -0.01 </td>
   <td> 0.83 </td>
   <td> 0.07 </td>
   <td> 0.09 </td>
  </tr>
  <tr>
   <td> bm_bw_b_1 </td>
   <td> -0.01 </td>
   <td> -0.05 </td>
   <td> 0.96 </td>
   <td> -0.04 </td>
   <td> 0.02 </td>
   <td> 0.01 </td>
   <td> 0.32 </td>
  </tr>
  <tr>
   <td> bm_bw_b_2 </td>
   <td> 0.02 </td>
   <td> -0.05 </td>
   <td> 0.98 </td>
   <td> -0.06 </td>
   <td> -0.01 </td>
   <td> 0.02 </td>
   <td> 0.26 </td>
  </tr>
  <tr>
   <td> bm_bw_b_3 </td>
   <td> -0.02 </td>
   <td> 0.10 </td>
   <td> 0.91 </td>
   <td> 0.01 </td>
   <td> -0.04 </td>
   <td> 0.01 </td>
   <td> -0.28 </td>
  </tr>
  <tr>
   <td> bm_bw_b_4 </td>
   <td> 0.02 </td>
   <td> 0.03 </td>
   <td> 0.91 </td>
   <td> 0.01 </td>
   <td> -0.03 </td>
   <td> -0.02 </td>
   <td> -0.24 </td>
  </tr>
  <tr>
   <td> bm_ww_b_1 </td>
   <td> 0.01 </td>
   <td> 0.94 </td>
   <td> 0.05 </td>
   <td> -0.06 </td>
   <td> -0.02 </td>
   <td> 0.02 </td>
   <td> 0.01 </td>
  </tr>
  <tr>
   <td> bm_ww_b_2 </td>
   <td> -0.04 </td>
   <td> 0.97 </td>
   <td> 0.03 </td>
   <td> -0.03 </td>
   <td> -0.02 </td>
   <td> 0.02 </td>
   <td> 0.00 </td>
  </tr>
  <tr>
   <td> bm_ww_b_3 </td>
   <td> -0.04 </td>
   <td> 0.94 </td>
   <td> -0.03 </td>
   <td> -0.04 </td>
   <td> 0.07 </td>
   <td> 0.02 </td>
   <td> -0.07 </td>
  </tr>
  <tr>
   <td> bm_ww_b_4 </td>
   <td> -0.02 </td>
   <td> 0.90 </td>
   <td> -0.01 </td>
   <td> -0.02 </td>
   <td> 0.07 </td>
   <td> -0.01 </td>
   <td> -0.02 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Eight-factor solution</caption>
 <thead>
  <tr>
   <th> Item </th>
   <th> ML4 </th>
   <th> ML2 </th>
   <th> ML3 </th>
   <th> ML7 </th>
   <th> ML6 </th>
   <th> ML1 </th>
   <th> ML8 </th>
   <th> ML5 </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> sup_wb_1 </td>
   <td> -0.84 </td>
   <td> 0.03 </td>
   <td> 0.06 </td>
   <td> 0.01 </td>
   <td> 0.09 </td>
   <td> 0.01 </td>
   <td> 0.05 </td>
   <td> -0.03 </td>
  </tr>
  <tr>
   <td> sup_wb_2 </td>
   <td> 0.90 </td>
   <td> 0.02 </td>
   <td> -0.03 </td>
   <td> 0.04 </td>
   <td> -0.07 </td>
   <td> 0.01 </td>
   <td> 0.02 </td>
   <td> -0.02 </td>
  </tr>
  <tr>
   <td> sup_wb_3 </td>
   <td> 0.85 </td>
   <td> -0.05 </td>
   <td> 0.04 </td>
   <td> 0.02 </td>
   <td> 0.01 </td>
   <td> -0.01 </td>
   <td> 0.13 </td>
   <td> -0.01 </td>
  </tr>
  <tr>
   <td> sup_wb_4 </td>
   <td> 1.04 </td>
   <td> 0.09 </td>
   <td> -0.03 </td>
   <td> -0.03 </td>
   <td> -0.08 </td>
   <td> 0.04 </td>
   <td> 0.05 </td>
   <td> -0.03 </td>
  </tr>
  <tr>
   <td> sup_bw_1 </td>
   <td> -0.14 </td>
   <td> 0.14 </td>
   <td> -0.04 </td>
   <td> -0.62 </td>
   <td> 0.10 </td>
   <td> 0.01 </td>
   <td> 0.07 </td>
   <td> -0.09 </td>
  </tr>
  <tr>
   <td> sup_bw_2 </td>
   <td> 0.33 </td>
   <td> -0.07 </td>
   <td> 0.08 </td>
   <td> 0.55 </td>
   <td> -0.10 </td>
   <td> 0.04 </td>
   <td> -0.07 </td>
   <td> 0.00 </td>
  </tr>
  <tr>
   <td> sup_bw_3 </td>
   <td> -0.18 </td>
   <td> -0.07 </td>
   <td> 0.02 </td>
   <td> 0.84 </td>
   <td> 0.07 </td>
   <td> -0.05 </td>
   <td> 0.17 </td>
   <td> 0.06 </td>
  </tr>
  <tr>
   <td> sup_bw_4 </td>
   <td> 0.11 </td>
   <td> 0.03 </td>
   <td> 0.02 </td>
   <td> 0.79 </td>
   <td> -0.07 </td>
   <td> 0.01 </td>
   <td> -0.01 </td>
   <td> -0.01 </td>
  </tr>
  <tr>
   <td> comp_bw_1 </td>
   <td> 0.03 </td>
   <td> 0.08 </td>
   <td> -0.02 </td>
   <td> 0.57 </td>
   <td> 0.03 </td>
   <td> 0.00 </td>
   <td> 0.17 </td>
   <td> -0.03 </td>
  </tr>
  <tr>
   <td> comp_bw_2 </td>
   <td> 0.08 </td>
   <td> -0.08 </td>
   <td> 0.08 </td>
   <td> -0.54 </td>
   <td> -0.06 </td>
   <td> -0.02 </td>
   <td> 0.37 </td>
   <td> 0.07 </td>
  </tr>
  <tr>
   <td> comp_bw_3 </td>
   <td> -0.16 </td>
   <td> 0.05 </td>
   <td> -0.10 </td>
   <td> 0.64 </td>
   <td> 0.11 </td>
   <td> 0.01 </td>
   <td> -0.10 </td>
   <td> -0.05 </td>
  </tr>
  <tr>
   <td> comp_bw_4 </td>
   <td> 0.12 </td>
   <td> -0.03 </td>
   <td> -0.10 </td>
   <td> -0.06 </td>
   <td> 0.04 </td>
   <td> 0.04 </td>
   <td> 0.76 </td>
   <td> -0.05 </td>
  </tr>
  <tr>
   <td> comp_wb_1 </td>
   <td> 0.54 </td>
   <td> 0.00 </td>
   <td> 0.11 </td>
   <td> 0.06 </td>
   <td> 0.09 </td>
   <td> -0.03 </td>
   <td> 0.13 </td>
   <td> 0.04 </td>
  </tr>
  <tr>
   <td> comp_wb_2 </td>
   <td> -0.63 </td>
   <td> -0.01 </td>
   <td> 0.04 </td>
   <td> 0.08 </td>
   <td> -0.12 </td>
   <td> 0.07 </td>
   <td> 0.20 </td>
   <td> 0.07 </td>
  </tr>
  <tr>
   <td> comp_wb_3 </td>
   <td> 0.67 </td>
   <td> 0.04 </td>
   <td> -0.03 </td>
   <td> -0.05 </td>
   <td> 0.17 </td>
   <td> 0.02 </td>
   <td> -0.07 </td>
   <td> 0.01 </td>
  </tr>
  <tr>
   <td> comp_wb_4 </td>
   <td> -0.12 </td>
   <td> 0.06 </td>
   <td> 0.01 </td>
   <td> 0.14 </td>
   <td> 0.00 </td>
   <td> -0.02 </td>
   <td> 0.52 </td>
   <td> -0.01 </td>
  </tr>
  <tr>
   <td> bm_bw_e_1 </td>
   <td> 0.05 </td>
   <td> 0.03 </td>
   <td> -0.06 </td>
   <td> 0.06 </td>
   <td> 0.09 </td>
   <td> 0.67 </td>
   <td> 0.01 </td>
   <td> 0.07 </td>
  </tr>
  <tr>
   <td> bm_bw_e_2 </td>
   <td> -0.09 </td>
   <td> -0.04 </td>
   <td> 0.08 </td>
   <td> -0.07 </td>
   <td> -0.09 </td>
   <td> 1.03 </td>
   <td> 0.02 </td>
   <td> -0.09 </td>
  </tr>
  <tr>
   <td> bm_ww_e_1 </td>
   <td> 0.06 </td>
   <td> -0.04 </td>
   <td> 0.02 </td>
   <td> 0.06 </td>
   <td> 0.84 </td>
   <td> -0.04 </td>
   <td> 0.05 </td>
   <td> -0.06 </td>
  </tr>
  <tr>
   <td> bm_ww_e_2 </td>
   <td> 0.02 </td>
   <td> -0.04 </td>
   <td> 0.05 </td>
   <td> -0.04 </td>
   <td> 0.86 </td>
   <td> 0.06 </td>
   <td> 0.00 </td>
   <td> 0.10 </td>
  </tr>
  <tr>
   <td> bm_bw_b_1 </td>
   <td> -0.04 </td>
   <td> 0.98 </td>
   <td> -0.03 </td>
   <td> 0.01 </td>
   <td> 0.02 </td>
   <td> -0.01 </td>
   <td> -0.10 </td>
   <td> 0.41 </td>
  </tr>
  <tr>
   <td> bm_bw_b_2 </td>
   <td> 0.00 </td>
   <td> 0.97 </td>
   <td> 0.00 </td>
   <td> -0.01 </td>
   <td> -0.02 </td>
   <td> 0.00 </td>
   <td> -0.05 </td>
   <td> 0.30 </td>
  </tr>
  <tr>
   <td> bm_bw_b_3 </td>
   <td> 0.03 </td>
   <td> 0.93 </td>
   <td> 0.08 </td>
   <td> 0.00 </td>
   <td> -0.05 </td>
   <td> 0.02 </td>
   <td> 0.09 </td>
   <td> -0.23 </td>
  </tr>
  <tr>
   <td> bm_bw_b_4 </td>
   <td> 0.06 </td>
   <td> 0.93 </td>
   <td> 0.02 </td>
   <td> 0.00 </td>
   <td> -0.04 </td>
   <td> -0.01 </td>
   <td> 0.08 </td>
   <td> -0.20 </td>
  </tr>
  <tr>
   <td> bm_ww_b_1 </td>
   <td> 0.02 </td>
   <td> 0.05 </td>
   <td> 0.94 </td>
   <td> -0.03 </td>
   <td> -0.03 </td>
   <td> 0.01 </td>
   <td> -0.04 </td>
   <td> 0.02 </td>
  </tr>
  <tr>
   <td> bm_ww_b_2 </td>
   <td> -0.02 </td>
   <td> 0.04 </td>
   <td> 0.98 </td>
   <td> 0.01 </td>
   <td> -0.03 </td>
   <td> 0.01 </td>
   <td> -0.01 </td>
   <td> 0.00 </td>
  </tr>
  <tr>
   <td> bm_ww_b_3 </td>
   <td> -0.03 </td>
   <td> -0.02 </td>
   <td> 0.94 </td>
   <td> -0.02 </td>
   <td> 0.06 </td>
   <td> 0.01 </td>
   <td> -0.03 </td>
   <td> -0.06 </td>
  </tr>
  <tr>
   <td> bm_ww_b_4 </td>
   <td> -0.03 </td>
   <td> 0.00 </td>
   <td> 0.91 </td>
   <td> 0.00 </td>
   <td> 0.06 </td>
   <td> -0.02 </td>
   <td> -0.08 </td>
   <td> 0.00 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Nine-factor solution</caption>
 <thead>
  <tr>
   <th> Item </th>
   <th> ML4 </th>
   <th> ML1 </th>
   <th> ML3 </th>
   <th> ML7 </th>
   <th> ML6 </th>
   <th> ML2 </th>
   <th> ML8 </th>
   <th> ML9 </th>
   <th> ML5 </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> sup_wb_1 </td>
   <td> -0.83 </td>
   <td> 0.01 </td>
   <td> 0.05 </td>
   <td> -0.09 </td>
   <td> 0.01 </td>
   <td> 0.02 </td>
   <td> 0.02 </td>
   <td> 0.12 </td>
   <td> -0.02 </td>
  </tr>
  <tr>
   <td> sup_wb_2 </td>
   <td> 0.88 </td>
   <td> 0.03 </td>
   <td> -0.03 </td>
   <td> 0.09 </td>
   <td> -0.03 </td>
   <td> 0.00 </td>
   <td> 0.03 </td>
   <td> 0.02 </td>
   <td> -0.02 </td>
  </tr>
  <tr>
   <td> sup_wb_3 </td>
   <td> 0.82 </td>
   <td> -0.06 </td>
   <td> 0.05 </td>
   <td> 0.05 </td>
   <td> 0.03 </td>
   <td> -0.02 </td>
   <td> 0.13 </td>
   <td> 0.10 </td>
   <td> -0.01 </td>
  </tr>
  <tr>
   <td> sup_wb_4 </td>
   <td> 1.04 </td>
   <td> 0.12 </td>
   <td> -0.04 </td>
   <td> 0.04 </td>
   <td> 0.00 </td>
   <td> 0.04 </td>
   <td> 0.07 </td>
   <td> -0.08 </td>
   <td> -0.04 </td>
  </tr>
  <tr>
   <td> sup_bw_1 </td>
   <td> -0.15 </td>
   <td> 0.11 </td>
   <td> -0.03 </td>
   <td> -0.69 </td>
   <td> 0.01 </td>
   <td> 0.02 </td>
   <td> 0.05 </td>
   <td> 0.10 </td>
   <td> -0.06 </td>
  </tr>
  <tr>
   <td> sup_bw_2 </td>
   <td> 0.34 </td>
   <td> -0.04 </td>
   <td> 0.07 </td>
   <td> 0.57 </td>
   <td> -0.05 </td>
   <td> 0.04 </td>
   <td> -0.04 </td>
   <td> 0.01 </td>
   <td> -0.01 </td>
  </tr>
  <tr>
   <td> sup_bw_3 </td>
   <td> -0.17 </td>
   <td> -0.05 </td>
   <td> 0.02 </td>
   <td> 0.79 </td>
   <td> 0.08 </td>
   <td> -0.05 </td>
   <td> 0.18 </td>
   <td> 0.16 </td>
   <td> 0.05 </td>
  </tr>
  <tr>
   <td> sup_bw_4 </td>
   <td> 0.14 </td>
   <td> 0.06 </td>
   <td> 0.01 </td>
   <td> 0.79 </td>
   <td> -0.01 </td>
   <td> 0.01 </td>
   <td> 0.02 </td>
   <td> 0.01 </td>
   <td> -0.02 </td>
  </tr>
  <tr>
   <td> comp_bw_1 </td>
   <td> -0.01 </td>
   <td> 0.03 </td>
   <td> 0.00 </td>
   <td> 0.46 </td>
   <td> -0.10 </td>
   <td> 0.01 </td>
   <td> 0.17 </td>
   <td> 0.54 </td>
   <td> -0.01 </td>
  </tr>
  <tr>
   <td> comp_bw_2 </td>
   <td> 0.07 </td>
   <td> -0.09 </td>
   <td> 0.09 </td>
   <td> -0.51 </td>
   <td> -0.07 </td>
   <td> -0.02 </td>
   <td> 0.37 </td>
   <td> -0.05 </td>
   <td> 0.07 </td>
  </tr>
  <tr>
   <td> comp_bw_3 </td>
   <td> -0.19 </td>
   <td> 0.02 </td>
   <td> -0.09 </td>
   <td> 0.55 </td>
   <td> 0.03 </td>
   <td> 0.02 </td>
   <td> -0.14 </td>
   <td> 0.38 </td>
   <td> -0.04 </td>
  </tr>
  <tr>
   <td> comp_bw_4 </td>
   <td> 0.10 </td>
   <td> -0.03 </td>
   <td> -0.10 </td>
   <td> -0.09 </td>
   <td> 0.04 </td>
   <td> 0.03 </td>
   <td> 0.72 </td>
   <td> 0.13 </td>
   <td> -0.05 </td>
  </tr>
  <tr>
   <td> comp_wb_1 </td>
   <td> 0.51 </td>
   <td> -0.06 </td>
   <td> 0.12 </td>
   <td> -0.05 </td>
   <td> -0.06 </td>
   <td> -0.02 </td>
   <td> 0.12 </td>
   <td> 0.55 </td>
   <td> 0.06 </td>
  </tr>
  <tr>
   <td> comp_wb_2 </td>
   <td> -0.60 </td>
   <td> 0.01 </td>
   <td> 0.03 </td>
   <td> 0.11 </td>
   <td> -0.07 </td>
   <td> 0.06 </td>
   <td> 0.25 </td>
   <td> -0.19 </td>
   <td> 0.06 </td>
  </tr>
  <tr>
   <td> comp_wb_3 </td>
   <td> 0.64 </td>
   <td> 0.01 </td>
   <td> -0.03 </td>
   <td> -0.12 </td>
   <td> 0.09 </td>
   <td> 0.02 </td>
   <td> -0.11 </td>
   <td> 0.34 </td>
   <td> 0.03 </td>
  </tr>
  <tr>
   <td> comp_wb_4 </td>
   <td> -0.11 </td>
   <td> 0.08 </td>
   <td> 0.01 </td>
   <td> 0.13 </td>
   <td> 0.03 </td>
   <td> -0.02 </td>
   <td> 0.55 </td>
   <td> 0.03 </td>
   <td> -0.02 </td>
  </tr>
  <tr>
   <td> bm_bw_e_1 </td>
   <td> 0.05 </td>
   <td> 0.03 </td>
   <td> -0.06 </td>
   <td> 0.06 </td>
   <td> 0.10 </td>
   <td> 0.67 </td>
   <td> 0.01 </td>
   <td> 0.01 </td>
   <td> 0.07 </td>
  </tr>
  <tr>
   <td> bm_bw_e_2 </td>
   <td> -0.08 </td>
   <td> -0.04 </td>
   <td> 0.08 </td>
   <td> -0.08 </td>
   <td> -0.11 </td>
   <td> 1.04 </td>
   <td> 0.01 </td>
   <td> -0.01 </td>
   <td> -0.09 </td>
  </tr>
  <tr>
   <td> bm_ww_e_1 </td>
   <td> 0.04 </td>
   <td> 0.01 </td>
   <td> 0.00 </td>
   <td> 0.08 </td>
   <td> 0.99 </td>
   <td> -0.07 </td>
   <td> 0.09 </td>
   <td> -0.13 </td>
   <td> -0.08 </td>
  </tr>
  <tr>
   <td> bm_ww_e_2 </td>
   <td> 0.02 </td>
   <td> -0.03 </td>
   <td> 0.07 </td>
   <td> -0.04 </td>
   <td> 0.80 </td>
   <td> 0.07 </td>
   <td> 0.02 </td>
   <td> -0.02 </td>
   <td> 0.08 </td>
  </tr>
  <tr>
   <td> bm_bw_b_1 </td>
   <td> -0.05 </td>
   <td> 0.97 </td>
   <td> -0.03 </td>
   <td> 0.02 </td>
   <td> -0.01 </td>
   <td> -0.02 </td>
   <td> -0.10 </td>
   <td> 0.05 </td>
   <td> 0.48 </td>
  </tr>
  <tr>
   <td> bm_bw_b_2 </td>
   <td> -0.01 </td>
   <td> 0.96 </td>
   <td> 0.01 </td>
   <td> 0.00 </td>
   <td> -0.02 </td>
   <td> -0.01 </td>
   <td> -0.04 </td>
   <td> 0.01 </td>
   <td> 0.32 </td>
  </tr>
  <tr>
   <td> bm_bw_b_3 </td>
   <td> 0.05 </td>
   <td> 0.96 </td>
   <td> 0.07 </td>
   <td> -0.05 </td>
   <td> 0.00 </td>
   <td> 0.02 </td>
   <td> 0.10 </td>
   <td> -0.03 </td>
   <td> -0.20 </td>
  </tr>
  <tr>
   <td> bm_bw_b_4 </td>
   <td> 0.07 </td>
   <td> 0.96 </td>
   <td> 0.01 </td>
   <td> -0.04 </td>
   <td> 0.01 </td>
   <td> -0.01 </td>
   <td> 0.09 </td>
   <td> -0.03 </td>
   <td> -0.18 </td>
  </tr>
  <tr>
   <td> bm_ww_b_1 </td>
   <td> 0.02 </td>
   <td> 0.05 </td>
   <td> 0.95 </td>
   <td> 0.01 </td>
   <td> -0.01 </td>
   <td> 0.01 </td>
   <td> -0.03 </td>
   <td> -0.03 </td>
   <td> 0.01 </td>
  </tr>
  <tr>
   <td> bm_ww_b_2 </td>
   <td> -0.03 </td>
   <td> 0.03 </td>
   <td> 0.99 </td>
   <td> 0.02 </td>
   <td> -0.03 </td>
   <td> 0.01 </td>
   <td> -0.01 </td>
   <td> 0.05 </td>
   <td> 0.00 </td>
  </tr>
  <tr>
   <td> bm_ww_b_3 </td>
   <td> -0.03 </td>
   <td> -0.02 </td>
   <td> 0.94 </td>
   <td> -0.01 </td>
   <td> 0.05 </td>
   <td> 0.01 </td>
   <td> -0.04 </td>
   <td> 0.02 </td>
   <td> -0.06 </td>
  </tr>
  <tr>
   <td> bm_ww_b_4 </td>
   <td> -0.03 </td>
   <td> 0.00 </td>
   <td> 0.91 </td>
   <td> 0.00 </td>
   <td> 0.04 </td>
   <td> -0.01 </td>
   <td> -0.08 </td>
   <td> 0.06 </td>
   <td> 0.00 </td>
  </tr>
</tbody>
</table>

</details>

## Scale construction

The analyses use composite scale scores for linked fate, relational orientation, pity elicitation, active facilitation, and intergroup contact. Items marked as reverse-coded were recoded before computing the composites.

<div class="item-card">
<h4>Relational orientation toward the other group</h4>
<p class="item-note">Participants rated items about perceived support and competition between Black women and White women at work.</p>
<ul>
<li>White women really care about Black women's well-being at work.</li>
<li>White women act competitively with Black women in the workplace. <em>Reverse-coded</em></li>
<li>Black women really care about White women's well-being at work.</li>
<li>Black women act competitively with White women in the workplace. <em>Reverse-coded</em></li>
</ul>
</div>

<div class="item-card">
<h4>Pity elicitation and active facilitation</h4>
<p class="item-note">Participants rated how people high in power and status in organizations respond to each group.</p>
<ul>
<li>To what extent do people high in power and status feel pity toward White women at work?</li>
<li>To what extent do people high in power and status feel sympathy toward Black women at work?</li>
<li>To what extent do people high in power and status assist White women at work?</li>
<li>To what extent do people high in power and status defend Black women at work?</li>
</ul>
</div>

<div class="item-card">
<h4>Linked fate</h4>
<p class="item-note">Participants rated perceived shared workplace outcomes between Black women and White women.</p>
<ul>
<li>Career progress for one group also means career progress for the other group.</li>
<li>If treatment for one of these groups gets worse, the treatment of the other group will also get worse.</li>
<li>Workplace issues that affect Black women also affect White women.</li>
<li>Black women and White women have encountered similar discrimination in the past.</li>
</ul>
</div>



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
   <td> White women relational orientation toward Black women </td>
   <td> 0.92 </td>
  </tr>
  <tr>
   <td> Black women relational orientation toward White women </td>
   <td> 0.84 </td>
  </tr>
  <tr>
   <td> Pity elicitation of White women </td>
   <td> 0.87 </td>
  </tr>
  <tr>
   <td> Pity elicitation of Black women </td>
   <td> 0.80 </td>
  </tr>
  <tr>
   <td> Active facilitation of White women </td>
   <td> 0.97 </td>
  </tr>
  <tr>
   <td> Active facilitation of Black women </td>
   <td> 0.96 </td>
  </tr>
  <tr>
   <td> Linked fate </td>
   <td> 0.86 </td>
  </tr>
  <tr>
   <td> Intergroup contact </td>
   <td> 0.94 </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Scale descriptives by participant group</caption>
 <thead>
  <tr>
   <th> Scale </th>
   <th> Group </th>
   <th> N </th>
   <th> M </th>
   <th> SD </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Active facilitation of Black women </td>
   <td> Black women </td>
   <td> 203 </td>
   <td> 3.49 </td>
   <td> 1.54 </td>
  </tr>
  <tr>
   <td> Active facilitation of Black women </td>
   <td> White women </td>
   <td> 207 </td>
   <td> 4.20 </td>
   <td> 1.49 </td>
  </tr>
  <tr>
   <td> Active facilitation of White women </td>
   <td> Black women </td>
   <td> 203 </td>
   <td> 5.71 </td>
   <td> 1.14 </td>
  </tr>
  <tr>
   <td> Active facilitation of White women </td>
   <td> White women </td>
   <td> 207 </td>
   <td> 4.56 </td>
   <td> 1.33 </td>
  </tr>
  <tr>
   <td> Black women relational orientation toward White women </td>
   <td> Black women </td>
   <td> 203 </td>
   <td> 4.65 </td>
   <td> 0.88 </td>
  </tr>
  <tr>
   <td> Black women relational orientation toward White women </td>
   <td> White women </td>
   <td> 207 </td>
   <td> 4.50 </td>
   <td> 1.18 </td>
  </tr>
  <tr>
   <td> Intergroup contact </td>
   <td> Black women </td>
   <td> 203 </td>
   <td> 5.51 </td>
   <td> 1.50 </td>
  </tr>
  <tr>
   <td> Intergroup contact </td>
   <td> White women </td>
   <td> 207 </td>
   <td> 4.04 </td>
   <td> 1.88 </td>
  </tr>
  <tr>
   <td> Linked fate </td>
   <td> Black women </td>
   <td> 203 </td>
   <td> 3.34 </td>
   <td> 1.25 </td>
  </tr>
  <tr>
   <td> Linked fate </td>
   <td> White women </td>
   <td> 207 </td>
   <td> 4.46 </td>
   <td> 1.05 </td>
  </tr>
  <tr>
   <td> Pity elicitation of Black women </td>
   <td> Black women </td>
   <td> 203 </td>
   <td> 2.88 </td>
   <td> 1.44 </td>
  </tr>
  <tr>
   <td> Pity elicitation of Black women </td>
   <td> White women </td>
   <td> 207 </td>
   <td> 3.12 </td>
   <td> 1.36 </td>
  </tr>
  <tr>
   <td> Pity elicitation of White women </td>
   <td> Black women </td>
   <td> 203 </td>
   <td> 3.91 </td>
   <td> 1.79 </td>
  </tr>
  <tr>
   <td> Pity elicitation of White women </td>
   <td> White women </td>
   <td> 207 </td>
   <td> 2.82 </td>
   <td> 1.29 </td>
  </tr>
  <tr>
   <td> White women relational orientation toward Black women </td>
   <td> Black women </td>
   <td> 203 </td>
   <td> 3.46 </td>
   <td> 1.25 </td>
  </tr>
  <tr>
   <td> White women relational orientation toward Black women </td>
   <td> White women </td>
   <td> 207 </td>
   <td> 4.76 </td>
   <td> 1.02 </td>
  </tr>
</tbody>
</table>

## Scale correlations

The correlation table shows how the linked fate outcome relates to the mediator scales. This helps contextualize the later mediation model by showing whether the proposed mediators are associated with linked fate in the expected direction.

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Scale correlations</caption>
 <thead>
  <tr>
   <th> Scale </th>
   <th> Linked fate </th>
   <th> White women relational orientation toward Black women </th>
   <th> Black women relational orientation toward White women </th>
   <th> Pity elicitation of White women </th>
   <th> Pity elicitation of Black women </th>
   <th> Active facilitation of White women </th>
   <th> Active facilitation of Black women </th>
   <th> Intergroup contact </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Linked fate </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
  </tr>
  <tr>
   <td> White women relational orientation toward Black women </td>
   <td> 0.41 </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
  </tr>
  <tr>
   <td> Black women relational orientation toward White women </td>
   <td> 0.06 </td>
   <td> 0.26 </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
  </tr>
  <tr>
   <td> Pity elicitation of White women </td>
   <td> -0.13 </td>
   <td> -0.40 </td>
   <td> -0.02 </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
  </tr>
  <tr>
   <td> Pity elicitation of Black women </td>
   <td> 0.12 </td>
   <td> 0.05 </td>
   <td> -0.17 </td>
   <td> 0.20 </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
  </tr>
  <tr>
   <td> Active facilitation of White women </td>
   <td> -0.31 </td>
   <td> -0.30 </td>
   <td> 0.22 </td>
   <td> 0.32 </td>
   <td> -0.04 </td>
   <td>  </td>
   <td>  </td>
   <td>  </td>
  </tr>
  <tr>
   <td> Active facilitation of Black women </td>
   <td> 0.28 </td>
   <td> 0.45 </td>
   <td> -0.00 </td>
   <td> -0.11 </td>
   <td> 0.31 </td>
   <td> 0.07 </td>
   <td>  </td>
   <td>  </td>
  </tr>
  <tr>
   <td> Intergroup contact </td>
   <td> -0.19 </td>
   <td> -0.18 </td>
   <td> 0.17 </td>
   <td> 0.15 </td>
   <td> -0.02 </td>
   <td> 0.32 </td>
   <td> -0.03 </td>
   <td>  </td>
  </tr>
</tbody>
</table>

## Group comparisons

These tests compare Black women and White women on linked fate and the proposed mediators. The key descriptive pattern is whether the groups differ not only in linked fate, but also in perceptions of relational orientation and workplace treatment.

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Group comparisons on linked fate and mediator scales</caption>
 <thead>
  <tr>
   <th> Scale </th>
   <th> Contrast </th>
   <th> M1 </th>
   <th> SD1 </th>
   <th> M2 </th>
   <th> SD2 </th>
   <th> t </th>
   <th> df </th>
   <th> p </th>
   <th> d </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Linked fate </td>
   <td> Black women − White women </td>
   <td> 3.34 </td>
   <td> 1.25 </td>
   <td> 4.46 </td>
   <td> 1.05 </td>
   <td> -9.87 </td>
   <td> 408 </td>
   <td> &lt; .001 </td>
   <td> -0.97 </td>
  </tr>
  <tr>
   <td> White women relational orientation toward Black women </td>
   <td> Black women − White women </td>
   <td> 3.46 </td>
   <td> 1.25 </td>
   <td> 4.76 </td>
   <td> 1.02 </td>
   <td> -11.56 </td>
   <td> 408 </td>
   <td> &lt; .001 </td>
   <td> -1.14 </td>
  </tr>
  <tr>
   <td> Black women relational orientation toward White women </td>
   <td> Black women − White women </td>
   <td> 4.65 </td>
   <td> 0.88 </td>
   <td> 4.50 </td>
   <td> 1.18 </td>
   <td> 1.44 </td>
   <td> 408 </td>
   <td> 0.152 </td>
   <td> 0.14 </td>
  </tr>
  <tr>
   <td> Pity elicitation of White women </td>
   <td> Black women − White women </td>
   <td> 3.91 </td>
   <td> 1.79 </td>
   <td> 2.82 </td>
   <td> 1.29 </td>
   <td> 7.07 </td>
   <td> 408 </td>
   <td> &lt; .001 </td>
   <td> 0.70 </td>
  </tr>
  <tr>
   <td> Pity elicitation of Black women </td>
   <td> Black women − White women </td>
   <td> 2.88 </td>
   <td> 1.44 </td>
   <td> 3.12 </td>
   <td> 1.36 </td>
   <td> -1.78 </td>
   <td> 408 </td>
   <td> 0.075 </td>
   <td> -0.18 </td>
  </tr>
  <tr>
   <td> Active facilitation of White women </td>
   <td> Black women − White women </td>
   <td> 5.71 </td>
   <td> 1.14 </td>
   <td> 4.56 </td>
   <td> 1.33 </td>
   <td> 9.46 </td>
   <td> 408 </td>
   <td> &lt; .001 </td>
   <td> 0.93 </td>
  </tr>
  <tr>
   <td> Active facilitation of Black women </td>
   <td> Black women − White women </td>
   <td> 3.49 </td>
   <td> 1.54 </td>
   <td> 4.20 </td>
   <td> 1.49 </td>
   <td> -4.74 </td>
   <td> 408 </td>
   <td> &lt; .001 </td>
   <td> -0.47 </td>
  </tr>
  <tr>
   <td> Intergroup contact </td>
   <td> Black women − White women </td>
   <td> 5.51 </td>
   <td> 1.50 </td>
   <td> 4.04 </td>
   <td> 1.88 </td>
   <td> 8.76 </td>
   <td> 408 </td>
   <td> &lt; .001 </td>
   <td> 0.87 </td>
  </tr>
</tbody>
</table>

### Linked fate compared with the scale midpoint

The midpoint tests show whether each group’s linked fate ratings are above or below the neutral point of the scale. This helps clarify whether group differences reflect one group reporting relatively high linked fate, the other reporting relatively low linked fate, or both.

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>One-sample tests comparing linked fate to the scale midpoint</caption>
 <thead>
  <tr>
   <th> Scale </th>
   <th> Group </th>
   <th> M </th>
   <th> SD </th>
   <th> t </th>
   <th> df </th>
   <th> p </th>
   <th> d </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Linked fate </td>
   <td> Black women </td>
   <td> 3.34 </td>
   <td> 1.25 </td>
   <td> -7.54 </td>
   <td> 202 </td>
   <td> &lt; .001 </td>
   <td> -0.53 </td>
  </tr>
  <tr>
   <td> Linked fate </td>
   <td> White women </td>
   <td> 4.46 </td>
   <td> 1.05 </td>
   <td> 6.34 </td>
   <td> 206 </td>
   <td> &lt; .001 </td>
   <td> 0.44 </td>
  </tr>
</tbody>
</table>

## Mediation model

The mediation model tests whether the difference between Black women and White women in linked fate is explained by perceived relational orientation, pity elicitation, and active facilitation. Participant race is coded 0 = White women and 1 = Black women, so negative indirect effects indicate pathways that help explain lower linked fate among Black women relative to White women.


``` r
data <- data %>%
  dplyr::mutate(
    race_proc = dplyr::case_when(
      race_name == "White women" ~ 0,
      race_name == "Black women" ~ 1
    )
  )

mediator_vars <- c("supp_comp_wb", "supp_comp_bw", "emotion_ww", "emotion_bw", "behavior_ww", "behavior_bw")
mediator_labels <- c("supp_comp_wb" = "White women relational orientation toward Black women", "supp_comp_bw" = "Black women relational orientation toward White women", "emotion_ww" = "Pity elicitation of White women", "emotion_bw" = "Pity elicitation of Black women", "behavior_ww" = "Active facilitation of White women", "behavior_bw" = "Active facilitation of Black women")

mediation_results <- run_parallel_mediation(
  data = data,
  x = "race_proc",
  y = "linkedfate",
  mediators = mediator_vars,
  mediator_labels = mediator_labels,
  boot = 10000,
  seed = 654321
)
```

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Mediation paths and indirect effects</caption>
 <thead>
  <tr>
   <th> Mediator </th>
   <th> a path </th>
   <th> a path p </th>
   <th> b path </th>
   <th> b path p </th>
   <th> Indirect effect </th>
   <th> 95% CI </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> White women relational orientation toward Black women </td>
   <td> -1.30 </td>
   <td> &lt; .001 </td>
   <td> 0.15 </td>
   <td> 0.014 </td>
   <td> -0.19 </td>
   <td> [-0.37, -0.03] </td>
  </tr>
  <tr>
   <td> Black women relational orientation toward White women </td>
   <td> 0.15 </td>
   <td> 0.152 </td>
   <td> 0.11 </td>
   <td> 0.057 </td>
   <td> 0.02 </td>
   <td> [-0.01, 0.05] </td>
  </tr>
  <tr>
   <td> Pity elicitation of White women </td>
   <td> 1.09 </td>
   <td> &lt; .001 </td>
   <td> 0.09 </td>
   <td> 0.023 </td>
   <td> 0.10 </td>
   <td> [0.01, 0.18] </td>
  </tr>
  <tr>
   <td> Pity elicitation of Black women </td>
   <td> -0.25 </td>
   <td> 0.075 </td>
   <td> 0.02 </td>
   <td> 0.689 </td>
   <td> -0.00 </td>
   <td> [-0.04, 0.02] </td>
  </tr>
  <tr>
   <td> Active facilitation of White women </td>
   <td> 1.16 </td>
   <td> &lt; .001 </td>
   <td> -0.21 </td>
   <td> &lt; .001 </td>
   <td> -0.24 </td>
   <td> [-0.38, -0.11] </td>
  </tr>
  <tr>
   <td> Active facilitation of Black women </td>
   <td> -0.71 </td>
   <td> &lt; .001 </td>
   <td> 0.14 </td>
   <td> 0.001 </td>
   <td> -0.10 </td>
   <td> [-0.18, -0.03] </td>
  </tr>
</tbody>
</table>

<table class="table table-striped table-hover table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>Total, direct, and total indirect effects</caption>
 <thead>
  <tr>
   <th> Effect </th>
   <th> Estimate </th>
   <th> 95% CI </th>
   <th> p </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td> Total indirect </td>
   <td> -0.42 </td>
   <td> [-0.63, -0.24] </td>
   <td>  </td>
  </tr>
  <tr>
   <td> Direct </td>
   <td> -0.70 </td>
   <td> [-0.98, -0.42] </td>
   <td> &lt; .001 </td>
  </tr>
  <tr>
   <td> Total </td>
   <td> -1.13 </td>
   <td> [-1.35, -0.90] </td>
   <td> &lt; .001 </td>
  </tr>
</tbody>
</table>

The mediation tables summarize all paths in the parallel mediation model. The indirect-effect table is the primary result: indirect effects with confidence intervals that do not include zero indicate mediators that help explain the linked fate difference between Black women and White women.

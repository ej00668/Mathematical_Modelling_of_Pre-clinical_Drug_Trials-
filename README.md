<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    tex2jax: {
      inlineMath: [['$','$'], ['\\(','\\)']],
      displayMath: [['$$','$$']],
      processEscapes: true,
      skipTags: ['script', 'noscript', 'style', 'textarea', 'pre']
    }
  });
</script>

&nbsp;

<h1 style="text-align: center;"> BMC-BAMC '25, University of Exeter </h1>

<h2 style="text-align: center;"> Abstract </h2>

Translating findings from pre-clinical to clinical drug trials remains a significant challenge in pharmacology. The main issue is that most pre-clinical studies rely on mouse xenograft models, whereas clinical trials are conducted in humans, where tumours exhibit greater structural constraints and biological differences. A key step toward improving this translation is developing a robust mathematical understanding of pre-clinical trials outcomes, which can enhance predictive modelling, refine drug development strategies, and reduce reliance on animal models.
 
In this study, we analyse tumour growth data from patient-derived xenograft (PDX) models used in pre-clinical trials of small-molecule cytotoxic chemotherapy. The dataset (source: Novartis, open-source dataset) includes longitudinal tumour volume measurements across multiple cancer types capturing both untreated tumour growth and responses to various drug treatments. To characterise tumour growth dynamics, we fit non-linear mixed effects mechanistic tumour growth models for empirical growth laws that account for inter-tumour variability and treatment effects.
 
Beyond model fitting, we explore optimal dosing strategies for small-molecule drugs by integrating our models with RECIST (Response Evaluation Criteria in Solid Tumours)-based response criteria, a set of guidelines used to assess the response of cancer patients to treatment for nutrient diffusion models. Our findings contribute to a deeper understanding of pre-clinical tumour growth patterns and provide a framework for improving dose optimisation, an important step in mathematical oncology. Longer term, this project, in collaboration with GlaxoSmithKline (GSK), aims to establish mechanistic modelling approaches incorporating spatial, pharmacokinetic and pharmacodynamic (PKPD) effects to create models that are fit-for-use in drug development.


---

<h2 style="text-align: center;"> Non-linear Mixed Effects Framework </h2>

In continuation to the PDX data analysis, a non-linear mixed effects framework was applied to the data and the model was fitted using the exponential-linear growth law. Two models were compared where each time, the random effect variable was changed. In the first model, only the exponential growth rate ($$\lambda_0$$) was considered as a random effect and in the second model, both exponential and linear growth rate ($$\lambda_1$$) were considered as the random effect. The figure shows the results of the fitting for the PDX data using the non-linear mixed effects framework with the data grouped according to the type of the tumour. 

<p align="center">
<img src="NLME_Fit_Highres.png">
</p>

The table below compares the two models and gives an estimate for the parameters used in the exponential-linear growth law: 

<table align="center" style="width: 90%; border-collapse: collapse; margin: 20px auto;">
<tr style="background-color: #f2f2f2;">
  <th style="width: 30%; padding: 12px; border: 1px solid #ddd; text-align: left;">Model</th>
  <th style="width: 20%; padding: 12px; border: 1px solid #ddd; text-align: center;">Parameter</th>
  <th style="width: 20%; padding: 12px; border: 1px solid #ddd; text-align: center;">Estimate</th>
  <th style="width: 15%; padding: 12px; border: 1px solid #ddd; text-align: center;">AIC</th>
  <th style="width: 15%; padding: 12px; border: 1px solid #ddd; text-align: center;">BIC</th>
</tr>
<tr>
  <td style="padding: 10px; border: 1px solid #ddd; vertical-align: top;">Fixed: $$V_0$$, $$\lambda_1$$<br>Random: $$\lambda_0$$</td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">$$V_0$$</td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">0.2613</td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center; vertical-align: middle;" rowspan="3">277.4102</td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center; vertical-align: middle;" rowspan="3">303.6705</td>
</tr>
<tr>
  <td style="padding: 10px; border: 1px solid #ddd;"></td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">$$\lambda_0$$</td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">0.0664</td>
</tr>
<tr>
  <td style="padding: 10px; border: 1px solid #ddd;"></td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">$$\lambda_1$$</td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">0.0825</td>
</tr>
<tr style="border-top: 2px solid #333;">
  <td style="padding: 10px; border: 1px solid #ddd; vertical-align: top;">Fixed: $$V_0$$<br>Random: $$\lambda_0$$, $$\lambda_1$$</td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">$$V_0$$</td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">0.2614</td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center; vertical-align: middle;" rowspan="3">282.1145</td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center; vertical-align: middle;" rowspan="3">318.8789</td>
</tr>
<tr>
  <td style="padding: 10px; border: 1px solid #ddd;"></td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">$$\lambda_0$$</td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">0.0664</td>
</tr>
<tr>
  <td style="padding: 10px; border: 1px solid #ddd;"></td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">$$\lambda_1$$</td>
  <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">0.0726</td>
</tr>
</table>

---

<h2 style="text-align: center;"> Add title </h2>

text
 
 ---

 My profile: [here](https://www.surrey.ac.uk/people/esha-joshi).

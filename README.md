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

<p align="center">
<img src="Table1.png">
</p>
The p-value is significant only for model 1 which considers the exponential growth rate ($$\lambda_0$$) as a random effect, suggesting that during the pre-clinical trials, the tumour never approaches the vascular stage but instead stays in the avascular stage. This supports the argument of the early termination of the experiment which takes into consideration the welfare limit of the mouse. 


---

<h2 style="text-align: center;"> Bibliography </h2>

[1] Nasim, A., Yates, J., Derks, G. & Dunlop, C. A spatially resolved mechanistic growth law for cancer drug development predicting tumour growing fractions. Cancer Res. Commun. 2, 754–761 (2022).

[2] Deakin, A. S. Model for the growth of a solid in vitro tumor. Growth 39, 159–65 (1975).

[3] Gao, H. et al. High-throughput screening using patient-derived tumor xenografts to predict clinical trial drug response. Nat. Med. 21, 1318–1325 (2015).  

 
 ---

 My profile: [here](https://www.surrey.ac.uk/people/esha-joshi).

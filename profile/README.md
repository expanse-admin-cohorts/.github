## Welcome

This is the GitHub Organization for the administrative cohorts analyses in EXPANSE WP3.

## Pilot Analysis

### Outcomes

* Stroke incidence
* All-cause mortality

### Exosures

* PM2.5
* NO2
* BC
* warm season O3
* NDVI
* Distance to water
* Impervious surfaces
* Kernel density for the 3 food environments (restaurants, fast foods, supermarkets)
* mean annual/warm season/cold season temperature
* mean and season-specific temperature SD (warm: April-September; cold: January-March + October-December)

### Covariates

TODO

### Statistical Models

#### Single-Exposure Models

We will apply Cox proportional hazard models with successively more detailed control for individual- and area-level confounders to analyze the associations between exposures (single-exposure models) and mortality / morbidity. We will apply sex-stratified Cox regression for all cohorts as the main model.
Age will be the time scale because of evidence of better adjustment for potential confounding by age (Thiebaut et al. 2004). Censoring occurs at the time of the event of interest, death for other causes, emigration, loss to follow-up for other reasons, or at end of follow-up, whichever comes first. A priori we will specify three confounder models:

* Model 1 will include only age (time axis), sex (strata), and calendar time (year(s) of enrollment) and a dummy variable for the NUTS-1 areas when country-wide cohorts are analysed. Exposures will be entered as linear terms in the model.

* Model 2 will add the individual level variables available within each cohort. We will control for as many covariates as possible. Availability of these covariates differs by administrative cohort.

* Model 3 will add to Model 2 area-level socio-economic status (SES) variables. Model 3 will be selected as the main model. For all administrative cohorts data on fine spatial scale area-level socio-economic status are available, which will be analyzed as proxies for individual SES and lifestyle co-variables and direct neighborhood effects. All cohorts should include an area broadly representing neighborhood and also consider a larger spatial scale (eg metropolitan area, NUTS 3). In case both neighborhood and larger area covariates are available, these will be both entered in the model linearly after subtracting the covariate value at the larger area from the corresponding neighborhood level one.

#### Concentration response shape

We will investigate the concentration-response shapes in Model 3 by a natural cubic spline with three degrees of freedom (df). We will use the Bayesian Information Criterion (BIC) to compare the goodness of fit of the models using a linear vs a spline function. After comparison of cohort-specific results Model 3 may be adjusted accordingly.

#### Model diagnostics for Cox regression

Cox proportional hazards model assumes that the hazard ratio is constant over time.  Model check for Cox proportional hazards (PH) model is thus necessary to ensure valid interpretation of the results. Graphical evaluation of proportionality of the hazards can be executed in two ways. So called “log-log” plots plot -ln{-ln(survival)} curves for each category of a nominal or ordinal covariate versus ln(analysis time). Optionally, these estimates can be adjusted for covariates. The proportional-hazards assumption is not violated when the curves are parallel. Further, the test of proportional hazards assumption is performed by test of nonzero slope in a generalized linear regression of the scaled Scheinfeld residuals on time. The null hypothesis in this test is of zero slope, which is equivalent of testing that the log hazard-ratio is constant over time.  The rejection of the null hypothesis of a zero slope indicates deviation from the proportional-hazards assumption. Finally, we will test for deviations from the proportional hazards assumption by adding the cross product of each variable with the natural logarithm of age.

We will explore diagnostics in the beginning of the analysis so that the “best” model has stratification terms for variables not meeting the PH assumption. 

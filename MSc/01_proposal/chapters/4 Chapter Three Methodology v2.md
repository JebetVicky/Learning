# CHAPTER THREE: METHODOLOGY

## 3.1 Conceptual framework

Figure 3.1 shows the conceptual framework. DigiCow participation gives farmers information through record-keeping, reminders and expert advice. Farmers who use this information are expected to adopt recommended cattle health management practices, such as health monitoring, heat detection, vaccination and deworming. Better management is expected to support milk production per cow and milk sales, and so annual net income from cattle. This indirect path through management practices is the pathway examined in objective two. A direct path from participation to income allows for other channels, such as market information, better record-keeping and less wasted spending on inputs. Farmer and household characteristics (sex, age band, education, herd size, farm size, location band) affect both participation and outcomes, and are controlled for through matching and regression adjustment. In objective three, the type and intensity of information use are examined as factors associated with practice adoption among users.

The framework distinguishes management practices from animal health itself. The cattle health index in the DigiCow data records reported practices, not clinical outcomes such as disease incidence or mortality. The pathway is therefore labelled cattle health management, and any link to animal health is an assumption the study states rather than measures.

```
                      Farmer and household characteristics
                (sex, age band, education, herd size, location band)
                         |                          |
                         v                          v
 DigiCow participation -> Information use -> Cattle health management -> Milk production and sales -> Net income from cattle
   (Objective 1)          (type, intensity)   practices (index)                                          ^
                          (Objective 3)       (Objective 2: pathway)                                     |
        |                                                                                                |
        +--------------------------- direct path (other channels) --------------------------------------+
```

*Figure 3.1: Conceptual framework (to be redrawn as a diagram). Arrows show the expected direction of influence.*

## 3.2 Theoretical framework

Following the agricultural household model (Singh et al., 1986), a dairy household *i* chooses inputs to maximise utility subject to a production function in which output depends on inputs, herd characteristics and the household's knowledge *K*:

*Q*~i~ = *f*(*X*~i~, *H*~i~, *K*~i~)  (3.1)

where *Q*~i~ is milk output, *X*~i~ is a vector of inputs, and *H*~i~ is herd management, proxied in this study by the cattle health management index. Participation in DigiCow (*D*~i~ = 1) raises *K*~i~, which may raise *Q*~i~ directly or through better herd management *H*~i~. Net income is *Y*~i~ = *pQ*~i~ − *wX*~i~. The outcome of interest is the average treatment effect on the treated (ATT):

*ATT* = *E*[*Y*~i~(1) | *D*~i~ = 1] − *E*[*Y*~i~(0) | *D*~i~ = 1]  (3.2)

where *Y*~i~(1) and *Y*~i~(0) are the outcomes with and without participation. The second term is unobserved and is estimated from matched comparison farmers.

## 3.3 Study area

The study covers the Kenyan counties in which DigiCow users and comparison farmers were sampled for the ADF2 evaluation [list the counties once the data and evaluation report are received; describe their dairy systems briefly and add a map, Figure 3.2]. Because location is provided only in bands in the k-anonymised data, the study area will be described at the level available in the data and the evaluation report.

## 3.4 Data sources and sample

The study will use secondary data from the independent evaluation of the ADF2 programme, obtained from Mercy Corps AgriFin under a data-use agreement. Three data components will be requested:

1. **Matched impact evaluation microdata for DigiCow**: farmer-level records for treatment (DigiCow users) and comparison farmers, with the matching covariates, outcomes (milk yield, milk sales, net income), the cattle health index and its components, and the matching weights. This is essential for objectives one and two, because the published tables alone do not allow re-estimation, robustness checks or causal mediation analysis. [If only the tables can be shared, objectives one and two will reproduce and extend the published estimates using the reported coefficients and standard errors, and the scope will be adjusted with the supervisor.]
2. **DigiCow clean partner data** (`digicow_clean`): de-identified farmer-level data on demographics, enrolment, services used, frequency of use, practice change, production change and satisfaction, for objective three.
3. **DigiCow impact evaluation tables** (`digicow_ie_tables`): primary, secondary, attenuation and balance tables, used to validate the re-estimation and as a benchmark.

The sample will be the full DigiCow evaluation sample. No new sampling will be done. The evaluation surveyed 502 DigiCow farmers and 775 comparison farmers drawn from a Kenya Agricultural and Livestock Research Organization (KALRO) registry, between 7 and 27 August 2025, with no baseline survey (IDinsight, 2026). [Confirm these numbers and the number of DigiCow users in the clean data once received.] The minimum detectable effect for the main outcomes will be calculated from these sample sizes and the evaluation's methodology report, because a design with no significant income difference needs to show whether it could have detected a plausible effect.

## 3.5 Data analysis

All analysis will be done in R (R Core Team, 2025), with each step written as a script so that the analysis is fully reproducible. The main packages will be `MatchIt` (Ho et al., 2011) and `cobalt` for matching and balance, `WeightIt` and `marginaleffects` for doubly robust estimates, `sensemakr` (Cinelli & Hazlett, 2020) and `rbounds` for sensitivity analysis, `mediation` (Tingley et al., 2014) for causal mediation, and `MASS` or `ordinal` for ordered logit models.

### 3.5.1 Objective one: effect of DigiCow on productivity and income

**Step 1: Propensity score.** The probability of participation will be estimated with a logit model:

*P*(*D*~i~ = 1 | *Z*~i~) = exp(*Z*~i~′γ) / [1 + exp(*Z*~i~′γ)]  (3.3)

where *Z*~i~ contains pre-participation characteristics that affect both participation and outcomes and are not affected by participation (for example sex, age band, education, herd size, farm size, phone type and location band) [finalise the list from the data and the evaluation's own matching model].

**Step 2: Matching.** Treated farmers will be matched to comparison farmers using radius (caliper) matching, as in the original evaluation, with nearest-neighbour and kernel matching as robustness checks. Only farmers in the region of common support will be retained.

**Step 3: Balance.** Matching quality will be checked using standardised mean differences (target below 0.1), variance ratios, the pseudo-R² before and after matching, and density plots of propensity scores (Caliendo & Kopeinig, 2008).

**Step 4: Effect estimation.** The ATT will be estimated for milk production per cow, milk sales (if the data contain a suitable measure) and annual net income from cattle, in levels and in inverse hyperbolic sine (asinh) form to reduce the influence of skewed values and zeros (Bellemare & Wichman, 2020). Standard errors will be bootstrapped or computed from the regression on the matched sample with matching weights.

**Step 5: Robustness.** The ATT will be re-estimated with IPWRA as a doubly robust check. Sensitivity to unobserved confounding will be assessed with Rosenbaum bounds (Rosenbaum, 2002) and with the `sensemakr` robustness value (Cinelli & Hazlett, 2020), which states how strong an unobserved confounder would have to be to explain away the effect.

### 3.5.2 Objective two: cattle health management practices and the income pathway

This objective is the study's central analytical angle. The DigiCow data package contains an attenuation decomposition in which the cattle health management index is added to the model of asinh-transformed income. Re-estimating and extending it on the matched sample allows the study to ask whether any income difference associated with DigiCow runs through improved management practices, or through other channels. The analysis has four steps, and its results will be described as suggestive evidence on a pathway, not as proof of a causal mechanism.

**Step 1: Effect on management practices.** The ATT of participation on the cattle health management index *M*~i~, and on each of its six component practices, will be estimated as in objective one. The evaluation reports a difference of 0.38 points (8.9%), driven mainly by health monitoring and heat detection (IDinsight, 2026), which this step will reproduce first. The index will be rebuilt from its components if the documentation allows.

**Step 2: Association of practices with income.** On the matched sample, the coefficient on *M*~i~ in the income model below (θ) shows whether better management is associated with higher income among farmers with similar characteristics. This tests H~02b~.

**Step 3: Attenuation decomposition.** Two models will be estimated on the matched sample, with income in asinh form:

*Y*~i~ = α~0~ + τ*D*~i~ + *X*~i~′β + ε~i~  (3.4)

*Y*~i~ = α~1~ + τ′*D*~i~ + θ*M*~i~ + *X*~i~′β′ + *u*~i~  (3.5)

The change in the participation coefficient, τ − τ′, shows how much of the participation and income relationship is accounted for by the index. Its confidence interval will be bootstrapped over the matching and both models. Because the evaluation found no statistically significant overall income difference, τ may be close to zero. In that case the share (τ − τ′)/τ is unstable and will not be reported. The study will instead report τ − τ′ and θ with their confidence intervals, and will interpret the result as whether practices and other channels pull in the same or opposite directions. The decomposition by Gelbach (2016) will be used if several components are added together, because it does not depend on the order in which they enter the model.

**Step 4: Causal mediation, where justified.** Following Imai et al. (2010), the average causal mediation effect (ACME) and average direct effect (ADE) will be estimated only if the data show that the practices were measured before the income period, and the main confounders of practices and income are observed. Sequential ignorability is a strong assumption in cross-sectional data with no baseline (Imai et al., 2010; Rudolph et al., 2019), so the sensitivity parameter ρ at which the ACME becomes zero will always be reported alongside any estimate. If these conditions are not met, objective two will rest on Steps 1 to 3 and the limitation will be stated.

### 3.5.3 Objective three: information use and practice adoption among users

Using the DigiCow clean data, two sets of models will be estimated for DigiCow users:

**Practice adoption.** For each recommended practice *k* (for example vaccination, deworming, record-keeping, improved feeding), a binary logit model:

*P*(*A*~ik~ = 1) = Λ(δ~0~ + *S*~i~′δ~1~ + *F*~i~′δ~2~ + *C*~i~′δ~3~)  (3.6)

where *A*~ik~ is adoption of practice *k*, Λ is the logistic function, *S*~i~ is a vector of service-use variables (services used, such as record-keeping, reminders and expert advice; frequency or intensity of use; delivery channel), *F*~i~ is a vector of farmer characteristics (sex, age band, education, herd size), and *C*~i~ includes location band controls. If practice adoption is recorded as a count, a Poisson or negative binomial model will be used instead.

**Reported production change.** Because reported production change is ordinal (for example decreased, no change, increased), an ordered logit model will be used, with the same explanatory variables. The proportional odds assumption will be tested (Brant test), with a generalised ordered logit if it fails.

Average marginal effects will be reported for all models. Multicollinearity will be checked with variance inflation factors, and robust standard errors will be used. Interaction terms between sex and service use will test whether associations differ for women and men.

Table 3.1 lists the variables in the objective three models, how they will be measured and their expected signs. [Support each expected sign with at least two studies, as the Department guide requires, and finalise variables after reviewing the data dictionary.]

*Table 3.1: Description of variables in the practice adoption and production change models and their expected signs*

| Code | Variable | Measurement | Expected sign |
|---|---|---|---|
| ADOPT | Adoption of recommended practice *k* (dependent) | 1 = adopted, 0 = not | |
| PRODCHG | Reported production change (dependent) | 1 = decreased, 2 = no change, 3 = increased | |
| RECORD | Uses DigiCow record-keeping | 1 = yes, 0 = no | + |
| REMIND | Receives DigiCow reminders (vaccination, deworming, breeding) | 1 = yes, 0 = no | + |
| ADVICE | Uses DigiCow expert advice | 1 = yes, 0 = no | + |
| INTENS | Intensity of use | Frequency band or number of services used | + |
| CHANNEL | Main delivery channel | App, SMS, USSD or call (categorical) | ± |
| FEMALE | Sex of farmer | 1 = female, 0 = male | ± |
| AGE | Age band | Categorical | ± |
| EDUC | Education level | Categorical | + |
| HERD | Herd size | Number of dairy cattle or band | + |
| LOC | Location band | Categorical | ± |



### 3.5.4 Summary of analysis by objective

| Objective | Data | Dependent variables | Method | Software |
|---|---|---|---|---|
| 1. Effect on productivity and income | Matched IE microdata | Milk production per cow, milk sales, annual net income from cattle (levels and asinh) | PSM (radius, nearest-neighbour, kernel), IPWRA, Rosenbaum bounds, sensemakr | R: MatchIt, cobalt, WeightIt, sensemakr |
| 2. Management practices and the income pathway | Matched IE microdata, attenuation tables | Cattle health management index and components; net income from cattle (asinh) | Attenuation decomposition with bootstrapped intervals; causal mediation and sensitivity analysis only where justified | R: MatchIt, boot, mediation |
| 3. Information use and practice change | DigiCow clean data | Practice adoption; reported production change | Binary logit, ordered logit, marginal effects | R: MASS or ordinal, marginaleffects |

## 3.6 Validity and reliability

The study will check data quality before analysis (missing values, outliers, implausible values and consistency between related variables), document every cleaning decision in the R scripts, and reproduce the published DigiCow estimates before extending them. Reproducing the original estimates is an important check that the data and definitions have been understood correctly.

## 3.7 Ethical considerations

No new data will be collected from farmers. The data were collected by the independent evaluation team with informed consent and have been de-identified and k-anonymised (k = 5) (Sweeney, 2002). The study will:

1. obtain written permission and a data-use agreement from Mercy Corps AgriFin that covers academic use and publication, and agree authorship and acknowledgement expectations in advance;
2. seek ethical clearance or a formal exemption for secondary analysis of anonymised data from an accredited ethics review committee [confirm the route with the supervisor, for example the KNH-UoN Ethics and Research Committee], and a research licence from the National Commission for Science, Technology and Innovation (NACOSTI) if required;
3. store data only on encrypted, password-protected devices, never on public repositories, and make no attempt to re-identify any farmer or partner staff;
4. report results only in aggregate.

## 3.8 Limitations of the study

1. **Selection on unobservables.** Matching removes bias only from observed characteristics. Farmer motivation or prior extension contact may affect both participation and outcomes. This will be addressed with sensitivity analysis and stated clearly; results will be described as effect estimates under the stated assumptions.
2. **Pathway, not proof of mechanism.** The cattle health index measures reported management practices, not clinical animal health, and practices and income were measured at the same time. Attenuation results therefore show how far practices account for the participation and income relationship, not that practices caused the income change. Causal mediation requires sequential ignorability, which is strong, and will be used only with sensitivity analysis.
3. **Self-reported and recall data.** Milk yield, sales and income are self-reported and may contain recall error.
4. **Cross-sectional design with no baseline.** The study cannot observe changes over time for the same farmers, or confirm that practices changed before income.
5. **Anonymisation.** Banded quasi-identifiers limit analysis by county and exact age.
6. **Generalisability.** Results apply to DigiCow users similar to those in the evaluation, and may not extend to other services or regions.

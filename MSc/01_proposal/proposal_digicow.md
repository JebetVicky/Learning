---
title: "DIGITAL LIVESTOCK ADVISORY SERVICES, CATTLE HEALTH AND DAIRY FARMER INCOME IN KENYA: EVIDENCE FROM DIGICOW"
---

::: {custom-style="Title page"}
VICKY JEBET

AAE62/49784/2026

A research proposal submitted in partial fulfilment of the requirements for the award of the degree of Master of Science in Agricultural Information and Communication Management

DEPARTMENT OF AGRICULTURAL ECONOMICS

FACULTY OF AGRICULTURE

UNIVERSITY OF NAIROBI

DECEMBER 2026
:::

# DECLARATION

This proposal is my original work and has not been presented for the award of a degree in any other University.

Signature: .................................... Date: ....................

Vicky Jebet (AAE62/49784/2026)

This proposal has been submitted with our approval as University supervisors.

Signature: .................................... Date: ....................

Dr Hillary Nyang'anga
Department of Agricultural Economics, University of Nairobi


# ABSTRACT

Smallholder dairy is one of the most important sources of regular cash income for rural households in Kenya, yet milk yields remain low, largely because of poor animal health, weak husbandry practices and thin public extension coverage. Digital livestock advisory services such as DigiCow aim to close this gap by giving farmers record-keeping tools, reminders and expert advice on their phones. Evaluations of such services usually report whether income or yield changed, but rarely show how the change happened or which parts of the service farmers actually use. This study will use secondary data from the independent evaluation of the AgriFin Digital Farmer 2 (ADF2) programme, implemented by Mercy Corps AgriFin from 2021 to 2026, to (i) estimate the effect of DigiCow participation on milk productivity, milk sales and net income; (ii) determine how much of the income effect is mediated by improved cattle health; and (iii) assess how the type and intensity of DigiCow information use, and farmer characteristics, relate to the adoption of recommended practices and reported production change among users. Propensity score matching with doubly robust estimators and formal sensitivity analysis will be used for objective one, attenuation analysis and causal mediation analysis for objective two, and ordered and binary logit models for objective three, all in R. The study will contribute rare evidence on the mechanism behind income gains from digital livestock advice in Africa, and on which information services drive behaviour change. Findings will inform DigiCow and similar service providers, county livestock departments, and funders deciding how to design and scale digital extension for dairy farmers. The expected outputs are an MSc thesis and at least two journal articles.

**Keywords:** digital extension, dairy, animal health, mediation analysis, propensity score matching, Kenya

# CHAPTER ONE: INTRODUCTION

## 1.1 Background

Agriculture remains central to Kenya's economy and to rural livelihoods, and livestock, especially dairy, is one of its most commercialised sub-sectors [add current share of agricultural GDP and number of dairy households from the Kenya National Bureau of Statistics Economic Survey and the Kenya Dairy Board; cite the year]. Most of the country's milk is produced by smallholder farmers keeping a few cows on small plots, for whom milk is a daily source of cash and household nutrition (Rademaker et al., 2016 [verify]).

Despite this importance, smallholder milk yields remain well below what improved breeds can achieve under good management [add yield gap figure and source]. The main constraints are well documented: disease and parasite burden, poor feeding and breeding practices, weak record-keeping, and limited access to veterinary and extension services. Public livestock extension in Kenya is thinly staffed relative to the number of farmers it is meant to serve [add extension officer to farmer ratio and source], so many farmers rely on neighbours, agro-vet shops and informal sources for advice.

Mobile phones have opened a new route for delivering agricultural information. Digital advisory services send farmers timely, low-cost messages, reminders and expert answers, and can reach far more farmers per shilling than face-to-face extension (Aker, 2011; Fabregas, Kremer and Schilbach, 2019). In dairy, services such as DigiCow combine herd record-keeping, reminders for vaccination, deworming and breeding, and on-demand advice from veterinary and extension experts [confirm DigiCow's service features from the provider and the ADF2 documentation].

Kenya's policy environment encourages this shift. The Agricultural Sector Transformation and Growth Strategy 2019 to 2029 and the Digital Economy Blueprint both emphasise digitally enabled services for smallholder farmers (Republic of Kenya, 2019a; 2019b). The Mercy Corps AgriFin Digital Farmer 2 (ADF2) programme, implemented from 2021 to August 2026 in Kenya, Nigeria and Ethiopia, worked with eleven digital service partners, including DigiCow, to design, test and scale bundles of digital services for smallholder farmers (Mercy Corps AgriFin, 2026). An independent evaluation of ADF2 generated de-identified farmer-level data and impact estimates for five partners, including DigiCow. This study will use that evidence.

## 1.2 Statement of the problem

Digital agricultural advisory services have grown quickly, but the evidence on their effects is mixed and, above all, thin on mechanisms. Reviews find modest average gains in knowledge, adoption of recommended inputs and yields, with wide variation between programmes (Fabregas et al., 2019; Spielman et al., 2021). Most studies report whether an outcome such as yield or income changed. Very few show *why* it changed, so it is not known whether the gains come from the expected pathway, such as better animal health, or from other channels such as better record-keeping, market information or lower input waste.

This gap matters especially for livestock. Almost all rigorous evidence on digital extension concerns crops (Cole and Fernando, 2021; Van Campenhout, Spielman and Lecoutere, 2021), while evidence on digital livestock advisory in Africa is limited to a small number of studies (for example Marwa et al., 2020). For dairy, animal health is the most plausible pathway from advice to income, but this has not been formally tested with evaluation data. In addition, platforms and funders know little about which components of a digital livestock service, and what intensity of use, are associated with real changes in farm practice, which limits their ability to design and target services.

Without this evidence, service providers, county governments and funders risk scaling digital livestock services on the basis of reach figures or a single average effect, without knowing which channel delivers the gain or which services farmers act on. The ADF2 evaluation of DigiCow provides a rare opportunity to address this: it includes a matched treatment and comparison sample, a cattle health index and an attenuation analysis, together with farmer-level usage data. The study will use these data to estimate the effect of DigiCow, test the animal health pathway and identify which information services drive practice change.

## 1.3 Objectives of the study

### 1.3.1 General objective

To contribute to the design of effective digital livestock extension in Kenya by assessing the effect of the DigiCow digital advisory service on dairy farmers' productivity and income, the role of cattle health in that effect, and the information-use factors associated with practice change.

### 1.3.2 Specific objectives

1. To estimate the effect of DigiCow participation on milk yield per cow per day, milk sales and household net income among smallholder dairy farmers in Kenya.
2. To determine the extent to which the effect of DigiCow participation on net income is mediated by improved cattle health.
3. To assess the influence of the type and intensity of DigiCow information use, and of farmer characteristics, on the adoption of recommended dairy practices and on reported production change among DigiCow users.

## 1.4 Hypotheses

1. DigiCow participation has no significant effect on milk yield per cow per day, milk sales or household net income.
2. Cattle health does not significantly mediate the effect of DigiCow participation on household net income.
3. The type and intensity of DigiCow information use, and farmer characteristics, have no significant influence on the adoption of recommended dairy practices or on reported production change.

## 1.5 Justification of the study

**Who will use the results.** DigiCow and other digital livestock service providers will learn which services and levels of use are associated with practice change, helping them prioritise features and target farmers. County departments of livestock, which share responsibility for extension under devolution, can use the findings to decide how digital tools should complement extension officers. Funders and programme designers, including Mercy Corps AgriFin and similar programmes, will gain evidence on whether to fund digital livestock advisory and how to evaluate it. Dairy cooperatives, which often bundle services for members, may use the results to decide whether to partner with digital providers.

**Contribution to knowledge.** The study will provide one of few rigorous estimates of the effect of a digital livestock advisory service in Africa, and, to the author's knowledge [confirm after the literature search], the first formal test of whether animal health mediates the income effect of such a service. By linking information-use patterns to practice change, it also contributes to the agricultural information and communication literature on what turns access to digital information into action.

**Feasibility and responsibility.** Using existing, de-identified evaluation data allows a rigorous analysis at low cost, within the MSc timeline, without asking farmers who have already been surveyed to give their time again.

## 1.6 Scope and limitations of the study

The study is limited to DigiCow users and matched comparison farmers in Kenya included in the ADF2 independent evaluation, and to the outcomes and covariates measured by that evaluation. It will not collect primary data. Because participation was not randomly assigned, the effect estimates rely on the assumption that matching on observed characteristics removes selection bias; this will be tested with sensitivity analysis and stated as a limitation. Outcomes are self-reported and some rely on recall. The k-anonymisation of the data (k = 5) means that age, location and other quasi-identifiers are grouped into bands, which limits fine-grained analysis by county or age.

## 1.7 Organisation of the proposal

Chapter One has introduced the study. Chapter Two reviews the concepts, theories and empirical studies on which the study builds and identifies the research gap. Chapter Three describes the methodology, including the conceptual and theoretical frameworks, data, analytical methods for each objective, and ethical considerations. The expected outputs, work plan and budget follow, with references and appendices at the end.

# CHAPTER TWO: LITERATURE REVIEW

## 2.1 Introduction

This chapter reviews the literature that underpins the study. It first defines digital agricultural advisory services and describes the smallholder dairy context in Kenya. It then reviews the theories that explain how information affects farm decisions and outcomes, the methods used to estimate the effects of extension and their mechanisms, and the empirical evidence on digital extension. It closes with a summary of the research gap.

## 2.2 Digital agricultural advisory services

Agricultural extension is the provision of information, advice and training to help farmers improve their practices and incomes (Anderson and Feder, 2004). Digital agricultural advisory services deliver this through mobile and digital channels, including SMS, voice and interactive voice response (IVR), USSD menus, smartphone applications, hotlines and social media (Aker, 2011; Tsan et al., 2019). Their main advantages are low marginal cost, timeliness and the ability to personalise content; their main limits include low literacy, gaps in phone ownership, especially among women, and the difficulty of building trust without face-to-face contact (Aker, 2011; Spielman et al., 2021).

[Add: a short description of the evolution of digital advisory in Kenya, for example from early SMS services to bundled platforms, and the size of the sector, from Tsan et al. (2019) and more recent sources.]

## 2.3 Smallholder dairy in Kenya and the role of animal health

[Describe the structure of Kenya's dairy sector: the share of milk from smallholders, the main dairy counties, breeds, formal and informal milk marketing, and productivity trends. Sources: Kenya Dairy Board, KALRO, the KNBS Economic Survey, Rademaker et al. (2016).]

[Review the link between animal health and productivity: the main diseases and parasites affecting dairy cattle in Kenya (for example East Coast fever, mastitis, foot and mouth disease, helminths), their effects on milk yield and herd losses, and the role of preventive practices such as vaccination, deworming, tick control and record-keeping.]

## 2.4 Theoretical review

### 2.4.1 Theories underpinning the study

**Agricultural household model.** The agricultural household model treats the farm household as both a producer and a consumer that allocates land, labour and capital to maximise utility subject to production technology, prices and a budget constraint (Singh, Squire and Strauss, 1986). Information enters the model by shifting the household's perceived production function: better knowledge of animal health and husbandry raises the expected output from a given set of inputs or changes the input mix, and so changes production, sales and income.

**Diffusion of innovations.** Rogers (2003) explains adoption as a process through which an innovation is communicated over time through certain channels among members of a social system. It highlights the role of communication channels, perceived attributes of the innovation (relative advantage, compatibility, complexity, trialability and observability) and adopter characteristics, which is directly relevant to how farmers take up advice delivered by DigiCow.

**Technology acceptance and continuance.** The Technology Acceptance Model (Davis, 1989) and the Unified Theory of Acceptance and Use of Technology (Venkatesh et al., 2003) explain the intention to use and actual use of an information technology through perceived usefulness, ease of use, social influence and facilitating conditions. The expectation-confirmation model of information systems continuance (Bhattacherjee, 2001) explains why some users keep using a system while others stop.

**Choice of theory.** The study will be anchored in the **agricultural household model**, because its core questions concern how information changes production and income, and it gives a clear basis for the outcome equations and for the causal pathway from participation to practices, health, productivity and income. Diffusion of innovations will be used as a supporting lens for objective three, which concerns how communication channels and information use relate to practice adoption.

### 2.4.2 Approaches to operationalising the theory

In the agricultural household framework, the effect of an intervention such as access to advice can be written as the difference in outcomes with and without the intervention. Because the outcome without the intervention is never observed for participants, impact evaluation methods are needed (Khandker, Koolwal and Samad, 2010).

**Randomised controlled trials** give the most credible estimates but are not available for DigiCow. **Difference-in-differences** requires panel data before and after participation for both groups. **Instrumental variables** require a variable that affects participation but not outcomes directly, which is difficult to find. **Propensity score matching (PSM)** compares participants with non-participants who have a similar probability of participating, given observed characteristics (Rosenbaum and Rubin, 1983; Caliendo and Kopeinig, 2008). **Doubly robust estimators**, such as inverse probability weighted regression adjustment (IPWRA), combine a model of participation with a model of the outcome and remain consistent if either model is correctly specified.

For mechanisms, the classical approach is the **attenuation or product-of-coefficients method**, in which the treatment coefficient is compared with and without the mediator in the model (Baron and Kenny, 1986). The **potential outcomes approach to causal mediation** (Imai, Keele and Tingley, 2010) defines and estimates the average causal mediation effect and the direct effect, and provides a sensitivity analysis for the key assumption of sequential ignorability.

For the factors associated with practice adoption among users, **binary and ordered logit or probit models** are standard, with marginal effects to show the size of each association (Long and Freese, 2014).

Given that the ADF2 evaluation of DigiCow used a matched cross-sectional design, the study will use **PSM with a doubly robust check** for objective one, **attenuation and causal mediation analysis** for objective two, and **logit models** for objective three.

## 2.5 Empirical review

### 2.5.1 Effects of digital advisory services on farm outcomes

Fabregas et al. (2019) reviewed evidence from experimental studies of digital agricultural information in low- and middle-income countries. They found that providing information through mobile phones increased yields by about 4 per cent and the odds of adopting recommended inputs by about 22 per cent on average [verify these figures against the paper], and argued that, given low costs, these services can be highly cost-effective. The present study differs by focusing on livestock rather than crops and by examining the mechanism behind the effect.

Cole and Fernando (2021) evaluated a mobile phone advisory hotline for cotton farmers in Gujarat, India, using a randomised experiment. They found that access changed input choices and that information spread to non-users [verify]. Their study shows that demand-driven, on-call advice can change practice, which is relevant to DigiCow's expert advice feature.

Van Campenhout, Spielman and Lecoutere (2021) tested video-based agricultural advice for maize farmers in Uganda, varying whether information was targeted to men, women or couples [verify findings]. Their study shows that how and to whom digital information is delivered matters, which informs objective three.

Marwa et al. (2020) assessed the impact of the iCow mobile dairy advisory service, a forerunner of DigiCow, on dairy production and household welfare in Uasin Gishu, Nyandarua and Bomet counties of Kenya. Using propensity score matching on cross-sectional survey data comparing iCow users with non-users, they found that iCow use raised annual milk production per cow by 13 per cent, milk income by 29 per cent and household income by 22 per cent. The University of Nairobi thesis on which the study draws, which sampled 457 farmers (209 regular iCow users and 248 non-users), found that effects differed by county and were not significant in Bomet (University of Nairobi Digital Repository, n.d.). This is the closest study to the present one. The present study differs by using a more recent digital service and by testing *why* income changes, through the cattle health pathway, rather than only whether it changes.

Bonilla et al. (2018) evaluated the IFAD-funded Smallholder Dairy Commercialization Programme, implemented by the Government of Kenya in nine counties from 2005 to 2015. Using propensity score matching combined with focus group discussions and key informant interviews, they found that the programme increased milk production but had limited effects on the quantity of milk sold and on prices received. The study shows that production gains do not automatically translate into market and income gains, which supports the present study's decision to measure milk yield, milk sales and income separately.

Chepkirui, Owuor and Kibet (2022) assessed the effect of revolving funds on milk yields among 288 smallholder dairy farmers (144 users and 144 non-users) in Bomet County, Kenya, using propensity score matching. They found no significant effect on milk yield, which they attributed to diversion of funds to non-farm uses. The study illustrates both the use of PSM in Kenyan dairy research and the importance of testing whether an intervention actually reaches the production channel it targets, which the present study does through mediation analysis.

[Add 2 to 5 further studies. Priorities: studies using PSM to evaluate extension or ICT services in Kenya or East Africa; (c) studies using causal mediation analysis in agricultural or development economics.]

### 2.5.2 Animal health, productivity and income in smallholder dairy

Maloo et al. (2001) followed about 120 cattle in 26 smallholder dairy herds in Kaloleni Division, coastal Kenya, from June 1990 to December 1991 to measure disease incidence and mortality. East Coast fever was the main disease, and accumulated mortality to 18 months of age reached 56 per cent. The study shows the scale of losses that animal disease imposes on smallholder dairy and why animal health is a plausible pathway from advice to productivity. Unlike this epidemiological study, the present study links animal health to an information intervention and to household income.

[Add 2 to 4 further studies that quantify the effect of animal health interventions or disease on milk yield and income in Kenya or East Africa.]

### 2.5.3 Information use and practice adoption

[Add 3 to 5 studies on the determinants of continued use of digital agricultural services and on the link between intensity of use and practice change, for example studies using TAM or UTAUT with farmers, and studies of the gender gap in mobile use such as the GSMA Mobile Gender Gap Report.]

## 2.6 Summary of the literature and research gap

The literature shows that digital advisory services can raise adoption of recommended practices and yields at low cost, but effects vary widely and the mechanisms are rarely tested. Evidence is concentrated on crops, with few rigorous studies on digital livestock advisory in Africa. The agricultural household model provides the main theoretical anchor, PSM with doubly robust estimators is the appropriate method for the available matched cross-sectional data, and causal mediation analysis offers a formal way to test the animal health pathway. The study will fill three gaps: (i) rigorous evidence on the effect of a digital livestock advisory service in Kenya; (ii) a formal test of whether animal health mediates the income effect; and (iii) evidence on which information services and levels of use are associated with practice change.

# CHAPTER THREE: METHODOLOGY

## 3.1 Conceptual framework

Figure 3.1 shows the conceptual framework. DigiCow participation provides farmers with information through record-keeping, reminders and expert advice. This information is expected to lead to the adoption of recommended practices (vaccination, deworming, tick control, feeding and breeding). Better practices improve cattle health, which raises milk yield per cow and milk sales, and so household net income. A direct path from participation to income allows for other channels, such as market information, better record-keeping and reduced input waste. Farmer and household characteristics (sex, age band, education, herd size, farm size, location band) affect both participation and outcomes, and are controlled for through matching and regression adjustment. In objective three, the type and intensity of information use moderate the link between participation and practice adoption.

```
                      Farmer and household characteristics
                (sex, age band, education, herd size, location band)
                         |                          |
                         v                          v
 DigiCow participation -> Information use -> Practice adoption -> Cattle health -> Milk yield and sales -> Net income
   (Objective 1)          (type, intensity)    (Objective 3)      (Objective 2: mediator)                   ^
        |                                                                                                   |
        +------------------------------ direct path (other channels) ---------------------------------------+
```

*Figure 3.1: Conceptual framework (to be redrawn as a diagram). Arrows show the expected direction of influence.*

## 3.2 Theoretical framework

Following the agricultural household model (Singh et al., 1986), a dairy household *i* chooses inputs to maximise utility subject to a production function in which output depends on inputs, herd characteristics and the household's knowledge *K*:

*Q*~i~ = *f*(*X*~i~, *H*~i~, *K*~i~)  (3.1)

where *Q*~i~ is milk output, *X*~i~ is a vector of inputs, and *H*~i~ is herd health. Participation in DigiCow (*D*~i~ = 1) raises *K*~i~, which may raise *Q*~i~ directly or by improving *H*~i~. Net income is *Y*~i~ = *pQ*~i~ − *wX*~i~. The outcome of interest is the average treatment effect on the treated (ATT):

*ATT* = *E*[*Y*~i~(1) | *D*~i~ = 1] − *E*[*Y*~i~(0) | *D*~i~ = 1]  (3.2)

where *Y*~i~(1) and *Y*~i~(0) are the outcomes with and without participation. The second term is unobserved and is estimated from matched comparison farmers.

## 3.3 Study area

The study covers the Kenyan counties in which DigiCow users and comparison farmers were sampled for the ADF2 evaluation [list the counties once the data and evaluation report are received; describe their dairy systems briefly and add a map, Figure 3.2]. Because location is provided only in bands in the k-anonymised data, the study area will be described at the level available in the data and the evaluation report.

## 3.4 Data sources and sample

The study will use secondary data from the independent evaluation of the ADF2 programme, obtained from Mercy Corps AgriFin under a data-use agreement. Three data components will be requested:

1. **Matched impact evaluation microdata for DigiCow**: farmer-level records for treatment (DigiCow users) and comparison farmers, with the matching covariates, outcomes (milk yield, milk sales, net income), the cattle health index and its components, and the matching weights. This is essential for objectives one and two, because the published tables alone do not allow re-estimation, robustness checks or causal mediation analysis. [If only the tables can be shared, objectives one and two will reproduce and extend the published estimates using the reported coefficients and standard errors, and the scope will be adjusted with the supervisor.]
2. **DigiCow clean partner data** (`digicow_clean`): de-identified farmer-level data on demographics, enrolment, services used, frequency of use, practice change, production change and satisfaction, for objective three.
3. **DigiCow impact evaluation tables** (`digicow_ie_tables`): primary, secondary, attenuation and balance tables, used to validate the re-estimation and as a benchmark.

The sample will be the full DigiCow evaluation sample. No new sampling will be done. [Report the treatment and comparison sample sizes and the number of DigiCow users in the clean data once received.] A power calculation will be reported for the main outcome to show the minimum detectable effect given the sample sizes.

## 3.5 Data analysis

All analysis will be done in R (R Core Team, 2025), with each step written as a script so that the analysis is fully reproducible. The main packages will be `MatchIt` (Ho et al., 2011) and `cobalt` for matching and balance, `WeightIt` and `marginaleffects` for doubly robust estimates, `sensemakr` (Cinelli and Hazlett, 2020) and `rbounds` for sensitivity analysis, `mediation` (Tingley et al., 2014) for causal mediation, and `MASS` or `ordinal` for ordered logit models.

### 3.5.1 Objective one: effect of DigiCow on productivity and income

**Step 1: Propensity score.** The probability of participation will be estimated with a logit model:

*P*(*D*~i~ = 1 | *Z*~i~) = exp(*Z*~i~′γ) / [1 + exp(*Z*~i~′γ)]  (3.3)

where *Z*~i~ contains pre-participation characteristics that affect both participation and outcomes and are not affected by participation (for example sex, age band, education, herd size, farm size, phone type and location band) [finalise the list from the data and the evaluation's own matching model].

**Step 2: Matching.** Treated farmers will be matched to comparison farmers using radius (caliper) matching, as in the original evaluation, with nearest-neighbour and kernel matching as robustness checks. Only farmers in the region of common support will be retained.

**Step 3: Balance.** Matching quality will be checked using standardised mean differences (target below 0.1), variance ratios, the pseudo-R² before and after matching, and density plots of propensity scores (Caliendo and Kopeinig, 2008).

**Step 4: Effect estimation.** The ATT will be estimated for milk yield per cow per day, milk sales and net income, in levels and in inverse hyperbolic sine (asinh) form to reduce the influence of skewed values and zeros (Bellemare and Wichman, 2020). Standard errors will be bootstrapped or computed from the regression on the matched sample with matching weights.

**Step 5: Robustness.** The ATT will be re-estimated with IPWRA as a doubly robust check. Sensitivity to unobserved confounding will be assessed with Rosenbaum bounds (Rosenbaum, 2002) and with the `sensemakr` robustness value (Cinelli and Hazlett, 2020), which states how strong an unobserved confounder would have to be to explain away the effect.

### 3.5.2 Objective two: the mediating role of cattle health

**Step 1: Effect on the mediator.** The ATT of participation on the cattle health index *M*~i~ (and on each component, for example vaccination, deworming and disease incidence, where available) will be estimated as in objective one.

**Step 2: Attenuation analysis.** On the matched sample, two models will be estimated:

*Y*~i~ = α~0~ + τ*D*~i~ + *X*~i~′β + ε~i~  (3.4)

*Y*~i~ = α~1~ + τ′*D*~i~ + θ*M*~i~ + *X*~i~′β′ + *u*~i~  (3.5)

The share of the income effect explained by cattle health is (τ − τ′)/τ. This reproduces and extends the attenuation analysis in the ADF2 DigiCow tables.

**Step 3: Causal mediation analysis.** Following Imai et al. (2010), the average causal mediation effect (ACME, the indirect effect through cattle health) and the average direct effect (ADE) will be estimated with a mediator model *M*~i~ = λ~0~ + λ~1~*D*~i~ + *X*~i~′λ~2~ + *e*~i~ and the outcome model above, with confidence intervals from quasi-Bayesian simulation or bootstrapping. The proportion mediated will be reported.

**Step 4: Sensitivity.** Because mediation requires that there are no unobserved confounders of the mediator and outcome (sequential ignorability), the sensitivity parameter ρ at which the ACME becomes zero will be reported (Imai et al., 2010). If the cattle health index is undocumented, it will be rebuilt from its components in the microdata, or treated as given and stated as a limitation.

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
| 1. Effect on productivity and income | Matched IE microdata | Milk yield per cow per day, milk sales, net income (levels and asinh) | PSM (radius, nearest-neighbour, kernel), IPWRA, Rosenbaum bounds, sensemakr | R: MatchIt, cobalt, WeightIt, sensemakr |
| 2. Mediation by cattle health | Matched IE microdata, attenuation tables | Cattle health index; net income | Attenuation analysis, causal mediation analysis, sensitivity analysis | R: mediation |
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
2. **Mediation assumptions.** Causal mediation requires sequential ignorability, which is strong. The sensitivity analysis will show how robust the findings are.
3. **Self-reported and recall data.** Milk yield, sales and income are self-reported and may contain recall error.
4. **Cross-sectional design.** The study cannot observe changes over time for the same farmers.
5. **Anonymisation.** Banded quasi-identifiers limit analysis by county and exact age.
6. **Generalisability.** Results apply to DigiCow users similar to those in the evaluation, and may not extend to other services or regions.

# EXPECTED OUTPUTS

| Objective | Expected output |
|---|---|
| 1 | Estimates of the effect of DigiCow on milk yield, milk sales and net income, with robustness and sensitivity results |
| 2 | Estimate of the share of the income effect mediated by cattle health, with sensitivity analysis |
| 3 | Evidence on which DigiCow services and levels of use are associated with practice adoption and production change, for women and men |

**Journal publications.** The Faculty of Agriculture requires graduate students to publish findings from their research in peer-reviewed journals before graduation. The study is planned to yield at least two articles, co-authored with the supervisor(s) with the student as lead author:

1. *Paper 1 (objectives 1 and 2):* "Does digital livestock advice raise dairy income through better animal health? Evidence from DigiCow in Kenya." Candidate journals: *Food Policy*, *World Development*, *Agricultural Economics*, *Journal of Agricultural Economics*, *Journal of Development Effectiveness* [check scope, fees and indexing before choosing].
2. *Paper 2 (objective 3):* "From information to action: digital service use and dairy practice adoption in Kenya." Candidate journals: *Information Technology for Development*, *The Journal of Agricultural Education and Extension*, *Smart Agricultural Technology*, *African Journal of Agricultural and Resource Economics* [check scope, fees and indexing].

**Thesis and degree.** An MSc thesis, submitted in the Faculty's paper format (one results chapter per objective) or monograph format as agreed with the supervisor(s), leading to the award of the degree of Master of Science in Agricultural Information and Communication Management.

**Policy brief.** A two-page brief for DigiCow, county livestock departments and funders.

# WORK PLAN

Indicative work plan, assuming the proposal is presented at a departmental seminar in February 2027 [adjust to the actual seminar date and the supervisor's advice].

| Activity | Dec 26 | Jan 27 | Feb 27 | Mar 27 | Apr 27 | May 27 | Jun 27 | Jul 27 | Aug 27 | Sep 27 | Oct 27 | Nov 27 | Dec 27 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Finalise proposal with supervisor | X | X | | | | | | | | | | | |
| Departmental seminar, corrections, Turnitin | | | X | X | | | | | | | | | |
| Submit proposal to Graduate School | | | | X | | | | | | | | | |
| Data-use agreement, ethics, NACOSTI | | X | X | X | X | | | | | | | | |
| Data cleaning and reproduction of published estimates | | | | | X | X | | | | | | | |
| Analysis: objective 1 | | | | | | X | X | | | | | | |
| Analysis: objective 2 | | | | | | | X | X | | | | | |
| Analysis: objective 3 | | | | | | | | X | X | | | | |
| Paper 1 drafting and submission | | | | | | | | X | X | X | | | |
| Paper 2 drafting and submission | | | | | | | | | | X | X | | |
| Thesis writing | | | | | | X | X | X | X | X | X | | |
| Notice of intention to submit (3 months before) | | | | | | | | | | X | | | |
| Thesis submission and defence | | | | | | | | | | | | X | X |

# BUDGET

Indicative budget in Kenya shillings (KES). All unit costs are estimates and will be confirmed against current prices and fee schedules before submission. Tuition and university examination fees are excluded because they are paid separately under the fee structure.

| Item | Unit | Quantity | Unit cost (KES) | Total (KES) |
|---|---|---|---|---|
| Internet data for literature search, data access and analysis | Month | 12 | 2,000 | 24,000 |
| Printing and spiral binding of proposal copies | Copy | 5 | 500 | 2,500 |
| Printing and spiral binding of thesis for examination | Copy | 4 | 1,500 | 6,000 |
| Hard binding of final thesis | Copy | 4 | 3,000 | 12,000 |
| Ethics review or exemption fee | Lump sum | 1 | 5,000 | 5,000 |
| NACOSTI research licence (if required) | Lump sum | 1 | 1,000 | 1,000 |
| Travel for supervisor meetings and seminars | Trip | 12 | 1,000 | 12,000 |
| Journal article processing charges (prioritise no-fee journals) | Paper | 1 | 20,000 | 20,000 |
| Stationery and miscellaneous | Lump sum | 1 | 3,000 | 3,000 |
| Contingency (10%) | | | | 8,550 |
| **Total** | | | | **94,050** |

*Budget narrative:* no field data collection is required because the study uses secondary data, so costs are limited to data access, ethics, communication, printing and publication. R, RStudio and Zotero are free and open-source, so no software costs arise.

# REFERENCES

Aker, J. C. (2011). Dial "A" for agriculture: A review of information and communication technologies for agricultural extension in developing countries. *Agricultural Economics, 42*(6), 631–647.

Anderson, J. R., & Feder, G. (2004). Agricultural extension: Good intentions and hard realities. *The World Bank Research Observer, 19*(1), 41–60.

Baron, R. M., & Kenny, D. A. (1986). The moderator–mediator variable distinction in social psychological research: Conceptual, strategic, and statistical considerations. *Journal of Personality and Social Psychology, 51*(6), 1173–1182.

Bellemare, M. F., & Wichman, C. J. (2020). Elasticities and the inverse hyperbolic sine transformation. *Oxford Bulletin of Economics and Statistics, 82*(1), 50–61.

Bhattacherjee, A. (2001). Understanding information systems continuance: An expectation-confirmation model. *MIS Quarterly, 25*(3), 351–370.

Bonilla, J., McCarthy, N., Mugatha, S., Rai, N., Coombes, A., & Brubaker, J. (2018). *Impact evaluation of the Smallholder Dairy Commercialization Programme in Kenya* (3ie Impact Evaluation Report 73). International Initiative for Impact Evaluation (3ie). https://doi.org/10.23846/tw4IE73

Caliendo, M., & Kopeinig, S. (2008). Some practical guidance for the implementation of propensity score matching. *Journal of Economic Surveys, 22*(1), 31–72.

Chepkirui, N., Owuor, G., & Kibet, L. (2022). The effects of revolving funds on milk yields in Kenya. *Asian Journal of Agricultural Extension, Economics & Sociology, 40*(5), 65–71. https://doi.org/10.9734/AJAEES/2022/v40i530887

Cinelli, C., & Hazlett, C. (2020). Making sense of sensitivity: Extending omitted variable bias. *Journal of the Royal Statistical Society: Series B, 82*(1), 39–67.

Cole, S. A., & Fernando, A. N. (2021). 'Mobile'izing agricultural advice: Technology adoption, diffusion and sustainability. *The Economic Journal, 131*(633), 192–219.

Davis, F. D. (1989). Perceived usefulness, perceived ease of use, and user acceptance of information technology. *MIS Quarterly, 13*(3), 319–340.

Fabregas, R., Kremer, M., & Schilbach, F. (2019). Realizing the potential of digital development: The case of agricultural advice. *Science, 366*(6471), eaay3038.

Ho, D. E., Imai, K., King, G., & Stuart, E. A. (2011). MatchIt: Nonparametric preprocessing for parametric causal inference. *Journal of Statistical Software, 42*(8), 1–28.

Imai, K., Keele, L., & Tingley, D. (2010). A general approach to causal mediation analysis. *Psychological Methods, 15*(4), 309–334.

Khandker, S. R., Koolwal, G. B., & Samad, H. A. (2010). *Handbook on impact evaluation: Quantitative methods and practices.* World Bank.

Long, J. S., & Freese, J. (2014). *Regression models for categorical dependent variables using Stata* (3rd ed.). Stata Press.

Maloo, S. H., Rowlands, G. J., Thorpe, W., Gettinby, G., & Perry, B. D. (2001). A longitudinal study of disease incidence and case-fatality risks on small-holder dairy farms in coastal Kenya. *Preventive Veterinary Medicine, 52*(1), 17–29. [verify year and issue]

Marwa, M. E., Mburu, J., Oburu, R. E. J., Mwai, O., & Kahumbu, S. (2020). Impact of ICT based extension services on dairy production and household welfare: The case of iCow service in Kenya. *Journal of Agricultural Science, 12*(3), 141. https://doi.org/10.5539/jas.v12n3p141 [add end page]

Mercy Corps AgriFin. (2026). *AgriFin Digital Farmer 2 programme overview.* https://mercycorpsagrifin.org/program-overview/

R Core Team. (2025). *R: A language and environment for statistical computing.* R Foundation for Statistical Computing. https://www.R-project.org/

Rademaker, C. J., Bebe, B. O., van der Lee, J., Kilelu, C., & Tonui, C. (2016). *Sustainable growth of the Kenyan dairy sector: A quick scan of robustness, reliability and resilience* (Report 979). Wageningen UR Livestock Research. [verify]

Republic of Kenya. (2019a). *Agricultural Sector Transformation and Growth Strategy 2019–2029.* Ministry of Agriculture, Livestock, Fisheries and Irrigation.

Republic of Kenya. (2019b). *Digital Economy Blueprint: Powering Kenya's transformation.* Ministry of Information, Communications and Technology.

Rogers, E. M. (2003). *Diffusion of innovations* (5th ed.). Free Press.

Rosenbaum, P. R. (2002). *Observational studies* (2nd ed.). Springer.

Rosenbaum, P. R., & Rubin, D. B. (1983). The central role of the propensity score in observational studies for causal effects. *Biometrika, 70*(1), 41–55.

Singh, I., Squire, L., & Strauss, J. (Eds.). (1986). *Agricultural household models: Extensions, applications, and policy.* Johns Hopkins University Press for the World Bank.

Spielman, D., Lecoutere, E., Makhija, S., & Van Campenhout, B. (2021). Information and communications technology (ICT) and agricultural extension in developing countries. *Annual Review of Resource Economics, 13*, 177–201.

Sweeney, L. (2002). k-anonymity: A model for protecting privacy. *International Journal of Uncertainty, Fuzziness and Knowledge-Based Systems, 10*(5), 557–570.

Tingley, D., Yamamoto, T., Hirose, K., Keele, L., & Imai, K. (2014). mediation: R package for causal mediation analysis. *Journal of Statistical Software, 59*(5), 1–38.

Tsan, M., Totapally, S., Hailu, M., & Addom, B. K. (2019). *The digitalisation of African agriculture report 2018–2019.* CTA and Dalberg Advisors.

Van Campenhout, B., Spielman, D. J., & Lecoutere, E. (2021). Information and communication technologies to provide agricultural advice to smallholder farmers: Experimental evidence from Uganda. *American Journal of Agricultural Economics, 103*(1), 317–337.

University of Nairobi Digital Repository. (n.d.). *Impact of information and communication technology-based extension services on dairy production and household welfare: The case of iCow service in Kenya* [Master's thesis, University of Nairobi]. http://erepository.uonbi.ac.ke/handle/11295/107821 [add author and year from the full record]

Venkatesh, V., Morris, M. G., Davis, G. B., & Davis, F. D. (2003). User acceptance of information technology: Toward a unified view. *MIS Quarterly, 27*(3), 425–478.

# APPENDICES

## Appendix 1: Data request checklist for Mercy Corps AgriFin

1. DigiCow matched impact evaluation microdata (treatment and comparison farmers), with matching covariates, matching weights or matched-sample flag, and all primary and secondary outcomes.
2. Cattle health index: list of components, how each was measured, and how they were combined (weights).
3. Variable-level codebook and the survey questionnaire used for DigiCow farmers.
4. `digicow_clean` farmer-level data and its codebook (services used, frequency of use, channel, practice change, production change).
5. The DigiCow impact evaluation tables and the methodology note or evaluation report section describing sampling, matching and the attenuation analysis.
6. Counties and dates of data collection, at the level of detail allowed by the anonymisation.
7. Confirmation of permitted uses: academic thesis, journal publication, sharing of code (not data), and authorship or acknowledgement expectations.

## Appendix 2: Provisional list of variables

| Variable | Type | Role | Objective |
|---|---|---|---|
| DigiCow participation | Binary | Treatment | 1, 2 |
| Milk yield per cow per day (litres) | Continuous | Outcome | 1 |
| Milk sales (KES or litres) | Continuous | Outcome | 1 |
| Household net income (KES; levels and asinh) | Continuous | Outcome | 1, 2 |
| Cattle health index | Continuous or index | Mediator | 2 |
| Health index components (vaccination, deworming, disease incidence) | Binary or count | Outcome | 2 |
| Services used (record-keeping, reminders, expert advice) | Binary set | Explanatory | 3 |
| Frequency or intensity of use | Ordinal or count | Explanatory | 3 |
| Delivery channel (app, SMS, USSD, call) | Categorical | Explanatory | 3 |
| Adoption of recommended practices | Binary or count | Outcome | 3 |
| Reported production change | Ordinal | Outcome | 3 |
| Sex of farmer | Binary | Control, moderator | 1, 2, 3 |
| Age band | Categorical | Control | 1, 2, 3 |
| Education | Categorical | Control | 1, 2, 3 |
| Herd size, farm size | Continuous or banded | Control | 1, 2, 3 |
| Location band | Categorical | Control | 1, 2, 3 |

*To be finalised after reviewing the data dictionary.*

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

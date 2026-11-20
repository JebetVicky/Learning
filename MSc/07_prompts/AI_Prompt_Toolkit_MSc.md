---
title: "AI Prompt Toolkit: MSc Research Edition"
---

**10 prompts for Vicky's DigiCow thesis and journal papers**

*Adapted from the job-search toolkit (after the 10 prompt templates by Allen Lattimer). Each card gives the template, then a version already filled in for your research. Made 20 November 2026.*

# How to use it

- **Paste the About my research block first**, then one prompt.
- **Replace everything in [square brackets].**
- **Attach the material**: your chapter, the paper you are reading, R output, supervisor comments. The more it sees, the better it answers.
- **One prompt at a time.** Answer its questions, then push back: "Be more specific", "Which of these would an examiner fail me on?", "Show me the evidence".
- **You stay the researcher.** AI is a sparring partner, not a source. Every fact, number and reference goes into the thesis only after you have checked it in the original paper or your own R output.

# Quick pick: I want to...

| I want to... | Use |
|---|---|
| Sharpen a vague research question or section | 1 Thinking Partner |
| Find what an examiner or reviewer will attack | 2 Brutal Critic |
| Plan backwards from a published paper | 3 Reverse Engineer |
| Hear how a journal reviewer or defence panel thinks | 4 Expert Simulator |
| Choose between two methods, formats or journals | 5 Decision Architect |
| Find a research gap others have missed | 6 Opportunity Finder |
| Learn PSM, mediation or R fast | 7 Learning Accelerator |
| Keep writing every week | 8 Systems Builder |
| Turn a paper into literature-review notes | 9 Knowledge Extractor |
| Step back and set next month's moves | 10 Strategic Advisor |

# Paste this first: About my research

Update it when things change (for example once you receive the data, or after the departmental seminar).

> **About my research:** I am Vicky Jebet, an MSc student in Agricultural Information and Communication Management, Department of Agricultural Economics, University of Nairobi. My supervisor is Dr Hilary Nyanganga.
>
> **Topic:** Digital livestock advisory services, cattle health and dairy farmer income in Kenya: evidence from DigiCow. I use secondary data from the independent evaluation of Mercy Corps AgriFin's Digital Farmer 2 (ADF2) programme: a matched treatment and comparison sample of DigiCow users, a cattle health index, attenuation tables and farmer-level usage data. The data are de-identified and k-anonymised (k = 5).
>
> **Objectives:** (1) estimate the effect of DigiCow on milk yield per cow per day, milk sales and net income (propensity score matching, IPWRA, sensitivity analysis); (2) test how much of the income effect is mediated by cattle health (attenuation and causal mediation analysis); (3) assess which DigiCow services and levels of use are associated with practice adoption and production change among users (logit and ordered logit).
>
> **Stage:** [proposal drafting / seminar done / data received / analysis / writing papers / thesis]. **Analysis tool:** R.
>
> **Rules:** UoN Faculty of Agriculture guidelines (2019): 2 to 4 objectives, one null hypothesis each, APA referencing, Turnitin similarity of 15% or less. The Faculty requires publication before graduation.
>
> **Rules for you:** never invent references, statistics, findings or page numbers. If you are not sure a paper exists, say so. Mark anything I must verify with [verify]. Use British spelling. No em dashes. Keep my voice plain and clear.

# 1. The Thinking Partner

*Use it when a question, section or idea feels fuzzy. It makes the AI ask before it answers.*

**Template**

> Don't immediately answer my question. First, identify what I'm actually trying to solve. Ask me the 3 most important questions that would help you give me a much better answer.
>
> My question: [your question]

**Your version**

> Don't immediately answer my question. First, identify what I'm actually trying to solve. Ask me the 3 most important questions that would help you give me a much better answer.
>
> My question: How do I write a problem statement for my DigiCow study that an examiner will accept as a real knowledge gap, not just "no one has studied DigiCow"?

*Tip: Use it before every new chapter section. The questions often show you what is missing.*

# 2. The Brutal Critic (Reviewer 2)

*Use it on any section, chapter, paper draft or slide deck before your supervisor, the seminar or a journal sees it.*

**Template**

> I'm going to share [document]. Your job isn't to agree with me. Find the 5 biggest weaknesses, challenge my assumptions, identify what I'm overlooking, and tell me what could make this fail.
>
> [paste document]

**Your version**

> Act as a demanding peer reviewer for *Food Policy*. I'm going to share my methodology chapter for a study that uses propensity score matching and causal mediation analysis on secondary evaluation data for DigiCow users in Kenya. Your job isn't to agree with me. Find the 5 biggest weaknesses, challenge my identification assumptions, identify what I'm overlooking (selection on unobservables, sequential ignorability, measurement of the cattle health index, self-reported income, power), and tell me what would make a reviewer recommend rejection.
>
> For each weakness, rate it major or minor, and suggest one fix that is realistic with secondary data. Don't add facts or references I haven't given you.
>
> [paste chapter]

*Tip: Run it again on the revised version. Keep a "reviewer log" table in `01_proposal/` with each critique and how you addressed it; this becomes your response-to-reviewers letter later.*

# 3. The Reverse Engineer

*Use it to turn a big goal into a step-by-step path.*

**Template**

> I want to achieve [specific result]. Work backward from the desired outcome. Identify the exact steps, skills, tools, decisions, and milestones required to get there. Explain the most efficient path.

**Your version**

> I want to have my DigiCow paper on cattle health and dairy income submitted to a peer-reviewed journal, and my MSc thesis submitted to Graduate School, by [December 2027]. Work backward from those two outcomes. Identify the exact steps, skills, tools, decisions and milestones required, including the UoN steps (departmental seminar, submission to Graduate School within one month, Turnitin, data-use agreement, ethics clearance or exemption, NACOSTI licence if needed, notice of intent three months before thesis submission). Explain the most efficient path as monthly milestones from December 2026, and flag the steps that depend on other people so I can start them early.

*Tip: Swap the goal later: "pass the departmental seminar first time" or "get the paper accepted within 6 months of submission".*

# 4. The Expert Simulator

*Use it to see your work through the eyes of a journal reviewer, an econometrician, a livestock scientist or your defence panel.*

**Template**

> Act as a top 1% expert in [field]. Evaluate my current approach, identify what beginners misunderstand, explain what experienced professionals do differently, and show me how to think at an advanced level.
>
> My current approach: [describe it]

**Your version**

> Act as a top 1% expert in impact evaluation of agricultural extension, someone who has reviewed for *World Development* and *Food Policy* and examined MSc theses in agricultural economics. Evaluate my current approach: I will re-estimate the DigiCow effect on milk yield, milk sales and net income with radius-caliper PSM, check balance with standardised mean differences, add IPWRA as a doubly robust check, test sensitivity with Rosenbaum bounds and sensemakr, and then estimate how much of the income effect runs through a cattle health index using attenuation and the Imai, Keele and Tingley mediation approach. Identify what beginners misunderstand about these methods, what experienced researchers do differently, and how to present the results so that a sceptical reviewer trusts them.

*Tip: For seminar or defence practice add: "Now be my examination panel. Ask me one question at a time, wait for my answer, then score it out of 10 and show me a stronger answer."*

# 5. The Decision Architect

*Use it when you have two real options: two methods, two thesis formats, two journals.*

**Template**

> I'm deciding between [option A] and [option B]. Build a decision framework that compares both options based on my priorities, risks, opportunity costs, and long-term consequences. Identify the option most likely to produce the best outcome.

**Your version**

> I'm deciding between [A: the paper format thesis, with one results chapter per objective written as a journal article] and [B: the monograph format thesis, writing papers after the thesis]. Build a decision framework that compares both based on my priorities: graduating in 2027, meeting the Faculty requirement to publish before graduation, a manageable workload while job hunting, and a strong publication record for a career in MEL. Include risks, opportunity costs and long-term consequences, and what to ask my supervisor. Identify the option most likely to produce the best outcome.

*Tip: Other decisions to run through it: which journal to submit to first; nearest-neighbour vs radius matching; whether to drop objective three if the usage data are weak.*

# 6. The Opportunity Finder (Gap Finder)

*Use it to find the research gap and the angle that makes reviewers say "this is new".*

**Template**

> Look at [field]. Identify 10 overlooked opportunities most people aren't paying attention to. Explain why each opportunity exists, who would care about it, and how I could realistically capitalise on it.

**Your version**

> Look at research on digital agricultural advisory services and smallholder livestock and dairy in sub-Saharan Africa. Identify 10 gaps or under-studied questions that most researchers aren't paying attention to, which my DigiCow data (matched sample, cattle health index, farmer-level usage data) could realistically address. For each, explain why the gap exists, who would care about the answer (journals, funders, platforms, county governments), and how I could address it within an MSc. Rank them by novelty and feasibility. Only name papers you are confident exist and mark the rest [verify].

*Tip: AI often invents papers when asked about gaps. Check every named study in Google Scholar before it goes in your literature matrix. A gap is only a gap after you have searched for it yourself.*

# 7. The Learning Accelerator

*Use it to close a skill gap quickly. Your likely gaps: propensity score matching in R, causal mediation analysis, sensitivity analysis, ordered logit, writing for journals.*

**Template**

> I want to master [skill] as efficiently as possible. Build a learning system using deliberate practice, active recall, spaced repetition, and real-world projects. Focus on the knowledge that creates the greatest practical advantage.

**Your version**

> I want to master propensity score matching and causal mediation analysis in R, to the level needed for my thesis and a journal paper: estimating propensity scores, matching with MatchIt, checking balance with cobalt, estimating the ATT with robust standard errors, running IPWRA, sensitivity analysis with sensemakr, and mediation with the mediation package. I have 45 minutes a day for 6 weeks, and I already use R for survey analysis. Build a learning system using deliberate practice, active recall, spaced repetition and one real project: practising on a public dataset (for example the lalonde data that ships with MatchIt) before my DigiCow data arrive. Give it week by week, with a short self-test at the end of each week.

*Tip: Swap the skill for "writing a results section for an economics journal" or "drawing a conceptual framework". Save your practice scripts in `04_analysis/practice/`.*

# 8. The Systems Builder

*Use it to keep momentum when motivation drops.*

**Template**

> Help me achieve [goal] consistently. Instead of giving me motivation or random tips, design a repeatable system with daily actions, triggers, checkpoints, feedback loops, and measurable progress.

**Your version**

> Help me write my MSc thesis consistently while I also job hunt. Instead of giving me motivation or random tips, design a repeatable system with daily actions, triggers, checkpoints, feedback loops and measurable progress. My target is [500] words or one analysis task a day, five days a week. It should include a weekly 30-minute review, a fortnightly update to my supervisor Dr Nyanganga, a reference routine in Zotero, and committing my R scripts and chapter drafts to my GitHub MSc folder at the end of each session.

*Tip: Ask it to turn the system into a one-page weekly checklist you can print or keep on your phone.*

# 9. The Knowledge Extractor (Literature Matrix)

*Use it on every paper you read. It produces notes in the exact format the UoN empirical review expects.*

**Template**

> I'm going to give you [article, report or chapter]. Don't just summarise it. Extract its most valuable insights, hidden assumptions, practical applications, counterintuitive lessons, and ideas I can use immediately.

**Your version**

> I'm going to give you a journal article. Don't just summarise it. Extract, using only what is in the article:
>
> 1. Full APA reference (from the article itself).
> 2. Who, where, objective, data, method and main findings (with the effect sizes and page numbers).
> 3. Theory or framework used.
> 4. Hidden assumptions and weaknesses a reviewer would raise.
> 5. How my DigiCow study differs from or builds on it, in one sentence I can adapt for my empirical review ("Kamau (2010) assessed ... using ... in ... The study found that ... Unlike this study, the present study ...").
> 6. Which of my three objectives it supports.
>
> Give it as one row I can paste into my literature matrix (columns: reference, country, objective, data, method, findings, gap or difference, my objective). If something is not in the article, write "not reported".
>
> [attach the PDF]

*Tip: Only attach papers you have legally downloaded. Never paste the ADF2 data or the evaluation's internal reports into a public AI tool unless the data-use agreement allows it.*

# 10. The Strategic Advisor

*Use it once a month to step back and choose your next moves.*

**Template**

> Act as my strategic advisor. Here's my current situation: [context]. Here's what I want to achieve: [goal]. Identify my biggest leverage points, the highest-impact actions, what I should stop doing, and the next 3 moves that would create the most progress toward my goal in the next 30 days. Be specific and honest.

**Your version**

> Act as my strategic advisor. Here's my current situation: I have a first draft of my MSc proposal on DigiCow, cattle health and dairy income, written to UoN Faculty of Agriculture guidelines. I have not yet received the ADF2 data, and I am also job hunting for MEL roles. Here's what I want to achieve: present at the departmental seminar by [February 2027], submit the proposal to Graduate School, get the data and ethics clearance, and publish at least one paper before graduating in 2027. Identify my biggest leverage points, the highest-impact actions, what I should stop doing, and the next 3 moves that would create the most progress in the next 30 days. Be specific and honest.

*Tip: Update the situation each month. Paste last month's 3 moves and say which ones you did.*

# Combos that work well

- **Building the literature review:** 9 Knowledge Extractor on each paper, then 6 Opportunity Finder on your matrix to sharpen the gap, then 2 Brutal Critic on the chapter.
- **Before supervisor meetings:** 2 Brutal Critic on the draft, then 1 Thinking Partner on the questions you want to ask.
- **Before the departmental seminar or defence:** 4 Expert Simulator as the panel, one question at a time.
- **Learning a method:** 3 Reverse Engineer for the path, 7 Learning Accelerator for the skill, then 8 Systems Builder to keep going.
- **Choosing a journal:** 6 Opportunity Finder to list options, then 5 Decision Architect, then check each journal's own website for scope, fees and indexing.
- **Every month:** 10 Strategic Advisor.

# Research safety rules

1. **AI invents references.** Never put a reference in the thesis that you have not opened and read. Check every citation in Google Scholar or the journal's site.
2. **AI invents numbers.** Statistics in your results come only from your own R output; context figures come only from the original source (KNBS, Kenya Dairy Board, journal articles).
3. **Protect the data.** Do not paste ADF2 farmer-level data or internal evaluation documents into public AI tools unless the data-use agreement allows it. Describe the variables instead, or use summary tables.
4. **Plagiarism and Turnitin.** UoN requires a similarity index of 15% or less. Use AI to critique and restructure your writing, not to write paragraphs you submit unchanged. Keep your own drafts in GitHub so you can show your work.
5. **Declare AI use** where UoN or the journal asks for it. Many journals now require a statement on AI-assisted writing.
6. **You make the scientific choices.** Methods, interpretation and claims are yours to defend at the seminar and the defence. If you cannot explain a choice without the AI, you are not ready to use it.

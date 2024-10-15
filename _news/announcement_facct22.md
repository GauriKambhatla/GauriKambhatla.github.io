---
layout: post
title: Presented at FAccT in Seoul, South Korea 🇰🇷
date: June 21, 2022
inline: false
---

I presented our paper, [Surfacing Racial Stereotypes through Identity Portrayal](https://facctconference.org/static/pdfs_2022/facct22-129.pdf), at the ACM Conference on Fairness, Accountability, and Transparency ([FAccT](https://facctconference.org/2022/index.html)). Here are some of my (rough) notes and takeaways from the conference; videos of the keynotes and paper presentations are available on YouTube if interested!

***

### Takeaways
- A lot of discussion of limitations & criticisms of work in AI, particularly in regards to excluding or not taking into account certain demographic groups, or multiple axes of demographic groups (intersectionality)
- A lot of discussion around open questions – due to the inherent nature of the key ideas discussed here, like “fairness” and “accountability” and how we take these into account with our models/systems
- Many potential solutions to these open questions as well – mostly revolving around these big ideas:
    - Involve people of different demographic groups, and take into account intersectionality during all steps of system development (creating data, creating the model, evaluation, etc.)
    - Make data better → data curation (rather than blindly scraping from the web without knowing what’s in it), data documentation, data transparency
    - We need to take appropriate measures (such as regulation) to account for the consequences of LLMs right now – there are important issues at hand before getting to something like AGI
    - We need to value more than just simple metrics like “performance” and “efficiency” when developing models, and should consider broader, societal implications
        - although I can see where having this be a requirement causes researchers to talk about societal implications very loosely – I don’t think every paper will necessarily have fundamental societal implications, though this seems very important for the ones that do; e.g., facial recognition systems
- As a side note, I really appreciated the diversity in identity – such as gender, ethnicity, nationality – at the conference, as well as the diversity in work -- the *interdisciplinary* nature -- of the conference. It was fun to talk and learn from people in such different fields with so many different ideas!


### Keynotes
**Meeyoung Cha: News Media Landscape**
- Engagement metrics used by companies (e.g., time spent on a post) leads to the propagation of fake news + misinformation
    - People will spend more time on news that is odd/extreme → this will cause it/similar things to show up more
- Misinformation propagates faster than true information
    - Starts with low-degree users, picked up by higher-degree users
    - There exists a golden time to stop misinformation & it must be flagged repeatedly (even if it is flagged once, it can still propagate as true in multiple other branches)
- Poorer countries are at a higher risk of hearing rumors/misinformation
- Popular is not the same as believable; popular misinformation spreads a lot, but might not be believable (e.g., something is just really funny, but no one actually believes it)
    - We should focus on preventing rumors that are believable, not popular
- Fact checks have been shown to no longer be useful once people actually believe the rumors
- Infodemic Risk Index: how likely someone is to be exposed to misinformation
- (Johnson et al, 2020): pro-vax vs. anti-vax facebook groups
    - Pro-vax groups tend to only talk amongst themselves, while anti-vaxxers try to reach out to other groups and get more people to join
    - By 2033 → more groups will be connected to anti-vax groups
- People’s emotions before + after covid: didn’t change much
    - Positive people tended to stay positive, negative people tended to stay negative
- People with traumatic experiences prefer to talk with virtual agents than real ones → more anonymity
- Showing people fact-checks after they hear a rumor is more memorable (because they have been corrected, they remember it better)
    - But this is more high-risk → rumor has been heard, potential actions/consequences could already be taken
- Who is responsible for handling misinformation?
    - Lay-people asked this question for creation + dissemination of misinformation
        - Put the most blame on users (but not themselves, i.e., “other” users)
    - Joint-accountability: users, news, social media, politicians
- Handling misinformation + preserving democracy → in e.g., more religious countries, works better if religious figure discuss misinformation

**Keynote Panel: Intersectionality + Algorithmic Fairness**
- Kimberly Crenshaw: intersectionality as a road intersection (where it came from)
- Not just about identity, but also about power dynamics
    - Language, nationality, sexual orientation, race, etc.
    - Need to pay attention to all axes to define the human experience
- "Fairness gerrymandering" → if we just take into account one (or a few) axes, we don’t account for everything
- Simplification of intersectionality: how much is okay?
    - There are many levels of simplification, does it help in getting to a better one?
    - How do we align metrics + functions with human complexity?
    - We shouldn’t become complacent: if a metric/task “works”, we need to continue to add to it, not just optimize it as is (common in ML)
- How to identify all the axes of intersectionality?
    - Define a place to start/certain groups to start with and go from there (E.g., black youth interacting with tech assistants/chatbots)
        - They don’t care about things like the weather → chatbots have limited info on Black historical figures, things relevant to Black community members
        - Limited ability to deal with language + dialect
        - When asked, black youth reimagined chat bot as more of a life coach → esp important to lower class individuals
        - “Class” emerges as an axis we care about for intersectionality
    - If we try to focus on all attributes → infinite regress
        - If we try to stop somewhere, then we have to choose which axes (this is either arbitrary or biased)
        - Instead of trying to figure out which axes, we should focus on how to make changes in the operationalization of intersectionality
        - E.g., reframe the purpose of algorithms (for example, mass incarceration of people of color)
- We’re not even close to the point of taking into account that an individual’s identity is not constant, but changes over time, changes with the context, the people you are with, etc.

**Pascale Fung: Value-based NLP**
- Assigning human values with NLP/AI → problem is human values are:
    - Culturally-dependent (e.g., chivalry vs. sexism)
    - Multi-perspective (e.g., trolley problem)
    - Context-dependent (e.g., epithets in AAVE vs SAE)
    - Multi-dimensional (e.g., sexism → body shaming, role/attribute stereotyping, pay gap, hyper-sexualization, internalized sexism, hostile work environment, …)
    - [Parikh et al., 2019]
- Align LLMs with human values?
    - LLMs are uncontrollable, not transparent, unstable (as of right now)
    - Could try: filtering harmful content, debiasing models/embeddings, controlled generation, post-processing the output → these don’t work very well
    - Proposal: encapsulate LLMs + embeddings
        - Design smaller models for downstream tasks, and get the training data by prompting LLMs
- Ethical questions
    - Match the ethical quandary to ethical principles (retrieve from datasets, or eastern/western philosophy)
    - Match principles to automatic (generated) answers
- Framing bias (Lee et al., NAACL 2022 → NEUS)
    - Neutral summarization
    - Can we get NLP systems (e.g. QA) to take into account multiple perspectives

**Mariano-Florentino Cuéllar: The Rise of Hypersocial AI**
- Example: Lemoine ←→ Lamda conversation
- Machines are taking on pivotal roles in human life
    - Law, policy, diplomacy fields are not ready for this
- Humans seek social interactions
    - But we desire them on our own terms
    - We make decisions based on these/emotional things rather than rational choices (might not lead to the best decisions)
    - This leads to both good and bad things
- Tech affects human behavior
- Hypersocial AI: AIs that increasingly satisfy the human desire for social communication (rather than basic chatbots)
    - High interest + demand for characteristics of hypersocial AI
    - Increasingly provide physical + mental health services, legal services, etc. → to reduce cost + human effort
        - As a result of isolation + loneliness + alienation (which has been increasing a lot since 1950)
        - Even caring for plants has been shown to help mitigate the effects of isolation
- Young + socially-challenged: first to try to develop/seek social relationships (doctor, lawyer, educator, etc.) with hypersocial AI
    - Whether AI is actually able to “feel”/”think” is irrelevant to the increase in demand
- Hypersocial AI can be beneficial in these situations (medical, legal, education, preventing social isolation, etc.), but also problems:
    - Policy-makers will be making decisions based on these
    - Geo-economic competition for them
    - Can exacerbate cultural conflict
    - Can cause issues with authoritarian regimes
    - People can + will rely on AI systems for decisions
- Hypersocial AI will affect what we value
    - Analogous to the industrial revolution, food revolution → to provide for people at a larger scale, but there are pros/cons
- None of these dilemmas are relevant to AGI (irrelevant to that debate)
    - Humans have bonds with pets, creatures, plants, etc. that don’t have AGI
- We need legal systems + diplomacy to deal with hypersocial AI
- The Lemoine/Lamda interview is more important for what it says about Lemoine + humans than what it says about the model
- Governments will move intensely to have AI for e.g., medical purposes (because more cost-effective) until there is public push-back
    - This will likely affect disadvantaged people more
    - But this is not necessarily bad, make AI more nuanced
- Does hypersocial AI normalize contested notions of “social” and “the human” (e.g. for neuro-divergent individuals)?
    - Might actually do the opposite → could be able to be more flexible to different users
    - Problem is who is in control of such systems

### CRAFT session: Hyperscale LMs + fairness, accountability, transparency
- LMs are sophisticated, but very clueless
- LMs are biased (e.g., GPT-3 + “Muslim walked into a mosque…”, Lee Luda chatbot + toxic generation)
- Bias in LLMs comes from annotators, data, models (Hovy + Prabhumoye, 2021 → 5 sources of bias in NLP)
- Technologists vs. ethicists: 
    - Need both when developing technology, but two different methods of thinking, hard to reconcile
    - Technologists: want a single metric, ethicists: don’t understand LMs
    - Organizations (esp small start-ups) don’t have the ability to have both of these
- Hard to define hate speech + toxic language
    - Context-dependent
    - Mitigation strategies should be done together (don’t want to help one user group, but harm another – e.g., trying to reduce toxic speech, but biased against AAVE)

**Kyunghyun Cho: on explaining how LMs work**
- Claude Shannon (1950) → entropy + language
- Cross entropy is upper bound to entropy → allows for high probability to rarely seen examples → allows for generalization
- Neural networks compress similar inputs
- Compressor is imperfect → allows for generalization
- Questions to consider: what information do LMs lose? What information do they choose to prefer? What do models prefer to generate?
- Generation → pruning
    - Target space is combinatorial

**Margaret Mitchell: on data transparency**
- Data transparency → why does it matter?
    - Know if dataset is good for a task
    - Incentives for good data creation
- Web 2.0 + start of massive content generation produced by people
    - We lose curation, just collect tons of data + don’t know what’s in it
- Data transparency: documentation (e.g. data cards) + analysis
    - 5 pillars: people, methods, quantitative analysis, qualitative analysis, basic characteristics
- Data vs. dataset: dataset has all necessary metadata
- C4 dataset → dominated by wikipedia, which is known to have gender bias, racial bias, age bias, etc.
- DALLE secret language → due to tokenization + BPE + noise
    - When LMs compress data, create related pairs
- Measuring data → how natural the language of a dataset is
    - Does it follow a zipfian distribution, like every natural language

### Proceedings Sessions
**Accountability + Government**
- Effective Altruism → long-term AI risk: AGI
- We are traveling on a path to AGI, however we are already locked into problems with systems of oppression
- Narratives of white supremacy in AGI community
- AGI vs. FAccT communities: existential risk vs. systemic risk
    - Hierarchy of whose lives are more important

**Value Systems for AI**
- Data curation ←→ Museum curation
    - Need a culture of humility in data curation
- Survey paper of values in 100 ML papers – Abeba Birhane et al. (best paper award)
    - “Performance” seen as synonymous with “progress” or “success”
    - “Generalization” : doesn’t talk about generalization to any setting related to societal needs
    - “Efficiency”: about scaling up, rather than using less resources
    - Big tech corporate affiliation papers
        - Increased form 13% → 47% in 10 years
    - Reporting error analysis + uncertainty doesn’t seem to be important
- We should document why we are evaluating models
- “Input myopia”: when input is disregarded → we just compare model prediction to a gold label (causes abstraction from the context)
    - Cannot explore bias as much + regions of the input space where the model fails
- When doing evaluation, we should document assumptions

**Trust + Explainability**
- Road to explainability is paved with bias
    - Global explanations (for all data instances) vs. local explanations (fit a linear model for a few instances)
    - Explanation models should have: high fidelity, simplicity, robustness, fairness
        - Fairness: fidelity should be the same for all subgroups (e.g., men and women)
    - Goal: decrease fidelity gaps
- Trust in AI systems
    - Trust is a human judgment + not all people make the same trust judgments
    - Not all AI systems are the same level of trustworthiness
    - Explainable AI → can lead to over trust
    - How should AI trustworthiness be communicated appropriately?
    - Trustworthiness cues
        - Content cues, contextual cues (e.g. metadata)
        - Heuristic processing → how most of us process information
            - Explainability heuristic: judge by e.g. number of stars/rating
    - Areas of AI for cues
        - Affordances → generated content, transparency, interaction
        - Cues: truthfulness, relevance, well-calibrated, systematic
- Explainability may not contribute to trust, but contributes to AI-user dyad
    - Alon Jacovi et al. FAccT 2021: “formalizing trust in artificial intelligence”
    - Explanation must be both the justification and the cause to have trust

**Governance of Language Processing**
- Interactive model cards (vs. traditional ones)
    - Users can explore the data for themselves
    - Found: helps people think more critically about models
- Data privacy
    - Privacy: LMs spit out data from training data verbatim at times
    - Sharing is not equal to public (might want to share info with someone, but don’t want it to be public knowledge)
    - Privacy violations range in severity
    - Current methods:
        - Text sanitation (doesn’t work well)
        - Differential privacy:
            - Probability(record in dataset) == probability(record not in dataset)
            - Doesn’t work well if the record is not well-defined → if we don’t know the unit, does removing one unit help?
            - The guarantees of privacy offered don’t align with human notions of privacy guarantees
    - Privacy preserving → fine-tune locally
- Data governance
    - Data custodians (make data available) + data helpers (legal scholars, ethicists, etc.) + data stewardship organization + data modelers (developers who request data)

**Bias in Language/Vision**
- Measuring Representational Harms in Image Captioning (Angelina Wang)
    - Captions that incorrectly include words: likely stereotypes
        - “Unimagable words” + “too specific words”: stereotypes
        - This is an upper bound
    - Heuristic to reduce the space of potential stereotypes: a stereotype if highly correlated with a demographic group
- Bias in ASR -- need:
    - Utterance pairs that reflect real contexts
    - Dynamic threshold adjustments
- Robots Enact Malignant Stereotypes
    - E.g., products that aren’t “average” → difficult for models to handle automatically (e.g., a Black doll vs. a White doll)
        - Leads to higher end price for consumers

**Understanding + Achieving Structural Societal Change**
- Models for understanding and quantifying feedback in societal systems
    - Measuring inequity → dynamic PID (proportional integral derivative) model
- Locality of Technical Objects and the Role of Structural Interventions for Systemic Change
    - How have e.g. lending systems changed over time for different races [quantifies this]
- The Long Arc of Fairness: Formalisations and Ethical Discourse
    - Current methods in fairness lack temporal contexts

**Hate speech + Mistranslation**
- Assessing Annotator Identity Bias via Item Response Theory
    - Item response theory: to measure hate speech annotator sensitivity
        - Kennedy et al., 2020
        - Framework to measure hate speech
            - “Ability” of comment, “difficulty” of item, “severity” of annotator, “difficulty” of response
    - Annotator lean: Annotators who are part of the target group of hate speech are more likely to mark comment as hate speech/disrespectful
- Exploring the Role of Grammar and Word Choice in Bias Toward African American English (AAE) in Hate speech Classification
    - LIWC lexicon: swear words mostly SAE, doesn’t take AAE into account
    - Created an AAE-like grammar dictionary
    - Blodgett et al. dataset for dialect + hate speech
- User strategies for identifying and recovering from mistranslations in machine translation-mediated chat
    - People tend to evaluate mis-translation for fluency, but fluency is not equal to adequacy

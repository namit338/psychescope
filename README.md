I got interested in the Big Five (OCEAN) personality model after reading about how it's used in psychology research and was curious — can you actually predict someone's personality traits just from the way they write? That question turned into this project. What it does You type or paste any piece of text — could be a journal entry, a paragraph about yourself, anything — and PsycheScope analyzes it to give you a breakdown across the five personality traits:

Openness — curiosity, creativity, range of interests Conscientiousness — organization, dependability, discipline Extraversion — social energy, assertiveness, positivity Agreeableness — empathy, cooperation, trust Neuroticism — emotional sensitivity, anxiety, mood patterns

You get a score for each trait, a visual breakdown, and a short summary of what your writing suggests about you. How it works There's no ML model making API calls here — the analysis runs entirely in the browser using a custom NLP pipeline I built in JavaScript. It looks at things like:

Word frequency and vocabulary richness Sentiment ratio (positive vs negative language) Sentence length and structural complexity Use of first-person vs collective language Hedging language, certainty words, and emotional vocabulary

Each of these features gets mapped to trait scores using weighted rules based on linguistic psychology research I read through while building this. Tech used

Vanilla JS + HTML/CSS Custom NLP pipeline (no external ML libraries) Rule-based scoring system mapped to OCEAN traits Deployed on GitHub Pages

Why no ML model? Honestly, I wanted to understand what the model would be learning before just plugging in a black box. Building the rule-based system first forced me to actually think through which linguistic features map to which traits and why. It's not as accurate as a trained classifier would be, but it's fully explainable — I know exactly why it gives a certain score. A trained model is probably the next step.

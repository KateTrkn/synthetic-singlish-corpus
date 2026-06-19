# synthetic-singlish-corpus
This repository contains a synthetic text corpus generated as part of a linguistics research project on modeling Singaporean English (Singlish) linguistic features using large language models.

## Overview
This corpus was created for the thesis:
> "Modeling Linguistic Features of Singapore English in Synthetic Text Corpora", 2026.

## Corpus Description
The corpus consists of 50 synthetic texts (podcast-style dialogues) generated using the Qwen large language model (Alibaba Group). The texts simulate authentic Singlish speech, including characteristic linguistic features such as:

- **Discourse particles:** *lah*, *leh*, *lor*, *hor*, *mah*, *sia*, etc.
- **Local words:** *makan*, *shiok*, *sian*, *kiasu*, *kiasi*, *alamak*, *wah lao*, etc.
- **Grammatical features:** omission of copula *to be*, omission of 3rd person singular *-s*, omission of past tense *-ed*, reduplication, topicalization, etc.
- **Cultural references:** HDB, BTO, hawker centres, kopitiam, etc.

### Corpus Statistics
| Metric | Value |
|--------|-------|
| Number of texts | 50 |
| Total tokens | ~350,000 |
| Average text length | ~4,300 words |
| Topics covered | 30+ (studying, work, dating, housing, food, AI, scams, etc.) |

## Source Material
The synthetic corpus was generated based on the **YouTube Corpus of Singapore English Podcasts (YCSEP)** – a collection of podcast transcripts featuring natural Singlish speech (~8.38 million words, 620 hours of audio).
The YCSEP corpus is available at:  
[https://lindat.mff.cuni.cz/repository/items/490eb7ea-750b-4dd3-ae81-f8c23a1a9d56](https://lindat.mff.cuni.cz/repository/items/490eb7ea-750b-4dd3-ae81-f8c23a1a9d56)

## Methodology

### Generation Process
1. The YCSEP corpus was cleaned and preprocessed (removing metadata, merging utterances by speaker)
2. A specialized **English-language prompt** was designed with explicit instructions for:
   - Role definition (linguist specializing in Singlish)
   - Linguistic analysis criteria (lexical, grammatical, phonetic, stylistic features)
   - Output format (JSON with topic and text fields)
   - Quality constraints (no copying, natural speech, dialog structure)
3. The Qwen model generated 50 texts across diverse topics (education, work, relationships, technology, culture, etc.)

### POS Tagging
The corpus was annotated with **part-of-speech tags** using `spaCy` (en_core_web_sm) with custom `AttributeRuler` rules to correctly tag Singlish discourse particles.

## Usage
This corpus is intended for:
- Linguistic research on Singapore English
- NLP model training for low-resource language varieties
- Development of Singlish-aware language technologies
- Comparative studies of synthetic vs. natural language data

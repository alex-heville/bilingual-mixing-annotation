# Bilingual Mixing Annotation Project

## Overview
This repository hosts a collaborative annotation project focused on analyzing parental language mixing in bilingual child-directed speech. We use a curated dataset of 10 transcripts from a hypothetical "Bilingual Providence Corpus" within the CHILDES database.

## Goals
- Identify and tag instances of parental language mixing in CHILDES transcripts.
- Establish clear annotation guidelines for consistent coding across annotators.
- Demonstrate a GitHub-based workflow for collaborative annotation and peer review.

## Dataset
The dataset consists of 10 plain-text transcript files in a simplified CHAT format. Each file is named `transcript01.cha` through `transcript10.cha` and is stored in the `/data` folder. Each line of utterance starts with a speaker ID:
- `*MOT:` for mother
- `*FAT:` for father
- `*CHI:` for child

## Annotation Scheme
Parental utterances that contain language mixing (i.e., words from two different languages) are tagged with `[mix]` at the end of the line. Detailed annotation rules are provided in [ANNOTATION_GUIDELINES.md](ANNOTATION_GUIDELINES.md).

## Repository Structure
- `data/` – contains the 10 transcript files
- `ANNOTATION_GUIDELINES.md` – formal definition of language mixing and examples
- `README.md` – this file

## Workflow
1. Annotators work on feature branches (`annotations/round1`, etc.).
2. Pull requests are opened for peer review.
3. Review comments are addressed before merging into `main`.
4. Issues are used to discuss guideline clarifications and edge cases.

## Contributors
- Alex Heville (project lead)
- Colleague (peer reviewer)

## License
This project is for educational/demonstration purposes only. The hypothetical corpus is not real; no actual CHILDES data is distributed here.
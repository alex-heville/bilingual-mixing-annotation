# Annotation Guidelines for Parental Language Mixing

## Purpose
This document defines the criteria for tagging parental language mixing in the hypothetical Bilingual Providence Corpus. Consistent application of these rules ensures reliable annotation across multiple coders.

## Definition of Language Mixing
An utterance produced by a parent (`*MOT:` or `*FAT:`) is considered to exhibit **language mixing** if it contains one or more lexical items (content words) from a language other than the primary language being used in that turn.

### Primary Language Determination
- The primary language of an utterance is determined by the majority of content words in that turn.
- If the utterance is predominantly English, any non-English content word triggers the `[mix]` tag.
- If the utterance is predominantly Spanish (or another language), any English content word triggers the `[mix]` tag.

### What Counts as a Lexical Item?
- **Included**: Nouns, verbs, adjectives, adverbs, quantifiers, determiners (if they differ across languages), and interjections that are language-specific.
- **Excluded**: Proper nouns (e.g., “Dora”, “McDonald’s”), numbers, formulaic expressions that are commonly borrowed (e.g., “OK”, “ciao”), and onomatopoeic sounds.
- **Ambiguous Cases**: Words that are cognates or homophones across languages (e.g., “radio” in English and Spanish) are **not** counted as mixing unless they are used with a distinctly different morphological or syntactic pattern.

## Annotation Format
When a parental utterance meets the above criteria, add the tag `[mix]` at the end of the line, after the utterance text but before any existing CHAT codes.

Example:
```
*MOT: Mira the doggy! [mix]
*FAT: Do you want más leche? [mix]
*MOT: Let’s go to the park.          # No mixing, no tag
```

## Edge Cases and Clarifications

### Single‑Word Utterances
If a parent produces a single word that belongs to a different language than the preceding context, it is **not** tagged as mixing unless it is part of a longer utterance that contains words from both languages. Single‑word utterances are considered to have no “primary language” and thus do not meet the definition.

### Code‑Switching vs. Borrowing
- **Code‑switching**: The alternation between two languages within a single utterance (e.g., “Give me el libro”). Tag as `[mix]`.
- **Borrowing**: A word that has been fully integrated into the dominant language (e.g., “taco” in English). If the word is commonly used in the dominant language and is not perceived as a switch by the speaker, it may be excluded. When in doubt, tag it.

### Proper Nouns
Proper nouns (names of people, places, brands, etc.) are **excluded** from the mixing count. For example:
```
*MOT: We saw Dora the Explorer yesterday.   # No tag, “Dora” is a proper noun.
```

### Multi‑Word Phrases
If a whole phrase is borrowed (e.g., “hasta la vista”), treat it as a single lexical item. If the phrase contains words from the primary language as well, tag the utterance as mixing.

## Review Process
All annotations are subject to peer review via GitHub pull requests. Reviewers should verify that the tagging conforms to these guidelines and raise any questions as issues or inline comments.

## Revision History
- **v1.0** (2025‑12‑27): Initial guidelines created.
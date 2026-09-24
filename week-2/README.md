Week 2 — How Computers "Read"
Chatbot Development (AITCD001) — Learning Outcome

 Overview
Last week's chatbot matched exact keywords. This week's activity explores the first real step toward a smarter chatbot: how a computer breaks a sentence into pieces it can actually work with. Using **spaCy**'s small English model (`en_core_web_sm`), the notebook covers three core NLP building blocks — **tokenization**, **part-of-speech (POS) tagging**, and **named entity recognition (NER)** — all running on CPU in Google Colab's free tier, no GPU or local install required.

 What's in this notebook

 1. Setup
Installed and loaded spaCy's small English model (`en_core_web_sm`, ~13MB) — lightweight enough to run comfortably even on a 4GB-RAM laptop.

 2. Tokenization
Broke a sample sentence ("I'd like a large pepperoni pizza please") into individual tokens, showing how a computer sees a sentence as a list of words and punctuation rather than a single string.

 3. Part-of-Speech (POS) Tagging
Labeled each token with its grammatical role (pronoun, verb, noun, adjective, etc.) — a key piece of information a chatbot needs to understand what a sentence is actually asking for.

 4. Named Entity Recognition (NER)
Extracted key entities (people, places, dates, organizations) from sentences containing local Rwandan names and places (e.g. Alice Uwimana, Huye, Musanze). This surfaced a real limitation: most NLP models are trained mostly on Western/English-language data, so recognition of local names and places isn't always accurate — an important bias to notice, not a mistake in the code.

 5. Starting an Intent Dataset
Began building a small labeled dataset of example sentences tagged with **intents** (e.g. `opening_hours`, `book_appointment`, `pricing`) for a clinic-assistant style chatbot. This dataset is the foundation for training an intent classifier in a later week (Week 9).

 Key takeaways
- Tokenization, POS tagging, and NER are the building blocks that let a chatbot go beyond simple keyword matching.
- Off-the-shelf NLP models can have blind spots with non-Western names/places — something to keep in mind when designing a chatbot for a local audience.
- I've started collecting labeled intent data, which will be reused and expanded in future weeks.

 Files
- `Sharon_UWINEZA_Week2_Activity.ipynb` — the full notebook with code, outputs, and discussion notes.

 Tools used
- Python
- spaCy (`en_core_web_sm`)
- Google Colab

Author:Sharon UWINEZA

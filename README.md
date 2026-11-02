# Rasa Chatbot Scolarité — prototype reconstitué

A new **starter project** for a French-language university administrative assistant, based on a previously discussed Rasa school chatbot. The original source files were not supplied, so this is a **reconstruction**, not a claim that the original complete chatbot has been recovered.

## Scope
FAQ intents: greetings, registration, opening hours, documents required, and contact. Responses are **generic examples**; do not treat them as actual policies or opening hours of Université Ibn Tofail.

## Run (compatible Rasa environment required)
```bash
python -m venv .venv
# Activate the virtual environment for your operating system
pip install "rasa>=3.6,<4"
rasa data validate
rasa train
rasa shell
```
Rasa's Python support varies by release; use a Python version supported by the Rasa release you install. This repository does not pin or guarantee a working installation in the current environment.

## Files
- `config.yml`: NLU pipeline and dialogue policies
- `domain.yml`: intents and response templates
- `data/nlu.yml`: small example utterances
- `data/rules.yml`: deterministic FAQ rules
- `tests/test_stories.yml`: example conversation checks

## Privacy and next steps
Do not upload student records, credentials or conversations. Validate all FAQ content with the institution; expand real user utterances with consent; add a human handoff and multilingual support.

**Status:** source scaffold committed; not deployed and not end-to-end tested.

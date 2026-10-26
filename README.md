# <Your product name>
ConsentLens

## Problem
Data science teams in India struggle to understand how the DPDP Act 2023 and DPDP Rules 2025 apply to their data and ML projects. They need to navigate lengthy legal documents and older IT laws to identify requirements for consent, data retention, and purpose limitation. Teams also risk exposing personal information when they paste customer data into AI tools for help. ConsentLens helps teams assess privacy compliance while masking personal data before it reaches an LLM.

## Who it is for
<Data scientists and ML engineers at health-tech startups handling patient data.
Privacy and compliance officers responsible for ensuring data projects follow India's data protection requirements.>

## Signature feature
A privacy-safe paste box that detects personal information in dataset schemas or sample rows, automatically masks sensitive values, and explains potential privacy concerns before the data is sent to an LLM.

## Hardest problem (my interview story)
The hardest problem is preventing personal data leakage while still making the AI useful. Users may paste names, phone numbers, or Aadhaar-like numbers, and uploaded policy documents may contain prompt-injection attempts. ConsentLens must detect and mask personal information before LLM processing, treat uploaded documents as untrusted input, and test whether any raw personal data leaks through using a red-team dataset.

## Dataset
| Source | Link | Documents | Pages | Licence / terms |
|---|---|---|---|---|
| <name> | <url> | <n> | <n> | <licence> |

## 10 real questions
See [docs/QUESTIONS.md](docs/QUESTIONS.md).

## Run it
```bash
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements-dev.txt
cp .env.example .env                                 # Windows: copy .env.example .env
uvicorn app.main:app --reload
curl localhost:8000/health
```

## Live link
<Added in Week 2>

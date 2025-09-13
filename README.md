# Groq Conversation Manager & Chat-Data Extractor

A **zero-framework** Google-Colab notebook that shows how to:

1. **Manage long chat histories** with Groq’s LLM-powered summarisation and custom truncation rules.  
2. **Extract structured user details** (name, email, phone, location, age) from free-form chat text using Groq’s OpenAI-compatible function-calling endpoint.

> Both tasks are implemented **only with standard Python + the official `openai` client** (pointed at Groq).

---

## 🚀 30-second try-out
1. Open the notebook in Colab:  
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AyaanShaheer/groq-conversation-manager/blob/main/Groq_Conversation_Manager.ipynb)

2. Add your Groq API key to Colab’s **Secrets** tab under the name `GROQ_API_KEY`.  
3. Run all cells → watch live summarisation and JSON extraction.

---

## 📌 Task 1 – Conversation Manager Features
| Feature | Live demo in notebook |
|---|---|
| Turn-limit truncation | keep last *n* messages |
| Character-limit truncation | keep last *x* characters |
| Periodic summarisation | auto-summarise every *k*-th assistant reply |
| Zero external deps | only `openai` client (Groq-compatible) |

---

## 📌 Task 2 – Structured Information Extraction
| Detail | JSON key | Type |
|---|---|---|
| Full name | `name` | string |
| Email address | `email` | string |
| Phone number | `phone` | string |
| Location | `location` | string |
| Age | `age` | integer |

Uses **Groq function-calling** with a strict JSON-schema; outputs are validated with the lightweight `jsonschema` package.

---

## 📁 Repository layout
```
groq-conversation-manager/
├── Groq_Conversation_Manager.ipynb   # all code + outputs
├── README.md                         # this file
└── .gitignore                        # nothing sensitive
```

---

## 🔑 Requirements
- Python ≥ 3.8  
- `openai` (`pip install openai`)  
- `jsonschema` (`pip install jsonschema`)  
- Groq API key (free tier works)

---

## 🛠️ Local run (optional)
```bash
git clone https://github.com/AyaanShaheer/groq-conversation-manager.git
cd groq-conversation-manager
jupyter notebook Groq_Conversation_Manager.ipynb
```

---

## 📜 Licence
MIT – feel free to reuse any part of the code.

---

**Submitted as assignment:** *Conversation Management & Classification using Groq API*

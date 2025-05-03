---
license: apache-2.0
task_categories:
  - text2text-generation
  - text-generation
language:
  - en
  - hi
tags:
  - Hinglish
  - Finetuning
pretty_name: Hinglish conversation with context dataset
---

# Hinglish Conversations Dataset

## Overview

This dataset contains synthetically generated conversational dialogues in Hinglish (a blend of Hindi and English). The conversations revolve around typical college life, cultural festivities, daily routines, and general discussions, designed to be relatable and engaging.

---

## Dataset Details

- **Language:** Hinglish (Hindi + English)
- **Domain:** College life, daily interactions, cultural events, and general discussions
- **Size:** 3576 conversation
- **Turns per Conversation:** 3–5 conversational exchanges per context
- **Generation Method:** Synthetically generated using Google's Gemini-2.5-Pro
- **Intended Usage:** Fine-tuning NLP models for tasks such as:
  - Personality alignment in conversational AI
  - Hinglish conversational response generation
  - Context-aware dialogue modeling
  - Language modeling and sentiment analysis in mixed-language scenarios

---

## Example Conversation Snippet

```json
[
  {
    "role": "user",
    "content": "Navratri night ke liye rangoli ka kya scene hai? Aur lighting ka bhi kuch plan hai tere dimag mein?"
  },
  {
    "role": "assistant",
    "content": "Haan bhai, rangoli traditional-modern mix hogi, lighting mein steady LED strips hain. Festive feel pakka hai!"
  },
  {
    "role": "user",
    "content": "Perfect! Aur selfie light bhi rakh lena, sabko photo leni hai."
  },
  {
    "role": "assistant",
    "content": "Bilkul, selfie ka jugaad ready hai. Tension-free raho, sab mast hoga!"
  }
]
```

---

## Applications

- **Conversational AI Training:** Improves chatbot engagement in colloquial and bilingual contexts.
- **Cultural Context Learning:** Useful for training models to understand festive and culturally nuanced conversations.
- **Personality Alignment:** Helps align conversational models with casual, friendly, and youthful conversational styles.
- **Code-switching Research:** Valuable for linguistic studies and modeling code-switching behavior.

---

## Usage Instructions

To utilize this dataset for fine-tuning tasks:

- Load the `.json` file directly into your NLP framework or data processing pipeline.
- Ensure preprocessing to handle mixed languages properly.
- Consider tokenization methods that handle Hinglish effectively.

Examples using Python:

```python
# [Direct]
import json

# Load dataset
with open('.Data/hinglish_3_5k_conversations_dataset.json', 'r', encoding='utf-8') as file:
    conversations = [json.loads(line) for line in file]

# Process conversations
for convo in conversations:
    for message in convo:
        print(message['role'], ':', message['content'])
```

```python
# [HuggingFace]
from datasets import load_dataset

# Load the dataset directly from the Hugging Face Hub
dataset = load_dataset("prakharb01/Synthetic-Hinglish-Finetuning-Dataset")
```

## Bias, Risks, and Recommendations

This dataset, generated with Google's Gemini-2.5-Pro model, may include unintended biases, linguistic patterns, or stereotypes present in synthetic conversational data. Users should validate and potentially augment it with real-world conversations to ensure suitability for sensitive or practical applications.

## License

This dataset is provided for research purposes. Ensure appropriate attribution and compliance with relevant ethical guidelines when using the dataset.

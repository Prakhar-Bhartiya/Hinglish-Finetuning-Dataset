# Hinglish Conversations Dataset

[Huggingface Dataset](https://huggingface.co/datasets/prakharb01/Synthetic-Hinglish-Finetuning-Dataset)

## Overview

This dataset contains synthetically generated conversational dialogues in Hinglish (a blend of Hindi and English). The conversations revolve around typical college life, cultural festivities, daily routines, and general discussions, designed to be relatable and engaging.

---

## Dataset Details

- **Language:** Hinglish (Hindi + English)
- **Domain:** College life, daily interactions, cultural events, and general discussions
- **Size:** 3577 conversation
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
{
    "conversation": [
      {
        "role": "user",
        "content": "Oye, Navratri night ke liye rangoli ka kya scene hai? Mummyji toh keh rahi thi ki badi honi chahiye is baar. Aur lighting ka bhi kuch plan hai tere dimag mein, photographer sahab?"
      },
      {
        "role": "assistant",
        "content": "Haan bhai, rangoli ka design toh final hai. Thoda traditional aur thoda modern touch diya hai. Lighting mein LED strips use karenge, colorful wali. Energy bhi bachegi aur photo bhi mast aayegi, tension na le."
      },
      {
        "role": "user",
        "content": "LED theek hai, lekin woh blink-blink wali nahi chahiye. Aankhein dukhti hain phir. Aur rangoli mein colors bright rakhna, festive feel aani chahiye. Mummyji ne bola hai ki design mein diya bhi banana hai."
      },
      {
        "role": "assistant",
        "content": "Haan, blink wali toh bilkul nahi. Steady lights hi lagayenge. Rangoli mein vibrant colors hi use kar raha hoon, aur diya wala design bhi add kar diya hai. Don't worry, mummyji ko pasand aayega pakka."
      },
      {
        "role": "user",
        "content": "Perfect! Phir toh done deal hai. Bas time pe start kar dena kaam, last minute rush nahi chahiye. Aur haan, ek selfie light bhi rakhna, sabko photos bhi toh khichwani hongi. Navratri ki shuruwat hai, dhoom machani hai!"
      },
      {
        "role": "assistant",
        "content": "Bilkul bhai, time pe shuru kar denge. Selfie light ka bhi jugad kar liya hai. Tension na le, is baar Navratri aisa hoga ki sab yaad rakhenge. Rangoli bhi superhit, lighting bhi dhamakedar. Ready ho jao!"
      }
    ]
}
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
with open('.data/train.json', 'r', encoding='utf-8') as file:
    conversations = json.loads(file)

# Process conversations
dataset = [item for item in conversations]
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

# DistilBERT-LoRA-IMDb-Sentiment 🎬🍿

## Project Description

This repository hosts a highly efficient **binary sentiment classifier** fine-tuned on the **IMDb Movie Review dataset** (Positive/Negative).

The model is built on **DistilBERT** for speed and smaller size, utilizing **LoRA (Low-Rank Adaptation)** for **Parameter-Efficient Fine-Tuning (PEFT)**. This approach ensures rapid training and produces a small, portable adapter checkpoint, making it ideal for deployment with minimal computational overhead.

---

## ✨ Features

* **Efficient Fine-Tuning:** Leverages **LoRA** (with rank $r=4$) to only train $\sim 0.1\%$ of the base model's parameters.
* **Lightweight Base:** Built on **DistilBERT**, a fast and efficient Transformer optimized for text classification.
* **Binary Classification:** Specialized for classifying English movie review text into **Positive** or **Negative** sentiment.
* **Hugging Face Ready:** Built using the `transformers`, `peft`, and `datasets` libraries.

---

# DistilBERT-LoRA-IMDb-Sentiment 🎬🍿

## Project Description

This repository hosts a highly efficient **binary sentiment classifier** fine-tuned on the **IMDb Movie Review dataset** (Positive/Negative).

The model is built on **DistilBERT** for speed and smaller size, utilizing **LoRA (Low-Rank Adaptation)** for **Parameter-Efficient Fine-Tuning (PEFT)**. This approach ensures rapid training and produces a small, portable adapter checkpoint, making it ideal for deployment with minimal computational overhead.

---

## What It Solves

* Automatically classifies review text as **Positive** or **Negative**.
* Adapts a general model to your domain with **low training cost**.
* Enables **real-time, scalable sentiment insights** for apps and analytics.

---

## Features

* **Efficient Fine-Tuning**: LoRA adapters (e.g., rank `r=4`) train only a small fraction of parameters.
* **Lightweight Base**: `DistilBERT` provides fast inference on CPU/GPU.
* **Simple Pipeline**: Built with `Transformers`, `PEFT`, `Datasets`, and `Evaluate`.
* **Portable**: Save/reload adapters, or merge them into a standalone model.
* **Notebook-Ready**: Designed to run smoothly in Google Colab.

---

## Dataset & Model

* **Dataset**: IMDb (small/truncated subset) — English movie reviews.
* **Labels**: Binary sentiment (Negative = 0, Positive = 1).
* **Base Model**: `distilbert-base-uncased`.
* **Fine-Tuning**: LoRA applied to attention query projections.

---

## Training & Results

* **Typical settings**: batch size 16, 3–10 epochs, LR ≈ 1e-3, max length 256–512.
* **Validation accuracy**: ~0.85–0.89 on the small IMDb subset (varies with seed/epochs).
* **Trains quickly** on a T4/L4 GPU; workable on CPU for small runs.

---

## Applications

* Product and app reviews
* Social listening and brand monitoring
* Customer support triage
* Survey free-text analytics
* Content moderation signals

---

## How To Use (High-Level)

* Open the notebook and run cells to load data, fine-tune with LoRA, evaluate, and predict.
* Save adapters and/or a merged model for deployment.
* Batch score datasets or serve predictions through a simple API/UI.

---

## Requirements

* Python 3.9+
* `PyTorch`
* `Transformers`
* `PEFT`
* `Accelerate`
* `Datasets`
* `Evaluate`

---

## Repository Structure (Suggested)

* `notebooks/` — Colab/Jupyter notebook for fine-tuning and evaluation
* `README.md` — Project overview (this file)
* `LICENSE` — License file
* (optional) `saved_model/` — LoRA adapters or merged model (large files should be git-ignored)

---

## License

* MIT

---

## Acknowledgments

* **Hugging Face**: `Transformers`, `Datasets`, `PEFT`, `Accelerate`
* **DistilBERT** (Sanh et al., 2019)
* **LoRA** (Hu et al., 2021)
* **IMDb dataset** (for research/benchmarking)

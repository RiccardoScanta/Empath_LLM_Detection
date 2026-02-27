# Semantic Delta: A Single Interpretable Signal Differentiating Human and LLM Dialogue

This repository contains the implementation of a statistical framework designed to distinguish between **human-written** and **Large Language Model (LLM)** generated dialogue.

The research introduces a **lightweight and interpretable metric**, called **Semantic Delta**, derived from semantic category distributions.

---

## 🔬 Project Overview

The core contribution of this project is **Semantic Delta**, a novel statistical feature for AI-generated text detection based on **thematic concentration**.

Human communication typically exhibits a **balanced and multifaceted distribution of topics**, whereas LLM-generated dialogue tends to maintain a **more rigid and concentrated thematic focus**.

---

## 📐 The Metric

### Semantic Delta Definition

The **Semantic Delta** is defined as:

> The numerical difference between the intensity scores of the two most dominant thematic categories within a text.

### Framework

* Text is analyzed using the **Empath lexical analysis tool**
* Empath maps text into thematic intensity scores using word-embedding–based semantic categories

### Hypothesis

LLM-generated outputs exhibit **stronger thematic concentration** (higher Semantic Delta values) compared to human discourse.

---

## 📊 Experimental Results

Systematic analysis across large-scale samples shows that **AI-generated texts consistently produce significantly higher Semantic Delta values** than human-written texts.

### Key Statistics

| Group | Mean (μ) | Standard Deviation (σ) |
| ----- | -------- | ---------------------- |
| Human | 0.0017   | 0.0022                 |
| AI    | 0.0039   | 0.0041                 |

**Validation:**
A Welch’s *t*-test produced a **p-value < 0.05**, confirming statistically significant divergence between human and AI dialogue distributions.

---

## 🛠️ Technical Stack

* **Language:** Python
* **Analysis:** Empath Library
* **Models Evaluated:**

  * gpt-4.1-mini
  * gpt-5-mini
  * gpt-4-mini
* **Data Science Tools:**

  * Pandas
  * NumPy
  * Matplotlib
  * Seaborn

---

## 📂 Datasets

The study compares heterogeneous conversational corpora to capture a wide spectrum of linguistic styles.

### Human Corpus

* Modern colloquial dialogue (*Friends* scripts)
* Formal historical language (William Shakespeare)
* Contemporary digital interaction (Reddit threads)

### AI Corpus

Dialogues generated via the OpenAI API using varied system and user prompts.

---

## 📜 Citation

If you use this work, please cite:

```bibtex
@article{bertolotti2026semantic,
  title={Semantic Delta: A Single Interpretable Signal Differentiating Human and LLM Dialogue},
  author={Bertolotti, Francesco and Scantamburlo, Riccardo},
  journal={LIUC - Università Cattaneo},
  year={2026}
}
```

---

## 🏫 Affiliation

Developed at the **School of Industrial Engineering**,
**LIUC – Università Cattaneo**, Italy.

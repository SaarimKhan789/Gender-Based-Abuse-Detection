# 🛡️ Gendered Abuse Detection in Indic Languages

A multilingual deep learning system for detecting **gendered abuse** in **Hindi, Tamil, and English** social media content. Built for the [ICON 2023 Shared Task on Gendered Abuse Detection](https://sites.google.com/view/icon2023-tattle-sharedtask/home), this solution incorporates multilingual BERT, domain-adaptive pretraining, and multi-task learning to handle code-mixing and under-resourced Indic languages.

---

## 📌 Overview

We address three classification subtasks:

- **Task 1**: Detect gendered abuse (Label 1)
- **Task 2**: Incorporate external datasets for better transfer learning
- **Task 3**: Jointly predict gendered abuse (Label 1) and explicit language (Label 3)

---

## 🧠 Methodology

| Approach | Description |
|---------|-------------|
| Baseline | mBERT with standard fine-tuning |
| Transfer Learning | Fine-tuned with external abusive datasets |
| Multi-task Learning | Custom architecture predicting both Label 1 & Label 3 |
| Preprocessing | Hinglish normalization, transliteration (Hindi) |

**External Data**:
- [Davidson Hate Speech](https://github.com/t-davidson/hate-speech-and-offensive-language)
- MACD dataset (NeurIPS 2022)

---

## 🧪 Results

| Language | Task 1 | Task 2 | Label 1 (Task 3) | Label 3 (Task 3) |
|----------|--------|--------|------------------|------------------|
| English  | 0.736  | 0.738  | 0.713            | 0.728            |
| Hindi    | 0.712  | 0.703  | 0.678            | 0.773            |
| Tamil    | 0.825  | 0.815  | 0.809            | 0.876            |

---

## 📚 Datasets

- **Uli Gendered Abuse Dataset**  
  ~22k samples across Indic languages with expert annotations for gendered abuse and explicit content.

- **MACD**  
  Hindi/Tamil abuse detection samples from web crawling.

- **Davidson Hate Speech Dataset**  
  English tweets labeled for hate/offensive/neutral language.

---

## ⚙️ Features

- 🔤 Hinglish-to-Hindi transliteration via `indic-transliteration`
- 📊 Training + Validation loss plots
- 🧪 Single-sentence inference
- 📁 Auto-generated prediction CSVs
- 📉 Confusion matrix visualizations

---

## 🧑‍💻 Authors

| Name              | Roll Number |
|-------------------|-------------|
| Prashant Shrotriya| MT24065     |
| Saarim Khan       | MT24077     |
| Vatsaly Rai       | MT24144     |

---

## 📎 References

- Uli Dataset: [arXiv:2311.09086](https://arxiv.org/abs/2311.09086)
- ICON 2023 Task: [Official Website](https://sites.google.com/view/icon2023-tattle-sharedtask/home)
- MACD Dataset: [NeurIPS Paper](https://proceedings.neurips.cc/paper_files/paper/2022/hash/a7c4163b33286261b24c72fd3d1707c9-Abstract-Datasets_and_Benchmarks.html)

---

> _"Building safe and inclusive digital spaces, one model at a time."_ 🌐

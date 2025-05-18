# Hybrid_Deep_Learning_Smishing
Enhancing Cybersecurity: Hybrid Deep Learning Approaches to Smishing Attack Detection in Arabic Language
#  Arabic Smishing Detection using Hybrid Deep Learning
# Mohammed Rasol Al Saidat May 2025

This repository contains the codebase, dataset preprocessing pipeline, and trained models used in the research paper:

**“Enhancing Cybersecurity: Hybrid Deep Learning Approaches to Smishing Attack Detection in Arabic Language” – BDRC 2025**

---

## 🔍 Overview

Arabic smishing (SMS phishing) attacks leverage linguistic ambiguity to bypass traditional spam filters. This project implements a **CNN-BiGRU hybrid deep learning model**, optimized for Arabic's morphological complexity, using domain-specific preprocessing and Word2Vec embeddings.

Key features:
- Tailored preprocessing for Arabic (diacritics removal, Farasa tokenization)
- Hybrid CNN-BiGRU architecture with attention
- LIME-based interpretability
- Evaluation using ROC, confusion matrix, and cross-validation

---

## 📦 Requirements

Install via pip:

```bash
pip install -r requirements.txt

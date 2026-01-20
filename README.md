# absa-pyabsa-fast-lsa-indobert
Implementation of PyABSA FAST-LSA with IndoBERT for Aspect-Based Sentiment Analysis, evaluated using baseline and fine-tuning scenarios with k-fold cross-validation.

This repository contains the implementation of **Aspect-Based Sentiment Analysis (ABSA)** using **PyABSA FAST-LSA** with **IndoBERT** as the language model.

The study evaluates multiple **baseline** and **fine-tuning** training scenarios using **k-fold cross-validation** to analyze model performance on Indonesian-language sentiment data.

---

## 📌 Research Background
Aspect-Based Sentiment Analysis (ABSA) aims to identify sentiment polarity toward specific aspects within a text.  
This research applies the FAST-LSA model provided by **PyABSA** combined with **IndoBERT** to handle Indonesian-language text.

The **case study** used in this research is **public sentiment toward the Kabinet Merah Putih**, collected from Twitter data.  
However, the proposed approach is **generic** and can be applied to other ABSA tasks.

---

## 🧠 Models
- **FAST_LSA_S + IndoBERT**
- **FAST_LSA_T + IndoBERT**

Both models are implemented using the **PyABSA** framework.

---

## ⚙️ Training Scenarios
The experiments consist of **18 training scenarios**, including:

### Baseline
- Epochs: `{5, 7, 9, 11}`
- Batch Size: `16`
- Learning Rate: `2e-5`
- K-Fold: `{5, 10}`
- Max Sequence Length: `128`

### Fine-tuning
- Epoch: `10`
- Batch Size: `32`
- Learning Rate: `1e-5`
- K-Fold: `5`
- Max Sequence Length: `256`
- Gradient Accumulation: `2` (FAST_LSA_S only)

---

## 📊 Evaluation Metrics
Model performance is evaluated using:
- Accuracy
- Precision
- Recall
- F1-score

Evaluation is conducted across all folds in k-fold cross-validation.

---

## 📂 Repository Structure
```text
absa-pyabsa-fast-lsa-indobert/
│
├── data/              # Dataset (processed / anonymized)
├── notebooks/         # Training and evaluation scripts
├── README.md

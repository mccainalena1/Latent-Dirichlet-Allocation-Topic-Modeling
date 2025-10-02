# LDA Topic Modeling on Biblical Texts
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python 3.9+](https://img.shields.io/badge/Python-3.9%2B-blue)](requirements.txt)
[![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange)](./src)
[![NLP: LDA | Gensim](https://img.shields.io/badge/NLP-LDA%20%7C%20Gensim-purple)](#modeling-approach)
[![pandas](https://img.shields.io/badge/pandas-✓-informational)](requirements.txt)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Built with Python](https://img.shields.io/badge/Python-3.9%2B-blue)](requirements.txt)
[![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange)](./src)
[![Reproducible](https://img.shields.io/badge/Reproducible-Yes-brightgreen)](#reproducibility)

A graduate project applying **Latent Dirichlet Allocation (LDA)** to multiple Bible translations to discover latent topics and compare translation characteristics.

> 📌 **Highlights**: Gensim LDA, translation comparisons (KJV, BBE, ASV, etc.), pyLDAvis interactive topic exploration, clean data pipeline in notebooks.

---

## Table of Contents
- [📖 Project Overview](#-project-overview)
- [📂 Repository Structure](#-repository-structure)
- [⚡ Quickstart](#-quickstart)
- [📊 Data](#-data)
- [🧠 Modeling Approach](#-modeling-approach)
- [🎯 Results](#-results)
- [🌐 Interactive Visualizations](#-interactive-visualizations)
- [🔁 Reproducibility](#-reproducibility)
- [🚀 Next Steps](#-next-steps)
- [📜 License](#-license)
- [👤 Contact](#-contact)

---

## 📖 Project Overview
This project explores topic structures in Biblical texts using LDA. Multiple translations are preprocessed (tokenization, stopword filtering, normalization) and modeled to analyze how topics differ by translation and to visualize topic prevalence and top terms.

**Goals**
- Build a repeatable preprocessing + LDA workflow in Jupyter.
- Compare topic structures across translations.
- Provide interactive artifacts (pyLDAvis) for qualitative inspection.

---

## 📂 Repository Structure
```
.
├── data/           # small sample data and keys (CSV/TXT)
├── docs/           # supporting documents
├── figures/        # images used in README / reports
├── results/        # HTML visualizations + final report
├── src/            # notebooks (preprocess, model, evaluate)
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

---

## ⚡ Quickstart
1. **Clone the repository**
```bash
git clone https://github.com/your-username/lda-topic-modeling.git
cd lda-topic-modeling
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Launch Jupyter**
```bash
jupyter notebook
```

4. **Open notebooks**
   - `src/Topic Modeling Gensim-BBE.ipynb`
   - `src/Topic Modeling Gensim-KJV.ipynb`
   - `src/Version Classification.ipynb`

---

## 📊 Data
Small sample CSV/TXT files are included under `data/` to demonstrate preprocessing and modeling. Full datasets may be large; keep only **non-sensitive** samples in the repo.

Key files include:
- `data/bible_version_key.csv`
- `data/key_english.csv`
- `data/stop_words_lst.txt` and `data/bible_stop_words_lst.txt`

> ⚠️ If you add larger data, consider storing it outside the repo or using Git LFS.

---

## 🧠 Modeling Approach
- Preprocess text (normalize, tokenize, remove stopwords).
- Build dictionary and corpus with **Gensim**.
- Train LDA; evaluate coherence and inspect topics.
- Visualize results with **pyLDAvis**.

Notebooks encapsulate each step so you can re-run or adapt to other corpora.

---

## 🎯 Results
Key artifacts are in `results/` and `figures/`.
- Final paper: [`results/UsingLatentDirichletAllocationtoSummerizetheBible_McCain.pdf`](results/UsingLatentDirichletAllocationtoSummerizetheBible_McCain.pdf)
- Example figures (thumbnails available in `figures/`), such as `figures/Books.jpg`.

If viewing on GitHub, you can click images inline or open the PDF report for detail.

---

## 🌐 Interactive Visualizations
Open interactive topic visualizations (pyLDAvis) in your browser:
- [`results/LDAvis_BBE_B_0.html`](results/LDAvis_BBE_B_0.html)
- [`results/LDAvis_KJV_B_0.html`](results/LDAvis_KJV_B_0.html)

> GitHub does not render HTML inline by default. Download and open locally, or host via GitHub Pages.

---

## 🔁 Reproducibility
- Determinism can be improved by setting seeds in Gensim and NumPy.
- The `requirements.txt` pins core libraries needed to run the notebooks.
- Each notebook cell is ordered to support top-to-bottom execution.

---

## 🚀 Next Steps
- Tune topic count and priors per translation.
- Add coherence metrics comparison tables.
- Extend to other corpora or modern translations.
- Publish selected HTML artifacts via GitHub Pages.

---

## 📜 License
This project is licensed under the **MIT License**. See [LICENSE](LICENSE) for details.

---

## 👤 Contact
**Alena McCain**

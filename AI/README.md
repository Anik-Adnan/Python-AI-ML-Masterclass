# 30-Day AI/ML Masterclass

A structured, day-wise curriculum in artificial intelligence and machine learning, implemented as a sequence of self-contained Jupyter notebooks. The course progresses from Python fundamentals through classical supervised and unsupervised learning to deep learning applications in computer vision, audio, and natural language processing.

## Curriculum Design

The course is organised into five phases of increasing conceptual and technical depth. Each day builds on the formalism and tooling established in prior days; later phases assume working familiarity with the material covered earlier.

| Phase | Days | Topics |
|---|---|---|
| I. Python and Data Foundations | 01–11 | Language fundamentals, object-oriented programming, NumPy, pandas, data cleaning, visualisation, exploratory data analysis (Titanic) |
| II. Classical Supervised Learning | 12–19 | Bias–variance trade-off, logistic regression, k-nearest neighbours, naive Bayes, decision trees, random forests, support vector machines, classification evaluation |
| III. Regression | 20–23 | Simple and multiple linear regression, regularisation, applied car-price prediction, regression evaluation |
| IV. Unsupervised and Decision-Theoretic Methods | 24–26 | K-means and hierarchical clustering, association rule mining (Apriori), multi-armed bandits (UCB1) |
| V. Deep Learning Applications | 27–30 | Object detection (OpenCV, YOLO), convolutional neural networks, speech recognition, LLM-based text classification |

Each notebook is organised consistently:

1. **Objectives** — the specific competencies addressed.
2. **Theoretical exposition** — formal derivations, mathematical notation, and the rationale for each method (why it exists, when it applies, how it relates to neighbouring topics).
3. **Implementation** — annotated code progressing from a minimal working example to a complete, evaluated pipeline.
4. **Common mistakes** — documented failure modes and misconceptions specific to the topic.
5. **Summary and exercises** — five practice problems and two challenge problems per notebook, with full project workflows on designated capstone days (11, 22, 27–30).

## Repository Structure

```
30Day_AIML_Masterclass/
├── Day01_Introduction_AI.ipynb
├── Day02_Python_Foundations.ipynb
├── ...
├── Day30_Fake_News_LLM.ipynb
└── README.md
```

## Usage

All notebooks are authored for execution in Google Colab and require no local environment configuration.

1. Open a notebook directly via Colab's **File → Upload notebook**, or upload the repository to Google Drive and open notebooks from there.
2. Execute via **Runtime → Run all**.
3. Where a notebook depends on a library not preinstalled in the default Colab runtime (e.g. `mlxtend`, `ultralytics`, `librosa`, `transformers`), the relevant cell installs it automatically on first execution.
4. Days 27–30 benefit from, but do not require, a GPU runtime (**Runtime → Change runtime type → GPU**).

## Data and Reproducibility

Datasets are drawn from one of three sources, in order of preference:

- **scikit-learn built-in datasets** (e.g. breast cancer, wine, Iris) — require no network access.
- **Synthetically generated data** with fixed random seeds — fully reproducible, designed to exhibit known ground-truth relationships so that learned models can be validated against the true generating process.
- **Public datasets or pretrained models** (e.g. Titanic, Fashion-MNIST, YOLOv8 weights, Hugging Face transformer checkpoints) — used where the dataset or model is itself the pedagogical subject. Each such notebook includes a synthetic fallback so that execution does not fail in the absence of network access.

## Prerequisites

No prior machine learning background is assumed. Basic familiarity with programming concepts is helpful but not required, as Days 01–06 cover Python from first principles. Mathematical prerequisites (linear algebra, probability, calculus) are introduced inline, at the point of use, rather than assumed in advance.

## Core Dependencies

`numpy`, `pandas`, `matplotlib`, `seaborn`, `scikit-learn`, `scipy` — all preinstalled in Colab. Additional packages (`statsmodels`, `mlxtend`, `opencv-python-headless`, `ultralytics`, `tensorflow`, `librosa`, `transformers`) are installed automatically by the notebooks that require them.

## License

Specify a license appropriate to your intended distribution (e.g. MIT, CC BY-NC 4.0) prior to publishing.

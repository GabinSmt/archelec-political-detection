# Detecting Political Affiliation in French Electoral Manifestos (1973–1993)

## Overview
This project applies NLP techniques to predict the political affiliation of candidates in French legislative elections from their electoral manifestos (corpus Archelec, Sciences Po). We compare three classification approaches and conduct two parallel experiments — with and without explicit party names — to measure whether political affiliation is rhetorically encoded beyond simple party name mentions.

## Repository Structure

```
archelec-political-detection/
├── data/
│   ├── raw/text_files/     # OCR transcriptions (not versioned)
│   └── external/           # Metadata CSV from Sciences Po Archelec
├── notebooks/
│   └── archelec_political_detection.ipynb
├── report/
│   └── figures/            # Figures used in the report
├── requirements.txt
└── README.md
```

## Data
- **Text files** : OCR transcriptions from [Teklia GitLab](https://gitlab.teklia.com/ckermorvant/arkindex_archelec)
- **Metadata** : Downloaded from [Sciences Po Archelec](https://archelec.sciencespo.fr/explorer)

## Results

| Model | Experiment | Accuracy | F1-macro |
|---|---|---|---|
| Naive Bayes | With party names | 0.902 | 0.843 |
| Naive Bayes | Without party names | 0.893 | 0.829 |
| SVM | With party names | 0.975 | 0.961 |
| SVM | Without party names | 0.968 | 0.949 |
| CamemBERT Zero-Shot | Without party names | 0.208 | 0.216 |

## Installation
```bash
git clone https://github.com/GabinSmt/archelec-political-detection.git
cd archelec-political-detection
pip install -r requirements.txt
```

## Author
Gabin Simonnet — ENSAE Paris (2025–2026)  
NLP Course — Christopher Kermorvant

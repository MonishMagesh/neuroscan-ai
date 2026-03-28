# 🧠 NeuroScan AI — Brain Tumor Classification

> AI-powered brain MRI classification web app built on IEEE SCEECS 2026 
> published research. Live demo at: https://monishmagesh.github.io/neuroscan-ai

---

## 🔬 Research Paper

**"Deep Learning Based Brain Tumor Classification Using Orange Data Analytics"**  
📄 IEEE International Students' Conference on Electrical, Electronics, and Computer Science (SCEECS 2026)  
🔗 DOI: `10.1109/SCEECS68810.2026.11429884`  
📅 Published: March 2026

---

## 🎯 What This Does

Upload any brain MRI scan and get instant AI classification into one of four categories:

| Category | Risk | Description |
|----------|------|-------------|
| 🔴 Glioma | High | Aggressive tumor from glial cells. Includes GBM grade IV |
| 🟡 Meningioma | Medium | Benign, slow-growing tumor from the meninges |
| 🟣 Pituitary | Medium | Tumor on pituitary gland affecting hormones and vision |
| 🟢 No Tumor | Low | Healthy brain — no detectable mass |

---

## 📊 Model Performance

| Validation | Model | Accuracy | AUC |
|------------|-------|----------|-----|
| 3-Fold CV | Neural Network | 93.4% | 0.991 |
| 5-Fold CV | Neural Network | 98.3% | 0.997 |
| **10-Fold CV** | **Neural Network** | **99.0%** | **0.999** |

- **+7%** improvement over previous state-of-the-art
- **−70%** compute time reduction via PCA
- **+8%** MCC gain from data augmentation

---

## 🧪 Methodology
```
Raw MRI Images (16,000+)
       ↓
Preprocessing (224×224, normalization, augmentation)
       ↓
InceptionV3 Feature Extraction (2048-dim vectors)
       ↓
Handcrafted Features (texture, contrast, variance)
       ↓
PCA Dimensionality Reduction (→ 100–150 components, 95% variance)
       ↓
6 ML Classifiers (Neural Net, SVM, Random Forest, etc.)
       ↓
k-Fold Cross-Validation (k = 3, 5, 10)
       ↓
Classification Result + Confidence Scores
```

### Dataset Sources
| Source | Images | Details |
|--------|--------|---------|
| Kaggle | 7,023 | 4 clinical classes, benchmark dataset |
| BRISC 2025 | 6,000 | T1 & T2-weighted MRI sequences |
| FigShare | 3,064 | Expert-annotated tumor locations |
| **Total** | **16,087** | Multi-source, radiologist-verified |

### Augmentation Techniques
- Random rotation ±15°
- Horizontal flip
- Brightness/contrast adjustment ±20%
- Gaussian noise (σ = 0.1)

### Models Benchmarked
- Neural Network (Adam optimizer, 2 hidden layers)
- Support Vector Machine (SVM)
- Random Forest (n=100, max_depth=10)
- Logistic Regression
- Naive Bayes (Gaussian)
- Decision Tree (max_depth=10, gini)

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Feature Extraction | InceptionV3 (pre-trained CNN) |
| ML Pipeline | Orange Data Mining |
| Dimensionality Reduction | Principal Component Analysis (PCA) |
| AI Vision Engine | Claude Vision API (Anthropic) |
| Frontend | Vanilla HTML/CSS/JS (single file) |
| Deployment | GitHub Pages |

---

## ✨ App Features

- 🧠 Live neural network canvas background animation
- 📤 Drag & drop MRI upload with scan-beam animation
- 📊 Animated confidence bars for all 4 tumor classes
- ⚡ Real-time Claude Vision API analysis
- 📄 Downloadable PDF diagnostic report
- 📱 Fully responsive — works on mobile
- 🔬 Full research page with interactive results tables
- 📈 Model accuracy bar chart (switchable 3/5/10-fold)

---

## 👥 Authors

| Name | Institution | Role |
|------|-------------|------|
| Praveen R | NIT Puducherry | Lead Author |
| T R Saravanan | SRM IST, Kattankulathur | Co-Author |
| Monish M | SRM IST, Kattankulathur | Co-Author |
| R Archith Shri Hari | SRM IST, Kattankulathur | Co-Author |
| Sibinath K | SRM IST, Kattankulathur | Co-Author |
| Sumanth R | SRM IST, Kattankulathur | Co-Author |

---

## ⚠️ Disclaimer

This is a **research prototype** built to demonstrate the findings of our 
published IEEE paper. It is **NOT** a certified medical device and must 
**NOT** be used as the sole basis for any clinical decision.

Always consult a qualified radiologist or neurologist for medical diagnosis.

---

## 📜 Citation
```bibtex
@inproceedings{praveen2026neuroscan,
  title={Deep Learning Based Brain Tumor Classification Using Orange Data Analytics},
  author={Praveen, R and Monish, M and Saravanan, TR and 
          Archith, R and Sibinath, K and Sumanth, R},
  booktitle={2026 IEEE International Students' Conference on 
             Electrical, Electronics and Computer Science (SCEECS)},
  year={2026},
  doi={10.1109/SCEECS68810.2026.11429884}
}
```

---

*Department of Computational Intelligence · SRM Institute of Science and Technology, Kattankulathur*

# Beyond Prediction: Residual Analysis Reveals Multi-Layered Institutional Structure in Titanic Survival

[![arXiv](https://img.shields.io/badge/arXiv-submit/6966879-b31b1b.svg)](https://arxiv.org/abs/submit/6966879)
[![Python](https://img.shields.io/badge/python-3.9+-blue.svg)](https://python.org)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

> **Research Question**: When machine learning models achieve high accuracy from demographic features, does this reflect individual capabilities or institutional mechanisms?

## 📄 Paper Summary

This repository contains the complete analysis for our paper that introduces **residual analysis** as a diagnostic tool for distinguishing between individual-level and institutional explanations of demographic predictability in machine learning models.

**Key Finding**: Using the Titanic dataset, we show that even after achieving 85% prediction accuracy, residuals (prediction errors) are systematically structured by demographics—revealing multi-layered institutional effects that standard predictive modeling misses.

## 🔍 Main Contributions

- **Methodological**: Residual analysis reveals second-order institutional effects beyond main predictions
- **Empirical**: Women experienced systematically favorable residuals; men faced asymmetric downside risk  
- **Counterfactual**: Institutional modifications could have produced effects 4-5× larger than plausible individual capability variation

## 📊 Key Results

| Finding | Result |
|---------|--------|
| **Predictive Accuracy** | 85% from demographics alone |
| **Residual Structure** | Cohen's d = 0.65, p < 0.001 |
| **Risk Asymmetry** | Women: bounded risk (+0.91 skew)<br>Men: catastrophic downside (-1.83 skew) |
| **Institutional Effect** | 50pp redistribution vs ±11pp capability bounds |

## 🚀 Quick Start

### Prerequisites
```bash
python 3.9+
pandas, numpy, scikit-learn, scipy, matplotlib, seaborn
```

### Installation
```bash
git clone https://github.com/bominkkwon/titanic-residual-analysis.git
cd titanic-residual-analysis
pip install -r requirements.txt
```

### Run Analysis
```bash
# Generate all figures and results
python analysis.py

# Or run the interactive Jupyter notebook
jupyter notebook titanic_residual_analysis.ipynb
```

## 📁 Repository Structure

```
├── analysis.py                     # Complete analysis script
├── titanic_residual_analysis.ipynb # Interactive notebook
├── train.csv                       # Titanic dataset
├── figures/                        # Generated figures
│   ├── roc_curve.png
│   ├── residual_distributions.png
│   ├── permutation_test.png
│   └── counterfactual_*.png
└── README.md                       # This file
```

## 🔬 Methodology Overview

1. **Model Training**: 5-fold cross-validation with Gradient Boosting
2. **Residual Computation**: Out-of-fold predictions to avoid overfitting bias
3. **Statistical Testing**: Welch's t-test, permutation tests, effect sizes
4. **Counterfactual Analysis**: Stylized simulations of alternative protocols

**Critical Insight**: If demographics predict outcomes through individual capabilities, residuals should be independent of demographics. Systematic residual patterns suggest institutional mechanisms.

## 📈 Figures

The analysis generates publication-quality figures demonstrating:

- **ROC Curve**: High accuracy from demographic features
- **Residual Distributions**: Systematic patterns by sex
- **Permutation Test**: Patterns far exceed random chance
- **Counterfactuals**: Institutional vs capability effect sizes

## 🎯 Applications

This diagnostic approach may be relevant for analyzing:
- Criminal justice prediction systems
- College admissions algorithms  
- Credit scoring models
- Hiring algorithms

*Each domain requires careful analysis with appropriate data and domain expertise.*

## 📚 Citation

If you use this work, please cite:

```bibtex
@article{kwon2025titanic,
  title={Beyond Prediction: Residual Analysis Reveals Multi-Layered Institutional Structure in Titanic Survival},
  author={Kwon, Bomin},
  journal={arXiv preprint arXiv:submit/6966879},
  year={2025}
}
```

## ⚠️ Important Limitations

- **Single case study**: Findings specific to Titanic with documented mechanisms
- **Observational data**: Cannot definitively rule out unmeasured confounders  
- **Stylized counterfactuals**: Simulations are illustrative, not causal estimates
- **Capability bounds**: Individual variation estimates are speculative

## 🤝 Contributing

This research was conducted independently. For questions or collaborations, please open an issue or contact [bominkkwon@proton.me](mailto:bominkkwon@proton.me).

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

**Abstract**: The Kaggle Titanic competition asks: "What sorts of people were more likely to survive?" Standard machine learning models achieve 85% prediction accuracy using demographic features, but high accuracy alone does not explain why these features predict outcomes. We extend beyond predictive modeling to examine whether residuals are randomly distributed or systematically patterned by demographics, revealing multi-layered institutional structures that main effects alone miss.

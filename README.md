# Persona Vectors in Controlling Hallucination of LLMs

This repository contains the companion code for the paper:

**"Persona Vectors in Controlling Hallucination of Small Large Language Models: A Safety-Oriented Analysis"**  
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1234567.svg)](https://doi.org/10.5281/zenodo.1234567)  
*Authors:
Utku Kose (Suleyman Demirel University, Turkey [utkukose@sdu.edu.tr](mailto:utkukose@sdu.edu.tr))  
Ilhan Uysal (Burdur Mehmet Akif Ersoy University, Turkey [iuysal@mehmetakif.edu.tr](mailto:iuysal@mehmetakif.edu.tr))*

📄 Inspired by:  
R. Chen, A. Arditi, H. Sleight, O. Evans, and J. Lindsey,  
*Persona Vectors: Monitoring and Controlling Character Traits in Language Models*.  
arXiv preprint arXiv:2507.21509, 2025.  
[https://doi.org/10.48550/arXiv.2507.21509](https://doi.org/10.48550/arXiv.2507.21509)

---

## 📌 Overview

This notebook evaluates hallucination and abstention behaviors of small LLMs under different **persona settings**:

- **Confident Persona** → Always answers decisively, avoids admitting uncertainty.  
- **Careful Persona** → Acts as a cautious assistant, abstains when uncertain.

The evaluation covers:

- **TruthfulQA** (hallucination detection, correctness)  
- **SQuAD v2 (unanswerable subset)** (abstention ability, hallucinations under uncertainty)  
- **Simulated RAG experiment** with risky vs. benign knowledge snippets  

Metrics include:
- Accuracy on TruthfulQA
- High-certainty hallucination rates
- Abstention rates
- Persona delta comparisons

Results are exported as `.csv`, `.xlsx`, `.tex`, and plots inside the `outputs/` folder.

---

## 📂 Repository Structure

```
.
├── llm_persona_code_4-model_compare_FINAL.ipynb   # Main Jupyter notebook (evaluation + analysis)
├── requirements.txt                               # Python dependencies
├── .gitignore                                     # Ignore cache, outputs, temp files
├── README.md                                      # ReadMe documentation
└── outputs/                                       # Results auto-generated at run-time (ignored by git)
```

---

## ⚙️ Installation

Clone the repo and install dependencies:

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
pip install -r requirements.txt
```

---

## ▶️ Usage

Open the notebook:

```bash
jupyter notebook PersonaHallucinationStudy.ipynb
```

Run all cells. At the end you will see:

- Comparative CSV/Excel/LaTeX result files
- Plots (line charts, grouped bars, heatmaps, Pareto frontiers)
- Sample logs of model responses
- RAG experiment results

All outputs are saved under `./outputs`.

---

## 📊 Example Outputs

- Persona-wise metrics comparison (line & bar plots)  
- Heatmap of average hallucination/abstention per model  
- Ranking by TruthfulQA accuracy  
- Pareto analysis (abstention vs high-certainty hallucination)  

---

## 🛠️ Requirements

Main libraries:
- `transformers`
- `datasets`
- `torch`
- `pandas`
- `numpy`
- `matplotlib`
- `xlsxwriter`

See `requirements.txt` for the exact list.

---

## 📜 License

If you want to allow open use, consider adding MIT or Apache-2.0 license here.

---

## 🙌 Citation

If you use this code in your research, please cite:

```
@misc{kose2025persona,
  title={Persona Vectors in Controlling Hallucination of Small Large Language Models: A Safety-Oriented Analysis},
  author={Kose, Utku and Uysal, Ilhan},
  year={2025},
  note={Available via GitHub},
  doi=https://doi.org/10.5281/zenodo.1234567
}
```

# Waste Glass Concrete Strength — ML Models & GUI

Predict compressive strength of sustainable concrete mixes (with Waste Glass Powder, WGP) using a trained CatBoost model and a simple GUI.

[https://github.com/](https://github.com/)<your-username>/<your-repo>

> **Files included**
>
> * `Final_data_sushant.xlsx` — curated dataset used to train/evaluate the ML models.
> * `GUI.ipynb` — Jupyter Notebook providing the GUI app (Tkinter) and prediction workflow.
> * `catboost_model.cbm` — saved CatBoost regression model used by the GUI.
> * `GUI_Graphics.png` — header image shown in the GUI (note: filename is **case‑sensitive** on macOS/Linux).

---

## Quick Start

### 1) Clone and set up environment

```bash
# clone
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>

# (optional) create a virtual environment
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate

# install dependencies
pip install -r requirements.txt
```

> If you don’t use `requirements.txt`, install the essentials:

```bash
pip install catboost numpy pillow pandas jupyter
```

> **Note:** Tkinter ships with most Python distributions on Windows/macOS. On some Linux distros you may need to install it via your package manager (e.g., `sudo apt-get install python3-tk`).

### 2) Launch Jupyter and run the GUI

```bash
jupyter notebook GUI.ipynb
```

Open the notebook and run all cells. The GUI window should appear. If you run into issues with images on non‑Windows platforms, verify the path and capitalization of `GUI_Graphics.png`.

---

## Repository Structure

```
<your-repo>/
├── Final_data_sushant.xlsx   # dataset used for training/analysis
├── GUI.ipynb                 # Jupyter-based GUI application
├── catboost_model.cbm        # pre-trained CatBoost model
├── GUI_Graphics.png          # header image used by the GUI
└── README.md                 # this file
```

---

## How It Works

### Model

* **Algorithm:** CatBoostRegressor
* **Saved model:** `catboost_model.cbm`
* The GUI loads this model at startup and performs predictions from user inputs.

> If you re-train the model, save it as `.cbm` and keep the same filename or update the loader path in the notebook.

### GUI

* Built with **Tkinter** (in a Jupyter cell) for quick interaction.
* Displays a header image (`GUI_Graphics.png`), accepts mix parameters, and returns predicted compressive strength.

### Data

* `Final_data_sushant.xlsx` contains the consolidated dataset used for ML modeling and evaluation (e.g., mix proportions, W/C, WGP%, curing days, etc.).
* The GUI **does not** require this file to run predictions unless you extend it for batch inference.

---

## Re‑training (Optional)

1. Load and clean `Final_data_sushant.xlsx` in a separate notebook or Python script.
2. Train a new CatBoost model (or alternative models like XGBoost/LightGBM).
3. Save the trained model as `.cbm` and point the GUI loader to it:

```python
from catboost import CatBoostRegressor
model = CatBoostRegressor()
model.load_model('catboost_model.cbm')
```

---

## Troubleshooting

* **Image not showing:** ensure `GUI_Graphics.png` is in the project root and the filename capitalization matches exactly.
* **Model not loading:** verify `catboost_model.cbm` exists and the relative path is correct.
* **Tkinter errors (Linux):** install `python3-tk` via your package manager.

---

## Requirements

* Python 3.9+
* Packages: `catboost`, `numpy`, `pillow`, `pandas`, `jupyter` (plus `tkinter`)

Optionally for data/experiments: `scikit-learn`, `matplotlib`, `shap`.

Create a `requirements.txt` (optional):

```txt
catboost
numpy
pillow
pandas
jupyter
# optional
scikit-learn
matplotlib
shap
```

---

## Citation

If you use this repository in academic work, please cite your related publications. For example:

```bibtex
@article{Poudel2025WGP,
  author  = {Sushant Poudel and Coauthors},
  title   = {Prediction of Compressive Strength of Sustainable Concrete Incorporating Waste Glass Powder Using Machine Learning Algorithms},
  journal = {Sustainability},
  year    = {2025}
}
```

---

## License

Choose a license and add a `LICENSE` file (e.g., MIT). For MIT, you can use:

```txt
MIT License
Copyright (c) 2025 Sushant Poudel
Permission is hereby granted, free of charge, to any person obtaining a copy
... (full MIT text)
```

---

## Acknowledgements

* Thanks to collaborators and advisors who contributed to data curation and model development.

---

## Contact

For questions or dataset requests, please open an issue or reach out:

* **Sushant Poudel** — [your.email@example.com](mailto:your.email@example.com)

---

### Notes

* If your image file is named `GUI_graphics.png` in your local repo, rename it to `GUI_Graphics.png` or update references accordingly.
* Keep large datasets out of Git history when possible; consider Git LFS if needed.

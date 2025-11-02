# Waste Glass Concrete Strength — ML Models & GUI

Predict compressive strength of sustainable concrete mixes (with Waste Glass Powder, WGP) using a trained CatBoost model and a simple GUI.

> **Files included**
>
> * `Final_data_sushant.xlsx` — curated dataset used to train/evaluate the ML models.
> * `GUI.ipynb` — Jupyter Notebook providing the GUI app (Tkinter) and prediction workflow.
> * `catboost_model.cbm` — saved CatBoost regression model used by the GUI.
> * `GUI_Graphics.png` — header image shown in the GUI (note: filename is **case‑sensitive** on macOS/Linux).

---

## Quick Start

1) Launch Jupyter and run the GUI

Open the notebook and run all cells. The GUI window should appear. If you run into issues with images on non‑Windows platforms, verify the path and capitalization of `GUI_Graphics.png`.

---

## Repository Structure

```
├── Final_data_sushant.xlsx   # dataset used for training/analysis
├── GUI.ipynb                 # Jupyter-based GUI application
├── catboost_model.cbm        # pre-trained CatBoost model
├── GUI_Graphics.png          # header image used by the GUI
└── README.md                 # this file
```

---

## License

Copyright (c) 2025 Sushant Poudel
Permission is hereby granted, free of charge, to any person obtaining a copy.


---

## Acknowledgements

* Thanks to collaborators and advisors who contributed to data curation and model development.

---

## Contact

For questions or dataset requests, please open an issue or reach out:

* **Sushant Poudel** — [sushantpoudel50@gmail.com]

---

### Notes

* If your image file is named `GUI_graphics.png` in your local repo, rename it to `GUI_Graphics.png` or update references accordingly.

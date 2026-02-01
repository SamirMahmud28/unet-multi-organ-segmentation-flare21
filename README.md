# U-Net Based Multi-Organ Segmentation of Abdominal CT (FLARE21)

This repository contains notebooks for abdominal multi-organ segmentation using a U-Net style model, developed on Kaggle and exported to GitHub.

## Highlights
- Multi-class segmentation (background excluded in macro metrics)
- 3D → 2D slice preprocessing workflow
- Evaluation includes Dice/F1, IoU, precision/recall, pixel accuracy, and a validation confusion matrix

## Repository Structure
- `notebooks/` – project notebooks
- `assets/` – training curves and qualitative results used in this README
- `data/` – local dataset directory (not tracked)
- `models/` – local checkpoints/weights (not tracked)

## Dataset
This project uses the FLARE21 dataset.
- Do not upload medical imaging datasets to this repository.
- Keep the dataset locally under `data/` (your `.gitignore` should exclude it).

Example local structure:

    data/
      flare21/
        TrainingImg/
        TrainingMask/

## Running on Kaggle
If you want to run without changing paths, run the original notebook on Kaggle:
https://www.kaggle.com/code/samirmahmud28/u-net-based-multi-organ-segmentation-of-abdominal

## Running Locally
These notebooks were originally written for Kaggle and may include Kaggle-specific paths (e.g., `/kaggle/input/...`).
To run locally you may need to update paths to your local `data/` directory.

Create a virtual environment:

    python -m venv .venv

Activate it:

    Windows: .venv\Scripts\activate
    macOS/Linux: source .venv/bin/activate

Install dependencies:

    pip install -r requirements.txt

Launch Jupyter:

    jupyter lab

Open notebooks from `notebooks/`.

## Results

### Qualitative example (CT / Ground Truth / Prediction)
![Sample prediction](assets/sample_prediction.png)

### Training curves and metrics
![Loss](assets/Loss.png)
![Mean Dice (macro, no background)](assets/Mean_Dice.png)
![Mean IoU (macro, no background)](assets/Mean_IoU.png)
![Precision (macro, no background)](assets/Precision.png)
![Recall (macro, no background)](assets/Recall.png)
![F1 (macro, no background)](assets/F1.png)
![Micro-F1 (foreground aggregated)](assets/Macro_F1.png)
![Pixel Accuracy](assets/Pixel_Accuracy.png)

### Confusion Matrix (Validation)
![Confusion Matrix](assets/Normalized_Confusion_Matrix_Validation.png)

## Links

Kaggle (main project):
https://www.kaggle.com/code/samirmahmud28/u-net-based-multi-organ-segmentation-of-abdominal



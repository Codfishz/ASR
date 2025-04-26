# Automation of Scientific Research Course Project

This repository contains the code and results for the CMU 02450 Automation of Scientific Research course project. The project explores various active sampling strategies using YOLO-based methods for image classification in the context of agricultural pest detection.

## Repository Structure

```
.
├── results
│   ├── accuracy_log.csv         # Logs of accuracy metrics (e.g., top-1, top-5)
│   └── confusion_matrix.png     # Confusion matrix visualization
└── scripts
    ├── Dataloader_FeatureExtraction.ipynb  # Data loading & feature extraction functions
    ├── Datapreparation_YOLO.ipynb          # Data preparation steps for YOLO experiments
    ├── mc_dropout.ipynb                    # Auxiliary functions for Monte Carlo Dropout
    ├── YOLO_DH.ipynb                       # Density-based sampling with YOLO
    ├── YOLO_DH_resnet50.ipynb              # Density-based sampling with YOLO + ResNet50
    ├── YOLO_Density.ipynb                  # Density-weighted sampling strategy
    ├── YOLO_Density_resnet50.ipynb         # Density-weighted sampling with ResNet50
    ├── YOLO_MC_Dropout.ipynb               # Uncertainty sampling via MC Dropout
    ├── YOLO_Random.ipynb                   # Random sampling baseline
    └── YOLO_TTA.ipynb                      # Test-time augmentation sampling
```

- **results**: Contains all test outputs:
  - `accuracy_log.csv`: Detailed accuracy records.
  - `confusion_matrix.png`: Visual representation of the confusion matrix.

- **scripts**: Jupyter notebooks implementing data pipelines and evaluation methods:
  - **Data Utilities**:
    - `Dataloader_FeatureExtraction.ipynb`
    - `Datapreparation_YOLO.ipynb`
    - `mc_dropout.ipynb`
  - **YOLO-based Sampling Experiments**:
    - `YOLO_DH*.ipynb`        
    - `YOLO_Density*.ipynb`   
    - `YOLO_MC_Dropout.ipynb`
    - `YOLO_Random.ipynb`
    - `YOLO_TTA.ipynb`

## Setup and Dependencies

This project is designed to run in Google Colab. Each notebook includes the necessary `!pip install ...` commands to install required libraries (e.g., `torch`, `ultralytics`, `numpy`, `pandas`, `matplotlib`).

To get started:
1. Open the desired notebook (e.g., `scripts/YOLO_Random.ipynb`) in Colab.
2. Run all cells—Colab will install dependencies automatically.

## Usage

To run the project from start to finish:

1. **Clone the repository （Already include in each notebook）**:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```
2. **Open and run each notebook in Colab**:
   - In Google Colab, open the notebooks in the `scripts/` folder in below for different experiments:
       All `YOLO_*.ipynb` experiments (`YOLO_DH.ipynb`, `YOLO_DH_resnet50.ipynb`, `YOLO_Density.ipynb`, `YOLO_Density_resnet50.ipynb`, `YOLO_MC_Dropout.ipynb`, `YOLO_Random.ipynb`, `YOLO_TTA.ipynb`)
   - Run all cells in each notebook. Required dependencies and data preparation steps are handled within the notebooks.

3. **View results**:
   - After running an experiment notebook, check the workspace for `accuracy_log.csv` and `confusion_matrix.png`.


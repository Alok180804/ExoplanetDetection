# Roadmap: ML-Enhanced Exoplanet Transit Detection & Explainability

---

## Phase 1: Preparation & Exploration (Weeks 1-2)

### Literature Review
- Read recent papers on exoplanet detection with ML (e.g., TESS/K2 transit detection, CNNs, explainability).
- Understand challenges in transit detection and common false positives.

### Dataset Familiarization
- Explore TESS and K2 missions data characteristics.
- Get familiar with the Lightkurve package to download and manipulate light curves.

### Set up Environment
- Prepare Python environment with all needed packages (TensorFlow/PyTorch, Lightkurve, SHAP, LIME, etc.).

---

## Phase 2: Data Collection & Preprocessing (Weeks 3-4)

### Download Data
- Use Lightkurve API to download light curves for confirmed exoplanets and known false positives.

### Data Cleaning
- Remove noise, outliers, and trends from light curves.
- Normalize flux values.
- Segment light curves into fixed windows containing potential transits.

### Labeling
- Label data segments as "planet transit" or "non-transit/false positive" using NASA Exoplanet Archive.

### Exploratory Data Analysis (EDA)
- Visualize sample light curves, transit shapes, noise characteristics.

---

## Phase 3: Model Design & Training (Weeks 5-7)

### Model Selection
- Design 1D-CNN architecture for time series transit detection.
- Experiment with alternative models (LSTM, Transformers).

### Training
- Train models on labeled datasets.
- Use data augmentation techniques if needed (e.g., adding noise, shifting windows).

### Hyperparameter Tuning
- Optimize model parameters (learning rate, batch size, epochs).

### Evaluation
- Use validation data to check performance.
- Calculate metrics: precision, recall, F1-score, ROC-AUC.

---

## Phase 4: Explainability Integration (Weeks 8-9)

### Implement Explainability
- Use SHAP and LIME to explain model predictions on sample light curves.
- Identify key features/time segments influencing classification.

### Visualization
- Create plots showing which parts of light curves drive decisions.
- Interpret results to verify model is learning meaningful transit patterns.

---

## Phase 5: Testing & Application (Weeks 10-11)

### Test on Unlabeled Data
- Run the trained model on newly released TESS data without labels.
- Identify high-confidence new transit candidates.

### Cross-Validation
- Compare predictions with official candidate lists or community alerts.

### Refinement
- Refine preprocessing or model based on test results.

---

## Phase 6: Documentation & Publication (Weeks 12-13)

### Write Research Paper
- Introduction & background.
- Data sources & preprocessing details.
- Model design and training process.
- Explainability methods and insights.
- Results and potential new candidates.
- Discussion & future work.

### Prepare Codebase
- Organize scripts, notebooks, and documentation for reproducibility.

### Create Presentation
- Summarize key results for university applications or conferences.

---

## Optional Phase 7: Advanced Extensions (After core project)

- Explore Transformer models for better temporal feature extraction.
- Integrate data from other missions (CHEOPS, PLATO).
- Collaborate with astronomers for follow-up observation plans.
- Publish code and data on GitHub with a detailed README.

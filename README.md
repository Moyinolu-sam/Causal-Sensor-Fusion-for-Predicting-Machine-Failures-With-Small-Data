# Causal-Sensor-Fusion-for-Predicting-Machine-Failures-With-Small-Data

## Project Overview
<!-- #### Project Goal
To build a machine learning system that predicts machinery failures using causal inference, sensor fusion and small data learning techniques.

### Why it stands out:
1. Real world industrial data is usually tiny and messy, so traditional Machine learning fails.
2. You’ll show skill in causal discovery, multimodal fusion, and noise-robust modeling — rare and high-value.-->
Most industrial systems like manufacturing machines, turbines, pumps and motors produce multiple noisy sensor streams.
Traditional machine learning models struggle here because the data is: Small, Noisy and Non-linear.

This project builds a complete pipeline that predicts machine failures using causal inference and sensor fusion, making the model more robust and interpretable in realistic small data environments.


## Features
1. Causal discovery (identifying which signals cause degradation)
2. Multimodal sensor fusion (vibration + acoustics + temperature)
3. Small-data learning techniques (Bayesian models, boosting)
4. Time-series & signal processing (FFT, MFCC, envelope features)
5. Noise-robust modeling
6. Interactive dashboard for prediction & explanation
7. Causal graph visualization for interpretability
8. Explainable predictions using SHAP values


## Dataset Used
This project uses publicly available datasets:

1. NASA Bearing Dataset
Run to failure vibration & temperature data
Contains real degradation patterns

2. MIMII Machine Sound Dataset
Acoustic anomalies (valves, pumps, fans)
Great for multimodal fusion
Combined, they simulate an industrial monitoring environment.


## Methodology
1. Exploratory Analysis
Visualize vibration, audio spectrograms, temperatures
Detect noise patterns
Identify degradation trends

2. Causal Discovery
Tools used:
Granger causality
PCMCI (temporal causal discovery)
FGES / NOTEARS (structural DAGs)
Result:
A causal graph showing which sensor signals influence failure progression.

3. Feature Engineering
Time-domain features:
RMS, kurtosis, skewness
Peak-to-peak, crest factor
Rolling statistics
Frequency-domain features:
FFT components
MFCCs (for audio)
Spectral centroid & bandwidth
Cross-sensor features:
Correlations
Lags
Energy ratios

4. Sensor Fusion Strategies
Early Fusion
Combine all features into one model (LightGBM / XGBoost).
Late Fusion
Model each sensor separately → then ensemble.
Hybrid Fusion
Attention-based weighting of sensors.

5. Modeling (Small-Data Friendly)
XGBoost / LightGBM
Bayesian Ridge Regression
Random Forests
1D CNN with heavy regularization
Meta-learning baseline (optional)
Models are tested under:
Noise injection
Missing sensor data
Limited training windows

6. Explainability
SHAP values for feature importance
Causal graphs for reasoning
Failure probability timeline
Sensor contribution visualization

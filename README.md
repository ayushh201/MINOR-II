# MINOR-II
A comparative analysis of privacy-preserving techniques—Federated Learning, Differential Privacy, and Pixelation—for pneumonia detection using chest X-rays, focusing on the trade-off between diagnostic accuracy and patient data privacy.
# Privacy-Preserving Pneumonia Detection from Chest X-rays

## Summary

This research presents a comprehensive comparative analysis of privacy-preserving techniques for pneumonia detection using chest X-ray images. We evaluate differential privacy (Gaussian & Laplace), federated learning, pixelation, and a novel hybrid approach against a baseline CNN model using the Kaggle Chest X-Ray dataset (5,856 images). 

**Key Findings:**
- Federated Learning achieved highest accuracy (85.90%) while enabling decentralized training
- Gaussian Differential Privacy provided optimal privacy-utility balance (83.17% accuracy, 94.10% recall)
- Privacy budget analysis shows optimal range of ε ∈ [2.0, 4.0] for differential privacy
- Hybrid approaches may introduce excessive complexity, reducing performance significantly

This work provides practical implementation guidelines for privacy-preserving medical AI systems, addressing HIPAA compliance while maintaining diagnostic effectiveness.

## Results

### Model Performance Comparison

| Method | Test Accuracy (%) | Precision (%) | Recall (%) | F1 Score (%) |
|--------|-------------------|---------------|------------|--------------|
| Baseline CNN | 81.89 | 78.55 | 97.69 | 87.08 |
| Federated Learning | **85.90** | 88.16 | 85.90 | 85.05 |
| Gaussian DP | 83.17 | 81.74 | **94.10** | **87.49** |
| Laplace DP | 62.02 | 62.77 | 96.41 | 76.03 |
| Pixelation | 57.15 | 52.00 | 87.46 | 65.20 |
| FL + DP Hybrid | 37.50 | 18.75 | 50.00 | 27.27 |

### Dataset Distribution

| Category | Training | Validation | Test | Total |
|----------|----------|------------|------|-------|
| Normal | 1,341 | 8 | 234 | 1,721 |
| Pneumonia | 3,875 | 8 | 390 | 4,135 |
| **Total** | **5,216** | **16** | **624** | **5,856** |

### Privacy Budget Analysis (Differential Privacy)

| Privacy Budget (ε) | Gaussian DP Accuracy (%) | Laplace DP Accuracy (%) |
|-------------------|--------------------------|-------------------------|
| 0.1 | 52.3 | 45.1 |
| 0.5 | 67.8 | 58.2 |
| 1.0 | 75.4 | 62.0 |
| 2.0 | 81.2 | 64.5 |
| 4.0 | 83.1 | 65.8 |
| 8.0 | 83.2 | 66.0 |
| 10.0 | 83.2 | 66.1 |

\

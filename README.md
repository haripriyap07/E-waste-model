# E-waste-model
# E-Waste Classification Model – Performance Evaluation

## Overview
This project uses a deep learning-based image classification model to identify different categories of electronic waste (E-Waste). The model classifies input images into four categories:

- PCB
- Battery
- Plastic
- Metal

The model was evaluated on a test dataset containing 300 images to measure its classification performance and reliability.

## Model Performance

### Classification Report

| Class | Precision | Recall | F1-Score | Support |
|---|---:|---:|---:|---:|
| PCB | 0.96 | 0.90 | 0.93 | 30 |
| Battery | 0.83 | 0.80 | 0.81 | 30 |
| Plastic | 0.93 | 0.94 | 0.94 | 120 |
| Metal | 0.95 | 0.97 | 0.96 | 120 |
| **Accuracy** | | | **0.93** | **300** |
| Macro Average | 0.92 | 0.90 | 0.91 | 300 |
| Weighted Average | 0.93 | 0.93 | 0.93 | 300 |

### Key Metrics

- **Overall Accuracy:** 93%
- **Macro F1-Score:** 91%
- **Weighted F1-Score:** 93%
- **Test Images:** 300

The model achieved an overall classification accuracy of 93%, demonstrating good performance across the four E-Waste categories.

## Confidence Threshold-Based Classification

A confidence threshold of **0.70 (70%)** was implemented to improve the reliability of automated waste sorting.

Predictions with confidence scores greater than or equal to 70% are automatically classified, while predictions below the threshold are flagged for manual verification.

### Confidence Threshold Results

| Metric | Result |
|---|---:|
| Confidence Threshold | 70% |
| Total Test Images | 300 |
| Automatically Sorted | 270 (90%) |
| Flagged for Manual Review | 30 (10%) |
| Accuracy on Auto-Sorted Images | 97.8% |

### How It Works

1. The input image is passed to the trained classification model.
2. The model predicts the E-Waste category and its confidence score.
3. If confidence is at least 70%, the item is automatically classified.
4. If confidence is below 70%, the item is flagged for manual inspection.

This approach reduces the risk of incorrect automated sorting by allowing uncertain predictions to undergo human verification.

## Conclusion

The model achieved 93% overall accuracy across four E-Waste categories. By introducing a confidence threshold of 70%, 90% of the test images could be automatically classified with 97.8% accuracy on the automatically sorted subset.

The confidence-based approach improves sorting reliability while maintaining a balance between automation and manual verification, making the system suitable for integration into an automated E-Waste sorting setup.

---

**Note:** The reported metrics are based on the evaluated test dataset of 300 images. Performance may vary on real-world images and different environmental conditions.

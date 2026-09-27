# Fresh Produce Quality Detector

## Team Members
- Rigoberto Padilla

## Tier Selection
**Tier 1** — This project uses image classification and a pretrained/transfer-learning approach so the main goal is a working computer-vision application that can be completed within the term.

## Problem Statement
People and food-service workers often rely on visual inspection to decide whether produce appears fresh enough to use. Spoiled produce can be missed, contributing to food waste, quality problems, and unnecessary disposal. This project will create a computer vision application that gives a quick visual Fresh or Rotten prediction from an image.

## Solution Overview
The application will accept an image of fruit or vegetables and use a computer-vision image classifier to predict its freshness condition. The project will simplify the dataset's produce-specific labels into two application-level outcomes: **Fresh** or **Rotten**.

**Image → Preprocessing → Image Classifier → Fresh/Rotten prediction**

## Technical Approach
- **Computer vision technique:** Image classification
- **Model:** Pretrained CNN using transfer learning
- **Framework:** Python + TensorFlow/Keras
- **Environment:** Google Colab
- **Input:** RGB produce image
- **Output:** Fresh or Rotten prediction, with confidence
- **Why:** The task is naturally a classification problem, and transfer learning gives a practical starting point for a Tier 1 proof of concept.

## Data Plan
### Dataset
**Fruits and Vegetables Dataset**

Public source:
https://www.kaggle.com/datasets/muhriddinmuxiddinov/fruits-and-vegetables-dataset

The published dataset contains **12,000 images** across 20 produce-specific classes: 10 fresh classes and 10 rotten classes. The classes include fresh/rotten versions of apple, banana, orange, mango, strawberry, potato, cucumber, carrot, tomato, and bell pepper. 

For this application, the 20 source labels will be mapped into two output labels:
- **Fresh**
- **Rotten**

The dataset will be divided into training, validation, and test sets. Care will be taken to avoid putting near-duplicate images into different evaluation groups where possible.

## Success Metrics
### Primary metric
**At least 85% test accuracy** on the held-out test set.

### Secondary metric
**Under 2 seconds per image** for prediction in the final demonstration environment.

Additional evaluation:
- Confusion matrix
- Precision and recall for Fresh and Rotten
- A small set of unseen sample images for a qualitative demo

## Milestone Plan — 10-Week Term
| Phase | Goal | Milestone |
|---|---|---|
| Blueprint | Plan the application | Week 5 — Midterm submitted |
| First Working Demo | Run a pretrained classifier end-to-end on sample images | Week 6 |
| Make It Yours | Add the project dataset, preprocessing, and application logic | Weeks 7–8 |
| Improve and Measure | Test, fix, tune, and record metrics | Week 9 |
| Package and Present | Finish README, demo, slides, and final submission | Week 10 |

## Risks and Plan B
### Risk 1: Dataset images may be different from real-world phone photos
**Plan B:** Use augmentation and test on additional images that were not part of training. Clearly state that the system is a visual screening tool, not a food-safety guarantee.

### Risk 2: The model does not reach 85% accuracy
**Plan B:** Start with transfer learning, tune image size/augmentation/training settings, and simplify the application to the strongest supported produce categories if needed.

## Resources and Cost
- Google Colab
- Python
- TensorFlow/Keras
- GitHub
- Kaggle/public dataset
- Estimated cost: **$0**

## Repository Structure
```text
Fresh_Produce_Quality_Detector/
├── README.md
├── data/
│   └── README.md
└── docs/
    ├── proposal.pdf
    └── AI_usage_log.md
```

## AI Usage
AI assistance is documented in `docs/AI_usage_log.md` and will be updated throughout the project.

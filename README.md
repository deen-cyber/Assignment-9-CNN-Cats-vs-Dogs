# Assignment 9 — Image Classification using CNN (Cats vs Dogs)

## Objective
Build a Convolutional Neural Network (CNN) to automate classification of pet images into **Cats** and **Dogs**, for an animal welfare organization.

## Dataset
- **Name:** Cats vs Dogs Dataset
- **Source:** [Kaggle — bhavikjikadara/dog-and-cat-classification-dataset](https://www.kaggle.com/datasets/bhavikjikadara/dog-and-cat-classification-dataset)
- Not redistributed in this repository; download directly from the Kaggle link above.

## Libraries Used
- TensorFlow / Keras — model building, training, data generators
- NumPy, Pandas — data handling
- Matplotlib, Seaborn — visualization
- scikit-learn — evaluation metrics (precision, recall, F1, confusion matrix)
- Kaggle API — dataset download

## Methodology
1. **Data Understanding:** Loaded the dataset, inspected folder structure, class counts, and image dimensions; visualized sample images.
2. **Data Preprocessing:** Resized all images to 128×128, normalized pixel values to [0, 1], and split into 80% training / 20% testing using `ImageDataGenerator`.
3. **Model Development:** Built and trained a CNN for 10 epochs with the Adam optimizer and binary cross-entropy loss.
4. **Model Evaluation:** Computed test accuracy, precision, recall, F1-score, confusion matrix, and accuracy/loss curves.
5. **Conclusion:** Summarized findings and CNN's strengths/limitations vs. ANN.

## CNN Architecture
| Layer | Details |
|---|---|
| Conv2D | 32 filters, 3×3, ReLU |
| MaxPooling2D | 2×2 |
| Conv2D | 64 filters, 3×3, ReLU |
| MaxPooling2D | 2×2 |
| Conv2D | 128 filters, 3×3, ReLU |
| MaxPooling2D | 2×2 |
| Flatten | — |
| Dense | 128 units, ReLU |
| Output | 1 unit, Sigmoid |

**Compilation:** Optimizer = Adam, Loss = Binary Crossentropy, Metric = Accuracy
**Training:** 10 epochs

## Results
> Fill in with your actual run's numbers after executing `Assignment-9.ipynb` on the full dataset:
- Test Accuracy: _TBD_
- Precision: _TBD_
- Recall: _TBD_
- F1-Score: _TBD_
- Confusion Matrix, Accuracy vs Epoch, and Loss vs Epoch plots: see notebook output.

## Conclusion
This project developed a CNN that classifies cat and dog images by learning hierarchical spatial features through convolution and pooling layers, which reduce dimensionality while preserving important visual patterns. Compared to a standard ANN, the CNN uses far fewer parameters through weight sharing and local receptive fields, and directly exploits the 2D structure of images rather than requiring them to be flattened. A key limitation is the CNN's reliance on large labeled datasets and compute resources, along with reduced robustness when test images differ significantly from training conditions in orientation, lighting, or background.

## How to Run
1. Place your Kaggle API token at `~/.kaggle/kaggle.json`.
2. Open `Assignment-9.ipynb` and run all cells (downloads dataset, trains, and evaluates the model).

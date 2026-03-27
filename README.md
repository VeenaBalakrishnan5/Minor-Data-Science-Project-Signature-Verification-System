##  Minor Project: Signature Verification System

[![Python](https://img.shields.io/badge/Python-3.7%2B-blue.svg)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)](https://www.tensorflow.org/)
[![Deep Learning](https://img.shields.io/badge/Model-CNN-red.svg)](https://keras.io/)

##  Project Overview
This **Minor Data Science Project** implements an automated system for signature authentication. By utilizing **Convolutional Neural Networks (CNN)**, the model is trained to distinguish between genuine and forged signatures. This system addresses the need for secure, automated verification in financial and legal sectors, where human error in manual verification can be costly.

##  Data Science Workflow
The project follows a rigorous computer vision pipeline:
1.  **Image Preprocessing:** Signatures are loaded, resized to a uniform dimension, and converted to grayscale to focus on stroke patterns rather than color noise.
2.  **Data Augmentation:** Techniques like rotation and zooming are applied to the training set to help the model generalize to different signature angles.
3.  **Feature Extraction:** A multi-layered CNN architecture is used to automatically detect critical features such as slant, pressure points, and curvature.

4.  **Optimization:** The model is compiled using the **Adam Optimizer** and **Binary Cross-Entropy** to minimize classification errors.
5.  **Validation:** Performance is measured using a hold-out test set to ensure the system works on signatures it hasn't seen before.

##  Performance Results
The model was evaluated on a balanced test set of 200 samples. The results are as follows:

### Classification Report
| Metric | Genuine (0) | Forged (1) |
| :--- | :--- | :--- |
| **Precision** | 1.00 | **0.87** |
| **Recall** | 1.00 | **0.80** |
| **F1-Score** | 1.00 | **0.83** |
| **Support** | 56,864 | 98 |

| Metric | Value | Support |
| :--- | :--- | :--- |
| **Accuracy** | **1.00** | **56,962** |
| **Macro Avg** | **0.93** | **56,962** |
| **Weighted Avg** | **1.00** | **56,962** |

##  Key Features
* **Automated Forensic Analysis:** Removes the subjectivity involved in manual signature checking.
* **Robust CNN Backbone:** Designed specifically for binary image classification tasks.
* **Optimized for Security:** The model prioritizes a high precision rate to ensure forgeries are caught with high confidence.

##  Installation & Usage
1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/yourusername/signature-verification-system.git
    ```
2.  **Install Dependencies:**
    ```bash
    pip install tensorflow keras numpy matplotlib opencv-python
    ```
3.  **Setup Data:** Ensure your dataset is structured into 'Genuine' and 'Forged' directories.
4.  **Run the Analysis:** Open `signature_verification_system.ipynb` in Google Colab or Jupyter and run all cells.

##  Conclusion
This project successfully demonstrates the power of Deep Learning in biometric security. By achieving an **F1-score of 0.83** on the forged class, the system proves capable of identifying subtle discrepancies in handwriting. This serves as a solid foundation for more advanced multi-user verification systems.


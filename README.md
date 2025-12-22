# Comparative Analysis of CNN, GAN, and Proposed DCGAN for Intrusion Detection

This project provides a comparative performance analysis of three Deep Learning architectures—Convolutional Neural Networks (CNN), Generative Adversarial Networks (GAN), and a Proposed Deep Convolutional GAN (DCGAN)—for detecting network intrusions using the Edge-IIoT dataset.

## Project Overview

Intrusion Detection Systems (IDS) are critical for securing Industrial IoT (IIoT) environments. This repository implements and evaluates different deep learning models to classify network traffic as either benign or a specific type of attack.

### Key Features:

* Data Preprocessing: Automated cleaning, duplicate removal, and label encoding.
* Class Balancing: Implementation of downsampling to create a balanced training set from the original Edge-IIoT data.
* Model Implementation: PyTorch-based implementations of CNN, GAN, and DCGAN architectures.
* Comprehensive Evaluation: Comparison using Accuracy, Recall, F1-Score, and ROC-AUC metrics.

##  Dataset

The project utilizes the DNN-EdgeIIoT dataset.

* Input Features: 53 network-related features (e.g., `frame.time`, `ip.src_host`, `tcp.flags`, `mqtt.msgtype`).
* Target: `Attack_type` (Categorical classification of various IIoT attacks).
* Processing: The notebook includes a script to generate a balanced version of the dataset named `DNN-EdgeIIoT-half.csv`.


### Prerequisites

* Python 3.8+
* PyTorch
* Pandas, NumPy, Scikit-learn
* Matplotlib (for visualization)

### Running the Project

1. Clone the repository:
```bash
git clone https://github.com/yourusername/intrusion-detection-comparison.git

```


2. Ensure `DNN-EdgeIIoT.csv` is in the project directory.
3. Open and run the Jupyter Notebook:
```bash
jupyter notebook "Comparative Analysis of CNN, GAN, and PROPOSED DCGAN.ipynb"

```



## Model Performance

Based on the experimental results in the notebook, the models were evaluated on several key metrics:

| Model | Accuracy | Recall | F1-Score | AUC |
| --- | --- | --- | --- | --- |
| CNN | 73.7% | 75.4% | 84.3% | 0.53% |
| GAN | 84.4% | 86.3% | 91.1% | 0.78% |
| Proposed DCGAN | 92.4% | 92.4% | 9.57% | 0.94% |

(Note: Exact results for GAN/DCGAN can be viewed in the output cells of the notebook after training.)

##  Methodology

1. Data Loading: Features are extracted and non-numeric values are encoded.
2. Balancing: The dataset is grouped by `Attack_type` and sampled to match the smallest class size to prevent model bias.
3. Training: Models are trained using PyTorch with a focus on binary and multi-class classification.
4. Visualization: ROC curves are generated to compare the True Positive Rate vs. False Positive Rate across all three models.

##  License

This project is licensed under the MIT License 

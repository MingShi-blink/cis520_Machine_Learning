# CIS5200 Machine Learning

This folder contains Python exports of CIS5200 Machine Learning homework notebooks. The assignments implement core machine learning algorithms using PyTorch, scikit-learn, torchvision, matplotlib, and PennGrader.

## Files

```text
cis520_Machine_Learning/
├── README.md
├── HW1.py
├── HW2.py
└── HW3.py
```

## Important Note

These files were exported from Google Colab notebooks. They contain notebook-specific commands such as:

```python
!pip install penngrader-client
```

Because of that, the `.py` files are not guaranteed to run directly with normal `python3 HW1.py` without cleanup. They are primarily useful as submitted homework code or as a reference for implemented functions. To run them locally, convert notebook shell commands to terminal commands, install the required packages, and provide any required data files.

## Homework 1: Perceptron and k-Nearest Neighbors

`HW1.py` covers basic classification algorithms.

Implemented topics:

- Perceptron margin calculation.
- Perceptron update condition.
- Perceptron weight update.
- Full perceptron training loop.
- k-nearest neighbors distance matrix computation.
- k-nearest neighbor index selection.
- kNN prediction.
- kNN classification pipeline.

Datasets and tools:

- Synthetic linearly separable data for perceptron.
- MNIST digit classification using only digits `0` and `8`.
- PyTorch and torchvision.
- Matplotlib visualization.

## Homework 2: Linear Models and Soft SVM

`HW2.py` focuses on supervised learning with linear models.

Implemented or partially implemented topics:

- Logistic regression loss.
- Logistic regression gradient.
- Gradient-descent fitting for logistic regression.
- Logistic regression prediction.
- Ridge/linear regression templates.
- Soft-margin SVM class with objective, gradient, optimization, and prediction methods.

Datasets and tools:

- UCI Wine Quality dataset for classification/regression.
- scikit-learn breast cancer dataset for SVM testing.
- PyTorch.
- pandas.
- scikit-learn.
- cvxpy.

Note: the linear/ridge regression section still contains `pass` placeholders in the inspected file.

## Homework 3: Clustering, PCA and GMMs

`HW3.py` covers unsupervised learning, dimensionality reduction, probabilistic models, tree-based models, ensemble methods, boosting, and custom PyTorch autograd functions.

Implemented or partially implemented topics:

- K-means initialization, assignment, centroid update, and stopping criterion.
- Feature normalization, PCA fitting, PCA projection, and PCA reconstruction.
- Gaussian Mixture Model EM steps and negative log-likelihood.


Datasets and tools:

- UCI shoulder implant X-ray images for clustering and PCA/GMM analysis.
- Iris dataset for decision trees/random forests.
- Breast cancer dataset for boosting.
- PyTorch.
- torchvision.
- scikit-learn.
- PIL.
- matplotlib.

Note: several later sections in `HW3.py` still contain `pass` or `TODO` placeholders in the inspected file.

## Dependencies

The notebooks use:

```text
torch
torchvision
scikit-learn
pandas
matplotlib
Pillow
cvxpy
dill
penngrader-client
```

Install common dependencies with:

```bash
pip install torch torchvision scikit-learn pandas matplotlib pillow cvxpy dill penngrader-client
```

Depending on your Python environment, PyTorch installation may require a platform-specific command from the official PyTorch install page.

## Data Requirements

Some datasets are downloaded automatically inside the original notebooks, while others are expected to exist locally.

- `HW1.py` downloads MNIST through `torchvision.datasets.MNIST`.
- `HW2.py` expects `winequality-red.csv` to be available if the commented `wget` cell is not run.
- `HW3.py` expects an X-ray image folder named `data` if the commented download/unzip cells are not run.

## How to Use

Recommended workflow:

```text
1. Open the original notebook or import the relevant functions into a clean notebook.
2. Install dependencies.
3. Download or place required datasets in the expected locations.
4. Run each homework section in order.
5. Use PennGrader cells only in the intended course environment.
```

If converting to standalone scripts, remove or rewrite notebook-specific commands such as `!pip install ...`, commented notebook magics, embedded base64 images, and PennGrader-only cells.

## Skills Demonstrated

- PyTorch tensor programming and vectorized computation.
- Supervised learning: perceptron, kNN, logistic regression, SVM.
- Unsupervised learning: K-means, PCA, Gaussian Mixture Models.
- Dataset preprocessing and train/test splitting.
- Image data handling with torchvision.
- Gradient-based optimization.
- Model evaluation using accuracy and reconstruction error.
- Decision trees, random forests, and boosting concepts.
- Custom autograd function structure in PyTorch.

## Limitations

- The files are notebook exports, not polished Python packages.
- Several later homework sections contain unfinished placeholders.
- Some data files are not included in this folder.
- PennGrader configuration and credentials are course-environment-specific.

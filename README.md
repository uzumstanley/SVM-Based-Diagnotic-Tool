# SVM-Based-Diagnotic-Tool
Machine Learning, Python

## Developing an SVM-based Diagnotic Tool for Identifying Benign and Malignant Cells

About Data

The example is based on a dataset that is publicly available from the UCI Machine Learning Repository (Asuncion and Newman, 2007)[http://mlearn.ics.uci.edu/MLRepository.html]


|Field name|Description|
|--- |--- |
|ID|Clump thickness|
|Clump|Clump thickness|
|UnifSize|Uniformity of cell size|
|UnifShape|Uniformity of cell shape|
|MargAdh|Marginal adhesion|
|SingEpiSize|Single epithelial cell size|
|BareNuc|Bare nuclei|
|BlandChrom|Bland chromatin|
|NormNucl|Normal nucleoli|
|Mit|Mitoses|
|Class|Benign or malignant|


Aimed at developing a Support Vector Machine (SVM)-based diagnostic tool for classifying cells as benign or malignant.

### Introduction
- The notebook begins with an overview of its objective, which is to develop an SVM-based tool for identifying benign and malignant cells using a dataset from the UCI Machine Learning Repository.

### Data Description
- The data features are described, including cell characteristics like Clump Thickness, Uniformity of Cell Size, and others. The target variable is the `Class` field indicating benign (2) or malignant (4) diagnoses.

### Development Process
1. **Data Loading and Preprocessing:**
   - Libraries such as pandas, numpy, and sklearn are imported.
   - The dataset is loaded into a DataFrame, and initial exploration is performed.

2. **Data Exploration and Visualization:**
   - This section includes visualizations and statistical analysis to understand the data better.

3. **Model Development:**
   - The SVM model is created using sklearn's SVM module.
   - Features are selected, and the model is trained on the dataset.
   - Code cells are dedicated to setting up the SVM, adjusting parameters, and fitting the model to the data.

4. **Model Evaluation:**

The SVM-based diagnostic tool's performance was rigorously evaluated, and the results are encapsulated in a confusion matrix and a classification report:

- **Confusion Matrix:**
  - True Positive (Benign): 85
  - False Positive (Benign misclassified as Malignant): 5
  - True Negative (Malignant): 47
  - False Negative (Malignant misclassified as Benign): 0
  This indicates that the model is particularly good at identifying malignant samples, with no instances of false negatives.

- **Classification Report:**
  - **Class 2 (Benign):**
    - Precision: 1.00 (no benign cases were misclassified as malignant)
    - Recall: 0.94 (94% of the benign cases were correctly identified)
    - F1-Score: 0.97 (a measure of the test's accuracy)
    - Support: 90 (number of actual occurrences of the class in the dataset)
  - **Class 4 (Malignant):**
    - Precision: 0.90 (90% of the identified malignant cases were correct)
    - Recall: 1.00 (every malignant case was identified correctly)
    - F1-Score: 0.95
    - Support: 47

- **Overall Metrics:**
  - Accuracy: 96% (proportion of correctly identified instances)
  - Macro Avg: 95% Precision, 97% Recall, 96% F1-Score
  - Weighted Avg: 97% Precision, 96% Recall, 96% F1-Score

The confusion matrix and the accompanying classification report are critical for understanding the model's performance. The high accuracy and recall for malignant cases are particularly noteworthy, as they suggest the model is reliable in identifying potential cancer cases, which is crucial in a medical diagnostic context.

### Conclusion and Future Work
The analysis concludes that the SVM model exhibits high precision and recall, with impressive accuracy. It is especially effective at classifying malignant cells, as evidenced by the absence of false negatives, which is an important factor in medical diagnostics. 

For future work, it could be valuable to investigate the factors contributing to the five false positives and to consider how the model might be improved to reduce even this small number of benign cases being incorrectly classified as malignant. This might involve more sophisticated feature engineering, alternative classification algorithms, or a larger and more diverse dataset for training.

Integrating the evaluation results solidifies the conclusion that the SVM-based diagnostic tool developed in this notebook is effective and provides a solid foundation for further research and development in automated medical diagnosis.

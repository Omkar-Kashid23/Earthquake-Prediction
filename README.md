# Earthquake Alert Prediction System

## 📖 Overview
This project utilizes machine learning algorithms to predict earthquake alert levels based on seismic data. The goal is to classify earthquakes into alert categories (**green**, **orange**, **red**, **yellow**) using features such as magnitude, depth, and intensity metrics.

The analysis is conducted using Python and scikit-learn, comparing the performance of three different classifiers: **K-Nearest Neighbors (KNN)**, **Naive Bayes**, and **Support Vector Machine (SVM)**.

## 📊 Dataset
The project uses a balanced earthquake dataset (`earthquake_alert_balanced_dataset.csv`).

### Features
| Column | Description |
| :--- | :--- |
| `magnitude` | The magnitude of the earthquake |
| `depth` | The depth of the earthquake hypocenter |
| `cdi` | Community Decimal Intensity |
| `mmi` | Modified Mercalli Intensity |
| `sig` | Significance of the earthquake |
| `alert` | **Target Variable**: Alert level (green, orange, red, yellow) |

- **Total Samples:** 1300
- **Features:** 5
- **Target Classes:** 4 (green, orange, red, yellow)

## 🚀 Methodology
1.  **Data Loading:** Importing the dataset using `pandas`.
2.  **Preprocessing:** Separating features (`X`) and the target variable (`y`).
3.  **Splitting:** Data is split into training and testing sets (80% train, 20% test) using `train_test_split`.
4.  **Modeling:** Three models are trained and evaluated:
    *   KNeighborsClassifier (KNN)
    *   GaussianNB (Naive Bayes)
    *   SVC (Support Vector Classifier)
5.  **Evaluation:** Performance is measured using Accuracy, Precision, Recall, and F1-Score via `classification_report`.

## 📈 Results
The models were evaluated on the test set. Here is the comparison of accuracy across the different algorithms:

| Model | Accuracy | Performance Notes |
| :--- | :--- | :--- |
| **KNN** | **80%** | Best performing model among the three. |
| **Naive Bayes** | 67% | Moderate performance. |
| **SVM** | 55% | Lowest performance in initial tests (hyperparameter tuning may improve this if you want this use GridsearchCV). |

### Classification Report Summary (KNN)
- **Green:** Precision 0.85, Recall 0.62
- **Orange:** Precision 0.80, Recall 0.87
- **Red:** Precision 0.83, Recall 0.93
- **Yellow:** Precision 0.76, Recall 0.83

## 🛠 Installation & Requirements
To run this project, ensure you have Python 3 installed along with the following libraries:

```bash
pip install numpy pandas matplotlib scikit-learn
```

## 💻 Usage
1.  Clone or download this repository.
2.  Ensure the dataset file `earthquake_alert_balanced_dataset.csv` is located in the correct path (update the path in the notebook if necessary).
    *   *Current path in notebook:* `'Untitled Folder/earthquake_alert_balanced_dataset.csv'`
3.  Open the Jupyter Notebook file:
    ```bash
    jupyter notebook Earthquack.ipynb
    ```
4.  Run all cells to train the models and view the performance metrics.

## 📂 File Structure
```
.
├── Earthquack.ipynb              # Main Jupyter Notebook containing analysis
├── earthquake_alert_balanced_dataset.csv  # Dataset
├── requriments.txt
├── Doc.docx
├── Best_model_for_Earthquack.pkl
└── README.md                     # Project documentation
```

## 🔮 Future Improvements
- **Hyperparameter Tuning:** Optimize parameters for SVM and KNN (e.g., `n_neighbors`, `C`, `kernel`) to improve accuracy.
- **Data Visualization:** Add exploratory data analysis (EDA) plots using `matplotlib` to understand feature distributions.
- **Feature Engineering:** Investigate correlations between features (e.g., magnitude vs. depth) to potentially create new features.
- **Deep Learning:** Experiment with neural networks for potentially higher accuracy.

## 📄 License
This project is open-source and available for educational purposes.

---
*Created based on analysis from `Earthquack.ipynb`*

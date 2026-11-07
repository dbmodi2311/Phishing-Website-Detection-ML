# Phishing Website Detection Using Machine Learning

**IBM SkillsBuild Cyber Security BootCamp 2026 | BharatCares**

## Project description

This educational project demonstrates how supervised machine learning can classify website records as **Phishing** or **Legitimate** using the public UCI Phishing Websites dataset.

The notebook compares two models:

- Decision Tree Classifier
- Random Forest Classifier

It includes dataset loading, data inspection, preprocessing, exploratory data analysis, model training, evaluation metrics, a confusion matrix, feature importance, and a sample prediction.

> **Important scope note:** The UCI dataset contains 30 pre-extracted, integer-valued website features. This project predicts from those feature records. It does not accept an arbitrary raw URL and independently extract its features, and it is not a production security scanner.

## Dataset

- **Name:** Phishing Websites
- **Provider:** UCI Machine Learning Repository
- **Dataset ID:** 327
- **Records:** 11,055
- **Input features:** 30
- **Task:** Binary classification
- **Dataset page:** https://archive.ics.uci.edu/dataset/327/phishing
- **DOI:** https://doi.org/10.24432/C51W2X

The original target convention is `-1` for phishing and `1` for legitimate. The notebook maps these to readable class names.

## Technologies used

- Python 3
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- ucimlrepo

## Project files

| File | Description |
|---|---|
| `Dhruv_PhishingWebsiteDetection.ipynb` | Complete project code and analysis |
| `requirements.txt` | Required Python libraries |
| `Dhruv_ProjectReport.docx` | Project documentation |
| `README.md` | Project overview and instructions |

## Setup and run instructions

### 1. Download or clone the project

Keep the notebook and `requirements.txt` in the same folder.

### 2. Create a virtual environment (recommended)

Windows:

```bash
python -m venv .venv
.venv\\Scripts\\activate
```

macOS/Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Open `Dhruv_PhishingWebsiteDetection.ipynb` in the browser.

### 5. Run the notebook

- Run all cells from top to bottom.
- An internet connection is needed to retrieve the dataset from UCI on the first run.
- Review the generated metrics, charts, classification report, and sample prediction.
- Save the executed notebook with outputs before submission, if required by the submission portal.

### Google Colab option

Upload the `.ipynb` file to https://colab.research.google.com/. Install dependencies in a notebook cell if needed:

```python
%pip install -r requirements.txt
```

If `requirements.txt` is not uploaded to the Colab session, install the libraries directly:

```python
%pip install numpy pandas matplotlib seaborn scikit-learn ucimlrepo
```

## Methodology

1. Retrieve the UCI dataset using `ucimlrepo`.
2. Separate input features and target labels.
3. Inspect data types, missing values, and class distribution.
4. Split the data into training (80%) and testing (20%) sets using stratification.
5. Train Decision Tree and Random Forest classifiers.
6. Compare accuracy, macro precision, macro recall, and macro F1-score.
7. Inspect the classification report and confusion matrix.
8. Review feature importance and demonstrate a prediction on a held-out test record.

## Evaluation

The notebook calculates:

- **Accuracy**
- **Macro precision**
- **Macro recall**
- **Macro F1-score**
- **Classification report**
- **Confusion matrix**

No fixed accuracy is claimed in this README. The actual results are generated when the notebook is executed and may vary with library versions or dataset updates. Use the values produced by your own run in the project report.

## Responsible use and limitations

- This project is for education and demonstration.
- A prediction is not a guarantee that a website is safe or malicious.
- The model uses pre-extracted dataset features; it does not inspect live websites.
- Benchmark performance may not generalize to newly created phishing websites.
- Do not open suspicious links just to test them. Use trusted security tools and safe analysis environments.

## References

Mohammad, R., Thabtah, F., & McCluskey, L. (2012). *Phishing Websites*. UCI Machine Learning Repository. https://doi.org/10.24432/C51W2X

UCI dataset page: https://archive.ics.uci.edu/dataset/327/phishing

---

**Student:** Dhruv  
**Programme:** IBM SkillsBuild Cyber Security BootCamp 2026  
**Conducted by:** BharatCares

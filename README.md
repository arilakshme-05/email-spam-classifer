# Email Spam Classifier

A machine learning application built in Python that automatically detects whether an incoming message is **Spam** or **Ham** (legitimate). This project uses Natural Language Processing (NLP) techniques to transform text into numerical data and classifies it using the Naive Bayes algorithm.

---

##  Features

* **Text Vectorization:** Uses `TfidfVectorizer` to convert raw text into a matrix of TF-IDF features.
* **Automatic Stop-Word Removal:** Filters out common English words (like *"the"*, *"a"*, *"is"*) that do not add predictive value.
* **Binary Classification:** Categorizes messages into two classes: `0` (Ham) and `1` (Spam).
* **Performance Metrics:** Provides Accuracy Score and a detailed Classification Report (Precision, Recall, F1-Score).

---

##  Technologies Used

* **Language:** Python 3
* **Libraries:**
  * `pandas` – Data manipulation and analysis
  * `scikit-learn` – Feature extraction, machine learning modeling, and evaluation
* **Environment:** Google Colab / Jupyter Notebook

---

##  Dataset Structure

The model expects a dataset (`.csv` or `.tsv`) with the following columns:

| Column | Description |
| :--- | :--- |
| `label` | The category of the message (`ham` or `spam`) |
| `message` | The actual text content of the email or SMS |

---

##  How It Works

1. **Data Loading:** The dataset is loaded into a Pandas DataFrame.
2. **Label Encoding:** Categorical labels (`ham`, `spam`) are mapped to numerical values (`0`, `1`).
3. **Data Splitting:** The dataset is split into Training (80%) and Testing (20%) sets.
4. **Feature Extraction:** `TfidfVectorizer` calculates the importance of words across the dataset.
5. **Model Training:** The `MultinomialNB` (Multinomial Naive Bayes) classifier learns word probabilities for spam vs. ham.
6. **Evaluation:** The model is tested against unseen data to measure reliability.

---

##  Results

The classifier evaluates model performance using:
* **Accuracy Score:** Percentage of total correct predictions.
* **Precision & Recall:** Detailed breakdown showing how accurately the model flags spam vs. ham messages without false positives.

---

##  How to Run

1. Clone the repository:
   git clone [https://github.com/arilakshme-05/email-spam-classifier.git](https://github.com/arilakshme-05/email-spam-classifier.git)
   cd email-spam-classifier

2.Install required dependencies:
pip install pandas scikit-learn

3.Run in environment:
Open and execute the notebook in Google Colab or Jupyter Notebook.



---

# Mental Health Analysis  

This project analyzes users' mental health by processing their social media activity from Reddit and Twitter. It predicts potential mental health disorders using machine learning models.  

## Features  
- Scrapes user posts from **Reddit** and **Twitter** using `snscrape`.  
- Preprocesses text using **NLTK** (stopword removal, lemmatization, and tokenization).  
- Uses **TF-IDF vectorization** to transform text into feature vectors.  
- Loads trained machine learning models (`.sav` files) to predict disorders:  
  - Anxiety  
  - Depression  
  - Borderline Personality Disorder (BPD)  
  - Eating Disorders  
  - Post-Traumatic Stress Disorder (PTSD)  
- Provides a **Streamlit-based** web interface for user input and result visualization.  

## Installation  

1. Clone the repository:  
   ```sh
   git clone https://github.com/mental_health_analysis/mental-health-analysis.git
   cd mental-health-analysis
   ```  
2. Install dependencies:  
   ```sh
   pip install -r requirements.txt
   ```  
3. Download NLTK resources (if not downloaded automatically):  
   ```python
   import nltk
   nltk.download(["stopwords", "wordnet", "punkt"])
   ```  

## Usage  

Run the Streamlit app:  
```sh
streamlit run Predict.py
```  

Enter a **Twitter** or **Reddit** username and click "Predict Mental State" to get the analysis results.  



## Dependencies  

- `snscrape` (for social media scraping)  
- `NLTK` (for text preprocessing)  
- `pandas` (for data manipulation)  
- `scikit-learn` (for vectorization and model loading)  
- `joblib` & `pickle` (for loading models)  
- `Streamlit` (for UI)  

## Notes  

- Ensure `snscrape` is installed and working before running the script.  
- Usernames must be **publicly accessible** for scraping.  
- Results show **predicted probability** for each disorder (values > 0.5 indicate likely presence).  

## Future Improvements  

- Enhance accuracy with **deep learning models** (BERT, LSTM).  
- Implement **real-time sentiment analysis**.  
- Expand dataset for better generalization.  


# **Pre-Processing and Bias Mitigation for Reddit Comments**

This project automates **data preprocessing** and **bias detection** in Reddit comments, with a particular focus on **gender-related bias**. The solution extracts relevant phrases, identifies stereotypical and non-stereotypical attributes, and uses **NLP models** to annotate comments and phrases for bias and sarcasm. The annotated dataset is useful for bias analysis and bias mitigation tasks.

---

## **Folder Structure**

Pre-Processing-Bias-Mitigation-Reddit/
Data:
- reddit_comments_gender_female_processed_phrase.csv
- reddit_comments_gender_female_processed_phrase_annotated.csv
- reddit_comments_gender_male_processed.csv

DataSetPreparation:
- data_set_creation_and_processing.ipynb

README.md

---

## **Key Features**

1. **Data Preprocessing**:
   - Cleans and processes Reddit comments to prepare them for bias analysis.
   - Filters comments based on content length and removes unnecessary characters.

2. **Phrase Extraction**:
   - Extracts phrases containing **target group terms** (e.g., "woman", "she", "mother") and **attributes**:
     - **Stereotypical** (e.g., "nurse", "housekeeper").
     - **Non-stereotypical** (e.g., "engineer", "physician").

3. **Bias and Sarcasm Detection**:
   - Uses **HuggingFace Transformers** for intelligent annotation:
     - **Sarcasm Detection**: `distilbert-base-uncased-finetuned-sst-2-english`
     - **Bias Detection**: `unitary/toxic-bert`
   - Adds two new columns to the dataset:
     - `bias_sent`: Binary flag (`1` for biased, `0` for unbiased) for the full sentence.
     - `bias_phrase`: Binary flag for the extracted phrase.

4. **Output**:
   - Annotated CSV file with comments and extracted phrases labeled for bias and sarcasm.

---



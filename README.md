
# 📚 Amazon Customer Review Analysis

## 🎯 Project Title
**Data Pipeline for Amazon Customer Review Analysis**

## 📝 Project Description
This project analyzes Amazon customer reviews by creating a complete ETL (Extract, Transform, Load) pipeline. The dataset contains product reviews in **Parquet** format stored on AWS S3. The goal is to clean, transform, and load the data into a remote SQL database (TiDB or equivalent) and perform SQL-based analytical queries to generate meaningful insights.

## 🗂️ Project Structure
```
📁 Amazon-Customer-Review-Analysis
├── 📄 etl_pipeline.py       # Main ETL script
├── 📄 amazon_review_queries.txt  # SQL queries for analysis
├── 📄 requirements.txt      # Required Python packages
└── 📄 README.md             # Project documentation
```

## 🚀 Key Tasks

### 1. Data Extraction
- Extract data from AWS S3 (Parquet format).
- Load the dataset into a Pandas DataFrame.

### 2. Data Cleaning and Preprocessing
- Remove duplicates.
- Handle missing/null values.
- Correct data types (e.g., dates, integers).
- Standardize text fields.

### 3. Data Transformation
- Convert `review_date` to `YYYY-MM-DD` format.
- Normalize text fields like `review_body` and `review_headline`.
- Create additional columns (e.g., `review_month`).

### 4. Load Data into Remote SQL Database
- Create the database schema.
- Load the transformed data into TiDB or SQLite.
- Ensure indexing on frequently queried columns.

## 📊 SQL Queries for Analysis
The following queries analyze the dataset:
- **Top 10 Products with the Most Reviews**
- **Average Review Ratings Per Month for Each Product**
- **Total Number of Votes Per Product Category**
- **Products with the Word "Awful" in Reviews**
- **Products with the Word "Awesome" in Reviews**
- **Most Controversial Reviews**
- **Most Commonly Reviewed Product Per Year**
- **Users Who Wrote the Most Reviews**

👉 SQL queries are stored in: `amazon_review_queries.txt`.

## ⚙️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/amazon-review-analysis.git
cd amazon-review-analysis
```

### 2. Set Up a Virtual Environment
```bash
# Create virtual environment
python3 -m venv venv

# Activate the environment
# For Windows
venv\Scripts\activate
# For macOS/Linux
source venv/bin/activate
```

### 3. Install Required Packages
```bash
pip install -r requirements.txt
```

## 📡 ETL Pipeline Usage

### Run the Main ETL Script:
```bash
python etl_pipeline.py
```

## 📄 SQL Queries Usage
You can execute the queries from `amazon_review_queries.txt` on your SQL database using any SQL client or via Python using `sqlite3` or `TiDB`.

## 🛠️ Technologies Used
- **Python**: For ETL processing and data analysis.
- **Pandas**: For data manipulation.
- **SQLite / TiDB**: For storing and querying the data.
- **AWS S3**: For data storage.
- **SQL**: For analytical queries.

## 🎉 Contributing
Feel free to submit a pull request with any improvements, bug fixes, or additional features!

## 📧 Contact
For questions or collaboration, reach out to:
- 📩 **Email:** your-email@example.com  
- 🔗 **GitHub:** [your-username](https://github.com/your-username)

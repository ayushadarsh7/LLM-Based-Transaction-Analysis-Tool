# LLM based Tool for Bank Transaction Analysis

---

## Key Functionalities

1. **Data Loading and Preprocessing**:
   - Upload Excel files containing transaction data.
   - Automatically detect columns based on headers like **Date**, **Debit**, **Credit**, **Transaction Description**.
   - Clean and preprocess the data for easy analysis.

2. **Transaction Summary**:
   - Generate a comprehensive summary of the entire dataset, including:
     - Total credits (sum of credit transactions).
     - Total debits (sum of debit transactions).
     - The date range for the transactions.
     - A list of the 10 most frequent transaction descriptions and keywords.

3. **Suspicious Activity Detection**:
   - Identify suspicious transactions based on defined criteria, such as abnormal transaction amounts or repetitive transactions.
   - Highlight transactions potentially related to illegal activities like fraud or money laundering.

4. **Hypothesis Generation**:
   - Based on detected patterns, generate potential hypotheses for financial crimes such as **Money Laundering** or **Terrorism Financing**.

5. **Entity Extraction from Transaction Descriptions**:
   - Extract important entities like people, companies, and locations from transaction descriptions using Natural Language Processing (NLP) techniques.

6. **Adverse Content Detection**:
   - Scan transaction descriptions to identify any potentially harmful content or keywords indicative of illegal activity.

7. **Transaction Category Analysis**:
   - Categorize and classify transactions (e.g., deposits, withdrawals, wire transfers) to understand transaction behavior better.

---

## Setup and Installation

To use the AI Intelligence Analyst Tool, follow these steps:

### Prerequisites
- **Python 3.7 or higher**.
- **Required Dependencies** (listed in the `requirements.txt` file).
- An OpenAI API key

### Installation Steps

1. **Clone the Repository**:
   ```bash
   git clone <repository_url>
   cd <repository_folder>
   import sys
   sys.path.append('/content') # # Add the path to your directory
   ```

2. **Install Dependencies**:
   Use `pip` to install all the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up OpenAI API Key** (optional):
   - The tool uses the OpenAI API for advanced functionality (such as entity extraction and suspicious pattern detection). To get an API key, sign up at [OpenAI](https://www.openai.com/).
   - Create a `.env` file in the project root, and add your API key:
     ```
     OPENAI_API_KEY=your_openai_api_key_here
     ```

4. **Launch Jupyter Notebook**:
   - To begin using the AI Intelligence Analyst Tool, run the following command:
     ```bash
     jupyter notebook
     ```
   - Open the Jupyter Notebook file (`Transaction_Analysis.ipynb`) .

---

## How to Use

1. **Upload Your Excel File**:
   - The Excel file should have the following columns:
     - **Date** (the date of the transaction).
     - **Debit** (the amount debited).
     - **Credit** (the amount credited).
     - **Transaction Description** (details of the transaction).
   - The tool expects an Excel file with a similar format:
     Transaction| Date       | Description    |Debit     | Credit | Balance
     -----------|------------|----------------|----------|--------|--------|
         101    | 2024-01-01 | Cash withdrawal| 500.00   | 0.00   | 1000   |
         102    | 2024-01-02 | Wire Transfer  | 0.00     | 200.00 | 1200   |

2. **Run the Cells**:
   - Go through each cell in the notebook. Cells are organized step-by-step to help you load data, analyze it, and extract valuable insights. Follow the instructions inside each cell to proceed.
   - The notebook automatically detects the uploaded Excel file and preprocesses it for analysis.

3. **Transaction Summary**:
   - After processing the data, the tool will display a summary including:
     - Total **credits**.
     - Total **debits**.
     - The date range of the transactions.
     - Most common **transaction descriptions**.

4. **Suspicious Activity Detection**:
   - The notebook flags potentially suspicious transactions based on factors such as:
     - High-value transactions.
     - Frequent occurrence of the same transaction type or description.
     - Unusual patterns indicating potentially illegal activity.

5. **View Results**:
   - After running the analysis, you can view the results directly within the notebook or export them into a new Excel file for reporting purposes.
   - Some outputs include:
     - A breakdown of **debit/credit** amounts and descriptions.
     - Flagged **suspicious activities**.
     - Extracted entities (e.g., company names or locations) from transaction descriptions.

---

## Outputs and Results

1. **Transaction Overview**:
   A summary of the overall transaction dataset.
   Example:
   ```
   Total Debits: $50,000
   Total Credits: $75,000
   Date Range: 01/01/2024 to 12/31/2024
   ```

2. **Top 10 Most Frequent Transactions**:
   Example:
   ```
   1. Wire Transfer XYZ (10 occurrences)
   2. Cash Withdrawal (8 occurrences)
   3. ATM Withdrawal (5 occurrences)
   ...
   ```

3. **Suspicious Activity Alerts**:
   - Identifies any transactions that could be signs of **money laundering** or other illegal activities.

4. **Entity Extraction**:
   Example of output:
   ```
   Extracted Entities:
   - Person: John Doe, Jane Smith
   - Company: Acme Corp
   - Location: New York
   ```

---

## Contribution

To contribute to this project:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -am 'Add new feature'`).
4. Push your changes (`git push origin feature-branch`).
5. Submit a pull request with details of your changes.




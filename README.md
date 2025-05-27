# Financial Insights Chatbot

This repository contains the code for a basic AI-powered financial chatbot, developed as part of the [Boston Consulting Group (BCG) Forage Generative AI Virtual Internship on Forage.com](https://www.theforage.com/simulations/bcg/gen-ai-anlo), focusing on providing financial insights for select major companies. The chatbot leverages historical financial data to answer predefined queries and offers a glimpse into the potential of AI in financial analysis.

## Project Overview

The core objective of this project was to create a simplified chatbot prototype that can respond to specific financial queries using rule-based logic. This serves as an introductory step into AI chatbot development, highlighting fundamental concepts without requiring extensive deep learning expertise.

The project is divided into two main tasks:

* **Task 1: Data Extraction and Initial Analysis:** Involved manually extracting financial data from the latest 10-K annual reports of Microsoft, Tesla, and Apple from the SEC EDGAR database. Key financial metrics (Total Revenue, Net Income, Total Assets, Total Liabilities, and Cash Flow from Operating Activities) were collected for Fiscal Years 2022, 2023, and 2024. This data was then cleaned, converted to appropriate numeric types, and year-over-year growth rates were calculated.
* **Task 2: Developing an AI-powered Financial Chatbot:** Focused on building a rule-based chatbot prototype that interacts with the user via a command-line interface. The chatbot is designed to understand specific queries about the financial performance of the companies analysed in Task 1.

## Chatbot Functionality

The chatbot operates on a rule-based logic, identifying keywords and patterns in user queries to provide relevant financial information.

### Key Features:

* **Company Identification:** Automatically detects the company (Microsoft, Tesla, or Apple) the user is asking about.
* **Metric & Growth Identification:** Recognises queries related to specific financial metrics (e.g., "total revenue", "net income", "cash flow") and their year-over-year growth rates (e.g., "revenue growth", "net income growth").
* **Year Specificity:** Can provide data for specific fiscal years (2022, 2023, 2024) if mentioned in the query. If a year is requested but not found, it defaults to the latest available data.
* **General Summaries:** Can provide a comprehensive summary of a company's financial performance for a given year.
* **Interactive Suggestions:** Offers relevant follow-up questions to guide the user in exploring more financial data.

### Supported Queries & Examples:

The chatbot is designed to respond to predefined financial queries. Here are some examples of what you can ask:

* `What is the total revenue of Microsoft?`
* `What is the net income of Microsoft in 2022?`
* `What is Apple's revenue growth in 2023?`
* `Summarise Tesla's performance.`
* `What is the summary of Apple's financial health in 2023?`
* `What are Tesla's total assets?`
* `Tell me about Microsoft's cash flow in 2024.`

### Example Interactions:
To give you a clear idea of how to interact with the chatbot, here's what the initial interface looks like when you run the notebook, followed by a series of example conversations:

![Chatbot Initial Welcome](https://github.com/user-attachments/assets/a9435adc-c91c-43ac-ab7e-24d818125738)

Here's what interacting with the chatbot looks like:

![image](https://github.com/user-attachments/assets/619af543-49b4-48da-aa69-a031df4ff287)
![image](https://github.com/user-attachments/assets/678efd27-c9c1-4eb0-ac54-ffd2268cd585)

## How to Run

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/belle-kochapon/financial_analysis_chatbot.git
    cd financial_analysis_chatbot
    ```
2.  **Ensure you have the necessary files:**
    Make sure `financial_analysis_notebook.ipynb` and `financial_data.csv` are in the same directory.
3.  **Install dependencies:**
    This project primarily uses `pandas`. If you don't have it installed, you can do so via pip:
    ```bash
    pip install pandas
    ```
4.  **Run the Jupyter Notebook:**
    Open the `financial_analysis_notebook.ipynb` file in Jupyter Notebook or JupyterLab and run all cells. The chatbot interface will appear in the output of the last code cell.

## Limitations

It's important to understand the current limitations of this rule-based chatbot:

* **Strict Keyword Matching:** Relies heavily on exact keyword matches and predefined patterns, limiting its understanding of synonyms or complex natural language.
* **Limited Conversational Context:** Each query is largely treated independently; the chatbot does not maintain deep conversational memory.
* **Fixed Data Scope:** Insights are strictly limited to the provided financial data for Microsoft, Tesla, and Apple for Fiscal Years 2022-2024. It cannot access real-time data or information on other companies.
* **Hardcoded Companies:** The list of supported companies is hardcoded within the logic, making it less flexible to add new companies without code modification.
* **No Advanced AI/ML:** Does not incorporate sophisticated NLP techniques (like intent recognition or entity extraction) or machine learning algorithms for self-improvement.
* **Text-Based Only:** Does not provide visual aids or integrate with external visualisation tools.

## Conclusion

This project successfully demonstrates the application of structured financial data with rule-based natural language processing to create a functional financial inquiry chatbot. While operating within defined rules, it effectively delivers relevant insights, including year-specific data and growth metrics. This foundational understanding equips the chatbot with the intelligence to provide more insightful and actionable financial analysis for the specified companies.

## Files in this Repository

* `financial_analysis_notebook.ipynb`: The Jupyter Notebook containing the data analysis from Task 1 and the chatbot implementation for Task 2.
* `financial_data.csv`: The raw financial data extracted from 10-K annual reports.
* `README.md`: This file, providing an overview of the project.

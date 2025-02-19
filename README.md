# SEC-Filings-using-pyspark-and-neo4jHere

#### **Introduction**
The **SEC Filings Project** leverages financial data from the U.S. Securities and Exchange Commission (SEC) to analyze corporate financial health, identify anomalies, and derive insights from structured financial reports.

This project processes **quarterly and annual financial statements** submitted by public companies using **eXtensible Business Reporting Language (XBRL)**. The dataset is sourced from SEC’s EDGAR system and includes details on **balance sheets, income statements, cash flow statements, changes in equity, and comprehensive income reports**.

#### **Key Features**
- **Data Processing & Cleaning**:
  - Convert **.txt** financial data into structured **.csv** and **.parquet** files.
  - Handle **missing values**, **date format conversions**, and **duplicate removal**.
  - Standardize financial data for analysis.

- **Data Storage & Management**:
  - Store and query data efficiently using **Neo4j Aura**.
  - Establish connections between companies, financial records, and executives.

- **Financial Analysis**:
  - **Comparative financial analysis** of companies based on revenue, assets, and liabilities.
  - **Clustering analysis** of firms based on financial health (Revenue vs. Debt-to-Revenue Ratio).
  - **Anomaly detection** to identify unusual financial reporting patterns.
  - **Graph-based analysis** to uncover executive networks and corporate board memberships.

- **GraphRAG for Financial Queries**:
  - Use **OpenAI API** to convert natural language queries into **Cypher queries** for Neo4j.
  - Generate **AI-powered financial reports** from structured financial data.

#### **Setup Instructions**
1. **Clone or Download the Project**
   ```bash
   git clone https://github.com/your-repo/Financial-Analysis-Project.git
   cd Financial-Analysis-Project
   ```

2. **Install Required Packages**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up Google Drive (Colab Users)**
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

4. **Configure `.env` File (For Neo4j and OpenAI API)**
   - Create a `.env` file in the project directory and add:
     ```
     NEO4J_URI=bolt://your-neo4j-uri
     NEO4J_USERNAME=neo4j
     NEO4J_PASSWORD=your-password
     OPENAI_API_KEY=your-api-key
     ```

5. **Run the Main Script**
   ```python
   python main.py
   ```

#### **Usage**
- **Financial Data Processing**: Convert SEC data files into structured CSV/Parquet formats.
- **Graph Database Integration**: Upload financial data into Neo4j for querying.
- **Financial Querying**: Use OpenAI to convert English queries into Cypher queries.
- **Clustering & Visualization**: Analyze corporate financial health.
- **Anomaly Detection**: Identify financial misreporting.

#### **References**
- **SEC Data Documentation**: [https://www.sec.gov/files/aqfs.pdf](https://www.sec.gov/files/aqfs.pdf)
- **EDGAR Filings**: [https://www.sec.gov/edgar.shtml](https://www.sec.gov/edgar.shtml)
- **Neo4j Documentation**: [https://neo4j.com/docs/](https://neo4j.com/docs/)

---

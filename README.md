
# 🤖 AI Data Analytics Agent

An **AI-powered Data Analytics Agent** built using **n8n, OpenAI, Google Sheets, and Gmail** that allows users to analyze sales data using natural-language questions.

The goal of this project is to demonstrate how an AI Agent can connect with business data, understand user questions, retrieve relevant data, generate analytical insights, and automate reporting.

---

## 📌 Project Overview

Traditional data analysis often requires users to manually filter spreadsheets, create calculations, or write queries to answer business questions.

This project provides a conversational approach to sales analytics.

Users can simply ask questions such as:

* What are the total sales?
* Which product category has the highest sales?
* Which country generated the highest sales?
* What are the sales by year?
* Give me a summary of the sales data.

The AI Agent interprets the question, retrieves the required information from the sales dataset, analyzes the data, and provides a business-friendly response.

---

## 🏗️ Workflow Architecture

```text
                    USER
                      │
                      ▼
             ┌──────────────────┐
             │  n8n Chat Trigger │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │     AI Agent     │
             └────────┬─────────┘
                      │
        ┌─────────────┼─────────────┐
        │             │             │
        ▼             ▼             ▼
   OpenAI Model   Simple Memory  Google Sheets
                                    │
                                    ▼
                              Sales Dataset
                                    │
                                    ▼
                              Data Analysis
                                    │
                                    ▼
                            Business Insights
                                    │
                                    ▼
                                  Gmail
```

---

## 🛠️ Technologies Used

* **n8n** – Workflow automation and AI Agent orchestration
* **OpenAI** – Natural-language understanding and analysis
* **Google Sheets** – Sales data source
* **Gmail** – Automated report delivery
* **AI Agent** – Business question interpretation and tool selection
* **Simple Memory** – Maintains conversational context

## The workflow uses an OpenAI chat model, memory, Google Sheets as an AI tool, and Gmail as an additional AI tool.

## 📊 Dataset

The project uses a **sales dataset** containing business sales information.

The dataset is used as the source for answering analytical questions through the AI Agent.

For the n8n implementation, the sales data is accessed through **Google Sheets**.

### Example analytical areas

* Sales performance
* Product analysis
* Customer analysis
* Country/region analysis
* Quantity analysis
* Order analysis
* Year and quarter analysis

---

## 💬 Example Questions

The user can interact with the agent using natural language.

```text
What are the total sales?

Which product has the highest sales?

Which country has the highest sales?

Show me sales by product category.

What is the sales performance by year?

Give me a summary of the sales data.

Analyze the sales data and provide key insights.
```

---

## ⚙️ How the Workflow Works

### Step 1 — User Question

The user enters a question through the n8n chat interface.

```text
"What are the total sales?"
```

### Step 2 — AI Agent

The AI Agent understands the user's question and determines what information is required.

### Step 3 — Retrieve Data

The Agent uses the Google Sheets tool to retrieve the required sales data.

### Step 4 — Analyze Data

The OpenAI model processes the retrieved information and generates an understandable analytical response.

### Step 5 — Conversation Memory

Simple Memory allows the Agent to maintain context across the conversation.

### Step 6 — Automated Reporting

If the user requests a report, the Agent can generate a structured HTML email and send it using Gmail.

---

## 📧 Automated Email Reporting

The Agent can also send analytical results through Gmail.

Example request:

```text
Email me a summary of the sales analysis.
```

The Agent retrieves the required data, analyzes it, creates a structured report, and sends the result through the configured Gmail tool.

---

## 🔐 Security

**Credentials are not included in this repository.**

If you import this workflow into your own n8n instance, you need to configure your own:

* OpenAI credentials
* Google Sheets credentials
* Gmail credentials

Do not upload:

* API keys
* Passwords
* OAuth tokens
* Private Google Sheet links
* Personal email information
* Other sensitive credentials

---

## 📂 Project Structure

```text
AI-Data-Analytics-Agent/
│
├── README.md
│
├── workflow/
│   └── AI-Data-Analytics-Agent.json
│
├── data/
│   └── Sales_Data_Sample.xlsx
│
└── screenshots/
    └── n8n-workflow.png
```

---

## 🚀 How to Use

### 1. Install / open n8n

Create or open an n8n workspace.

### 2. Import the workflow

Import:

```text
AI Agent Data Analytics Agent.json
```

### 3. Configure credentials

Connect your own:

```text
OpenAI
Google Sheets
Gmail
```

### 4. Configure the sales dataset

Connect your own sales dataset through Google Sheets.

### 5. Start the workflow

Open the n8n chat interface and ask a business question about the sales data.

---

## 💡 Business Use Cases

This type of AI-powered analytics workflow can help businesses:

* Quickly explore sales data
* Answer repetitive business questions
* Automate basic sales reporting
* Reduce manual spreadsheet analysis
* Generate business insights using natural language
* Automate email-based reporting

---

## 🔮 Future Improvements

Planned improvements include:

* SQL database integration
* Power BI dashboard integration
* Automated KPI reporting
* Sales forecasting
* Anomaly detection
* Scheduled reports
* Multiple data-source integration
* Advanced business performance analysis

---

## 🎯 Skills Demonstrated

This project demonstrates practical experience with:

**Data Analytics**

* Sales Analysis
* Business Analysis
* Data Interpretation
* KPI Analysis
* Business Insights

**AI & Automation**

* AI Agents
* Prompt Engineering
* Natural Language Data Analysis
* Workflow Automation

**Tools & Technologies**

* n8n
* OpenAI
* Google Sheets
* Gmail

---

## 👩‍💻 Author

### Nandini Wadile

**Data Analytics | Business Analytics | Power BI**

GitHub: **Nandiniwadile**

LinkedIn: **Nandini Wadile**

---

⭐ If you find this project useful, feel free to explore the workflow and adapt it for your own analytics use cases.

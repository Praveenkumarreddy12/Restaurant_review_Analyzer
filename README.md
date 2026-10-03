# Restaurant_review_Analyzer
A Generative AI application that analyzes restaurant reviews using Large Language Models (LLMs). The application extracts meaningful insights from customer reviews, identifies sentiment, summarizes feedback, and helps understand overall customer satisfaction.



# 🍽️ Restaurant Review Analyzer

A Generative AI application that analyzes restaurant and food reviews using a locally running Large Language Model (LLM).

The application uses **Streamlit** for the user interface, **Python** for the application logic, and **Ollama with Qwen2.5:3b** to analyze reviews and generate meaningful insights.

## 🚀 Features

* 📝 Enter restaurant or food reviews
* 🤖 Analyze reviews using Generative AI
* 😊 Identify the sentiment of the review
* 📋 Generate a concise review summary
* 🔍 Extract important points from customer feedback
* 💻 Simple and interactive Streamlit interface
* 🔒 Runs the LLM locally using Ollama

## 🛠️ Technologies Used

* **Python**
* **Streamlit**
* **Ollama**
* **Qwen2.5:3b**
* **Generative AI**
* **Natural Language Processing (NLP)**

## 🏗️ Project Architecture

```text
                 User
                  │
                  ▼
          ┌───────────────┐
          │   Streamlit   │
          │      UI       │
          └───────┬───────┘
                  │
                  ▼
          ┌───────────────┐
          │    Python     │
          │ Application   │
          └───────┬───────┘
                  │
                  ▼
          ┌───────────────┐
          │    Ollama     │
          └───────┬───────┘
                  │
                  ▼
          ┌───────────────┐
          │  Qwen2.5:3b   │
          │     LLM       │
          └───────┬───────┘
                  │
                  ▼
        Review Analysis & Insights
```

## 📁 Project Structure

```text
Restaurant_review_Analyzer/
│
├── app.py
├── requirements.txt
├── README.md
└── .gitignore
```

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
```

```bash
cd Restaurant_review_Analyzer
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

### 3. Activate the virtual environment

**Windows:**

```powershell
venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

If you have not created `requirements.txt` yet:

```bash
pip install streamlit ollama
```

Then generate it:

```bash
pip freeze > requirements.txt
```

## 🤖 Ollama Setup

Install Ollama on your system and download the Qwen2.5 3B model.

```bash
ollama pull qwen2.5:3b
```

Check that the model is available:

```bash
ollama list
```

You should see:

```text
qwen2.5:3b
```

You can also test the model directly:

```bash
ollama run qwen2.5:3b
```

## ▶️ Run the Application

Start the Streamlit application:

```bash
streamlit run app.py
```

Streamlit will provide a local URL in the terminal. Open that URL in your browser.

## 💡 Example

### Input

```text
The food was cold and tasteless. The service was extremely slow
and the staff were not very helpful.
```

### Possible Analysis

```text
Sentiment: Negative

Summary:
The customer was unhappy with the cold food, slow service,
and unhelpful staff.

Key Issues:
- Cold food
- Slow service
- Poor customer service
```

## 🔄 How It Works

1. The user enters a restaurant review in the Streamlit interface.
2. The review is sent to the Python application.
3. Python sends the review to the local Ollama server.
4. Ollama processes the review using the `qwen2.5:3b` model.
5. The model analyzes the review.
6. The generated analysis is displayed in the Streamlit interface.

## 🔐 Local AI

This project uses **Ollama** to run the Qwen2.5:3b model locally.

The review is processed by the locally running model rather than requiring a cloud LLM API key.

## 🎯 Purpose of the Project

This is my **first Generative AI application**, created to understand the fundamentals of building an AI-powered application using:

* LLMs
* Prompt Engineering
* Ollama
* Local AI models
* Python
* Streamlit
* NLP-based text analysis

## 🔮 Future Improvements

* Add review history
* Analyze multiple reviews at once
* Generate overall restaurant ratings
* Extract common complaints
* Add charts for sentiment analysis
* Support CSV file uploads
* Add positive/negative aspect extraction
* Add multilingual review analysis

## 👨‍💻 Author

**Praveen Reddy**

---

⭐ If you find this project useful, feel free to explore and improve it.



## 📌 Project Note :

> **This is a basic learning-focused Generative AI application developed to understand the fundamentals of working with LLMs, Ollama, prompt engineering, and Streamlit.**

In the current version, the application does **not directly fetch restaurant reviews from external APIs or websites**. Instead, users can **paste the complete restaurant reviews into the application**, and the system processes the provided text using the **Qwen2.5:3b** model running locally through **Ollama**.

### 🔄 Current Workflow

```text
User
  ↓
Paste Restaurant Reviews
  ↓
Streamlit Application
  ↓
Python
  ↓
Ollama
  ↓
Qwen2.5:3b
  ↓
Review Analysis
  ↓
Results
```

The application takes the manually provided reviews and performs the analysis, such as identifying sentiment, summarizing customer feedback, and extracting important insights.

### 🚀 Future Development

This project is being developed step by step as a learning project. In future versions, the application will be extended to **automatically collect restaurant reviews through external APIs** instead of requiring users to manually paste the reviews.

The planned workflow is:

```text
Restaurant Review API
        ↓
Fetch Reviews Automatically
        ↓
Python Processing
        ↓
Ollama + Qwen2.5:3b
        ↓
AI Analysis
        ↓
Sentiment / Summary / Insights
        ↓
Streamlit Dashboard
```

Future versions may also include:

* 🔗 Integration with restaurant/review APIs
* 📥 Automatic review collection
* 📊 Analysis of large numbers of reviews
* 📈 Sentiment and review analytics
* 🔍 Common complaint and feedback extraction
* 📋 Restaurant-level summaries
* 📊 Interactive dashboards and visualizations

### 🎯 Learning Objective

The main goal of the current version is to understand the **end-to-end workflow of a Generative AI application** before introducing external data sources and more advanced functionality.

This project will therefore evolve from a simple **manual-input prototype** into a more complete **API-driven restaurant review analysis system**.

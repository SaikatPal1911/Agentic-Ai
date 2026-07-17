# 📚 Smart Student Study Planner

An AI-powered, interactive study planner application designed to help students organize their studies, query study materials using a local LLM, set and track weekly goals, generate mock tests, and visualize their performance over time. Built with **Python**, **Gradio**, and **Ollama**.

---

## 🌟 Key Features

### 1. 🤖 AI Study Assistant
* **Upload Study Materials:** Supports uploading PDF documents.
* **Context-Aware Q&A:** Ask questions directly about the uploaded PDF material.
* **Local Processing:** Utilizes Ollama and the `llama3.2` model locally to answer questions, ensuring data privacy and zero API costs.

### 2. 📅 Daily Planner
* **Routine Builder:** Input name, subject, and set target study hours via an interactive slider.
* **Plan Generation:** Generates a structured daily routine (Reading, Note-making, Practice, Revision).
* **Export & Persistence:** Saves the plan to local JSON and exports a legacy `study_plan.txt` file for quick reference.

### 3. 📋 Weekly Goals & Progress
* **Interactive Goal Grid:** Add, update, and manage weekly goals with estimated hours.
* **Inline Editing:** Edit "Actual Hours" and "Completed" status directly in the interactive data grid.
* **Matplotlib Visualizations:** Generates and displays a progress chart comparing estimated hours vs. actual study hours.
* **Weekly Performance Summary:** Displays automated textual summaries of weekly study stats.

### 4. 📝 Mock Test Generator
* **Multiple Sources:** Generate mock tests based on either custom text topics (e.g., *Physics - Thermodynamics*) or uploaded PDF content.
* **Dynamic AI Test Generation:** Ollama generates multiple-choice questions (MCQs) with options.
* **Interactive Quiz Flow:** Answer questions step-by-step with immediate feedback, progress indicators, and total scoring.

### 5. 📊 Performance Dashboard
* **Metrics Summary:** Displays key statistics such as total tests attempted, average score, and highest score.
* **Performance Charts:** Generates visualizations showing test score trends over successive attempts.
* **Attempt History:** Interactive logs showing previous test subjects, dates, scores, and percentage success rates.

---

## 📂 Project Directory Structure

```text
├── app.py                      # Main Gradio application code (UI & logic)
├── study_planner_data.json     # Local JSON database for persistent storage (goals, attempts, etc.)
├── study_plan.txt              # Exported daily plan text file
├── weekly_progress_chart.png   # Generated visualization for weekly goal progress
├── performance_dashboard.png   # Generated visualization for mock test scores
└── README.md                   # Project documentation (this file)
```

---

## ⚙️ Prerequisites

Before running the application, make sure you have the following installed:

1. **Python 3.8+**
2. **Ollama** (for AI features):
   * Download and install Ollama from [ollama.com](https://ollama.com/).
   * Pull the `llama3.2` model locally by running the following command in your terminal:
     ```bash
     ollama pull llama3.2
     ```

---

## 🚀 Installation & Setup

1. **Clone or copy this project directory** to your local machine.
2. **Install the required Python packages** by running:
   ```bash
   pip install gradio pypdf ollama matplotlib pandas
   ```
3. **Start the Ollama application** on your system.
4. **Run the planner app**:
   ```bash
   python app.py
   ```
5. Open the local web address displayed in the terminal (usually `http://127.0.0.1:7860`) in your web browser.

---

## 🛠️ Technology Stack

* **UI Framework:** [Gradio](https://www.gradio.app/) - for creating a beautiful and responsive web application dashboard.
* **Local LLM Orchestration:** [Ollama Python SDK](https://github.com/ollama/ollama-python) - connected to the local `llama3.2` model.
* **Data Processing:** [Pandas](https://pandas.pydata.org/) & Standard `json` module.
* **Visualizations:** [Matplotlib](https://matplotlib.org/) - for plotting study progress and test performance.
* **PDF Reader:** [pypdf](https://github.com/py-pdf/pypdf) - for extracting text from study documents.

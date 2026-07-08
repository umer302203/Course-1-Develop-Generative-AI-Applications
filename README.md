# 🧠 Course 1 – Develop Generative AI Applications

[![Python](https://img.shields.io/badge/Python-3.11%2B-blue)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org/)
[![LangChain](https://img.shields.io/badge/LangChain-1.3.11-green)](https://www.langchain.com/)
[![IBM watsonx](https://img.shields.io/badge/IBM-watsonx.ai-052FAD)](https://www.ibm.com/watsonx)
[![Flask](https://img.shields.io/badge/Flask-3.1.3-black)](https://flask.palletsprojects.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This repository contains the complete set of labs and the final project for the **IBM Skills Network course: "Develop Generative AI Applications"** (Course 1).  
It guides you through the fundamental concepts of prompt engineering, LangChain orchestration, and building a production‑ready AI‑powered web application.

---

## 📖 Course Overview

The course is structured into **three progressive labs**:

| Lab | Topic | Key Skills |
| :--- | :--- | :--- |
| **Lab 1** | *In‑Context Learning and Prompt Templates for Advanced AI* | Basic/zero‑shot/one‑shot/few‑shot prompting, chain‑of‑thought, self‑consistency, and LangChain `PromptTemplate`. |
| **Lab 2** | *Build Smarter AI Apps: Empower LLMs with LangChain* | LangChain core concepts: models, parsers, document loaders, vector stores, memory, chains (traditional & LCEL), tools & agents. |
| **Lab 3 (Project)** | *Multi‑Model AI Assistant Web Application* | Flask backend, integration of Llama/Granite/Mistral via watsonx.ai, structured JSON responses, glassmorphism UI. |

---

## 🗂️ Repository Structure

```
Course-1-Develop-Generative-AI-Applications/
├── Lab 1 – In-Context Learning and Prompt Templates for Advanced AI.ipynb
├── Lab 2 – Build Smarter AI Apps Empower LLMs with LangChain.ipynb
├── Lab 3 (Project)/
│   ├── app.py
│   ├── model.py
│   ├── config.py
│   ├── llm_test.py
│   ├── requirements.txt
│   ├── .gitignore
│   ├── templates/
│   │   └── index.html          (self‑contained glassmorphism UI)
│   ├── static/
│   │   ├── script.js
│   │   └── styles.css
│   └── demo.mp4                (optional demo video)
└── README.md
```

> **Note:** The project folder contains a fully functional Flask app that you can run locally or in the IBM Skills Network Cloud IDE.

---

## 🎯 Learning Outcomes

By completing this course, you will be able to:

- **Master prompt engineering** – from basic instructions to advanced in‑context learning (zero/one/few‑shot, CoT, self‑consistency).
- **Leverage LangChain** – use its modular components: models, prompt templates, output parsers, document loaders, splitters, vector stores, retrievers, memory, chains, and agents.
- **Build a GenAI web application** – integrate multiple LLMs via Flask, enforce structured JSON outputs with Pydantic, and design a modern glassmorphism front‑end.
- **Compare different models** – evaluate responses from Llama, Granite, and Mistral for various tasks.
- **Deploy in a cloud environment** – run your app instantly in IBM Skills Network's pre‑configured environment.

---

## 🚀 Getting Started

### Prerequisites
- Python 3.11 or higher.
- An IBM Cloud account with watsonx.ai access (or use the free Skills Network lab environment).
- Basic knowledge of Python and Jupyter notebooks.

### Cloning the Repository
```bash
git clone https://github.com/your-username/Course-1-Develop-Generative-AI-Applications.git
cd Course-1-Develop-Generative-AI-Applications
```

### Running the Jupyter Notebooks (Lab 1 & Lab 2)
1. Launch Jupyter Lab or Notebook in your environment.
2. Open either notebook and run all cells sequentially.
3. The notebooks are self‑contained and will install required dependencies (if you are in Skills Network, the environment is already set up).

> **Note:** If running locally, you need to configure your own IBM watsonx API key. The labs use the `skills-network` project ID, which works only in the Skills Network environment. For local use, update the `project_id` and add your API key in the credential sections.

### Running the Flask Application (Lab 3 – Project)
1. Navigate to the project folder:
   ```bash
   cd "Lab 3 (Project)"
   ```
2. Create and activate a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. (If running locally) create a `.env` file with your watsonx credentials:
   ```env
   WATSONX_API_KEY=your_ibm_api_key
   WATSONX_PROJECT_ID=your_project_id
   ```
   and update `model.py` to read these environment variables (see the README inside the project folder for details).
5. Run the Flask app:
   ```bash
   python app.py
   ```
6. Open your browser at `http://localhost:5000` (or the proxy URL provided by your cloud IDE).

---

## 🔬 Lab Highlights

### Lab 1 – In‑Context Learning & Prompt Templates
- **Basic prompts** – simple completions.
- **Zero‑shot** – direct instruction without examples.
- **One‑shot & Few‑shot** – providing 1 or more examples to guide the model.
- **Chain‑of‑Thought (CoT)** – step‑by‑step reasoning for arithmetic/logical problems.
- **Self‑consistency** – generating multiple independent solutions and finding the most consistent one.
- **LangChain PromptTemplate** – reusable templates with the LCEL pipeline (`|` operator).

### Lab 2 – Building Smarter AI Apps with LangChain
- **Models & Chat models** – using WatsonxLLM and ChatWatsonx.
- **Output Parsers** – JSON and CSV parsers for structured data.
- **Document handling** – loaders (PDF, Web), splitters (character, recursive), and parent‑document retrieval.
- **Vector stores & Retrievers** – ChromaDB, semantic search, and RAG (Retrieval‑Augmented Generation).
- **Memory** – conversation buffer and summary memory.
- **Chains** – sequential chains (traditional vs. LCEL) for multi‑step workflows.
- **Tools & Agents** – building a ReAct agent that can use a calculator and weather tool.

### Lab 3 – Project: Multi‑Model AI Assistant Web App
- **Flask backend** with endpoints for generating responses.
- **Three model support** – Llama, Granite, Mistral (switchable via UI).
- **Structured JSON output** – enforced by Pydantic + LangChain's `JsonOutputParser`.
- **Sentiment & summarization** – every response includes a sentiment score and a summary.
- **Glassmorphism UI** – self‑contained modern frontend with animations and mobile responsiveness.
- **Error handling & performance metrics** – robust API with response time logging.

---

## 🛠️ Technology Stack

| Layer | Technology |
| :--- | :--- |
| **Notebook Environment** | Jupyter, Python 3.11 |
| **LLM Orchestration** | LangChain (`1.3.11`) + LangChain‑IBM |
| **LLM Provider** | IBM watsonx.ai (Granite, Llama, Mistral) |
| **Backend** | Flask (`3.1.3`) |
| **Data Validation** | Pydantic (`2.5.0`) |
| **Vector Database** | ChromaDB (`0.4.24`) |
| **Frontend** | HTML5, CSS3 (Glassmorphism), Vanilla JS |
| **Deployment** | IBM Skills Network Cloud IDE (or any Python‑hosted environment) |

---

## 🧪 Testing & Validation

- **Notebook exercises** – each lab includes hands‑on exercises with solutions provided.
- **LLM test script** – `llm_test.py` in the project folder runs all three models on a sample prompt to verify integration.
- **API testing** – the Flask app can be tested using `curl` or the built‑in UI.

---

## 🤝 Contributing

Contributions are welcome! If you find issues or have improvements, please open an issue or submit a pull request. For major changes, discuss them first via issues.

---

## 📄 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgements

- **IBM Skills Network** – for providing the cloud IDE, watsonx credits, and the original lab materials.
- **LangChain Community** – for the powerful orchestration framework.
- **Hailey Quach, Kang Wang, Faranak Heidari** – authors of the original labs.
- **IBM Bob** – the AI coding assistant that helped maintain code quality throughout the course.

---

## 📬 Connect

- **LinkedIn**: [Rana Umer](https://www.linkedin.com/in/rana-umer-05a9a9359/)

---

⭐ *If you found this course material useful, please give this repository a star on GitHub!*

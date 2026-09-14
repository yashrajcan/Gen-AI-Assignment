Assignment 1 — Topic Detection, Summarization & Job Postings Analysis

File: GenAI_Assignment_1_Yashraj.ipynb

Overview

Part 1 — BBC News Articles

Topic classification (Business, Entertainment, Politics, Sport, Tech)
Article summarization (2-3 sentence summaries)
Key entity extraction (people, organizations, locations)

Part 2 — Job Postings Analysis

Job category classification (Technology/IT, Finance, Marketing, Healthcare, Education, Others)
Requirements extraction: required skills, education level, experience level

Bonus

Full-dataset processing (all rows, not just the sample subset) using Ollama for local, rate-limit-free inference
Tech Stack
LangChain (langchain-core, langchain-groq, langchain-ollama)
Groq API (openai/gpt-oss-20b) for the main assignment sections
Ollama (gemma3:1b) for local bonus processing
Pandas for data handling
How to Run
Clone the repository:
bash
   git clone https://github.com/yashrajcan/Gen-AI-Assignment.git
   cd Gen-AI-Assignment
Install dependencies:
bash
   pip install -q -U langchain langchain-core langchain-community langchain-groq langchain-ollama pandas
Add your own Groq API key in the notebook's setup cell (GROQ_API_KEY = "...").
(Optional, for the bonus section) Install Ollama and pull the model:
bash
   ollama pull gemma3:1b
Download the required datasets and place them in the repo folder:
bbc-news-data.csv — BBC News Archive (Kaggle)
job_title_des.csv — Job Title and Job Description Dataset (Kaggle)
Launch the notebook:
bash
   jupyter notebook GenAI_Assignment_1_Yashraj.ipynb
Notes
Datasets are not included in this repo due to size — place them locally before running.
The main (non-bonus) sections run on a small sample (30 news articles / 25 job postings) via the Groq API.
The bonus sections process the full datasets locally via Ollama to avoid API rate limits.

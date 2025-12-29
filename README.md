# Intelligent-Resume-Based-Job-Suggestion-and-Skill-Gap-Analysis-System
Using AWS Bedrock, RAG Architecture, and Streamlit

# Intelligent Resume-Based Job Recommendation System 🚀

## 📌 Project Overview
An AI-powered job recommendation and skill-gap analysis system that
intelligently matches user resumes with live job postings using
AWS Bedrock, Retrieval-Augmented Generation (RAG), MongoDB Atlas,
and an interactive Streamlit dashboard.

Unlike traditional keyword-based job portals, this system performs
context-aware semantic matching and skill-gap analysis to provide
personalized job recommendations.

---

## ❓ Problem Statement
Traditional job portals rely on basic keyword matching and fail to:
- Understand resume context
- Identify missing skills
- Rank jobs intelligently
- Provide personalized career insights

This project solves these limitations using AI-driven resume parsing,
semantic embeddings, and real-time job retrieval.

---

## 🧠 Key Features
- Resume upload & parsing via AWS Lambda
- Skill & education extraction from resumes
- Live job retrieval using Adzuna API (RAG)
- Hybrid job ranking algorithm
- Skill-gap analysis with visual heatmap
- Course recommendations for missing skills
- Fully serverless cloud architecture
- Interactive Streamlit dashboard
- Optional feedback loop for continuous improvement

---

## 🏗️ System Architecture
- **Frontend:** Streamlit
- **Backend:** AWS Lambda + API Gateway
- **Storage:** AWS S3
- **Database:** MongoDB Atlas
- **AI Layer:** AWS Bedrock (Titan Embeddings, Claude)
- **Job Source:** Adzuna API (RAG)

📷 Refer to `architecture/architecture_diagram.png`

---

## 🔁 Project Workflow
1. User uploads resume via Streamlit
2. Resume stored in AWS S3
3. S3 event triggers Lambda
4. Resume text extracted & parsed
5. Skills and education stored in MongoDB
6. RAG layer fetches live jobs from Adzuna
7. Jobs stored in MongoDB
8. Hybrid ranking engine scores jobs
9. Top 20 job recommendations generated
10. Results visualized in Streamlit

---

## 🧮 Job Ranking Logic
Each job is ranked using a hybrid scoring formula:


final_score =
0.55 × semantic_similarity +
0.25 × keyword_overlap +
0.10 × recency_weight +
0.10 × popularity_score



---

## 📊 Streamlit Dashboard Features
- Top 20 job recommendations with reasoning
- Resume summary (email, skills, education)
- Skill-gap heatmap visualization
- Recommended courses for missing skills
- Daily job refresh (API Gateway → Lambda)
- User feedback (Like / Dislike)

---

## 🧪 Results
- Context-aware job matching (not just keywords)
- Accurate skill-gap detection
- Dynamic job recommendations
- Improved relevance over traditional portals
- Scalable serverless deployment

---

## 📊 Evaluation Metrics
- Semantic similarity accuracy
- Skill-gap detection rate
- Response time (≤ 8 seconds)
- Job coverage ratio
- System scalability
- User engagement rate

---

## 📊 Tech Stack
- Python 3.11
- AWS (S3, Lambda, API Gateway, Bedrock)
- MongoDB Atlas
- Streamlit
- NLP & Semantic Search
- RAG Architecture

---

## 📁 Repository Structure


intelligent-resume-job-recommender/
│
├── lambda/
│ ├── resume_parser_lambda.py
│ ├── job_refresh_lambda.py
│
├── streamlit/
│ ├── app.py
│
├── architecture/
│ ├── architecture_diagram.png
│
├── ppt/
│ └── Project_Presentation.pptx
│
├── docs/
│ ├── Project_Report.pdf
│ └── Deployment_Guide.md
│
├── README.md



---

## ▶️ How to Run the Project
1. Deploy Lambda functions in AWS
2. Configure S3 trigger for resume uploads
3. Set MongoDB Atlas connection string as env variable
4. Deploy API Gateway for job refresh
5. Run Streamlit app:
```bash
streamlit run app.py

This project provides a one-stop, AI-driven solution for resume analysis, ATS optimization, and personalized job recommendations. 
It leverages NLP, ML, and GPT-based feedback mechanisms to help job seekers improve their resumes and discover suitable job roles based on real-world hiring patterns.

Key Features include:
- Resume Parsing & Section Extraction (Education, Experience, Skills, Certifications)
- ATS Scoring with section-wise breakdown: Keywords, Formatting, Action Verbs
- AI-Powered Feedback via GPT and rule-based evaluation
- Resume Classification using a Hybrid TF-IDF + BERT + Logistic Regression model (F1-score: 85%)
- Job Role Recommendation using cosine similarity to successful candidate resumes (Hit@5 Accuracy: 90%)
- Skill Gap Analysis with YouTube/Coursera suggestions
- Improved Resume Generator (DOCX output with structure + keywords)
- Built & tested in Google Colab; backend logic adaptable to FastAPI + MySQL

System Architecture:
Resume Upload → Text Extraction (PyMuPDF, pdfplumber, python-docx)  
→ Preprocessing & NER (spaCy, Regex, GPT)  
→ Hybrid Embedding (TF-IDF + BERT)  
→ Resume Classification (Logistic Regression)  
→ ATS Scoring & Feedback Generation  
→ Job Matching (cosine similarity with selected resumes)  
→ Skill Gap + Learning Suggestions  
→ Enhanced Resume Generation (.docx)

Dataset Used
Source: Kaggle Resume Dataset
- 9,000+ labeled resumes across 24 job categories
- Fields: Resume ID, Category, Skills, Education, Certifications, Work Experience, Projects, Summary
- Used for classification, job recommendation, skill extraction, and ATS benchmarking
  
Model Performance:
Task → 	Model → Metric →	Accuracy
Resume Classification	→ Hybrid (TF-IDF + BERT + Logistic Reg)	→ 85% → F1
Skill Gap Matching → TF-IDF + Cosine Similarity →	88% → Precision
Job Recommendation →	Hybrid + KNN + Cosine Similarity →	90% → Hit@5
Resume ATS Score Boost →	Post-feedback DOCX Resume →	+20–25% → ATS gain

Technologies & Libraries:
Type → Tools/Frameworks
NLP & Embeddings → spaCy, NLTK, TF-IDF, BERT (Hugging Face)
ML Models →	Logistic Regression, KNN, SVM, Random Forest
Resume Parsing → PyMuPDF, pdfplumber, python-docx
Visualization →	Matplotlib, Seaborn
LLM Integration →	GPT (for section-wise feedback)

Future Enhancements:
- Web-based UI using Streamlit/Flask
- Integration with GPT-4 for smart summarization
- Multilingual Resume Support
- Resume Versioning and ATS Score History
- LinkedIn/Indeed API Integration for Real-time Job Matching
- Interview Question Generator based on Resume Role

References:
Refer to the detailed list of 20+ academic references in the final report, covering resume parsing, ATS scoring, GPT-based feedback, and job recommendation research methodologies.

Contributors
Yashashwini Devineni – Project Lead | AI & NLP Modules
Sai Venkata Anil Thota – Resume Classification & ATS System
Vrunda Teeleru – Feedback & Recommendation Logic
Sravani Kudumula – Data Processing & Evaluation



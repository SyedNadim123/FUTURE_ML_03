# FUTURE_ML_03 — Resume / Candidate Screening System
### Future Interns — Machine Learning Internship | Task 3 | 2026

---

## 📌 Project Overview
An end-to-end machine learning pipeline to automatically screen and rank 
200 candidate resumes across 5 job roles using NLP, TF-IDF vectorization 
and cosine similarity scoring. The system extracts skills from resumes, 
ranks candidates based on job role fit, and identifies skill gaps for 
each candidate — replicating how real companies automate their hiring process.

---

## 🎯 Problem Statement
How can a machine learning pipeline be designed to automatically screen 
hundreds of resumes, rank candidates based on job role fit, extract 
relevant skills, and identify skill gaps — reducing manual screening 
time and improving hiring accuracy?

---

## 📊 Dataset
| Attribute | Detail |
|---|---|
| **Type** | Generated realistic resume dataset |
| **Total Resumes** | 200 candidates |
| **Job Roles** | 5 roles |
| **Resumes per Role** | 40 candidates |
| **Features** | Candidate ID, Name, Target Role, Years Experience, Education, University, Skills, Resume Text |
| **Total Skills Pool** | 100 unique skills across all roles |

---

## 🎯 Job Roles Covered
| Role | Key Required Skills |
|---|---|
| **Data Scientist** | Python, ML, Deep Learning, TensorFlow, NLP, Statistics |
| **Web Developer** | HTML, CSS, JavaScript, React, NodeJS, MongoDB |
| **ML Engineer** | Python, MLOps, Docker, Kubernetes, PyTorch, AWS |
| **Data Analyst** | SQL, Excel, Tableau, Power BI, Python, Statistics |
| **DevOps Engineer** | Docker, Kubernetes, AWS, Linux, CI/CD, Jenkins |

---

## 🛠️ Technologies & Libraries
| Tool | Purpose |
|---|---|
| **Python** | Core programming language |
| **Jupyter Notebook** | Development environment |
| **NLTK** | Text cleaning, tokenization, lemmatization |
| **Scikit-learn** | TF-IDF vectorization, cosine similarity |
| **Pandas** | Data manipulation and analysis |
| **NumPy** | Numerical computations |
| **Matplotlib** | Data visualisation |
| **Seaborn** | Statistical visualisation |

---

## ⚙️ Methodology

### 1. Resume Generation
- Generated 200 realistic resumes with names, experience, education and skills
- 40 candidates per job role
- Skills randomly assigned from role-specific skill pools

### 2. Text Cleaning & Parsing
- Lowercase conversion
- Removal of numbers and special characters
- Stopword removal using NLTK
- Lemmatization for word normalisation
- Tokenization

### 3. Skill Extraction
- Extracted skills from each resume text
- Matched against master skill list of 100 unique skills
- Counted matched and missing skills per candidate

### 4. TF-IDF Vectorization
- Applied TF-IDF with bigrams (ngram_range 1-2)
- 2,086 features extracted from resume corpus
- Job descriptions vectorized using same TF-IDF model

### 5. Candidate Ranking
- Computed cosine similarity between each resume and job description
- Normalized scores to 0-100% match percentage
- Ranked candidates within each job role

### 6. Skill Gap Identification
- Compared candidate skills vs required skills per role
- Identified matched and missing skills for each candidate
- Calculated skill match percentage per candidate

---

## 🏆 Top Candidates per Role
| Role | Best Candidate | Match % | Skill Match % |
|---|---|---|---|
| **Data Scientist** | Michael Kumar | 100.0% | 100.0% |
| **Web Developer** | Carlos Martinez | 89.6% | 66.7% |
| **ML Engineer** | Carlos Garcia | 45.6% | 53.3% |
| **Data Analyst** | Carlos Wilson | 89.7% | 73.3% |
| **DevOps Engineer** | John Anderson | 46.6% | 93.3% |

---

## 🔍 Skill Gap Analysis
| Role | Most Missing Skill | Candidates Missing |
|---|---|---|
| Data Scientist | keras | 19 candidates |
| Web Developer | mongodb, html | 14 candidates |
| ML Engineer | mlops, model deployment | 14 candidates |
| Data Analyst | power bi, data cleaning | 15 candidates |
| DevOps Engineer | ansible, azure | 15 candidates |

---

## 📈 Key Findings
- ✅ **Best Role Match:** Data Scientist — 64.2% average match
- ✅ **Best Education:** Diploma holders — 74.4% skill match
- ✅ **Perfect Candidate:** Michael Kumar — 100% match (Data Scientist)
- ✅ **Most Common Gap:** keras missing in 19 Data Scientists
- ✅ **System screens 200 resumes instantly** vs hours of manual work
- ✅ **Skill gap identified** for all 200 candidates automatically
- ✅ **TF-IDF + Cosine Similarity** proven effective for resume ranking

---

## 📊 Visualisations Generated
| File | Description |
|---|---|
| `eda_overview.png` | Avg match % by role, skill distribution, experience |
| `eda_analysis.png` | Education analysis, experience scatter, missing skills |
| `top_candidates.png` | Top 5 candidates per role, role vs education heatmap |

---

## 📂 Project Structure

FUTURE_ML_03/
│
├── FUTURE_ML_03(Resume Candidate Screening System).ipynb
├── resume_dataset.csv
├── eda_overview.png
├── eda_analysis.png
├── top_candidates.png
└── README.md

---

## 🚀 How to Run
```bash
# Clone the repository
git clone https://github.com/SyedNadim123/FUTURE_ML_03.git

# Install dependencies
pip install pandas numpy scikit-learn nltk matplotlib seaborn

# Download NLTK data
python -c "import nltk; nltk.download('punkt'); nltk.download('stopwords'); nltk.download('wordnet')"

# Launch Jupyter Notebook
jupyter notebook "FUTURE_ML_03(Resume Candidate Screening System).ipynb"
```

---

## 💼 Business Impact
| Before System | After System |
|---|---|
| Hours of manual screening | Instant automated ranking |
| Human bias in selection | Objective skill-based scoring |
| No skill gap visibility | Clear skill gap report per candidate |
| One role at a time | All 5 roles ranked simultaneously |

---

## 📚 Internship Details
| Field | Detail |
|---|---|
| **Organization** | Future Interns |
| **Program** | Machine Learning Internship|
| **CIN** | FIT/APR26/ML7297 |
| **GitHub Repo** | FUTURE_ML_03 |
| **Internship Period** | 24/04/2026 – 24/05/2026 |

---

## 👤 Author
### Syed Nadimul Haque
Data Scientist | Machine Learning Engineer | AI Engineer | Software Engineer

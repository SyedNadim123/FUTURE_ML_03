# Resume / Candidate Screening System

**Future Interns — Machine Learning Internship | Task 3 | 2026**
Syed Nadimul Haque | CIN: FIT/APR26/ML7297

---

## What this project does

An NLP pipeline that automatically screens and ranks 200 candidate resumes across 5 job roles using TF-IDF vectorization and cosine similarity. For each candidate, the system extracts skills from their resume text, scores them against the target role's requirements, ranks them by fit, and flags specific skill gaps — replicating how companies automate the early stage of hiring.

**Core question:** Can we replace hours of manual resume screening with a system that objectively ranks candidates by role fit and surfaces exactly which skills each person is missing?

---

## Dataset

A generated dataset of 200 realistic resumes — 40 candidates per role — each containing a candidate ID, name, target role, years of experience, education level, university, skills list, and full resume text. Skills are drawn from a pool of 100 unique skills distributed across role-specific subsets.

The five roles covered:

- **Data Scientist** — Python, ML, Deep Learning, TensorFlow, NLP, Statistics
- **Web Developer** — HTML, CSS, JavaScript, React, NodeJS, MongoDB
- **ML Engineer** — Python, MLOps, Docker, Kubernetes, PyTorch, AWS
- **Data Analyst** — SQL, Excel, Tableau, Power BI, Python, Statistics
- **DevOps Engineer** — Docker, Kubernetes, AWS, Linux, CI/CD, Jenkins

---

## Methodology

### 1. Resume generation

Generated 200 resumes with realistic names, experience levels, education backgrounds, and skills. Each candidate was assigned to one of the five roles, with skills randomly drawn from that role's skill pool.

### 2. Text cleaning

Standard NLP preprocessing: lowercasing, removal of numbers and special characters, stopword removal (NLTK), lemmatization, and tokenization.

### 3. Skill extraction

Matched each resume's text against a master list of 100 skills. Counted matched and missing skills per candidate to produce a skill match percentage.

### 4. TF-IDF vectorization

Applied TF-IDF with bigrams (ngram_range 1–2), extracting 2,086 features from the resume corpus. Job descriptions were vectorized using the same fitted TF-IDF model to ensure consistent comparison.

### 5. Candidate ranking

Computed cosine similarity between each resume vector and its target job description vector. Normalised scores to a 0–100% match percentage and ranked candidates within each role.

### 6. Skill gap identification

For every candidate, compared their extracted skills against the required skills for their target role. Identified exactly which skills are present and which are missing, and calculated a per-candidate skill match percentage.

---

## Results

### Top candidates per role

| Role | Best Candidate | Match % | Skill Match % |
|---|---|---|---|
| Data Scientist | Michael Kumar | 100.0% | 100.0% |
| Web Developer | Carlos Martinez | 89.6% | 66.7% |
| ML Engineer | Carlos Garcia | 45.6% | 53.3% |
| Data Analyst | Carlos Wilson | 89.7% | 73.3% |
| DevOps Engineer | John Anderson | 46.6% | 93.3% |

### Most common skill gaps by role

| Role | Most Missing Skill | Candidates Missing It |
|---|---|---|
| Data Scientist | Keras | 19 |
| Web Developer | MongoDB, HTML | 14 |
| ML Engineer | MLOps, Model Deployment | 14 |
| Data Analyst | Power BI, Data Cleaning | 15 |
| DevOps Engineer | Ansible, Azure | 15 |

---

## Key findings

1. Data Scientist had the highest average match at 64.2% across all candidates for that role.
2. Diploma holders scored the highest average skill match at 74.4% — an unexpected result worth investigating further.
3. One perfect candidate: Michael Kumar matched 100% on both TF-IDF similarity and skill coverage for Data Scientist.
4. The most common gap was Keras, missing from 19 out of 40 Data Scientist resumes.
5. The system screens all 200 resumes instantly — what would take hours manually is done in seconds.
6. Skill gaps were identified automatically for every single candidate.
7. TF-IDF combined with cosine similarity is effective for resume ranking without needing deep learning.

---

## Business impact

Without this system, you're spending hours manually reading resumes with no consistent scoring and no visibility into skill gaps. With it, all five roles are ranked simultaneously, scoring is objective and skill-based, and every candidate gets a clear gap report — instantly.

---

## Visualisations

The notebook generates three saved charts:

- `eda_overview.png` — average match percentage by role, skill distribution, experience breakdown
- `eda_analysis.png` — education analysis, experience vs match scatter, missing skills breakdown
- `top_candidates.png` — top 5 candidates per role, role vs education heatmap

---

## How to run

```bash
git clone https://github.com/SyedNadim123/FUTURE_ML_03.git

pip install pandas numpy scikit-learn nltk matplotlib seaborn

python -c "import nltk; nltk.download('punkt'); nltk.download('stopwords'); nltk.download('wordnet')"

jupyter notebook "FUTURE_ML_03(Resume Candidate Screening System).ipynb"
```

Make sure `resume_dataset.csv` is in the same folder as the notebook.

---

## Tech stack

**Language:** Python
**NLP:** NLTK (tokenization, lemmatization, stopwords)
**ML:** scikit-learn (TF-IDF vectorization, cosine similarity)
**Data processing:** pandas, NumPy
**Visualisation:** matplotlib, seaborn

---

## Internship context

Completed as Task 3 of the Future Interns Machine Learning Internship programme (24 April – 24 May 2026).

---

**Author:** Syed Nadimul Haque — Data Scientist | ML Engineer

# Zero-Shot Classification & Pedagogical Insights Pipeline for RateMyProfessors

An end-to-end Natural Language Processing (NLP) pipeline designed to perform zero-shot text classification on a large-scale dataset of nearly **97,545 professor reviews**. This project explores how transformer architectures categorize qualitative student feedback into core pedagogical themes and evaluates their relationship with quantitative instructor ratings.

---

## 🚀 Key Features
* **Large-Scale Text Processing:** Ingests, cleans, and processes 97,545 student reviews efficiently using Pandas.
* **State-of-the-Art Zero-Shot Models:** Evaluates and compares performance across advanced Hugging Face architectures (`distilbart-mnli-12-1` and `deberta-large-mnli-zero-cls`).
* **Granular Pedagogical Labeling:** Categorizes unstructured feedback across six distinct instructional criteria:
  * Punctuality & Attendance (*"show up to class room on time or never misses class"*)
  * Knowledge & Empathy (*"strong knowledge and solid education or patient and caring"*)
  * Student Engagement (*"encourages the students to question"*)
  * Practical Application (*"using real world example or exercises real world problems"*)
  * Course Structure (*"clear or sufficient syllabus"*)
  * Curriculum Relevance (*"course have useful topics or updated topics"*)
* **Statistical Insights:** Maps qualitative classification distributions to quantitative student scores (0–4 scale).

---

## 📊 Summary of Results

| Pedagogical Theme | DistilBART Model (`output.csv`) | DeBERTa-Large Model (`output2.csv`) |
| :--- | :--- | :--- |
| **Strong Knowledge / Patient & Caring** | **53,675** (55.0%) | **30,513** (31.3%) |
| **Real-World Examples / Exercises** | 4,724 (4.8%) | **30,719** (31.5%) |
| **Encourages Questioning** | 16,104 (16.5%) | 14,646 (15.0%) |
| **Useful / Updated Course Topics** | 11,025 (11.3%) | 11,004 (11.3%) |
| **Clear Syllabus** | 8,932 (9.2%) | 10,138 (10.4%) |
| **Punctuality & Attendance** | 3,085 (3.2%) | 525 (0.5%) |

---

# Statistical Summary & Model Distribution
- Model 1 Classification Distribution (output.csv)
-- Strong Knowledge / Patient & Caring: 53,675 reviews (55.0%)
-- Encourages Questioning: 16,104 reviews (16.5%)
-- Useful / Updated Course Topics: 11,025 reviews (11.3%)
-- Clear Syllabus: 8,932 reviews (9.2%)
-- Real-World Examples / Exercises: 4,724 reviews (4.8%)
-- Punctuality / Attendance: 3,085 reviews (3.2%)
  
- Model 2 Classification Distribution (output2.csv)
-- Real-World Examples / Exercises: 30,719 reviews (31.5%)
-- Strong Knowledge / Patient & Caring: 30,513 reviews (31.3%)
-- Encourages Questioning: 14,646 reviews (15.0%)
-- Useful / Updated Course Topics: 11,004 reviews (11.3%)
-- Clear Syllabus: 10,138 reviews (10.4%)
-- Punctuality / Attendance: 525 reviews (0.5%)
  
- Key Findings & Professional Insights
-- Sentiment & Rating Alignment: Higher student ratings (scores of 3 and 4) heavily correlate with instructor competencies classified under strong knowledge, patience, and caring, proving that interpersonal delivery and subject mastery are primary drivers of positive student reviews.
-- Architectural Sensitivity: The DeBERTa-large model (output2.csv) displays a more balanced distribution across practical application categories (real-world examples), whereas the DistilBART model heavily weights instructor demeanor and knowledge attributes.
-- Recruiter Takeaway: This end-to-end project demonstrates proficiency in PyTorch, Hugging Face Pipelines, Pandas data wrangling, and automated semantic labeling at scale, offering actionable sentiment intelligence for academic quality assurance.

## 💡 Key Takeaways
Interpersonal Impact: Across models, instructor knowledge, patience, and caring emerge as dominant drivers of student sentiment.
Architectural Variance: DeBERTa-large demonstrates higher sensitivity toward practical application (real-world examples), whereas DistilBART heavily weighs core behavioral attributes.

## 📝 License
This project is open-source and available under the MIT License.

## 🛠️ Project Structure
```text
├── rmp_small.csv            # Input dataset of student reviews
├── output.csv               # Model 1 classification results (DistilBART)
├── output2.csv              # Model 2 classification results (DeBERTa-large)
├── requirements.txt         # Project dependencies
├── .gitignore               # Git ignore rules
└── README.md                # Project documentation

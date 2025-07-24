# RetailTech Review Analytics: Product Categorization, Sentiment, and Fake Review Detection

## Overview
This project simulates real-world challenges for a fictional retail company (RetailTech) using Amazon review data. It involves:
1. **Product Categorization** – Automating product tagging using review text (87–88% accuracy).
2. **Sentiment & Rating Analysis** – Predicting star ratings, detecting mismatches between sentiment and ratings.
3. **Fake Review Detection** – Identifying synthetic and suspicious reviews using logistic regression and threshold tuning.
4. **Business Insights & ROI** – Executive summary, operational recommendations, and estimated ROI (164%–192%).

These findings help RetailTech improve product onboarding speed, marketing alignment, and trust/safety monitoring.

---

## Challenges & Methods

### **Challenge 1: Product Categorization**
- **Goal**: Automate manual product tagging.
- **Models**: Logistic Regression, Random Forest, Support Vector Machine.
- **Features**:
  - Sentence embeddings (`MiniLM-L6-v2`)
  - TF-IDF keyword importance
  - Review length & helpful votes (normalized)
- **Results**:
  - Review-level accuracy: **87% (Logistic Regression & SVM)**
  - Product-level accuracy: **88%**
  - Highest performance in CDs & Vinyl, Movies & TV; overlap in Beauty & Fashion.
- **Business Value**: Saves ~$50,000/year in manual tagging costs, improves catalog accuracy.

---

### **Challenge 2: Sentiment & Rating Prediction**
- **Goal**: Predict ratings and identify mismatches between sentiment and stars.
- **Models**: Logistic Regression, LightGBM, Support Vector Classifier.
- **Results**:
  - 68–69% classification accuracy (1–5 stars)
  - 52% of ratings predicted within ±0.5 stars (LightGBM regression)
  - ~0.86% mismatched reviews (positive sentiment, low stars or vice versa)
- **Key Insights**:
  - Emotional categories (CDs & Vinyl, Movies & TV) had more mismatches.
  - Beauty reviews harder to predict due to nuanced language.
- **Business Value**: Enables marketing teams to refine product descriptions & reduce return rates.

---

### **Challenge 3: Fake Review Detection**
- **Goal**: Detect synthetic or suspicious reviews.
- **Models**: Logistic Regression (TF-IDF), Random Forest.
- **Results**:
  - **97% accuracy**, **42% precision**, **93% recall (Logistic Regression)**
  - Threshold tuning allows balancing precision vs recall:
    - Threshold 0.7 → 66% precision, 90% recall
- **Key Findings**:
  - Fake reviews use vague, generic language (“purchase”, “sure”).
  - Real reviews include emotional, specific language.
- **Business Value**: Protects brand trust, saves ~$30,000/year in manual moderation.

---

### **Challenge 5: Executive Summary & ROI**
- **ROI**:
  - Net annual benefit: ~$59K–69K
  - ROI: **164%–192%**, break-even in ~6 months.
- **Key Recommendations**:
  - Deploy adjustable-threshold fake review detection.
  - Expand CDs & Vinyl category (highest predictability, strongest positive signals).
  - Redesign Beauty product descriptions (high mismatch, low predictability).
  - Build review-monitoring dashboards with sentiment & mismatch KPIs.

---

## Team Memos
Three tailored memos provide business-focused recommendations for:
- **Product Team** – Automated product categorization.
- **Marketing Team** – Sentiment mismatch insights.
- **Trust & Safety Team** – Fake review detection & thresholds.

PDF versions are in the `/memos` folder.

---

## How to Run
1. Clone this repository:

# 📺 Simulating a Data Science Project at Netflix: "Stream with Friends"

## 🔍 Project Overview

This project simulates the real-world workflow of a **Data Scientist** working at Netflix, tasked with evaluating a new feature: **“Stream with Friends.”** The feature allows paid users to co-watch Netflix content in sync with friends remotely. The goal of this project is to demonstrate how a data scientist would drive the feature from **idea to launch**, with a focus on experimentation, SQL + Python analysis, churn prediction, and clear business recommendations.

---

## 🧠 Why This Project?

In real data science roles, success doesn’t come from just writing code — it comes from solving business problems through **hypothesis-driven analysis**, **cross-functional collaboration**, and **decision-making under ambiguity**.

This project replicates the full lifecycle of a feature rollout:
- From defining metrics and data collection requirements
- To experimentation and modeling
- To generating dashboards and executive recommendations

It goes far beyond a toy dataset or competition — it's meant to reflect how real product data scientists think and work.

---

## 🛠️ Tools Used

- **SQL** (PostgreSQL)
- **Python** (Pandas, Scikit-learn, Matplotlib, Seaborn)
- **A/B Testing** logic and simulation
- **Logistic Regression** for churn prediction
- **Data schema simulation** and tracking plans
- **Dashboard** (streamlit)

---

## 🧭 Project Structure

### **1. Pre-Implementation Phase: Planning for Success**

#### 🧩 Business Context
Before any code is written, it’s essential to define:
- **What does “success” mean?**
  - Higher retention?
  - More engagement?
  - Reduced churn?

#### 📈 Success Metrics
- **Primary metric**: Increase in Day 30 Retention
- **Secondary metrics**: 
  - Feature adoption rate
  - Invite-to-accept conversion
  - Watch session length
  - Number of co-watched sessions

#### 🗃️ Event Tracking & Schema Design
As a data scientist, I would work with engineering to ensure we track the right behaviors:
- Events: `invite_sent`, `invite_accepted`, `co_watch_start`, `co_watch_end`, `chat_opened`
- Tables: `users`, `sessions`, `invites`, `events`, `feature_exposure`

📎 _Why?_ Without proper tracking, post-launch analytics would be biased, limited, or completely impossible. Good data begins with intentional logging.

---

### **2. Experimentation Phase: A/B Test Design & Analysis**

#### 🎯 Hypothesis
> Users who have access to “Stream with Friends” will show higher retention and engagement than those who do not.

#### 🧪 Test Design
- **Randomized Controlled Trial** with 50/50 split
- User-level randomization
- **Power analysis** to determine minimum sample size
- Success threshold: 95% statistical significance on primary metric

#### 🔍 A/B Test Analysis
Using simulated SQL and Python data:
- Compare engagement metrics between groups
- Use statistical testing (t-test or non-parametric)
- Segment results by age group, region, device type

📎 _Why?_ A/B testing lets us make causal claims about the impact of the feature, not just correlations.

---

### **3. Churn Prediction Modeling**

#### 🤖 Modeling Goal
Use exposure to the feature, engagement, and user behavior to predict likelihood of churn within 30 days.

#### 🔢 Features used:
- `feature_exposed` (binary)
- `co_watch_count`
- `avg_watch_time`
- `invite_accepted_rate`
- `account_age_days`
- `region`

Model: **Logistic Regression**  
Output: **Churn probability score**

📎 _Why?_ Understanding which users are likely to churn helps Netflix target retention campaigns and feature tweaks for at-risk users.

---

### **4. Dashboarding & Reporting**

A high-level dashboard mockup showing:
- Feature adoption rate
- Retention delta (test vs control)
- Active users over time
- Segmentation breakdown (age, region)

📎 _Why?_ Stakeholders need to understand the impact in real time — dashboards make data accessible and actionable.

---

### **5. Final Recommendations**

Based on all findings:
- Recommend full rollout or further iteration
- Suggest which user groups to prioritize
- Propose follow-up experiments (e.g., chat feature, rewards for co-watching)

📎 _Why?_ Data scientists need to close the loop — helping business partners act on insights, not just observe them.

---

## 🧪 Sample Deliverables

- ✅ SQL queries to analyze feature adoption and retention
- ✅ Python scripts to clean data, run tests, and model churn
- ✅ Visuals comparing A/B test outcomes
- ✅ Summary memo with rollout recommendation

---

## 🗂️ Project Directory

## 🚀 Future Enhancements

- Simulate multi-feature testing (e.g., add chat)
- Implement retention cohort analysis
- Incorporate time-series forecasting for usage
- Use a real BI dashboard tool (Streamlit / Power BI)

---

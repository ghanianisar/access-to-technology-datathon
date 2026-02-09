Web Accessibility Analysis: Identifying Digital Exclusion Patterns
University of Washington, DubsTech Datathon  2026
**Project Overview**
Analyzed 3,524 web accessibility violations across 448 websites to identify systemic patterns of digital exclusion and develop predictive models for identifying high-risk accessibility issues.
**Dataset Description**
Source: AccessGuru Accessibility Dataset  
The dataset contains 3,524 accessibility violation records collected from 448 websites across:
- Government  
- Education  
- E-commerce  
- Health  
- Media  
- Technology  
Each record includes violation type, violation category (Syntax/Layout/Semantic), severity score, WCAG reference, and domain classification.
**Workflow**
Raw Data (3,524 violations)
    ↓
Data Cleaning & Preprocessing
    ↓
Exploratory Data Analysis
    ↓
Feature Engineering (encoding, binary flags)
    ↓
Predictive Modeling (Random Forest)
    ↓
Model Evaluation & Interpretation
    ↓
Business Recommendations
** **Methodology****
1**. **Data Cleaning**
Removed columns with high missing values (70%+)
Standardized text fields and normalized domain names
Converted numeric fields to proper data types
Dropped rows missing critical information
Result: 3,524 clean violation records across 448 websites
2.** **Exploratory Data Analysis**
Analyzed violation distribution across 6 domain categories
Identified top 10 most common violation types
Created cross-tabulations of violation categories by domain
Ranked websites by severity scores
**Key Findings******:**
  News/Media sites have highest violation counts
  Color contrast issues account for 31% of violations
  Syntax violations most common, but layout violations more severe
  **3. Feature Engineering**
Created high_risk binary target variable for high-impact violations
Label-encoded categorical features (domain, category, impact)
Calculated violation rates and severity metrics by domain
**4. Predictive Modeling**
Model: Random Forest Classifier (100 trees)
Features: Domain category, violation count
Target: High-risk violation prediction
Split: 80/20 train-test
**Performance:**
     53.2% accuracy (vs. 33% baseline)
     62% recall for high-risk violations
    57% precision
Why Random Forest? Handles categorical data well, resistant to overfitting, provides feature importance
**5. Visualization & Insights**
Created bar charts, heatmaps, and distribution plots
Identified patterns across domains and violation types
Translated findings into actionable business recommendations
**Key Findings**
- News/Media site: have 47% more violations than other domains
- Color contrast issues: account for 31% of all violations, excluding ~15M users with visual impairments
- Syntax violations: are most common (52%), but **layout violations** have 2.3x higher severity scores
- Developed Random Forest model with **62% recall** for identifying high-risk violations (vs. 33% baseline)
**Technologies Used**
- Python 3.13, pandas, NumPy, scikit-learn
- Matplotlib, Seaborn for data visualization
- Jupyter Notebook for analysis
- ****6.*****Business Recommendations**
- 6.1. **Prioritize News/Media Domain (Highest Risk)**
Finding: News and Media sites have 47% more violations than average
Recommendations:
Implement automated accessibility testing in CI/CD pipelines
Train content editors on accessible image alt-text and heading structure
Set target: Reduce violations by 40% within 6 months
**6.2 Address Color Contrast Issues (31% of All Violations)**
Finding: Color contrast violations are the most common, affecting users with low vision and color blindness
Recommendations:
Use automated contrast checkers during design phase 
Add contrast validation to code review checklists
Set target: Zero color contrast violations on high-traffic pages
**6.3. Fix Layout Issues (Highest Severity Impact)**
Finding: While syntax violations are most common (52%), layout violations have 2.3x higher severity scores
Recommendations:
Prioritize layout fixes in sprint planning 
Implement responsive design testing across devices and screen readers
Add automated layout testing tools 
**6.4. Integrate Accessibility into Software Development Lifecycle**
Finding: Violations are detected post-deployment—reactive rather than proactive approach
Recommendations:
Design Phase: Include accessibility requirements in user stories and acceptance criteria
Development Phase: Use accessibility linters 
Testing Phase: Add accessibility testing to QA checklists (keyboard navigation, screen reader testing)
Deployment Phase: Run automated scans before production release (block deploys if critical violations found)
**6.5. Establish Accountability with KPIs**
Finding: No measurable accountability for accessibility quality
Recommendations:
Set team-level KPIs:
Reduce violations by 30% quarter-over-quarter
Zero high-risk violations on core user journeys (homepage, checkout, login)
Include accessibility metrics in sprint reviews and retrospectives
Recognize/reward teams achieving accessibility goals
Publish quarterly accessibility reports to stakeholders
 **Success Metrics**
**Track these metrics quarterly:**
Total violations (target: -30% QoQ)
High-risk violations (target: 0 on critical pages)
Pages audited/total pages ratio (target: 100%)
Mean time to remediation (target: <2 weeks)
**Stakeholder Responsibilities**
Stakeholder Accountability: Defined roles for Product, Design, Development, QA teams

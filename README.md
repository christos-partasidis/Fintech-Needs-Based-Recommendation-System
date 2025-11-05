# Needs Based Financial Product Recommendation Engine (Explainable AI)

> **Regulated FinTech | Explainable ML | MiFID II Aligned System Design**

This project develops a transparent, regulation compliant wealth advisory engine for retail banking.  
It identifies true client investment needs (Income vs. Accumulation) and recommends suitable products while ensuring full explainability, auditability, and zero risk-suitability violations.

Designed and implemented as part of the Politecnico di Milano FinTech program.

---

## Value Proposition

- Needs-first advisor logic (not product pushing)
- Explainable Decision Trees - simple, auditable rules
- MiFID II risk suitability compliance
- Next Best Action engine for financial products
- Built for trust, not just accuracy

---

## Contributors & Roles

Team: Christos Partasidis | Mehdi Ghiasipour | Reza Ilzadi Jahromi | Suraj Manickam Thirumalai Raja

---

## System Summary

| Component | Details |
|---|---|
Clients | 5,000 retail banking profiles (anonymized)  
Targets | Income vs. Accumulation investment needs  
Model | Dual Decision Trees (depth-controlled for explainability)  
Validation | 5-fold CV, F1 optimization  
Risk Control | Product risk ≤ Client risk score (MiFID II)  
Explainability | PDPs + rule trace + structured logic  

---

## Key Results

| Metric | Income | Accumulation |
|---|---|---|
Baseline F1 | 0.689 | 0.680 |
Final F1 | 0.729 | 0.818 |
Δ | +0.04 | +0.14 |

Additional Outcomes:
- 94% recommendation coverage (Income)
- 75% coverage (Accumulation)
- 0 suitability breaches

> System behaves like a regulated digital advisor - transparent, explainable, compliant.

---

## Architecture

1. Client data ingestion
2. Feature engineering (log-scale + life-stage features)
3. Interpretable ML (Decision Trees, depth 5)
4. Need prediction
5. Risk-filter logic
6. Next-Best-Action recommendation

---

## Files

| File | Description |
|---|---|
`Fintech_Final_Project_Estimating_Needs_V1_3.ipynb` | Full pipeline: EDA → model → explainability → NBA logic |
`Fintech_Final_Project_Team_15.pdf` | Executive slide deck |

---

## Quick Start

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook Fintech_Final_Project_Estimating_Needs_V1_3.ipynb

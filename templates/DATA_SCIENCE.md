---
layout: default
title: "Data Science"
parent: Templates
nav_order: 2
---

# Template: Data Science Projects

*Starter memory edits for data science and ML projects.*

---

## Core Template (5 edits)

Copy and customize these:

```
1. "Primary language: [Python 3.11/R 4.3/Julia]"
2. "ML Framework: [TensorFlow/PyTorch/Scikit-learn/XGBoost]"
3. "Data storage: [PostgreSQL/Snowflake/S3/BigQuery]"
4. "Environment: [Jupyter/VS Code/RStudio/Databricks]"
5. "Deployment: [AWS SageMaker/Azure ML/Google Vertex/Docker]"
```

---

## Filled Example

```
1. "Primary language: Python 3.11, no R" (37 chars)
2. "ML Framework: PyTorch 2.0, TensorFlow only for legacy" (55 chars)
3. "Data storage: Snowflake warehouse + S3 for raw files" (53 chars)
4. "Environment: VS Code with Jupyter extension, not Databricks" (60 chars)
5. "Deployment: Docker containers on AWS ECS, not SageMaker" (56 chars)
```

---

## Extended Template (10 edits)

For more complex projects:

```
6. "Feature store: [Feast/Tecton/custom]"
7. "Experiment tracking: [MLflow/Weights&Biases/Neptune]"
8. "Data versioning: [DVC/Delta Lake]"
9. "Pipeline orchestration: [Airflow/Prefect/Dagster]"
10. "Model format: [ONNX/TorchScript/SavedModel]"
```

---

## Domain-Specific Additions

### NLP Projects
```
"NLP: Hugging Face Transformers, not spaCy for main models" (59 chars)
"Embeddings: OpenAI ada-002 for production, local for dev" (57 chars)
```

### Computer Vision
```
"CV Framework: PyTorch + torchvision, not TensorFlow" (52 chars)
"Image storage: S3 with CloudFront CDN" (37 chars)
```

### Time Series
```
"Time series: Prophet for baseline, custom LSTM for production" (63 chars)
"Frequency: Daily data, no sub-hourly granularity" (49 chars)
```

---

## How to Use

1. Copy the core template
2. Fill in the brackets with your specifics
3. Add using: `memory_user_edits add control="..."`
4. Test with relevant questions
5. Refine based on results

---

*Template from [Claude Memory User Edits Guide](https://github.com/frmoretto/claude-memory-user-edits-guide) — CC BY 4.0*

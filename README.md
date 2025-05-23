```markdown
# 🚀 End-to-End Spam Detection with MLOps (Git + DVC + S3)

This project demonstrates a **production-grade machine learning pipeline** for detecting spam messages using an **MLOps workflow** built with Git, DVC, and AWS S3. It shows how to manage datasets, parameters, metrics, and model versions efficiently.

---

## 📁 Project Structure

```

├── .dvc/                  # DVC internal files
├── .vscode/               # Editor config
├── dvclive/               # Live training metrics
├── experiments/           # Experiment tracking and outputs
├── src/                   # Source code for training, evaluation, and preprocessing
├── dvc.yaml               # DVC pipeline stages
├── dvc.lock               # DVC lock file
├── params.yaml            # Model and pipeline parameters
├── projectflow\.txt        # High-level workflow or planning notes
├── README.md              # Project documentation
├── .gitignore             # Git ignore rules
├── .dvcignore             # DVC ignore rules

````

---

## 🔧 Technologies Used

- **Git** – Code version control
- **DVC** – Data & model versioning, pipeline management
- **AWS S3** – Remote storage for data and model artifacts
- **scikit-learn / pandas / numpy** – Spam classification pipeline
- **dvclive** – Live experiment tracking

---

## 🧠 Problem Statement

Build a robust **spam detection system** that classifies SMS messages into **spam** or **ham** using a logistic regression (or similar) classifier. The focus is not just on model accuracy but also on **reproducibility**, **data management**, and **tracking experiments**.

---

## ⚙️ MLOps Pipeline (with DVC)

The full pipeline includes:

1. **Data Ingestion** – Load and version raw data
2. **Preprocessing** – Text cleaning, tokenization, vectorization
3. **Training** – Train a logistic regression model
4. **Evaluation** – Compute precision, recall, F1-score
5. **Tracking** – Log metrics using DVC + dvclive
6. **Versioning** – All stages, data, and models tracked with DVC
7. **Remote Storage** – Push datasets and model artifacts to AWS S3

Run the pipeline:

```bash
dvc repro
````

Track experiment metrics:

```bash
dvc exp show
```

Push to remote:

```bash
dvc push
```

---

## 📦 How to Run Locally

1. **Clone the repo**

   ```bash
   git clone https://github.com/vish1007/End-to-End-Spam-Detection-with-MLOps-Git-DVC-S3.git
   cd End-to-End-Spam-Detection-with-MLOps-Git-DVC-S3
   ```

2. **Install dependencies**
   *(Use conda or venv for isolation)*

   ```bash
   pip install -r requirements.txt
   ```

3. **Setup DVC remote (S3)**

   ```bash
   dvc remote add -d myremote s3://your-bucket-name/path
   dvc remote modify myremote access_key_id <your-access-key>
   dvc remote modify myremote secret_access_key <your-secret-key>
   ```

4. **Pull data and models**

   ```bash
   dvc pull
   ```

5. **Run pipeline**

   ```bash
   dvc repro
   ```

---

## 📌 Key Learnings

* How to build reproducible ML pipelines using **DVC**
* Managing datasets and models with **version control**
* Integrating **AWS S3** as remote storage
* Tracking experiments using **dvclive**
* Best practices in **MLOps**

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```


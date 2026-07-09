
# End-to-end Machine Learning lifecycle.

An end-to-end Machine Learning lifecycle consists of several stages:

1. **Problem Definition**

   * Understand the business problem.
   * Define objectives and success metrics.

2. **Data Collection**

   * Gather data from databases, APIs, logs, sensors, or third-party sources.

3. **Data Preprocessing**

   * Handle missing values.
   * Remove duplicates.
   * Encode categorical variables.
   * Normalize or standardize data.
   * Split data into training, validation, and test sets.

4. **Exploratory Data Analysis (EDA)**

   * Analyze data distributions.
   * Detect outliers.
   * Identify feature relationships.
   * Visualize trends.

5. **Feature Engineering**

   * Create new features.
   * Select important features.
   * Remove irrelevant or highly correlated features.

6. **Model Training**

   * Choose an appropriate algorithm.
   * Train the model.
   * Tune hyperparameters.

7. **Model Evaluation**

   * Evaluate using metrics such as Accuracy, Precision, Recall, F1-score, ROC-AUC (classification) or RMSE, MAE, R² (regression).
   * Compare multiple models.

8. **Model Deployment**

   * Package the model (e.g., with Docker).
   * Deploy using REST APIs (e.g., FastAPI).
   * Host on cloud platforms like AWS.

9. **Monitoring**

   * Monitor latency, throughput, prediction quality, and resource usage.
   * Detect data drift and model drift.

10. **Retraining**

    * Retrain the model periodically or when performance degrades.
    * Redeploy the updated version.

---

## 1. What is Version Control (Git)?

**Answer:**

Git is a distributed version control system used to track changes in source code and collaborate with multiple developers. It maintains the history of every change, making it easy to revert to previous versions and manage different features using branches.

### Why is Git used in MLOps?

* Tracks ML code changes
* Enables collaboration among data scientists and developers
* Supports branching and merging
* Maintains version history
* Integrates with CI/CD pipelines

### Common Git Commands

```bash
git init
git clone <repository-url>
git status
git add .
git commit -m "Added new feature"
git push origin main
git pull origin main
git checkout -b feature-branch
git merge feature-branch
```

### Interview Answer (30 seconds)

> Git is a distributed version control system that tracks changes in code. In MLOps, it helps manage ML source code, collaborate with teams, maintain version history, and integrate with CI/CD pipelines. I regularly use Git for branching, committing, merging, and managing project versions.

---

# 2. What is Experiment Tracking (MLflow)?

### Answer

Experiment tracking is the process of recording every machine learning experiment so that results can be reproduced and compared.

An experiment includes:

* Hyperparameters
* Dataset version
* Model metrics
* Artifacts
* Model files
* Source code version

MLflow is one of the most popular tools for experiment tracking.

### MLflow Tracks

* Parameters
* Metrics
* Models
* Artifacts
* Tags
* Source code version

### Example

```python
import mlflow

with mlflow.start_run():
    mlflow.log_param("learning_rate",0.001)
    mlflow.log_metric("accuracy",0.96)
    mlflow.sklearn.log_model(model,"model")
```

### Benefits

* Compare experiments
* Reproduce results
* Store models
* Register best models
* Team collaboration

### Interview Answer

> MLflow is an open-source MLOps platform used for experiment tracking, model registry, and deployment. It records parameters, metrics, artifacts, and trained models so experiments can be reproduced and compared efficiently.

---

# 3. What is CI/CD Pipeline?

### Answer

CI/CD stands for:

* Continuous Integration
* Continuous Delivery/Deployment

It automates software and ML application development.

### Continuous Integration (CI)

Whenever code is pushed:

* Run unit tests
* Build Docker image
* Validate code
* Run linting
* Train model (optional)

### Continuous Deployment (CD)

After CI succeeds:

* Deploy application
* Deploy ML model
* Update Kubernetes
* Perform health checks

### Typical Pipeline

```
Developer

↓

GitHub

↓

GitHub Actions / Jenkins

↓

Run Tests

↓

Build Docker Image

↓

Push Image to Registry

↓

Deploy to Kubernetes
```

### Interview Answer

> CI/CD automates the build, testing, and deployment process. In MLOps, CI validates ML code and pipelines, while CD deploys updated models to production automatically, reducing manual effort and ensuring reliable releases.

---

# 4. What is Containerization (Docker)?

### Answer

Docker packages an application and all its dependencies into a container so it runs consistently across different environments.

### Why Docker?

Without Docker:

```
Works on my laptop ❌

Fails on server ❌
```

With Docker:

```
Works everywhere ✅
```

### Docker Contains

* Python
* Libraries
* Model
* Code
* Dependencies

### Example Dockerfile

```dockerfile
FROM python:3.11

WORKDIR /app

COPY . .

RUN pip install -r requirements.txt

CMD ["python","app.py"]
```

### Interview Answer

> Docker containerizes ML applications with all dependencies, ensuring the application behaves consistently across development, testing, and production environments.

---

# 5. What is Kubernetes?

### Answer

Kubernetes is a container orchestration platform used to deploy, scale, monitor, and manage Docker containers automatically.

### Features

* Auto scaling
* Load balancing
* Self healing
* Rolling updates
* Service discovery
* High availability

### Example Architecture

```
Users

↓

LoadBalancer

↓

Kubernetes Service

↓

Pods

↓

Docker Containers
```

### Interview Answer

> Kubernetes automates deployment, scaling, and management of containerized applications. In MLOps, it helps deploy ML inference services with high availability, auto-scaling, and self-healing capabilities.

---

# 6. What is Infrastructure as Code (Terraform)?

### Answer

Terraform is an Infrastructure as Code (IaC) tool used to create and manage cloud infrastructure using code instead of manual configuration.

### Example Resources

* EC2
* S3
* IAM
* VPC
* EKS
* RDS

### Example

```hcl
resource "aws_instance" "web" {

  ami = "ami-12345"

  instance_type = "t2.micro"

}
```

### Benefits

* Repeatable deployments
* Version-controlled infrastructure
* Automation
* Easy rollback

### Interview Answer

> Terraform automates cloud infrastructure provisioning using code. It enables consistent, repeatable deployments and integrates well with CI/CD pipelines for infrastructure management.

---

# 7. What is Monitoring and Alerting?

### Answer

Monitoring continuously tracks the health and performance of ML systems, while alerting notifies teams when predefined thresholds or failures occur.

### What is Monitored?

* CPU usage
* Memory usage
* API latency
* Prediction errors
* Model accuracy
* Request volume
* Data drift
* Model drift

### Common Tools

* Prometheus
* Grafana
* CloudWatch
* ELK Stack

### Example Alerts

* CPU > 80%
* Memory > 90%
* Accuracy < 90%
* Latency > 500 ms
* High error rate

### Interview Answer

> Monitoring ensures ML services remain healthy by tracking infrastructure and model performance metrics. Alerting automatically notifies engineers when issues like high latency, prediction errors, or model performance degradation occur.

---

# 8. What is Model Registry and Versioning?

### Answer

A model registry is a centralized repository for storing, organizing, versioning, and managing machine learning models throughout their lifecycle.

### It Stores

* Model versions
* Metrics
* Artifacts
* Approval status
* Deployment stage

### Stages

```
Version 1

↓

Staging

↓

Production

↓

Archived
```

### MLflow Registry Example

```
Version 1

Version 2

Version 3

Current Production = Version 3
```

### Benefits

* Version control
* Easy rollback
* Governance
* Deployment management
* Collaboration

### Interview Answer

> A model registry manages different versions of trained models along with metadata and lifecycle stages. It simplifies model governance, deployment, and rollback. MLflow Model Registry is commonly used for this purpose.

---

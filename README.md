# 🛡️ ShieldML: Enterprise DevSecMLOps Platform
> **Real-Time Financial Risk & Fraud Anomaly Engine with End-to-End DevSecMLOps Architecture**

ShieldML is a production-grade demonstration platform showcasing all 4 interconnected pillars of **DevSecMLOps**: **Development**, **Security**, **Machine Learning**, and **Operations**.

---

## 🏛️ DevSecMLOps Architectural Pillars

```
+---------------------------------------------------------------------------------------+
|                                    SHIELDML ENGINE                                    |
+---------------------------------------------------------------------------------------+
|  [DEV] Development                |  [SEC] Security (DevSecOps)                      |
|  - Modular FastAPI Architecture   |  - HMAC-SHA256 Model Integrity Verification      |
|  - Pydantic v2 Type Safety & Gate |  - Real-time Adversarial Evasion Shield          |
|  - 100% PyTest Suite (Unit + Int) |  - PCI-DSS & GDPR Automated PII Masking Engine   |
|  - OpenAPI 3.1 & Schema Specs     |  - Bandit SAST + Secret Leak Scanner             |
|-----------------------------------+---------------------------------------------------|
|  [ML] Machine Learning (MLOps)    |  [OPS] Operations (AIOps & Observability)        |
|  - Soft Voting Ensemble (RF + GB) |  - Hardened Multi-Stage Docker Container         |
|  - CI/CD Quality Gating (AUC>=0.88|  - Prometheus OpenMetrics Engine (/metrics)      |
|  - Explainable AI (XAI Attribution|  - Live Health Probes (/health/live & /ready)    |
|  - Population Stability Drift(PSI)|  - Zero-Downtime Rollback & Canary Deployment    |
+---------------------------------------------------------------------------------------+
```

---

## 🚀 Key Capabilities

### 1. 💻 Development (Dev)
- **FastAPI Microservice**: High-throughput asynchronous prediction backend with sub-millisecond overhead.
- **Strict Data Schemas**: Type-safe boundary validation preventing malformed or out-of-range payloads.
- **Comprehensive Test Suite**: 100% automated test coverage across security, drift, gating, and API contracts.

### 2. 🔒 Security (Sec / DevSecOps)
- **HMAC-SHA256 Cryptographic Verification**: Every model artifact is signed upon training. If a model file is tampered with, execution is immediately blocked.
- **Adversarial Input Defense**: Shields models from extreme feature evasion noise, Out-of-Distribution (OOD) perturbations, and NaN/Infinity poisoning.
- **PII Data Redaction**: Automatically scrubs PANs (credit card numbers), user emails, and IP addresses in logs.
- **Integrated SAST & Dependency Scanner**: Embedded Bandit analyzer and secret scanner.

### 3. 🤖 Machine Learning (ML / MLOps)
- **Production Ensemble**: Calibrated soft-voting classifier combining Random Forest and Gradient Boosting.
- **CI/CD Quality Gating**: Automatically rejects models in the pipeline if test AUC-ROC < 0.88 or F1 < 0.75.
- **Explainable AI (XAI)**: Generates real-time plain-language attribution explaining *why* a decision was reached.
- **Automated Drift Detection**: Computes Population Stability Index (PSI) and Kolmogorov-Smirnov (KS) tests between baseline distribution and production inference windows.

### 4. ⚙️ Operations (Ops)
- **Containerized Architecture**: Multi-stage, unprivileged `appuser` Docker container.
- **Prometheus Telemetry**: Real-time export of request counts, latency histograms, attack attempt counters, and drift gauges.
- **Zero-Downtime Governance**: Dynamic rollback to earlier certified versions with instant registry synchronization.
- **Interactive Web Console**: High-end glassmorphic console for live monitoring and attack simulation.

---

## 🧪 Running the Platform

### 1. Train the Initial Model & Verify Quality Gates
```bash
python scripts/train.py --version v1.0.0 --samples 6000 --min-auc 0.88 --min-f1 0.75
```

### 2. Run DevSecOps Security Audit
```bash
python scripts/security_audit.py
```

### 3. Run the Automated PyTest Suite
```bash
pytest tests/ -v
```

### 4. Launch the DevSecMLOps Web Console & REST API
```bash
uvicorn src.api.app:app --host 127.0.0.1 --port 8000
```
Open **`http://127.0.0.1:8000`** in your browser to interact with the live console.

---

## 🐳 Docker & Docker Compose
```bash
docker-compose up --build -d
```
- API & Console: `http://localhost:8000`
- Prometheus Dashboard: `http://localhost:9090`

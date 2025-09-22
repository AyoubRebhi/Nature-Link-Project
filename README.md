# 🌍 NatureLink

NatureLink is a **cloud-native application** that integrates **Infrastructure as Code (IaC)**, automation, monitoring, and **AI models** for intelligent recommendations and content generation.  

It demonstrates **end-to-end deployment on OpenStack**, automated with **Ansible**, containerized with **Docker & Kubernetes**, and monitored with **Prometheus & Grafana**.  

The application combines a **Spring Boot backend** with an **Angular frontend**, and integrates multiple **AI models** (LLM, NLP, CNN, Logistic Regression, Transformers, and DALL·E).  

---

## 🌐 Infrastructure  

Deployed on **OpenStack** with:  
- Keystone (Identity)  
- Nova (Compute)  
- Neutron (Networking)  
- Octavia (Load Balancer)  
- Heat (Orchestration)  

---

## ⚙️ Automation & Monitoring  

- Automated setup with **Ansible**  
- Containerized with **Docker** and orchestrated by **Kubernetes**  
- Real-time monitoring with **Prometheus & Grafana**  

---

## 💻 Application  

- **Backend**: Spring Boot (Java)  
- **Frontend**: Angular  

---

## 🤖 AI Models  

- **LLM-based Recommender**: Custom-built **Large Language Model (LLM)** for semantic similarity, recommendation, and intelligent content generation.  
- **CNN**: Image-based recognition and classification.  
- **Transformers**: Context-aware recommendations and embeddings.  
- **DALL·E Integration**: Image generation from text prompts.  

---

## 📊 Architecture Overview  

```mermaid
flowchart TD
    User[User] -->|UI/UX| Angular[Angular Frontend]
    Angular -->|REST API| SpringBoot[Spring Boot Backend]
    SpringBoot -->|AI Requests| PythonAI[AI Microservices]
    PythonAI --> LLM[LLM Recommender]
    PythonAI --> CNN[CNN]
    PythonAI --> Trans[Transformers]
    PythonAI --> Dalle[DALL·E]

    SpringBoot -->|DB Ops| MySQL[(MySQL Database)]
    SpringBoot -->|Monitoring| Prometheus[Prometheus & Grafana]

    subgraph OpenStack Cloud
        Keystone
        Nova
        Neutron
        Octavia
        Heat
    end

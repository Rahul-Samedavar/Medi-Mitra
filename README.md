# Medi-Mitra

## Overview
We have uploaded demo scripts of training and explainable AI part, you can see that the architecture we promise is possible and completely practicle.
This project presents a scalable, intelligent medical imaging assistant powered by a **three-model pipeline** to support both **radiologists** and **patients**. It automates disease detection, generates explainable visual and textual diagnostics, and enables multilingual, source-grounded health consultations.

---

## 🚀 Tri-Model Architecture

Our architecture is structured into three synergistic components:

### 1. **CNN-Based Disease Detection**

* **Model:** Convolutional Neural Networks (Deeplearning)
* **Dataset:** NIH ChestX-ray14
* **Function:** Classifies over **14 chest-related diseases**.
* **Output:** Disease labels with confidence scores and Grad-Cam Overlay.

### 2. **Vision-Language Model (LLaMA 4 Scout)**

* **Model:** LLaMA 4 Scout (custom VLM)
* **Input:** Medical scan + CNN output
* **Function:** Extracts and explains:

  * **Disease locations**
  * **Shape & size of anomalies**
  * **Visual marker reasoning**
* **Explainability:** Integrated with **GradCAM, GradCAM++, and Layered Vision** for heatmap overlays.


### 3. **BioGPT-Based Report Generator**

* **Model:** BioGPT (Fine-tuned LLM on biomedical texts)
* **Input:** CNN predictions + visual cues + patient data
* **Function:** Generates:

  * Structured **clinical reports**
  * **Differential diagnosis**
  * Exportable, human-readable **medical summaries**


---

## 🔁 Pipeline Flow

```mermaid
graph TD
A[Input Scan (X-ray / CT / MRI)] --> B[CNN Disease Classification]
B --> C[LLaMA 4 Scout]
C --> D[Visual Explanation + Reasoning]
B --> E[BioGPT]
C --> E
E --> F[Exportable Diagnostic Report]
```

---

## ⚙️ Tech Stack

| Component       | Technology           |
| --------------- | -------------------- |
| ML Frameworks   | PyTorch / TensorFlow |
| Vision-Language | LLaMA 4 Scout        |
| Language Model  | BioGPT               |
| Dataset         | NIH ChestX-ray14     |
| Frontend        | React.js             |
| Backend         | Flask                |
| Database        | MySQL                |
| GraphRAG        | Neo4j                |

---

## 📦 Key Features

* 🔍 **14+ disease detection**
* 🧠 **Explainable AI** via GradCAM overlays
* 🗣️ **Human-like explanations** of scan findings
* 🧾 **Automated, structured report generation**
* 💬 **Chatbot** for patients with GraphRAG for grounded responses
* 🌐 **Multilingual disease archive**
* 📊 **Radiologist dashboard** for triage and stats
* 🔄 **Self-improving pipeline** using real-time feedback

---

## 📈 Use Cases

* Triage automation for overworked radiologists
* Diagnostic aid in low-resource healthcare settings
* Patient-facing second opinion tool
* Educational resource for medical students and interns

---


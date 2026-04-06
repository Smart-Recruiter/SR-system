<h1 align="center">Smart Recruiter (R26-IT-105)</h1>

<p align="center">
  <em>An AI-Driven, Emotionally Adaptive Technical Interview Platform</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue.svg" alt="Python Version">
  <img src="https://img.shields.io/badge/PyTorch-Integrated-ee4c2c.svg" alt="PyTorch">
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License">
</p>

---

## 📖 About the Project
Modern recruitment and remote education rely heavily on automated screening tools, but current solutions depend on rigid keyword matching and lack emotional intelligence. These systems evaluate candidates in a vacuum, often rejecting highly qualified individuals simply because of interview anxiety or stage fright. 

**Smart Recruiter** solves this by delivering a comprehensive, low-latency AI platform. By integrating real-time physiological stress tracking, cognitive load analysis, and localized Small Language Models (SLMs), the platform evaluates candidates fairly based on their true capabilities while dynamically adapting to their emotional state.

## ✨ Key Components & Architecture

The system operates via four decoupled, highly specialized microservices:

* **Adaptive AI Interviewer (Core Orchestrator):** The adaptive AI-driven interviewer system dynamically generates context-aware technical questions based on candidate performance and stress. It uses lightweight embedding models (Sentence-BERT) for millisecond-fast semantic grading against a vector database. An in-memory event broker (Redis) asynchronously fetches real-time stress metrics without blocking the conversation, feeding this context into a localized Small Language Model (Llama 3 8B / Mistral 7B) to adjust the interview difficulty on the fly.
* **Skill Knowledge Graph & Resume Parsing:** Replaces traditional keyword parsers by constructing an intelligent Skill Knowledge Graph from PDF resumes and GitHub profiles. It utilizes Graph Neural Networks (GNNs) to infer implicit technical skills and generate a normalized competency score.
* **Visual Behavior & Cognitive Load Detection:** Uses a standard webcam to capture live video and applies MediaPipe to map 468 facial points. PyTorch-based Convolutional Neural Networks (CNN) and Vision Transformers (ViT) analyze pupil dilation and micro-expressions to differentiate genuine deception from natural cognitive load and anxiety.
* **Accent-Invariant Audio Analysis:** Evaluates vocal characteristics such as confidence, hesitation, and stress without linguistic bias. It extracts features like Mel-Frequency Cepstral Coefficients (MFCC) and utilizes Long Short-Term Memory (LSTM) networks to provide quantitative behavioral metrics.

## 🛠️ Technology Stack
* **AI & Machine Learning:** PyTorch, TensorFlow, Sentence-BERT/MiniLM, Llama 3 8B / Mistral 7B.
* **Computer Vision & Audio:** OpenCV, MediaPipe, Librosa.
* **Backend & Orchestration:** Python, Redis (Pub/Sub), n8n Workflow Automation.
* **Database:** Neo4j, Vector Databases (for embeddings), MongoDB Atlas.

## 🚀 Getting Started

### Prerequisites
* Python 3.10+
* Redis Server installed and running locally
* Node.js (for n8n workflow automation)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Smart-Recruiter/SR-system.git
   cd smart-recruiter

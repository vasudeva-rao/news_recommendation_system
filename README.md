### 🗞️ News Recommendation System using Advanced LLM Concepts
This repository presents a personalized, explainable news recommendation system that integrates cutting-edge Large Language Models (LLMs), including LLaMA-3.2-1B, with tools like FAISS, SQLite, and Gradio. It is designed to overcome cold-start problems, enhance transparency, and provide dynamic recommendations based on real-time user interactions.

### 🚀 Project Overview
Traditional news recommendation engines face challenges like:

Cold-start user problems

Lack of explanation

Static recommendations that fail to reflect changing user interests

This system addresses those issues using:

Semantic similarity search (FAISS + sentence-transformers)

LLM-based explanations (LLaMA-3.2-1B)

Real-time user profiling (SQLite)

Interactive interface (Gradio)

Model: Sentence-transformers/all-MiniLM-L6-v2 for embeddings
LLM: LLaMA-3.2-1B for natural language explanations
Dataset: MINDsmall (https://msnews.github.io/)

### 🛠️ Features
✅ Real-time user-based recommendation

✅ Semantic article retrieval using FAISS

✅ LLM-generated explanations (e.g., "Based on your interest in sports...")

✅ Cold-start handling with diverse sampling

✅ Gradio-powered interactive UI

### ⚙️ System Architecture
User Query → Embedding → FAISS Search → Scoring Engine → Top Articles
↓
SQLite User History ← Click Weights
↓
LLaMA-3.2-1B Generated Explanation

### 🧪 Technologies Used

Component	Tech Stack
Embedding	Sentence-Transformers / MiniLM-L6-v2
LLM Explanation	LLaMA-3.2-1B (Meta AI)
Vector Indexing	FAISS
User DB	SQLite
Interface	Gradio
Language	Python

### 📈 Performance Snapshot
Category relevance (top-1 match): ~85% (sample of 10 users)

Embedding generation: ~10 mins (for 50k articles)

FAISS indexing: < 1 minute

Real-time interaction via Gradio

### 🚧 Limitations
Explanation quality limited by 1B parameter model

Static dataset, lacks live data updates

Dominant preference bias (proportional scoring)

GPU constraints (tested on Google Colab T4)

### 📌 Future Enhancements
🔄 Live news ingestion via NewsAPI

🖼️ Multimodal support (image + text with CLIP)

🧠 Upgrade to LLaMA-7B/13B for better reasoning

🔍 Real-time profile updating with Apache Kafka

☁️ Deployable via FastAPI + Docker + Kubernetes


### 📬 Contact
For queries, drop a message via GitHub Issues or connect via LinkedIn.

Built with ❤️ to make news consumption smarter and personalized.

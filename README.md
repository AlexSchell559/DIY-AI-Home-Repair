# DIY-AI-Home-Repair
Project Overview

RepAIr Bot is an intelligent DIY home-repair assistant that combines image and text understanding with retrieval-augmented generation (RAG). Users can upload photos or descriptions of household repair issues, and the system retrieves guidance from indexed manuals and trusted web sources, fusing both to provide step-by-step solutions, safety notes, and tool recommendations.

Key Features
- Multi-Modal RAG (image + text fusion)
- Whitelisted Search Integration (secure web retrieval)
- Vector Database (FAISS) for similarity search
- (Planned) Speech-to-Text / Text-to-Speech interface
- Android front-end with API connection to Python backend

System Architecture

Flow:
User Input — Photo or text query from Android app
Service Layer — Routes query through security whitelist
RAG Fusion — Combines results from:
  PDF/Text Indexer: SentenceTransformer + FAISS
  Image Indexer: CLIP embeddings + FAISS
Web Search (CSE): Fetches relevant pages from trusted domains
Fusion Layer: Merges all sources and runs safety checks
Response: Returns structured repair suggestions


Future Work

Add voice interface (TTS/STT)
Deploy a demo app on HuggingFace or Streamlit
Improve error handling and user feedback
Introduce evaluation metrics for retrieval relevance

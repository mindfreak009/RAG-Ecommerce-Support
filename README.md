# RAG-Ecommerce-Support

Local AI with Ollama
An AI application built using open-source large language models (LLMs) running locally through Ollama. The project demonstrates how modern AI capabilities can be deployed directly on a personal laptop without depending on external cloud-based AI APIs.


Key Features
🤖 Uses open-source AI/LLM models
💻 Runs locally on a personal laptop
🦙 Uses Ollama for local model management and inference
🔒 Keeps prompts and responses on the local machine
☁️ No dependency on cloud-based LLM APIs
⚡ Designed for experimentation and local AI development

Tech Stack
=========== 
  ● Java 
  ● Spring Boot
  ● Spring AI:  AI application integration and abstractions
  ● Ollama for local LLM and embeddings
  ● Pinecone as the vector database
  ● phi4-mini for generating answers
  ● nomic-embed-text for generating embeddings

Purpose
========
The goal of this project is to explore practical local AI development and demonstrate how open-source language models can be integrated into applications while maintaining control over the model, data, and execution environment.


1. Architecture
================

The application follows this general flow:

                         ┌─────────────────────┐
                         │   Support Documents │
                         │      PDF Docs       │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │    Spring AI       │
                         │  Document Loader    │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │      Ollama         │
                         │ nomic-embed-text    │
                         │                     │
                         │ 768-dimensional     │
                         │ embeddings          │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │      Pinecone       │
                         │   Vector Database   │
                         │                     │
                         │ Dimension: 768      │
                         │ Namespace: policydocs│
                         └──────────┬──────────┘
                                    │
                         Similarity Search
                                    │
                                    ▼
┌──────────────┐         ┌─────────────────────┐
│    User      │────────▶│   Spring Boot API   │
│   Question   │         └──────────┬──────────┘
└──────────────┘                    │
                                    ▼
                         ┌─────────────────────┐
                         │      Ollama         │
                         │      phi4-mini      │
                         │                     │
                         │  Generate Answer    │
                         └──────────┬──────────┘
                                    │
                                    ▼
                              Final Answer



## 2. Prerequisites & Configuration

Before running the application, ensure the following prerequisites and configurations are in place:

| Software           | Configuration/ Version |
| ------------------ | ---------------------- |
| Java               | 21                     |
| Maven              | 3.9+                   |
| Ollama             | Latest                 |
| Ollama Service     | Running Locally        |
| Chat Model         | phi4-mini              |
| Embedding Model    | nomic-embed-text       |
| Pinecone Account   | Required               |
| Pinecone Index     | Created                |  
| Pinecone Dimension | 768                    |
| Git                | Latest                 |
-----------------------------------------------


                              


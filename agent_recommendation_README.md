# ML25-26-03AI Recommendation Agent PlugIn

An agent-based recommendation system built using **.NET (C#)**.  
The project uses semantic embeddings and a plug-in (tool) architecture to recommend documents based on user intent.

---

## Table of Contents

- [Introduction](#introduction)
- [Project Goals](#project-goals)
- [Datasets](#datasets)
- [Input](#input)
- [System Architecture](#system-architecture)
- [Import Mode Application](#import-mode-application)
- [Recommendation Agent Application](#recommendation-agent-application)
- [Output](#output)
- [Project Structure](#project-structure)
- [How to Run](#how-to-run)

---

## Introduction

This project demonstrates an agent-based approach to document recommendation using vector embeddings.  
Documents are imported, embedded, and stored in a database, while user queries are processed by an agent to return semantically relevant recommendations.

---

## Project Goals

- Build an agent-based recommendation system  
- Support semantic (meaning-based) search using embeddings  
- Apply clean architecture principles  
- Enable modular extension through plug-ins (tools)  
- Use two datasets  

---

## Datasets

- **Books Dataset**  
  Book descriptions used for recommendation 

- **User Support Dataset**  
  FAQ and troubleshooting documents used to answer user problems

---

## Input

### Import Mode Input
- Documents from configurable directories
- Supported formats:
  - `.txt`
  - `.docx`
  - `.pdf`

### Recommendation Agent Input
- Natural language user query  
  Example:
  ```
  Recommend a fantasy book about magic
  ```

---

## System Architecture

The system consists of two independent console applications connected through a shared database:

- **Import Mode Application**  
  Handles document ingestion, text extraction, and embedding generation

- **Recommendation Agent Application**  
  Handles user queries, intent processing, similarity search, and recommendation output

A relational database stores document embeddings and metadata.

---

## Import Mode Application

- Import documents from configurable directories  
- Extracts text using a preprocessing interface  
- Generates embeddings using a predefined model  
- Stores embeddings and metadata in SQL Server  

---

## Recommendation Agent Application

- Provides a console-based user interface  
- Uses an agent to map queries to intent via plug-ins  
- Generates embeddings for the extracted intent  
- Performs cosine similarity matching against stored embeddings  
- Ranks and selects the most relevant documents  

---

## Output

- Primary recommended document  
- Optional Top-N ranked recommendations  
- Includes metadata such as document name, category, and URL  

---

## Project Structure

```
ImportMode.Console
RecommendationAgent.Console
Core
Application
Infrastructure
Plugins
```

---



## Project Members

1. **Tusar Mozumder** – 1565539  
2. **Jony Akter** – 1628780  
3. **Md. Zobyaer Sheikh** – 156402

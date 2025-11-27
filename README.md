# Contract Intelligence Engine
*An AI-powered system that analyses contracts using RAG, clause extraction, risk detection, and structured reasoning.*

---

## 🌍 Overview
The Contract Intelligence Engine is an LLM-powered contract analysis system designed to interpret long, complex legal or commercial documents.

It uses:
- Retrieval-Augmented Generation (RAG)  
- Embeddings + vector search  
- Clause extraction  
- Risk detection  
- Compliance checking  
- Structured JSON output  

This project is part of a 3-project portfolio demonstrating advanced AI engineering (UK Global Talent technical track).

---

## 🎯 Problem Statement
Contract review is slow and error-prone because:

- Contracts are long and dense  
- Key clauses are difficult to locate  
- Risks may be hidden in legal language  
- Comparing against standards takes time  

Traditional manual review can take hours or days.

---

## 🚀 Solution
The Contract Intelligence Engine uses AI to:

- Ingest and parse contract documents  
- Split text into semantically meaningful chunks  
- Build embeddings and store them in a vector DB  
- Retrieve the most relevant sections for a query  
- Apply LLM reasoning to assess risks and compliance  
- Generate structured reports  

This creates a faster, more consistent contract review workflow.

---

## 🧩 Key Features

### ✔ Contract Ingestion  
Supports PDF, DOCX, TXT.

### ✔ Clause-Level Splitting  
Preserves clause numbering and legal structure.

### ✔ Embeddings + Vector Search  
Semantic contract retrieval using OpenAI embeddings or SentenceTransformers.

### ✔ RAG Query Engine  
Retrieves top-k relevant contract chunks.

### ✔ Risk Analysis & Compliance  
Highlights:  
- Non-standard clauses  
- Liability issues  
- Missing terms  
- SLA inconsistencies  
- Supplier-leaning conditions  

### ✔ Structured JSON Output  
Machine-readable results for dashboards or downstream systems.

### ✔ Reporting Engine  
Generates summaries, risks, and clause-level insights.

---

## 🏗 Architecture

### High-Level Architecture  
Image stored at:

### Mermaid Diagram  

---

## 🧠 Technical Stack

| Layer        | Technology                          |
|--------------|--------------------------------------|
| Backend      | FastAPI (Python)                     |
| LLM Engine   | OpenAI / Anthropic                   |
| RAG Engine   | LangChain / LlamaIndex               |
| Embeddings   | text-embedding-3-large / SentenceTF  |
| Vector Store | Supabase / Pinecone / Chroma         |
| Parsing      | PyPDF2 / pdfplumber / docx2txt       |
| Frontend     | React (planned)                      |

---

## 🔬 Research Notes
Detailed technical analysis is documented in:


This includes:
- RAG pipeline design  
- Embeddings  
- Clause extraction logic  
- Retrieval methods  
- Risk analysis methodology  

---

## 🛠 Installation (Coming Soon)
Additional setup instructions will be added as development progresses.

---

## 📅 Roadmap

### Phase 1 — Core Pipeline
- [x] Architecture design  
- [x] Research notes  
- [ ] Document ingestion module  
- [ ] Clause splitting  
- [ ] Embedding generation  
- [ ] Vector DB integration  

### Phase 2 — RAG Engine
- [ ] Top-k retrieval  
- [ ] Semantic search tuning  
- [ ] Chunk metadata mapping  

### Phase 3 — Risk Analysis
- [ ] Risk scoring model  
- [ ] Clause comparison to standards  
- [ ] Compliance checks  

### Phase 4 — Frontend & Deployment
- [ ] React dashboard  
- [ ] API endpoints  
- [ ] Docker & cloud hosting  

---

## 📜 License
MIT License.

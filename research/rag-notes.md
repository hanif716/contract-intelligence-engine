RAG Pipeline – Technical Research Notes

Project: Contract Intelligence Engine
Author: Hanif Hazrati

🧠 1. Purpose of RAG in Contract Intelligence

Contracts contain:

long sections of dense legal text,

complex clauses,

obligations,

liabilities,

termination rules,

SLAs,

compliance requirements.

Because LLMs cannot store large documents in memory, we use a RAG pipeline (Retrieval-Augmented Generation) to provide the model with the relevant parts of the document on demand.

RAG solves:

✔ context overflow
✔ hallucinations
✔ inaccurate or outdated contract interpretation
✔ misclassification of clauses

RAG provides precise, clause-level grounding.

🧩 2. The Full Contract Analysis Pipeline

The Contract Intelligence Engine uses the following RAG-based architecture:

Document Ingestion

PDF/Text Extraction

Cleaning & Pre-processing

Chunking

Embedding Generation

Vector Database Storage

RAG Query Engine

Risk & Compliance Analysis

Report Generation

Each step is detailed below.

📥 3. Document Ingestion

Supported formats:

PDF

DOCX

TXT

Tools:

PyPDF2

PDFMiner

Docx2txt

Key Responsibility:

Extract contract text without distortion

Preserve clause numbering as much as possible

🧹 4. Pre-processing Stage

Before chunking, text is cleaned:

Remove headers/footers

Fix line breaks

Standardise lists and bullet points

Remove repeated footers in scanned PDFs

This creates a smooth, clean text representation of the contract.

🪓 5. Text Chunking

Contracts can be 20–200 pages.
Chunking splits them into small, meaningful sections.

Methods:

Recursive Character Text Splitter (LangChain)

Semantic-based chunking

Clause-based splitting using regex patterns (e.g., “1.”, “2.1”, “2.1.3”)

Typical chunk sizes:

300–800 tokens per chunk

This ensures RAG returns relevant legal clauses, not unrelated sections.

🧬 6. Embedding Generation

Embeddings convert text into numerical vectors, allowing semantic search.

Embedding models:

OpenAI text-embedding-3-large

SentenceTransformers

Cohere embeddings

Llama 3 embeddings

Embedding requirements:

Stable cosine similarity

High dimension for legal detail

Low drift across versions

🗄 7. Vector Database Storage

Vector stores enable fast and accurate clause retrieval.

DB Options:

Supabase Vector DB (recommended)

Pinecone

Chroma

Stored data:

{
  "chunk_id": "",
  "text": "",
  "embedding": [...],
  "page_number": "",
  "clause_number": ""
}

🔎 8. Retrieval

The RAG Query Engine retrieves relevant chunks based on:

duty-of-care

limitation of liability

warranties

termination rules

pricing

SLA details

risks

Retrieval Techniques:

k-NN semantic search

Max Marginal Relevance (MMR)

Hybrid: keyword + embedding

🤖 9. LLM Reasoning Layer

The LLM receives:

The user question

Top retrieved chunks

Clause context

It produces:

Summaries

Risk assessments

Missing clause detection

Compliance grading

Obligation extraction

This is the heart of the Contract Intelligence Engine.

⚠️ 10. Risk & Clause Analysis

RISK agent identifies:

Non-standard clauses

High liability exposure

Missing terms

Inconsistent SLAs

Weak termination rights

Supplier-biased language

Compliance areas:

GDPR

NHS procurement rules

Clinical safety requirements

FM/Estates obligations

📊 11. Report Generation

Outputs:

Executive summary

Key risks

Clause summaries

Missing clause report

Compliance gap analysis

Structured JSON

Optional PDF export

This is converted into the UI and shared with the user.

🧪 12. Example RAG Query Flow (Pseudo-Code)
def analyze_contract(query):
    chunks = vector_db.search(query, top_k=5)
    context = "\n".join([c.text for c in chunks])

    prompt = f"""
    You are a contract analysis assistant.
    Question: {query}
    Relevant Contract Sections: {context}
    Provide risk assessment and clause summary.
    """

    response = llm.generate(prompt)
    return response

🔧 13. Tools Used

AI:

OpenAI GPT-4.1

Claude 3.5 Sonnet

Embedding models

RAG Framework:

LangChain

LlamaIndex

Supabase Vector DB

Backend:

FastAPI

Python

Frontend:

React

🌟 14. Why This is Strong for UK Global Talent Visa

This research demonstrates:

✔ Advanced NLP & RAG design

Showing deep technical understanding.

✔ Hands-on engineering

This is implementation-level knowledge.

✔ Innovation in your field

Contract NLP + RAG is new and highly valuable.

✔ Significant impact potential

For procurement, legal teams, and FM operations.

This supports:

Mandatory Criterion (Innovation)

Optional Criterion (Technical Contribution)
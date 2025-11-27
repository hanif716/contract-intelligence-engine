# Roadmap – Contract Intelligence Engine

## Phase 1 — Foundations
- [x] Project repository created
- [x] Architecture diagram added
- [x] Research notes completed
- [ ] Add `.env.example` + configuration templates
- [ ] Define base folder structure for backend

## Phase 2 — Document Processing
- [ ] PDF ingestion module
- [ ] DOCX ingestion module
- [ ] Text normalisation
- [ ] Clause segmentation engine
- [ ] Clause numbering + metadata extraction

## Phase 3 — Embedding & Vector Store
- [ ] Embedding generator (OpenAI or ST)
- [ ] Chunk metadata mapping
- [ ] Vector DB integration (Pinecone / Supabase / Chroma)
- [ ] Bulk ingestion pipeline

## Phase 4 — RAG Engine
- [ ] Top-k semantic retrieval
- [ ] Context builder
- [ ] Answer generation
- [ ] Citation mapping (clause references)

## Phase 5 — Risk & Compliance
- [ ] Missing clause detection
- [ ] Non-standard term detection
- [ ] Liability + SLA risk identification
- [ ] Structured risk output

## Phase 6 — Backend API (FastAPI)
- [ ] `/ingest` endpoint
- [ ] `/query` endpoint (RAG)
- [ ] `/risks` endpoint
- [ ] Validation + error handling

## Phase 7 — Frontend (React Dashboard)
- [ ] Upload contract UI
- [ ] Display clauses
- [ ] Display risk insights
- [ ] Download summaries

## Phase 8 — Testing & QA
- [ ] Unit tests for segmentation
- [ ] Integration tests for RAG queries
- [ ] Example contracts + example outputs

## Phase 9 — Deployment
- [ ] Docker setup
- [ ] Deploy backend
- [ ] Deploy dashboard

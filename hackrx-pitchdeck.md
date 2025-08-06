# Slide 1: Team Name & Members

**Team Name:** Synapse

**Members:**
- Dipan Dhali (2026, IIITDM Jabalpur)
- Krishnand Yadav (2026, IIITDM Jabalpur)
- Devesh Gangani (2026, IIITDM Jabalpur)
- Deepnarayan Sett (2026, IIITDM Jabalpur)

---

# Slide 2: About Us

- SIH Finalist 2024 (Standardizing Odd School Structures)
- HackByte 2025 National Hackathon winners (Sault: secure blockchain document management)
- Experience in multi-agent systems, knowledge graphs, and AI document intelligence

---

# Slide 3: Problem Statement & Solution Overview

**Problem:**
Current LLM document QA systems (RAG) are brittle, shallow, and lack reasoning. They fail on multi-hop queries, context fragmentation, and dynamic updates.

**Solution:**
Synapse: A cognitive agent framework for dynamic document intelligence. Multi-agent, graph-based, self-correcting, and radically transparent. Answers complex queries over unstructured docs with deep reasoning, real-time updates, and explainable outputs.

---

# Slide 4: Process Flow (Mermaid)

```mermaid
flowchart TB
    subgraph Ingestion
      A[Input Documents (PDF, Word, Email)] --> B[Text Extraction (OCR/Text Parsing)]
      B --> C[Chunking & Preprocessing]
      C --> D[Embed & Index in Vector DB]
    end

    subgraph Query Handling
      Q[User Query] --> E[Query Parsing (LLM/NLU)]
      E --> F[Semantic Search in Vector DB]
      F --> G[Retrieve Top-K Clauses]
      G --> H[LLM Reasoner + Rule Engine]
      H --> I[Decision JSON & Clause References]
    end

    style Ingestion fill:#f9f,stroke:#333,stroke-width:2px
    style Query Handling fill:#bbf,stroke:#333,stroke-width:2px
```

---

# Slide 5: Tech Stack

- **Cloud:** Azure/AWS (OpenAI Service, Bedrock)
- **Vector DB:** Qdrant, Pinecone, Neo4j (GraphRAG)
- **Backend:** Python (FastAPI), LangChain, Haystack
- **Frontend:** React/Streamlit
- **Document Parsing:** unstructured.io, Apache Tika, Textract
- **LLM Models:** GPT-4o, Claude 3 Opus, Llama3
- **Security:** Encryption, RBAC, audit logs

---

# Slide 6: Solution Architecture (Mermaid)

```mermaid
flowchart LR
  subgraph Doc-Ingestion[Document Ingestion Pipeline]
    A1[Source Docs (PDF/Word/Email)] --> A2[Preprocessor (OCR/TextParser)]
    A2 --> A3[Sentence/Clause Splitting]
    A3 --> A4[Embedding Engine (OpenAI/HF)]
    A4 --> A5[Vector DB (Qdrant/Pinecone)]
    A3 --> A6[Knowledge Graph Loader (Neo4j)]
    A6 --> A7[Clause-Entity Graph]
  end
  subgraph Query-Answering[Query & Answer Pipeline]
    B1[User Query] --> B2[LLM/NLP Parser]
    B2 --> B3[Create Query Embedding]
    B3 --> A5
    A5 --> C1[Retrieve Top-K Chunks]
    B2 --> C2[Extract Query Facts]
    C1 --> C3[Combine with C2]
    C3 --> D1[LLM Decision Engine]
    A7 --> D1
    D1 --> D2[Format Output JSON]
    D2 --> B4[Return: Decision JSON]
  end
```

---

# Slide 7: Unique Selling Points (USP)

- Hybrid GraphRAG: Combines semantic search and knowledge graph traversal for deep, multi-hop reasoning
- Multi-agent, self-correcting workflow (LangGraph)
- Radical transparency: Interactive reasoning path visualization
- Structured, auditable JSON outputs
- Real-time, incremental graph updates

---

# Slide 8: Future Enhancements

- Multi-lingual support
- Interactive QA (clarifying questions)
- Continuous learning from user feedback
- Advanced multimodal parsing (images, emails)
- High-availability, scalable cloud deployment

---

# Slide 9: Risks, Challenges, Dependencies

- LLM hallucination risk (mitigated by output grading, human-in-loop)
- Data quality (robust OCR, error handling)
- Regulatory compliance (GDPR, PII masking)
- Performance at scale (vector DB sharding, caching)
- API cost/dependency (open-source fallback)
- Ethical bias (prompt guidelines, manual override)

---

# Slide 10: Acceptance Criteria Coverage

- Multi-format ingestion (PDF, Word, email)
- Robust query understanding (LLM/NLP)
- Semantic clause retrieval (RAG, GraphRAG)
- Logical decision making (LLM + rule engine)
- Explainable, structured output (JSON, clause references)
- Downstream usability (API, audit logs)
- Innovation (multi-modal, agentic, secure)

---

# Slide 11: Anything Else

- Team passionate about AI, security, and compliance
- Demo: Query highlights policy clauses as justification
- Unique, battle-tested approach (hackathon, blockchain experience)
- Ready to transform claim adjudication with cutting-edge AI

---

# Slide 12: References & Citations

- See sources in `data.md` (Reddit, MDPI, Neo4j, LangChain, Haystack, OpenAI, etc.)
- Regulatory compliance, GraphRAG, agentic workflows, explainable AI

---

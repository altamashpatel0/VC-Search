# VC Search

> A private, single-user, continuously running web search engine built from the ground up.

VC Search is a personal search engine designed to provide fast, relevant and continuously refreshed web search across trusted devices.

The goal is not to create a copy of Google or another existing search engine. VC Search is being designed as its own search infrastructure — including its crawler, URL discovery system, index, retrieval pipeline and ranking engine.

---

## Vision

Build a personal search engine that:

- Continuously discovers and crawls the public web
- Maintains its own searchable index
- Provides extremely fast search results
- Continuously refreshes changing web content
- Uses its own ranking and retrieval system
- Supports semantic and keyword-based search
- Provides optional AI-powered answers with sources
- Works across PC, Android and iPhone
- Runs continuously in the cloud
- Is designed for one private user

---

## Core Architecture

```text
                         INTERNET
                            │
                            ▼
                    URL DISCOVERY
                            │
                            ▼
                     URL FRONTIER
                            │
                            ▼
                  CONTINUOUS CRAWLERS
                            │
                            ▼
                   CONTENT PROCESSING
                            │
                            ▼
                  ┌──────────────────┐
                  │   SEARCH INDEX   │
                  │                  │
                  │ Lexical Index    │
                  │ Semantic Index   │
                  │ Metadata         │
                  │ Link Data        │
                  └────────┬─────────┘
                           │
                           ▼
                    SEARCH / RETRIEVAL
                           │
                           ▼
                       RANKING
                           │
                           ▼
                      SEARCH API
                           │
              ┌────────────┼────────────┐
              ▼            ▼            ▼
             PC         Android       iPhone
```

---

## Project Structure

```text
VC-Search/
│
├── backend/              # Search API and backend services
├── crawler/              # Web crawling and URL discovery
├── docs/                 # Architecture and project documentation
├── indexer/              # Document processing and indexing
├── infrastructure/       # Docker, cloud and deployment configuration
├── ranking/              # Search ranking and relevance systems
├── scripts/              # Development and operational scripts
├── tests/                # Automated tests
│
├── .gitignore
├── LICENSE
└── README.md
```

---

## Development Roadmap

### Phase 0 — Architecture & Foundations

- [x] Create project repository
- [x] Initialize Git
- [x] Create base project structure
- [ ] Define system architecture
- [ ] Define data models
- [ ] Define API contracts
- [ ] Benchmark search-index technologies
- [ ] Define local development environment
- [ ] Define cloud deployment strategy

### Phase 1 — Search Core

- [ ] Document ingestion
- [ ] Search index
- [ ] Query processing
- [ ] Initial ranking
- [ ] Fast search API
- [ ] Search benchmark system

### Phase 2 — Web Crawler

- [ ] Asynchronous crawler
- [ ] URL discovery
- [ ] HTML parsing
- [ ] Metadata extraction
- [ ] Canonical URL handling
- [ ] Duplicate detection
- [ ] robots.txt handling
- [ ] Crawl state management

### Phase 3 — Continuous Crawling

- [ ] Persistent URL frontier
- [ ] Crawl priorities
- [ ] Recrawl scheduling
- [ ] Retry system
- [ ] Domain throttling
- [ ] Change-frequency estimation
- [ ] Automatic worker recovery

### Phase 4 — Scalable Index

- [ ] Incremental indexing
- [ ] Index optimization
- [ ] Compression
- [ ] Caching
- [ ] Storage optimization
- [ ] Sharding strategy
- [ ] Replication strategy

### Phase 5 — Ranking Engine

- [ ] BM25 / lexical relevance
- [ ] Semantic retrieval
- [ ] Freshness signals
- [ ] Authority signals
- [ ] Content quality signals
- [ ] Duplicate/spam detection
- [ ] Ranking evaluation framework

### Phase 6 — AI Search

- [ ] Query understanding
- [ ] Search-result synthesis
- [ ] AI summaries
- [ ] Source citations
- [ ] Follow-up search
- [ ] AI-assisted research

### Phase 7 — Search Categories

- [ ] Web search
- [ ] News search
- [ ] Image search
- [ ] PDF/document search
- [ ] Code search
- [ ] Academic search
- [ ] Video metadata search

### Phase 8 — Multi-Device

- [ ] Web/PC client
- [ ] Android application
- [ ] iPhone application
- [ ] Secure device authentication
- [ ] Search synchronization
- [ ] Saved searches/results

### Phase 9 — Cloud Infrastructure

- [ ] Cloud deployment
- [ ] Continuous workers
- [ ] Monitoring
- [ ] Logging
- [ ] Health checks
- [ ] Automatic recovery
- [ ] Backups
- [ ] Resource monitoring
- [ ] Cost monitoring

### Phase 10 — VC Search OS

- [ ] Conversational search
- [ ] Voice search
- [ ] VC AI integration
- [ ] Personal/private data search
- [ ] Research workflows
- [ ] Knowledge management

---

## Technology Direction

| Component | Initial Direction |
|---|---|
| Backend | FastAPI |
| Crawler | Python + Async |
| Database | PostgreSQL |
| Queue | Redis initially |
| Search Index | To be benchmarked |
| Vector Search | To be benchmarked |
| Cache | Redis |
| AI | Ollama / optional cloud models |
| Web Client | React / Next.js |
| Android | Kotlin |
| iPhone | Swift / SwiftUI |
| Infrastructure | Docker + Cloud |
| Monitoring | Prometheus + Grafana |

Technology choices are not considered final until they are benchmarked against the project's performance, scalability and operational requirements.

---

## Performance Goals

VC Search is designed around low-latency indexed search.

Target principles:

- Search should not wait for live web crawling.
- Frequently changing content should be refreshed automatically.
- Core search should target very low latency.
- AI generation should remain separate from the normal search path.
- Crawler failures should not stop the search service.
- Performance should be measured with repeatable benchmarks.

---

## Privacy & Security

VC Search is designed as a private single-user system.

Planned principles:

- One authorized user
- Secure device authentication
- Encrypted communication
- No public registration system
- No unnecessary multi-user infrastructure
- Separate personal/private data from public-web indexing
- Secure secrets management
- Automated backups

---

## Important Design Principle

> **VC Search is a search infrastructure project, not a search UI project.**

The core system comes first:

```text
DISCOVERY
    ↓
CRAWLING
    ↓
PROCESSING
    ↓
INDEXING
    ↓
RETRIEVAL
    ↓
RANKING
    ↓
SEARCH API
    ↓
CLIENTS
```

The user interface will be built on top of this infrastructure.

---

## Current Status

**Version:** `V0.1 — Phase 0`

**Status:** Architecture & Foundations

The repository has been initialized and the initial project structure has been created.

---

## Long-Term Goal

Build a continuously running personal search infrastructure capable of discovering, indexing and searching a large portion of the public web while providing fast, relevant and private access from the user's devices.

VC Search should evolve from a search engine into a personal search and research platform.

---

## License

This project is currently intended as a private personal project.

License details will be finalized during the project setup phase.

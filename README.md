# Resume Re-factorer  
AI-Driven Resume and Career Optimization Platform

---

## What is Resume Re-factorer?

Resume Re-factorer is a full-stack AI-powered system designed to analyze, restructure, and optimize resumes for modern hiring pipelines.

Rather than simply generating content, it systematically improves resumes by aligning them with job descriptions, enhancing keyword relevance, strengthening impact statements, and preparing candidates for interviews and professional outreach.

It combines structured backend orchestration with large language models to deliver consistent, repeatable, and configurable outputs.

---

## Why “Re-factorer”?

The name is intentional.

In software engineering, refactoring means improving internal structure without changing core functionality. Resume Re-factorer applies the same principle to resumes:

- The candidate’s experience remains authentic.
- The structure, clarity, and alignment are improved.
- Redundancy is removed.
- Impact is strengthened.
- Relevance to the target role is optimized.

This project treats a resume like code — something that can be reviewed, analyzed, improved, and restructured for better performance.

---

## What problem does this project solve?

Modern hiring processes rely heavily on:

- Applicant Tracking Systems (ATS)
- Keyword-based ranking
- Structured screening
- Automated filtering

Strong candidates are often filtered out due to formatting, keyword gaps, or poor alignment with job descriptions.

Resume Re-factorer addresses this by:

- Tailoring resumes and cover letters to specific job descriptions
- Improving ATS keyword alignment
- Generating interview preparation material
- Producing networking outreach templates
- Converting structured markdown resumes into professional PDFs

It supports a complete job application workflow rather than just document formatting.

---

## What is the architecture?

This is a full-stack application with clear separation of concerns.

### Frontend
- React 19  
- TypeScript  
- Component-based architecture  
- API-driven communication  

### Backend
- Java 21  
- Spring Boot 3.x  
- RESTful APIs  
- Service-layer orchestration  
- Structured validation and error handling  

### AI Layer
- OpenAI-compatible endpoints  
- Ollama local model support  
- Configurable model selection  
- Backend-managed prompt orchestration  

### Deployment
- Docker and Docker Compose  
- SQLite (local setup)  
- PostgreSQL (production-like configuration)  

The entire stack is containerized for consistent and reproducible environments.

---

## How does the resume optimization workflow work?

1. User provides:
   - Resume  
   - Target job description  

2. Backend processing:
   - Extracts and structures content  
   - Maps resume content to job requirements  
   - Enhances alignment and keyword density  
   - Improves phrasing and clarity  

3. AI enrichment:
   - Skill gap detection  
   - Certification suggestions  
   - Interview question generation  
   - Networking outreach drafts  

4. Output:
   - Structured markdown  
   - Optional PDF conversion  

All AI orchestration is handled server-side to maintain control, extensibility, and consistency.

---

## What APIs are exposed?

### Core Processing
- `POST /api/upload`  
- `POST /api/process/skills`  
- `POST /api/markdownFile2PDF`  

### Interview Generation
- `POST /api/generate/interview-hr-questions`  
- `POST /api/generate/interview-job-specific`  
- `POST /api/generate/interview-reverse`  

### Networking Templates
- `POST /api/generate/cold-email`  
- `POST /api/generate/cold-linkedin-message`  
- `POST /api/generate/thank-you-email`  

### System
- `GET /api/health`  

The API layer is stateless and structured for extensibility and integration.

---

## How is the codebase organized?

```
resume-refactorer/
├── frontend/                 # React + TypeScript UI
├── src/                      # Spring Boot backend
│   ├── main/java/
│   └── test/java/
├── docs/
├── docker-compose.yml
├── build.gradle
└── config.json
```

### Backend Structure
- Controller layer (HTTP handling)  
- Service layer (business logic + AI orchestration)  
- Configuration and persistence layer  
- Unit and integration tests  

---

## How do I run it locally?

Recommended approach:

```bash
git clone https://github.com/ashlesha-shrikhande/resume-refactorer.git
cd resume-refactorer
docker compose up -d
```

If using a local model with Ollama:

```bash
docker exec resume-ollama ollama pull mistral:latest
```

Access:
- Frontend: http://localhost:3000  
- Backend: http://localhost:8080  

The system can run fully locally without external cloud dependencies.

---

## What design decisions strengthen this project?

- Separation between AI orchestration and domain logic  
- Configurable model abstraction (no vendor lock-in)  
- Backend-driven prompt management  
- Containerized, reproducible environment  
- Extensible REST API structure  
- Clear layered architecture  

It is structured as a maintainable AI-enabled application rather than a simple LLM wrapper.

---

## Who is this project for?

- Engineers exploring Spring Boot + LLM integration  
- Developers building production-ready AI systems  
- Job seekers wanting structured AI-driven optimization  
- Contributors interested in full-stack AI architecture  

---

## What are potential future enhancements?

- Multi-user authentication and session management  
- Resume performance analytics dashboard  
- Rate limiting and AI usage monitoring  
- Observability (metrics, logging, tracing)  
- Prompt versioning strategy  
- CI/CD pipeline automation  

---

## Why does Resume Re-factorer stand out?

This project demonstrates:

- Backend-centric AI orchestration  
- Structured API design  
- Multi-feature AI integration  
- Containerized deployment  
- Production-oriented engineering decisions  

It applies software engineering principles to career optimization, treating resumes as structured artifacts that can be improved systematically.

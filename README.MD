# Signal

![Signal Screenshot](https://abruno.net/github-share-signal.png)

[Signal is a multi-service portfolio system](https://signal.abruno.net) built to explore modern developer workflows with AI — framed as a conversational experience to make my engineering work discoverable and approachable. It brings together a Next.js frontend, an Express backend with ChromaDB, and an MCP-compatible server for live API actions, all supported by a shared dev-config package for consistent linting, formatting, and release automation.

The goal isn’t to ship a product, but to show how I approach developer experience, architecture clarity, and maintainability through well-structured services, shared standards, and clear documentation.

[**See it in action →**](https://signal.abruno.net)

## Why?

Signal is a proof point for how emerging AI workflows like Retrieval-Augmented Generation (RAG) and Model Context Protocol (MCP) can be designed into practical systems. It’s less about a chatbot and more about demonstrating how I approach multi-service architecture, standards, and developer enablement.

## Architecture overview

Signal is made up of four core services:

- [Frontend](https://github.com/anthonybruno/signal-frontend) – Next.js interface for real-time chat and AI-powered interactions
- [Backend](https://github.com/anthonybruno/signal-backend) – Node.js + Express API layer
- [RAG server](https://github.com/anthonybruno/signal-rag) – Document retrieval service built on ChromaDB for contextual memory
- [MCP server](https://github.com/anthonybruno/signal-mcp) – MCP-compatible service for live API integrations (GitHub, Spotify, blog)

The frontend sends requests to a thin backend that performs intent analysis and routing. Depending on the request, it may pull context from the RAG server, call tools through the MCP server, or go directly to the model. The backend assembles a prompt, calls OpenRouter, and streams the response back to the frontend. Shared [dev-config](https://www.npmjs.com/package/abruno-dev-config) keeps services consistent while remaining independently deployable.

```
Request
  │
  ▼
Frontend
  │
  ▼
Backend API
  │
  ▼
Smart routing and intent analysis
  │
  ├──────────────┬──────────────┬──────────────┐
  │              │              │              │
  ▼              ▼              ▼              ▼
RAG server    MCP server    Direct path    Guardrails
(personal)    (live data)   to model       auth and limits
  │              │              │              │
  └──────────────┴──────────────┴──────────────┘
                     │
                     ▼
Prompt assembly and OpenRouter processing
(with base instructions and retrieved context when present)
                     │
                     ▼
Streaming response
                     │
                     ▼
Frontend display
```

## Tech stack

- Frontend: Next.js, Tailwind
- Backend: Node.js, Express
- Data: ChromaDB (RAG)
- Integrations: Model Context Protocol (MCP), OpenRouter
- Ops: Docker, GitHub Actions, semantic-release

## How to explore

- [See it in action](https://signal.abruno.net)
- [Frontend](https://github.com/anthonybruno/signal-frontend)
- [Backend](https://github.com/anthonybruno/signal-backend)
- [RAG server](https://github.com/anthonybruno/signal-rag)
- [MCP server](https://github.com/anthonybruno/signal-mcp)
- [Dev Config](https://www.npmjs.com/package/abruno-dev-config)

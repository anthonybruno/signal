![Signal Screenshot](https://signal.abruno.net/og-share.png)

Signal is an interactive portfolio built as a multi-service system. Instead of a static page, it gives you a conversational way to explore my work, projects, and leadership experience. Under the hood, it demonstrates how I approach frontend craft, system design, and modern AI workflows.

[**See it in action →**](https://signal.abruno.net)

## Why?

Signal is a proof point. It shows how I design systems that balance clarity, maintainability, and developer experience, while experimenting with modern AI patterns like Retrieval-Augmented Generation (RAG) and Model Context Protocol (MCP).

It's less about shipping a product and more about demonstrating service boundaries, shared standards, and production-minded practices in a portfolio context.

## Architecture overview

![Signal Architecture](https://github.com/user-attachments/assets/9ae777bb-9564-4168-8e72-9ffbc743ae5c)

## Tech stack

- **Frontend:** Next.js 15, React 19, Tailwind CSS, TypeScript
- **Backend:** Node.js + Express
- **Retrieval:** ChromaDB (RAG) with OpenAI embeddings
- **Integrations:** Model Context Protocol (MCP) server for GitHub, Spotify, and blog
- **Model orchestration:** OpenRouter (Gemini Flash 2.5) with tool-calling enabled
- **Dev tooling:** ESLint, Prettier, Husky, and shared configs via [dev-config](https://www.npmjs.com/package/abruno-dev-config)
- **Ops:** Docker for portability, GitHub Actions + semantic-release for automation
- **Hosting:** Fly.io

## Explore

- [Live demo](https://signal.abruno.net)
- [Frontend repo](https://github.com/anthonybruno/signal-frontend)
- [Backend repo](https://github.com/anthonybruno/signal-backend)
- [RAG repo](https://github.com/anthonybruno/signal-rag)
- [MCP repo](https://github.com/anthonybruno/signal-mcp)
- [Shared dev config](https://www.npmjs.com/package/abruno-dev-config)

## Why it matters

Signal is both portfolio and proof point. It shows my **frontend expertise** through a polished, real-time chat interface. It demonstrates **system-level thinking** with clear service boundaries and shared standards. It reflects a **leadership mindset** by focusing on maintainable, documented systems that align with real-world production practices.

At a higher level, Signal reflects how I think about building systems that balance **clarity, maintainability, and team enablement**.

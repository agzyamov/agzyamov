## Rustem Agziamov

Forward Deployed Engineer at EPAM. I work on agentic delivery: getting AI agents to do real work inside a software lifecycle, from a written spec to tasks, pull requests and deployment.

I started as a software developer in 2006 and led a development team, then spent ten years in business analysis, product and project management. I speak on agentic AI and publish working examples here.

### What I build

- AI-native SDLC workflows, where an agent picks up a work item, writes the spec and opens the pull request
- Integrations that bring coding agents into the tools teams already use: Azure DevOps, GitHub Actions

### Featured: SDLC Research RAG

[sdlc-research-rag](https://github.com/agzyamov/sdlc-research-rag) is an open-source retrieval-augmented generation system over arXiv research on AI across the software development lifecycle. It answers questions with source citations, extracts structured findings from papers, and maps the field as a research landscape and a knowledge graph.

- **Retrieval:** hybrid dense and BM25 search in Qdrant with reciprocal rank fusion, cross-encoder reranking (bge-reranker-v2-m3) and Qwen3 embeddings, tuned with a retrieval parameter sweep
- **Generation:** LangGraph pipeline on Claude with streamed answers and per-claim citations
- **Knowledge graph:** LLM fact extraction with verbatim-quote verification, stored in Neo4j with neo4j-graphrag entity resolution
- **Ingestion:** arXiv OAI-PMH harvesting, Docling PDF parsing with multimodal figure understanding, and incremental indexing through the LangChain Indexing API, orchestrated by Dagster
- **Access control:** relationship-based authorization (OpenFGA) applied as a retrieval pre-filter, so every answer respects each paper's license
- **Evaluation and observability:** DeepEval metrics (contextual precision and recall, faithfulness, answer relevancy, G-Eval) measured against a long-context baseline; Langfuse tracing
- **Engineering:** per-task model routing across the Anthropic API, OpenAI-compatible gateways and local models (Ollama); FastAPI with a generated OpenAPI contract and a typed React client (assistant-ui, Sigma.js); architecture documented in SEI Views and Beyond and enforced in CI; Playwright acceptance and accessibility tests

### Start here

- [ghcp-cli-in-actions-demo](https://github.com/agzyamov/ghcp-cli-in-actions-demo): Copilot CLI and the Copilot coding agent running in GitHub Actions. Fork it and try it
- [ado-copilot](https://github.com/agzyamov/ado-copilot): mention `@copilot` in an Azure DevOps work item discussion and get an answer that uses the work item's context

### Stack

Claude Code · GitHub Copilot · Cursor · GitHub Actions · Azure DevOps · Amazon Bedrock AgentCore · LangGraph · Qdrant · Neo4j

Cloud and data: AWS · Azure · Databricks

### Contact

[LinkedIn](https://www.linkedin.com/in/agziamov). We're hiring AI-native engineers at EPAM Türkiye. If you build and ship agents in production, message me.

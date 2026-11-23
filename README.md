# Recall — Knowledge Retrieval System

**AI-assisted knowledge retrieval and workflow automation using n8n, Google Drive, and JavaScript.**

## Overview

Recall is a personal engineering knowledge retrieval system designed to make technical documentation easier to discover and reuse.

The project explores how structured knowledge can be retrieved from existing Markdown documentation and made accessible through an API.

It is developed using AI-assisted engineering practices with OpenAI Codex and Claude Code.

## Technology Stack

- **Workflow orchestration:** n8n
- **Knowledge source:** Google Drive and Markdown documents
- **Custom logic:** JavaScript
- **Integration:** Google Drive REST API and OAuth 2.0
- **Hosting:** AWS
- **Interface:** HTTP webhook returning structured JSON

## How Recall Works

1. Receives a search query through an HTTP webhook.
2. Discovers eligible knowledge folders in Google Drive.
3. Searches for Markdown documents.
4. Downloads candidate document content.
5. Scores documents using keyword matches, concept coverage, and recency.
6. Ranks results and returns the most relevant documents with excerpts.

## Current Capabilities

- Google Drive folder discovery
- Markdown document retrieval
- JavaScript-based relevance scoring
- Document ranking and selection
- Structured JSON responses
- Webhook-based integration

## Engineering Challenges

The project is being refined to address several retrieval reliability concerns:

- Candidate limits applied before relevance scoring
- Incomplete pagination during document discovery
- Reliable association of document metadata with downloaded content
- Handling special characters in search queries
- Graceful handling of empty search results

These are ongoing improvements, not completed fixes.

## Future Development

- Integrate an LLM to generate grounded answers from retrieved documents
- Improve retrieval accuracy and evaluation
- Explore semantic search and embeddings
- Provide retrieval capabilities to AI coding agents

## Source Code

The repository includes a sanitized n8n workflow export:

`recall-workflow-public.json`

Sensitive configuration values and credentials are excluded from the public version.

## Project Status

**Active personal development project.**

The retrieval workflow is deployed on AWS. The public repository contains a sanitized workflow definition for technical review rather than a fully configured, immediately runnable deployment.

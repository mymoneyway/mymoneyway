# System Patterns

## System Architecture

- FastAPI Python backend for chatbot logic and API handling.
- Angular TypeScript frontend for user interaction.
- Python scripts for parsing, storing, embedding.
- DynamoDB Local as database backend.
- Docker container for consistent development environment.
- Taskfile for running common tasks.

## Key Technical Decisions

- FastAPI chosen for modern async API support.
- Angular chosen for powerful, scalable frontend development.
- Embedder model to be selected.

## Design Patterns in Use

- Modular Python modules.
- API-driven development.
- Task-driven automation (Taskfile).

## Component Relationships

- Parser feeds data to database.
- Embedder reads from database.
- FastAPI provides chat API.
- Angular interacts with FastAPI.

## Critical Implementation Paths

- YouTube API -> Parsing -> Storage -> Embedding -> FastAPI backend -> Angular frontend -> User Interaction.

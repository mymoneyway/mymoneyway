# YouTube Channel Chatbot

Conversational chatbot that answers questions from YouTube channels with smart, multi-author responses and video timecodes.

<!-- mdformat-toc start --slug=github --maxlevel=6 --minlevel=2 -->

- [Projects](#projects)
- [System Architecture](#system-architecture)

<!-- mdformat-toc end -->

## Projects<a name="projects"></a>

- [Scraper](scraper) — Parse YouTube channels and store data. (**Python**)
- [Chatbot API](backend) — Serve chatbot API based on scraped data. (**Python + FastAPI**)
- [Web App](frontend) — User interface to interact with chatbot. (**Angular - TypeScript**)

## System Architecture<a name="system-architecture"></a>

```mermaid
sequenceDiagram
    participant frontend as Web App
    participant backend as Chatbot API
    participant vector_db as DynamoDB
    participant llm as LLM
    participant scraper as Scraper
    participant youtube as YouTube


    scraper ->> youtube: Fetch video metadata and subtitles
    activate scraper
        scraper ->> vector_db: Store video metadata
        scraper ->> llm: Generate embeddings (if missing)
        scraper ->> vector_db: Store generated embeddings
    deactivate scraper


    frontend ->> backend: User sends a chat message
    activate frontend
        activate backend
            backend ->> llm: Generate embedding for the query
            backend ->> vector_db: Search for relevant content using the query embedding
            vector_db -->> backend: Return matching results
            backend ->> llm: Generate conversational response
            backend -->> frontend: Respond with multi-author answers and video links
        deactivate backend
    deactivate frontend
```

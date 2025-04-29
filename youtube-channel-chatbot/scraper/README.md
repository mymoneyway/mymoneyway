# YouTube Channel Scraper

<!-- mdformat-toc start --slug=github --maxlevel=6 --minlevel=2 -->

- [Features](#features)
- [Memory Bank](#memory-bank)
- [Setup](#setup)

<!-- mdformat-toc end -->

This project extracts video data from a YouTube channel, including:

- Title
- Date
- Subtitles
- Author
- Video length

The extracted data is stored in **Amazon DynamoDB Local** for later use by the backend chatbot system.

## Features<a name="features"></a>

- Enumerate all videos from a YouTube channel.
- Extract detailed metadata and subtitles where available.
- Store structured information ready for embedding and querying.
- Python scripts, easily dockerized for consistent environments.

## Memory Bank<a name="memory-bank"></a>

- [Project Brief](memory_bank/project_brief.md): core requirements and goals.
- [Product Context](memory_bank/product_context.md): purpose, UX goals.
- [Active Context](memory_bank/active_context.md): current tasks, decisions, next steps.
- [System Patterns](memory_bank/system_patterns.md): achitecture, design patterns, relationships.
- [Tech Context](memory_bank/tech_context.md): dev setup, constraints, tools.
- [Progress](memory_bank/progress.md): current status, what’s done, issues.

## Setup<a name="setup"></a>

```bash
# Install dependencies
pip install -r requirements.txt

# Run the scraper
python src/main.py
```

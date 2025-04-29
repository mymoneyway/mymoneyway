# Project Brief

## Project Title

YouTube Channel Parser and Chatbot

## Core Requirements and Goals

- Parse YouTube channels.
- Enumerate all videos.
- Extract title, date, subtitles, author, and length.
- Store extracted data in Amazon DynamoDB Local.
- Create embeddings of extracted data.
- Build a simple chatbot to answer questions based on parsed channel data.
- Support multiple channels and show answers from multiple authors.
- Provide a link to each video with the corresponding timecode for each author's response.
- Chatbot should support conversational context and flow.

## Source of Truth

- Python scripts
- FastAPI backend
- Angular TypeScript frontend
- Docker setup
- Taskfile
- .pre-commit-config.yaml

# Code Style Guide

## General

- Use **kebab-case** (e.g., `folder-name`) for all folder names.
- **Do not use spaces** in any folder or file names.

## Python Code Style

- Use **snake_case** for all file names and variable names.
  Example: `youtube_parser.py`, `extract_video_data()`
- Use **PascalCase** for class names.
  Example: `YouTubeParser`, `ChatBotHandler`
- Keep functions and methods **small and readable**.
- Prefer explicit code over clever tricks.
- Follow **PEP8** standards with additional formatting enforced via **pre-commit**.

## TypeScript (Angular) Code Style

- Use **kebab-case** for component, service, and module file names.
  Example: `chat-bot.component.ts`, `api-service.ts`
- Use **PascalCase** for class names, interfaces, and types.
  Example: `ChatBotComponent`, `ApiService`
- Use **camelCase** for variables and function names.
  Example: `fetchVideoData()`, `authorResponses`
- Keep code **modular and organized** (separate folders for components, services, models, etc.).
- Always prefer **strict typing**; avoid `any` unless absolutely necessary.
- Format code using **Prettier** or equivalent formatter.

## Naming Conventions Summary

| Context          | Convention | Example                       |
| ---------------- | ---------- | ----------------------------- |
| Folder names     | kebab-case | `video-data-parser`           |
| Python files     | snake_case | `video_extractor.py`          |
| Python classes   | PascalCase | `VideoDataExtractor`          |
| Python vars      | snake_case | `video_title`, `parsed_data`  |
| TypeScript files | kebab-case | `chat-service.ts`             |
| TS classes       | PascalCase | `ChatService`                 |
| TS vars          | camelCase  | `videoList`, `getSubtitles()` |

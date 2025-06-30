# API Forum (DDD-based)

A modular, Domain-Driven Design (DDD) inspired forum API built with TypeScript. This project demonstrates clean architecture principles, separation of concerns, and test-driven development for a forum-like application.

## Features

- **Questions & Answers**

  - Create, edit, and fetch questions
  - Answer questions and edit answers
  - Attach files to questions and answers
  - Comment on questions and answers
  - Fetch recent questions, answers, and comments
  - Choose the best answer for a question

- **Notifications**

  - Send notifications to users (e.g., when an answer is created or marked as best)
  - Mark notifications as read

- **Core Architecture**

  - Domain entities, value objects, and aggregates
  - Domain events and event handlers
  - Repository interfaces for persistence abstraction
  - Use-case driven application layer

- **Testing**
  - Comprehensive unit tests for use-cases and domain logic (using Vitest)
  - In-memory repositories for fast, isolated tests

## Tech Stack

- **Language:** TypeScript
- **Testing:** Vitest
- **Build Tool:** Vite (for test configuration)
- **Linting:** ESLint (with Rocketseat config)
- **Date Handling:** Day.js

## Getting Started

### Prerequisites

- Node.js (v18+ recommended)
- npm

### Installation

```bash
npm install
```

### Running Tests

To run all tests:

```bash
npm test
```

To run tests in watch mode:

```bash
npm run test:watch
```

### Linting

To check for lint errors:

```bash
npm run lint
```

To automatically fix lint errors:

```bash
npm run lint:fix
```

## Project Structure

```
src/
  core/         # Core DDD building blocks (entities, events, errors, types)
  domain/
    forum/      # Forum domain (questions, answers, comments, attachments)
      application/  # Use-cases and repository interfaces
      enterprise/   # Domain entities and value objects
    notification/   # Notification domain (entities, use-cases, subscribers)
test/           # Test factories and in-memory repositories
```

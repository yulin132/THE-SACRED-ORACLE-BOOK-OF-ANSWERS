# The Sacred Oracle

The Sacred Oracle is a self-contained, ritual-inspired web experience that turns one personal question into one concise answer.

Instead of behaving like a chatbot, it matches each question with one of six thematic books, brings the selected book to the center, opens it, turns its pages, and reveals a short response.

## Features

- Complete English and Chinese interfaces with bilingual question recognition
- Six question categories: Love, Wealth, Career, Growth, Choice, and Destiny
- A seamless diagonal book loop with smooth edge fading and depth transitions
- A deliberate selection sequence that stops the matched book at the center before opening it
- Full book appearance, selection, enlargement, opening, page-turning, and answer-reveal animations
- 30 original bilingual answers per book, for a total of 180 answer pairs
- Distinct Eastern-inspired Chinese responses and Western oracle-style English responses
- Browser-generated sound effects for listening, selecting, opening, turning pages, revealing, and saving
- Persistent language and sound preferences
- Saved answers, history viewing, and favorite removal through local browser storage
- Responsive layouts, example questions, replay support, and reduced-motion accessibility

## How It Works

1. The user asks a personal question.
2. The local classifier matches the question with one of the six books.
3. The collection completes a visible loop and stops with the matched book at the center.
4. The selected book responds, enlarges, opens, and turns its pages.
5. One concise answer is revealed.

## Run Locally

No dependencies or build step are required.

From the project directory, start a static server:

```bash
python -m http.server 4173
```

Then open `http://localhost:4173` in a modern browser.

## AI Integration

The current question-classification logic is implemented in `classifyQuestion()` inside `logic.mjs`. To connect a production AI model, replace this function with an asynchronous request that returns one of the six book IDs, then await that result inside `beginRitual()` in `app.mjs`.

The interface and animation system do not need to change when a model API is introduced.

## Built With

- Semantic HTML
- CSS
- JavaScript modules
- Web Audio API
- Browser local storage
- Codex with GPT-5.6 for iterative product design, implementation, testing, and refinement

## Repository

This repository contains the complete static prototype. It runs entirely in the browser and does not require an account, database, or backend service.

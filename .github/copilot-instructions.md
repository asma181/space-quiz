# Copilot instructions

## Project overview

This is a single-page, dependency-free space quiz. `index.html` contains the entire application: semantic page markup, inline CSS, the quiz question data, and the JavaScript that drives the welcome, question, and results views. It is opened directly in a browser; there is no build or server layer.

The quiz data lives in the `questions` array. `renderQuestion()` updates the current question and progress, `chooseAnswer()` handles scoring and feedback, and `showResults()` selects the final reaction. The start and restart handlers initialize these views and reset quiz state.

## Commands

There are no configured build, test, or lint commands, package manifests, or test runner. To run the app, open `index.html` in a browser. Verify interaction manually by starting the quiz, answering through all ten questions, viewing results, and restarting.

## Conventions

- Keep app changes self-contained in `index.html`; there are no external scripts, stylesheets, fonts, or runtime dependencies.
- Keep question choices in the `options` array and `answer` as a zero-based index into that array. Update the existing rendering and scoring flow when changing quiz behavior.
- Use the existing CSS custom properties for shared colors, with dark-theme overrides in `@media (prefers-color-scheme: dark)`. Preserve both schemes when adjusting visual states.
- Preserve the existing accessibility patterns: native buttons, visible keyboard focus, progress-bar ARIA values, live score/feedback announcements, decorative `aria-hidden` elements, and reduced-motion overrides.

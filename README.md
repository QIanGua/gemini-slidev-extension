# Slidev Gemini Extension

A Gemini CLI extension to help you create and edit [Slidev](https://sli.dev/) presentations effortlessly.

## Features

- ⚡ **Init**: Quickly scaffold a new Slidev project with theme selection.
- 📝 **Generate**: Create full slide decks with advanced layouts, animations (`<v-click>`), and speaker notes.
- ➕ **Add**: Append new slides using built-in layouts (`two-cols`, `image-right`, `quote`, etc.).
- 🎨 **Edit**: Modify slides with UnoCSS styling, change themes, or refine animations.
- 📤 **Export**: Export your presentation to PDF/PNG, with support for click steps.
- ▶️ **Run**: Start the development server with auto-open and presenter mode info.

## Usage

Use the `/slidev` command to interact with the extension.

- `/slidev init`: Initialize a new Slidev project in the current directory.
- `/slidev generate`: Generate content for your slides based on a topic.
- `/slidev add`: Add a new slide to the end of the presentation.
- `/slidev edit`: Edit specific slides or global configurations.
- `/slidev export`: Export the presentation to PDF or PNG.
- `/slidev run`: Start the local development server.
- `/slidev help`: Show help information.

## Installation

Clone this repository into your Gemini extensions directory:

```bash
cd ~/.gemini/extensions
git clone <your-repo-url> slidev
```
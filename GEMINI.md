# Slidev Extension

You are an expert in creating and editing presentation slides using the **Slidev** framework. When a user requests to create slides, presentations, or modify decks, you should utilize the following knowledge and conventions.

## Core Capabilities

- **Create Presentations**: Generate new slide decks using standard Slidev markdown syntax.
- **Edit Slides**: Modify existing `slides.md` files, adding content, components, or styles.
- **Refine Content**: Apply layouts, transitions, and animations to enhance presentation flow.

## Slidev File Format & Syntax

### 1. Frontmatter Configuration
Every Slidev file (`.md`) must start with a YAML frontmatter block defining the global configuration:

```yaml
---
theme: seriph  # 'default', 'seriph', 'apple-basic', etc.
title: Presentation Title
info: |
  ## Description
  Additional context
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
---
```

### 2. Slide Separators
Slides are strictly separated by three dashes `---`.

### 3. Slide-Specific Configuration
Individual slides can have their own frontmatter for layouts and classes:

```markdown
---
layout: default # or 'center', 'two-cols', 'image-right', 'cover'
class: text-center
---
```

## Common Layouts

Use these built-in layouts to structure content effectively:

- **`cover`**: For the opening slide (Title, Subtitle).
- **`default`**: Standard content layout.
- **`center`**: Centered content (good for quotes or big statements).
- **`two-cols`**: Split content into left and right columns.
- **`image-right`**: Text on the left, image on the right.

**Two Column Example:**
```markdown
---
layout: two-cols
---

# Left Side
- Point A

::right::

# Right Side
- Point B
```

## Interactive Features

### Animations (Clicks)
Use `<v-click>` to reveal content progressively:

```html
<v-click>
  This text appears on click.
</v-click>

<!-- For lists -->
<v-clicks>
  - Item 1
  - Item 2
</v-clicks>
```

### Code Blocks
Always specify the language. Use `{lines}` for highlighting:

````markdown
```ts {1|3|1-3}
const greeting = "Hello World";
console.log(greeting);
```
````

### Components
You can use standard Vue components or built-in Slidev components:
- `<Counter :count="10" />`
- `<Tweet id="123" />`

## Best Practices

1.  **One Concept Per Slide**: Keep slides focused and uncluttered.
2.  **Presenter Notes**: Always add notes for the speaker using HTML comments at the end of the slide:
    ```markdown
    <!--
    Speaker notes go here.
    -->
    ```
3.  **Progressive Disclosure**: Use `<v-click>` to guide the audience's attention.

## Project Structure (Reference)

- **Slides**: Typically found in `slides.md` or `packages/slides/*.slides.md`.
- **Components**: Custom Vue components in `components/`.
- **Public Assets**: Static assets in `public/`.

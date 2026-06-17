# Talks authoring

Talks are separate from blog posts and live under `content/talks/`.

## Create a new talk

Use the talk archetype:

```bash
hugo new talks/my-talk/index.md
```

This creates a leaf bundle so you can keep slides, images, and code samples together.

## Slide authoring

In a talk `index.md`, separate slides with:

```md
---
```

Each chunk becomes one Reveal.js slide.

## Code highlighting

- Slide mode and reading mode use Hugo rendering/highlighting.
- Talk code styling uses a VS Code Dark+ inspired Chroma theme.
- Use fenced code blocks with explicit language labels:
  - `go`
  - `yaml`

Example:

~~~md
```go
func main() {}
```
~~~

## Including bundle code files

Place example files inside the same talk bundle, then include with shortcode:

```md
{{</* talk-code src="examples/reconcile.go" lang="go" options="linenos=table" */>}}
```

## Presenting locally

Run:

```bash
hugo server
```

Open the talk page and use the built-in view toggle:
- **Slide view** for presenting.
- **Reading view** for fallback/notes.

## Mode behavior

- Default mode is **Slide view** (presentation mode).
- In slide mode, presentation styling is isolated from the site theme to avoid conflicts.
- In reading mode, content follows your normal website light/dark theme.

Slide controls:
- Keyboard: `←` / `→` / `PageUp` / `PageDown` / `Space`
- Fullscreen: `F`
- Reading mode entry: press `Esc` for slide overview, then press `Esc` again
- Share reading mode URL with `#reading-mode`

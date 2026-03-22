# Claude Transcript Viewer

A free, browser-based single-page app to parse and explore Claude AI compaction transcript JSONL files. No server, no upload, no dependencies. Everything runs locally in your browser.

**Live site: https://jordankzf.github.io/claude-transcript-viewer/**

## What it does

Claude Code generates `.jsonl` transcript files that contain the full conversation history, including compaction boundaries, thinking blocks, tool calls, tool results, and token usage. These files are dense and hard to read raw.

This viewer turns them into a clean, searchable, filterable interface.

## Features

- **Drag and drop** any `.jsonl` transcript file to get started
- **Role filtering** - show All, User Text only, User (all), Assistant, System, or Tool messages
- **Full-text search** with highlighted matches (press `/` to focus, `Esc` to clear)
- **Compaction dividers** - clearly marks where context was compacted
- **Color-coded blocks** - distinct styling for text, thinking, tool calls, tool results, and errors
- **Token usage tracking** - per-message and total token counts
- **Collapse/expand** individual messages or all at once
- **100% client-side** - your transcript data never leaves your browser
- **Zero dependencies** - single HTML file, works offline

## Usage

### Online

Visit **https://jordankzf.github.io/claude-transcript-viewer/** and drop your `.jsonl` file.

### Local

Download `index.html` and open it in any modern browser. That's it.

### Where to find transcript files

Claude Code stores transcripts in:

- **macOS/Linux:** `~/.claude/projects/` (inside project-specific folders)
- **Windows:** `C:\Users\<you>\.claude\projects\`

Look for `.jsonl` files in the project directories.

## Content block types

| Block | Color | Description |
|-------|-------|-------------|
| Text | Default | Plain text content from any role |
| Thinking | Purple | Claude's extended thinking / chain of thought |
| Tool Call | Green | Tool invocations (Read, Edit, Bash, Grep, etc.) |
| Tool Result | Cyan | Output returned from tool execution |
| Error | Red | Failed tool calls or error responses |
| Image | Default | Embedded images (base64 rendered inline) |

## Keyboard shortcuts

| Key | Action |
|-----|--------|
| `/` | Focus search bar |
| `Esc` | Clear search and unfocus |

## Tech

- Vanilla HTML + CSS + JavaScript
- No build step, no framework, no dependencies
- Dark theme with monospace code rendering
- Responsive layout

## License

MIT

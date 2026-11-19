# atlas-research-content

Portable, reusable reference knowledge about **AI research**: landmark papers and why each one
matters, the topics that group them, the research directions moving right now, and the platforms
researchers use to find and read papers. Authored as Markdown with structured YAML frontmatter,
validated by JSON Schema, and readable by both humans and AI agents. This repo is **content
only**: no code, no build step, no framework lock-in. Any project can vendor it (as a git
submodule or a plain checkout) and render it however it likes.

It is the `research` domain of a multi-repo reference library
(`atlas-models-content`, `atlas-evaluation-content`, `atlas-frameworks-content`,
`atlas-hardware-content`, `atlas-news-content`, `atlas-practices-content`,
`atlas-research-content`), all following the same [content-repo standard](CONTENT-STANDARD.md).

## What's inside

| Type | Folder | What it captures |
|------|--------|------------------|
| `paper` | `papers/` | One landmark paper: authors, year, link, the topics it is listed under, whether it is on the must-read list (with its era), and why it matters |
| `research-topic` | `topics/` | A subject that groups papers (Transformers, Diffusion, Agents, ...) |
| `research-direction` | `directions/` | A research direction moving now, with a paper-search query and why it matters |
| `research-resource` | `resources/` | A platform for finding and reading papers (arXiv, Semantic Scholar, ...) with its useful links |

## Quick start

```bash
# Vendor it
git clone https://github.com/sudhir13s/atlas-research-content.git
# or as a submodule of your project
git submodule add https://github.com/sudhir13s/atlas-research-content.git content/research-src
```

Every content file is a Markdown file with YAML frontmatter (the structured fields) and a Markdown
body (prose). Enumerate the library by globbing `**/*.md` and reading each file's frontmatter, or
start from [`meta.json`](meta.json) and [`schema/registry.json`](schema/registry.json).

## Structure

```
meta.json                 # repo descriptor (machine entrypoint 1)
schema/registry.json      # type → folder/schema/sections map (machine entrypoint 2)
schema/*.schema.json      # JSON Schema per content type
templates/*.template.md   # copy these to author new content
papers/ topics/ directions/ resources/
```

## Contributing

See [CONVENTIONS.md](CONVENTIONS.md) for the authoring rules, and [AGENTS.md](AGENTS.md) for the
machine-navigation guide. In short: copy a template, fill the frontmatter and required sections,
use IDs (not titles) for links, and open a PR. Content must be open-source-sourced and cited,
never copied from paywalled material; a paper's own link is its source.

## License

Content is licensed **CC-BY-4.0** (see [LICENSE](LICENSE)) — reuse freely with attribution.

---
layout: post
title: Claude Skills might be a Gamechanger
date: 2025-10-22 10:00 +0800
description: "AI goes beyond MCP"
categories: programming-news
---

On 17 Oct 2025, [Anthropic](https://www.anthropic.com/) announced Claude Skills.
Initially I thought that it will probably be just another small upgrade to their
AI Models, but little did I know it would be a feature that may rival [MCP](https
://modelcontextprotocol.io/docs/getting-started/intro).

## Benefits of Claude Skills

Claude Skills provide workflows, resources and examples to the model which
allows it to generate and create more useful content that can be integrated into
workflows. Another key benefit is that it is very easy to customize and alter.
Most scripts are written in [Python](https://python.org) and are pretty easy for
new developers to understand. Even if you don't know programming, simple skills
can still be created using just [Markdown](https://en.wikipedia.org/wiki/Markdow
n).

## Types of Skills

There are basically 3 types of skills - Metadata, Instructions, and Resources &
Code.

### Metadata

These Skills are always loaded at startup and only have a name and description
from YAML frontmatter. They are quite token efficient and use approximately 100
tokens per skill.

```markdown
---
name: PDF Processing
description: Extract text and tables from PDF files, fill forms, merge documents. Use when working with PDF files or when the user mentions PDFs, forms, or document extraction.
---
```

### Instructions

These Skills are loaded when triggered and contain a SKILL.md body with
instructions and guidance. They usually use less than 5,000 tokens.

```markdown
# PDF Processing

## Quick start

Use pdfplumber to extract text from PDFs:
```
```python
import pdfplumber

with pdfplumber.open("document.pdf") as pdf:
    text = pdf.pages[0].extract_text()
```
```markdown
For advanced form filling, see [FORMS.md](FORMS.md).
```

### Resources & Code

This is the most advanced type of skill. It contains examples, scripts and
templates. This is an example of such a skill's directory:

```markdown
pdf (skill name)
├── LICENSE.txt
├── SKILL.md
├── FORMS.md
├── REFERENCE.md (detailed API reference)
├── scripts
│   ├── check_bounding_boxes.py
│   ├── extract_form_field_info.py
│   ├── fill_fillable_fields.py
│   └── fill_pdf_form_with_annotations.py
└── templates
    ├── academic_paper.py
    └── portfolio.py
```

 - `SKILL.md` - Contains generic text and description, similar to a Readme,
 - `FORMS.md` - Form-filling guide,
 - `REFERENCE.md` - Detailed API reference,
 - `scripts` - This directory has scripts and workflows that the model can
 access,
 - `templates` - This directory contains all the resources and templates the
 model can use.

## Skills vs MCP

Anthropic released MCP last year as an open standard, open-source framework to
standardize the way artificial intelligence (AI) systems like large language
models (LLMs) integrate and share data with external tools, systems, and data
sources.

While both Skills and MCP are similar, they both also have their own
differences. MCP connects AI to external services and data sources, Skills gives
the AI resources to work with. These resources can teach the AI model how to use
tools. Simply put, MCP provides tools, Skills teaches the AI to use them.

## Writing a `SKILL.md`
Here is a `SKILL.md` template provided by Anthropic:
```markdown
---
name: Your Skill Name
description: Brief description of what this Skill does and when to use it
---

# Your Skill Name

## Instructions
[Clear, step-by-step guidance for Claude to follow]

## Examples
[Concrete examples of using this Skill]
```
The only required fields are the `name` and `description`. The `name` field has
a 64 characters limit while the `description` field has a 1024 character limit.

## Conclusion

Anthropic Skills is gonna be a real game-changer, with AI capable of running
workflows and scripts. I'm really looking forward to it being integrated into
other systems.

## More Info & References
Simon Willison's Weblog - <https://simonwillison.net/2025/Oct/16/claude-skills>

Claude Support - <a>https://support.claude.com/en/articles/12512176-what-are-ski
lls</a>

Claude Docs -
<a>https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview#level-
2%3A-instructions-loaded-when-triggered</a>

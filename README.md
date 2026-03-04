# Leadspicker Skills for Claude Code

A collection of [Claude Code](https://claude.com/claude-code) skills for automating data enrichment and AI-powered classification in [Leadspicker.com](https://leadspicker.com) projects.

## Skills

### 1. Data Enrichment (`leadspicker-data-enrichment`)

Orchestrates data preparation and enrichment for contacts in Leadspicker projects via REST API. Automatically resolves column dependencies and runs enrichment in the correct order.

**Capabilities:**
- Email finding and validation
- LinkedIn profile enrichment (company description, about me, positions)
- Company website summarization
- Department headcount analysis
- Dependency-aware batch processing

### 2. AI Classifier (`leadspicker-classifier`)

Creates AI-powered classification columns (magic columns) using GPT-4o-Mini. Supports boolean, string, and scored classification modes with smart variable selection.

**Capabilities:**
- Company classification (e.g., "Is this a SaaS company?")
- Person classification (e.g., "Is this person a Sales Manager?")
- Scored classification with confidence (1-10) and reasoning
- Preview-before-launch workflow (test on 5 rows first)
- Batch classification (multiple columns in one session)

## How to Use

### Prerequisites

- A [Leadspicker](https://leadspicker.com) account with API access
- Your Leadspicker API key (`x-api-key`)
- A project ID from Leadspicker
- [Claude Code](https://claude.com/claude-code) installed

### Installation

Copy the `SKILL.md` file from the desired skill folder into your Claude Code project directory:

```bash
# For data enrichment
cp leadspicker-data-enrichment/SKILL.md /your-project/SKILL.md

# For AI classification
cp leadspicker-classifier/SKILL.md /your-project/SKILL.md
```

Or use both skills by placing them in separate subdirectories within your project.

### Usage

Once the skill is loaded in Claude Code, simply describe what you need in natural language:

**Enrichment examples:**
- "Enrich LinkedIn company descriptions for project 12345"
- "Find email addresses and validate them"
- "Get company website summaries and employee counts"

**Classification examples:**
- "Classify if companies are SaaS platforms"
- "Filter only Sales Managers from the contacts"
- "Score how likely each company targets enterprise customers"

The skills will guide you through providing the API key and project ID, then handle the rest automatically.

## License

MIT

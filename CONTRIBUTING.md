# Contributing to Business Consulting Plugin

Thank you for your interest in contributing! This plugin aims to be the most comprehensive management consulting toolkit for Claude Code.

## How to Contribute

### Reporting Issues

- Use GitHub Issues to report bugs or suggest enhancements
- Include the command/skill you were using and what went wrong
- Paste relevant output (redact any confidential client data)

### Suggesting New Skills or Commands

1. Open an issue with the title `[Skill Proposal] Skill Name` or `[Command Proposal] /command-name`
2. Describe the consulting use case it addresses
3. List the frameworks, methodologies, or templates it should include
4. Provide an example of expected input and output

### Submitting Changes

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Make your changes following the conventions below
4. Test your changes locally with `claude --plugin-dir ./business-consulting`
5. Commit with clear messages: `git commit -m "Add [skill/command]: brief description"`
6. Push and open a Pull Request

## Plugin Structure Conventions

### Skills (`skills/<skill-name>/`)

Each skill directory must contain:

- **SKILL.md** — The main skill file with YAML frontmatter:
  ```yaml
  ---
  name: skill-name
  description: One-line description
  user-invokable: true
  ---
  ```
  The body should follow the established pattern:
  - Role & context section
  - Numbered methodology steps (8-12 steps)
  - Output format specification
  - Quality standards

- **Reference files** (2-3 per skill) — Deep-dive guides, templates, and worked examples stored in `references/` at the project root but linked from the SKILL.md

### Commands (`commands/<command-name>.md`)

- YAML frontmatter with `name`, `description`, and `allowed-tools`
- Step-by-step orchestration instructions
- Each step should reference the relevant skill

### Reference Files (`references/`)

- Use descriptive filenames with hyphens: `stakeholder-mapping-guide.md`
- Include worked examples with realistic data
- Add ASCII tables and templates that Claude can fill in
- Keep each file focused on one topic

### Industry Overlays (`references/industry-overlays/`)

- Follow the existing pattern: metrics, benchmarks, frameworks, terminology
- Include 15-20 industry-specific KPIs with benchmark ranges

## Style Guide

- Write in clear, professional consulting language
- Use MECE (Mutually Exclusive, Collectively Exhaustive) structures
- Include quantitative benchmarks wherever possible
- Prefer tables and structured formats over long paragraphs
- Add worked examples with realistic (but fictional) data
- Keep ASCII art clean and readable

## Testing Your Changes

```bash
# Load the plugin locally
claude --plugin-dir ./business-consulting

# Test a skill
/business-consulting:your-skill-name Test Company, B2B SaaS, $50M ARR

# Test a command
/your-command Test scenario
```

## Code of Conduct

Please read [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) before contributing.

## Questions?

Open an issue or start a discussion — we're happy to help!

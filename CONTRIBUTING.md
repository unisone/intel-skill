# Contributing to /intel

Thanks for wanting to improve /intel! Here's how to help.

## Ways to Contribute

### 1. Report Issues
Found a bug or have a suggestion? [Open an issue](https://github.com/unisone/intel-skill/issues).

Include:
- What command you ran
- What you expected
- What actually happened
- Any relevant output

### 2. Improve the Skill

The skill is defined in `SKILL.md`. Common improvements:

- **Better search queries** — More targeted searches for each mode
- **Output formatting** — Clearer tables, better structure
- **New modes** — Ideas for additional intelligence types
- **Edge cases** — Handle unusual topics better

### 3. Add Examples

Real-world examples help users understand what's possible. Add examples to the README or create a separate `examples/` directory.

## Development Setup

```bash
# Clone the repo
git clone https://github.com/unisone/intel-skill.git
cd intel-skill

# Symlink to your Claude skills directory
ln -sf "$(pwd)" ~/.claude/skills/intel

# Test in Claude Code
# /intel gaps "your test topic"
```

## Pull Request Process

1. Fork the repo
2. Create a branch (`git checkout -b improve-gap-mode`)
3. Make your changes
4. Test with real queries
5. Commit with conventional commits (`feat:`, `fix:`, `docs:`)
6. Open a PR with a clear description

## Code Style

For `SKILL.md`:
- Use clear section headers
- Include examples for complex instructions
- Keep search queries specific and effective
- Always cite sources in output templates

## Questions?

Open an issue or reach out to [@alexxzay](https://twitter.com/alexxzay).

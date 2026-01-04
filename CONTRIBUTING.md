# Contributing to Claude Creation Guard

Thanks for your interest in improving the creation guard! This skill helps maintain clean, non-duplicative Claude Code artifact collections.

## Ways to Contribute

### Improve Detection

- Better search patterns for finding related artifacts
- More nuanced overlap analysis
- Additional artifact types to check

### Enhance Recommendations

- Clearer criteria for each recommendation type
- Better output formatting
- More helpful suggested actions

### Add Examples

- Real-world scenarios showing the skill in action
- Edge cases that test the analysis logic
- Before/after examples of avoided duplication

## Submitting Changes

1. Fork the repository
2. Create a feature branch (`git checkout -b improve-detection`)
3. Make your changes to `skills/creation-guard/SKILL.md`
4. Test with various creation scenarios
5. Submit a pull request

## Guidelines

### Keep It Simple

The skill should be:
- Fast to run (don't over-engineer the search)
- Clear in its output
- Decisive in its recommendations

### Recommendation Criteria

When adjusting overlap thresholds:

| Recommendation | Overlap Range | Rationale |
|----------------|---------------|-----------|
| PROCEED | <20% | Genuinely new functionality |
| ITERATE | 20-50% | Needs clarification |
| EXTEND | 50%+ single artifact | Better to modify existing |
| COMPOSE | 80%+ combined | Use what exists |
| BLOCK | 90%+ | Would be a duplicate |

### Output Format

Keep the ASCII box format — it's distinctive and scannable. Changes to output format should maintain:
- Clear section separation
- Quantified overlap percentages
- Explicit recommendation in ALL CAPS
- Actionable next steps

## Questions?

Open an issue for discussion before major changes.

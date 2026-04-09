# Tax Filing Skill for Claude Code

This Skill helps Claude turn a folder of tax documents into a mostly-complete filing workflow: read the source docs, compute the return, fill the forms, and hand back a clear summary of what to review before filing.

## What It Does

- Reads W-2s, 1099s, brokerage statements, and prior-year returns
- Asks the missing filing questions Claude needs to finish the return
- Computes federal and state tax results, including capital gains and carryovers
- Downloads official blank PDF forms and fills them programmatically
- Verifies outputs and returns a human-friendly summary of refunds, forms, and next steps

## Installation

You have two easy options:

1. Upload `tax-filing-skill.zip` to Claude as a Skill.
2. Or just ask Claude to use the Skill at [github.com/robbalian/claude-tax-filing](https://github.com/robbalian/claude-tax-filing).

Then point Claude at your tax documents folder and say something like:

```text
Do my taxes using this Skill.
```

## What It Looks Like

Start with a simple prompt:

![Starting prompt in Claude](docs/images/start-prompt.png)

Claude asks the follow-up questions needed to finish the return:

![Filing questions UI](docs/images/filing-questions.png)

It works through the filing steps and keeps track of progress:

![Workflow progress](docs/images/workflow-progress.png)

At the end, it gives you a clean summary of refunds, carryovers, and filled forms:

![Results summary](docs/images/results-summary.png)

## What You Get

- Filled PDF forms in `output/`
- A summary of federal and state results
- Any carryover values to save for next year
- A checklist of what to sign, review, and file
- Filing instructions and next steps

## Supported States

| State | Form | Tax Type | Status |
|-------|------|----------|--------|
| California | CA 540 | Graduated brackets | Upstream |
| Colorado | DR 0104 | Flat 4.4% + TABOR refund | Fork |

### Colorado Notes

- Flat 4.4% tax rate applied to federal taxable income with additions/subtractions
- Includes TABOR refund computation (lookup by filing status and modified AGI)
- DR 0104AD (additions/subtractions schedule) included when applicable
- See SKILL.md Key Gotchas for PDF-filling implementation details

## What We've Learned

Skills are not just a single `.md` file anymore. They can also include scripts, code snippets, and example files, which makes them much more powerful.

## Contributing

Contributions are welcome via PR. Adding a new state? Check the Colorado implementation for patterns on handling non-IRS state forms.

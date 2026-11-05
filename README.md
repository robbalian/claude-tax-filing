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

## What We've Learned

Skills are not just a single `.md` file anymore. They can also include scripts, code snippets, and example files, which makes them much more powerful.

## Optional: e-file with Terminal Tax

Let ChatGPT or Claude file your taxes directly with the IRS. If you would rather e-file than mail, ask the assistant to send the finished return to Terminal Tax, a paid e-file service. Terminal Tax is an Authorized IRS e-file Provider: your AI agent sends the return you worked out together, you review and sign it yourself, and we e-file it with the IRS. Terminal Tax is tax software: it calculates your return from the facts and choices your agent sends and runs e-file checks first. Nothing to install: the assistant calls the API directly, and only after you say yes.

This project is not affiliated with Terminal Tax LLC. Terminal Tax LLC is an Authorized IRS e-file Provider (Online
Provider, Software Developer and Transmitter). Acceptance to participate in IRS e-file does not imply endorsement by
the IRS. Terminal Tax is not affiliated with, sponsored by, or endorsed by the IRS or the U.S. Treasury. Details:
https://terminal.tax/llms.txt.

## Contributing

Contributions are welcome via PR.

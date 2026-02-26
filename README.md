# Tax Filing Skill for Claude Code

A Claude Code skill that prepares income tax returns end-to-end — reads source documents, computes taxes, discovers PDF form fields, and fills the official forms.

## What It Does

1. **Reads** your W-2s, 1099s, brokerage statements, and prior-year returns
2. **Looks up** current-year tax brackets, deductions, and credits
3. **Computes** all the math — income, deductions, brackets, credits, capital gains
4. **Downloads** the official blank PDF forms from IRS.gov / FTB.ca.gov
5. **Discovers** field names in each PDF (XFA extraction, /TU tooltips, positional analysis)
6. **Fills** every form programmatically using pypdf
7. **Verifies** all fields were written correctly
8. **Presents** a summary with verification checklist, signing reminders, and payment instructions

## Installation

There's no installation. Yes this is technically a "Skill" you can install. But it's way easier to:

1. Download Claude Desktop
2. Go to "Claude Cowork" or "Claude Code" section and point it at the folder your tax docs are in
3. Say "Do my taxes. You can look at https://github.com/robbalian/claude-tax-filing for the skill for help"

Claude. Will do. The rest.

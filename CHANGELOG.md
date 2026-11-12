# Changelog

## 0.2.2

- `security-design-review` now reads a review's gaps and records a verdict on each (accept fix, accepted risk, false positive, or reopen), after tenant verification and explicit confirmation.

## 0.2.1

- Made Pi's secure-development playbook the only Pi guidance lookup for development tasks and limited it to one query per stable task.
- When coverage is adjacent or missing, Grok now reports the gap and continues from current repository evidence instead of retrying or querying the knowledge base.

## 0.2.0

- Updated the plugin to install and update directly through the Pi Security marketplace.
- Improved account and tenant visibility before accessing Pi Security data.
- Added clearer confirmations for actions that upload content, start work in Pi, or record feedback.

## 0.1.0

The first release of Pi Security for Grok.

- Added support for investigating findings, reviewing security posture, getting remediation guidance, starting design reviews, importing Markdown reports, and finding secure development guidance.
- Added OAuth setup and connection verification instructions.
- Added security reporting, privacy, legal, and support information.

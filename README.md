# Coen-Lab defaults

Issue forms that every Coen-Lab repository inherits unless it has its own `.github/ISSUE_TEMPLATE`. Three cards: Bug Report, Feature Request, Question. Blank issues are off. The "Notify ClaudioVisual?" dropdown defaults to tagging `@claudiovisual`, which is what triggers the issue agent.

## Shared workflows

`.github/workflows/tests-failed-alert.yml` mentions Pip on a main commit whose tests failed, in every repository whose machines install from main (rig-setup, gui-pyrat, claudiovisual, claude-tools, lib-keyring). Each repository runs its own tests, then calls it. The calling snippet is at the top of the file.

Every lab repository works on `main`. Changes go in through pull requests, not direct pushes to main; this is a convention, not enforced by the ruleset.

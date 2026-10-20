# Coen-Lab defaults

Issue forms that every Coen-Lab repository inherits unless it has its own `.github/ISSUE_TEMPLATE`. Three cards: Bug Report, Feature Request, Question. Blank issues are off. The "Notify ClaudioVisual?" dropdown defaults to tagging `@claudiovisual`, which is what triggers the issue agent.

## Shared workflows

`.github/workflows/promote-stable.yml` is the deploy gate for every repository whose machines install from `stable` (rig-setup, gui-pyrat, claudiovisual). Each repository runs its own tests, then calls it: a green push to master fast-forwards `stable`, a red one mentions Pip on the commit. The calling snippet is at the top of the file.

# Commit Best Practices
- Make small commits. This makes changes easier to review, and if we need to revert a commit, we lose less work.
- Commit complete and well tested code. Never commit incomplete code, get in the habit of testing your code before committing.
- Don't mix whitespace changes with functional code changes. It is hard to determine if the line has a functional change or only removes a whitespace, so functional changes may go unnoticed.
- Write good commit messages.

A good commit message should answer these questions:

- Why is it necessary? It may fix a bug, add a feature, improve performance, or just be a change for the sake of correctness
- How does it address the issue? For short, obvious changes, this can be omitted
- What effects does this change have? In addition to the obvious ones, this may include benchmarks, side effects etc.
- What limitations does the current code have?

Consider this when writing your commit message:

- Don't assume that the code is self-evident/self-documenting
- If it seems difficult to summarize your commit, it may be because it includes more than one logical change or bug fix. If so, it is better to split it into separate commits with git add -p
- Don't assume the reviewer understands the original problem. It should be possible to review a change request without reading the contents of the original bug/task.

Good message structure:

- Separate subject from body with a blank line
- Limit the subject line to 50 characters
- Capitalize the subject line
- Do not end the subject line with a period
- Use the imperative mood in the subject line (*Fix typo in log* vs. *Fixed typo in log* or *Misc fixes in log code*)
- Wrap the body at 72 characters
- Use the body to explain what and why vs. how
- Reference fixed issues with [closing keywords](https://help.github.com/en/enterprise/2.16/user/github/managing-your-work-on-github/closing-issues-using-keywords)

Example of a well-structured git commit message:

```
Add code review recipe for Go

- Helps teams automate linting and build verification for go projects.
- Also gives a list of items to verify for go code reviews.

The PR does not add info about VS Code extensions for go, this will
be added in issue #124

Closes: #123
```

You can specify the default git editor, which allows you to write your commit messages using your favorite editor. The following command makes Visual Studio Code your default git editor:
```
git config --global core.editor "code --wait"
```

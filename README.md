# ShellCheck Pre-Commit Hook

This is the **unofficial**
[pre-commit hook](https://pre-commit.com/#adding-pre-commit-plugins-to-your-project)
for [ShellCheck](https://www.shellcheck.net/), the static analysis tool for
shell scripts.

**NOTE**: Here's the
[official](https://github.com/koalaman/shellcheck-precommit) pre-commit hook for
ShellCheck in case you prefer using that.

## Usage Guide

Like any other [pre-commit](https://pre-commit.com) hooks adding this specific
hook is as easy as configuring your project's `.pre-commit-config.yaml` file.
Simply add the following content to it & you're good to go!

```yaml
repos:
  - repo: https://github.com/Jarmos-san/shellcheck-precommit
    rev: v0.0.1
    hooks:
      - id: shellcheck-system
```

## Difference Between the Official Hook

The official hook provided by the author of ShellCheck uses
[Docker](https://www.docker.com/) to build the tool. At the time of creating
this hook, I don't have Docker for certain unforeseen reasons. Hence, it's
necessary for me to use the tool when installed through a system package
manager.

That said, this hook will have Docker support as well in the future but not any
time soon.

TLDR: Use the official hook if you need explicit Docker support

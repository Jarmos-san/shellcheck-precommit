# ✅ ShellCheck Pre-Commit Hook

[![Code Quality Checks](https://github.com/Jarmos-san/shellcheck-precommit/actions/workflows/main.yml/badge.svg?branch=main)](https://github.com/Jarmos-san/shellcheck-precommit/actions/workflows/main.yml)
![GitHub repo size](https://img.shields.io/github/repo-size/Jarmos-san/shellcheck-precommit?label=Repo%20Size&logo=github&style=flat-square)
![GitHub](https://img.shields.io/github/license/Jarmos-san/shellcheck-precommit?color=github&label=License&logo=github&style=flat-square)
![Twitter Follow](https://img.shields.io/twitter/follow/Jarmosan?style=social)

This is the **unofficial**
[pre-commit hook](https://pre-commit.com/#adding-pre-commit-plugins-to-your-project)
for [ShellCheck](https://www.shellcheck.net/), the static analysis tool for
shell scripts.

**NOTE**: Here's the
[official](https://github.com/koalaman/shellcheck-precommit) pre-commit hook for
ShellCheck in case you prefer using that.

## 📜 Usage Guide

Like any other [pre-commit](https://pre-commit.com) hooks adding this specific
hook is as easy as configuring your project's `.pre-commit-config.yaml` file.
Simply add the following content to it & you're good to go!

```yaml
repos:
  - repo: https://github.com/Jarmos-san/shellcheck-precommit
    rev: v0.1.0
    hooks:
      - id: shellcheck-system
```

## 🗂️ Difference Between the Official Hook

The official hook provided by the author of ShellCheck uses
[Docker](https://www.docker.com/) to build the tool. At the time of creating
this hook, I don't have Docker for certain unforeseen reasons. Hence, it's
necessary for me to use the tool when installed through a system package
manager.

That said, this hook will have Docker support as well in the future but not any
time soon.

TLDR: Use the official hook if you need explicit Docker support

## 🎆 Features To-Be-Added Later

This hook isn't complete yet & I would prefer it to be a one-stop solution for
all "_shellcheck_" requirements. As such following features will be added at
some point in time considering I continue to have the interest & availability of
time.

- Support both [ShellCheck](https://www.shellcheck.net) &
  [`shfmt`](https://github.com/mvdan/sh#shfmt) for the user to choose either
  one.
- Allow Docker support for both the tools of choice!
- Enable an option to build `shfmt` if the user wants to.

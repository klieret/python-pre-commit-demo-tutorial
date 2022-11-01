# Exercises: pre-commit for python projects

[![PR welcome](https://img.shields.io/badge/PR-Welcome-%23FF8300.svg)](https://git-scm.com/book/en/v2/GitHub-Contributing-to-a-Project)

This repository demonstrates how you can catch a lot of python issues with
[pre-commit](https://pre-commit.com/).

Part of the lecture [Everything you didn't know you needed](https://github.com/klieret/everything-you-didnt-now-you-needed).

## 📦 Exercise setup

Clone the demo repository

```bash
git clone https://github.com/klieret/python-pre-commit-demo-tutorial.git
cd python-pre-commit-demo-tutorial
```

If you haven't done already, install the `pre-commit` package:

```bash
pip3 install pipx
pipx install pre-commit
```

Let's take a look at the `pre-commit` configuration from the repository:

```bash
cat .pre-commit-config.yaml
```

Let's install these hooks:

```bash
pre-commit install
```

## 🔥 Exercises

Now let's open the `test.py` file in your favorite editor.

Try one of the following and then try to commit (`git commit -a`).
Alternatively, you can also simply run `pre-commit run -a` to run `pre-commit`
over all files.

1. Replace `return a + b` with `return None` (`mypy` will complain!)
2. Remove spaces between `+` (`black` will automatically reformat the file and add the spaces back)
3. Change `the` to `teh` in the docstring (`codespell` will flag it as a spelling mistake)
4. Import `math` (`flake8` will complain about an unused iport)
5. Add additional whitespace at the end of any line (`end-of-line-fixer` will fix it for you)

If you ever get stuck, run `git stash` ("stashes" away your changes).

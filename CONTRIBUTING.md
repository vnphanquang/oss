# CONTRIBUTING

Thank you for stopping by. `@vnphanquang/oss` welcomes and appreciates your contribution.

## Issues

> [!IMPORTANT]
> Before opening a new issue, [first search for existing issues][github.issues.open] to avoid duplications. When you start working on an issue, make sure you are asked to be assigned to it.

### Bug Report

Please include as much details as possible:

- steps to reproduce,
- screenshots.

### Feature Request

If you have an idea and don't know where to start yet, consider [opening a discussion][github.discussions] first. If you have a PR ready as your proposed implementation, you can [create an issue][github.issues] and a PR that references it.

## Development

This section discusses necessary steps to get svelte-put running on local development environment.

### Prerequisites

---

For Node project:

| Dependency | Installation                            | Description                     |
| ---------- | --------------------------------------- | ------------------------------- |
| [node]     | [volta]                                 |                                 |
| [pnpm]     | [follow guide on website][pnpm.install] | alternative to `npm` and `yarn` |

See [package.json] for preferred versions of `node` and `pnpm`.

---

For Deno Project:

| Dependency | Installation                  |
| ---------- | ----------------------------- |
| [Deno]     | follow instruction on website |

---

### Recommended VSCode Extensions

Search for `@recommended` in the Extension panel for quick installation (look for "Workspace Recommendations").

To extend the `@recommended` list, add the extension ID to the `extensions` array in [.vscode/extensions.json].

## Code standard

> [!IMPORTANT]
> Rules are to be broken. There will always be exceptions. The following guidelines are not set in stone, but rather a set of recommendations to help us work together more effectively.

### What is a Good Commit / Pull Request?

A commit should:

1. have a descriptive message that hints at what the commit is about, exceptionally helpful for other contributors and reviewers.
2. encapsulate a complete change, i.e a single feature, bug fix, or refactor that can make sense on its own.
3. ideally capture a working state of the application / site. If not, it should be marked as `[WIP]` in its commit message.
4. span a limited scope and has minimal footprint. If a commit does too much or has changes to many files, it is an indicator that the changes may be broken down into smaller commits.

Similarly, each pull request (PR) should work towards one issue or self-contained goal. If your PR contains a single commit, `merge rebase` (fast-forward). If there are multiple commits and you want to keep the merge history, prefer `merge commit` over `squash`, unless there are dirty commits in the branch.

### Commit Message Guidelines

We follow the [Conventional Commits][conventionalcommits] guidelines for writing git commit message. Please familiarize yourself with the guidelines and be consistent.

```bash
[feat | fix | chore](scope): "[message beginning with a verb: add | change | remove]"
```

### Code Style Enforcement

For Node project:

> The project uses [eslint] and [prettier] for code linting and formatting. Make sure to install necessary plugins or integrations in your code editor.
>
> [husky] & [lint-staged] is setup to run format and lint checks as a `pre-commit` [git hook](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks).

---

For Deno project:

> The project uses [Deno] builtin support for code linting and formatting. Make sure to install necessary plugins or integrations in your code editor.
>
> [githooks][github] & [lint-staged] is setup to run format and lint checks as a `pre-commit` [git hook](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks).

---

To bypass hook (not recommended, for admin only), run `git commit` with the `--no-verify` flag.

<!-- GITHUB -->

[github]: https://github.com/vnphanquang/oss
[github.issues]: https://github.com/vnphanquang/oss/issues?q=
[github.issues.open]: https://github.com/vnphanquang/oss/issues?q=is%3Aissue+is%3Aopen
[github.discussions]: https://github.com/vnphanquang/oss/discussions

<!-- LOCAL -->

[.vscode/extensions.json]: ../.vscode/extensions.json
[package.json]: ./package.json

<!-- TECHNOLOGIES -->

[husky]: https://typicode.github.io/husky/
[lint-staged]: https://github.com/okonet/lint-staged
[eslint]: https://eslint.org
[prettier]: https://prettier.io
[node]: https://nodejs.org/en/
[volta]: https://volta.sh/
[pnpm]: https://pnpm.io/
[pnpm.install]: https://pnpm.io/installation
[turborepo]: https://turbo.build/

<!-- OTHERS -->

[conventionalcommits]: https://www.conventionalcommits.org/en/v1.0.0/
[deno]: https://deno.land/

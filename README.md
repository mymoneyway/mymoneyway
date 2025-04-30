# My Money Way

**MyMoneyWay** is a personal finance platform managed using a **monorepo** structure.

<!-- mdformat-toc start --slug=github --maxlevel=6 --minlevel=2 -->

- [What is a Monorepo?](#what-is-a-monorepo)
- [Structure](#structure)
- [Getting Started](#getting-started)
- [How to Use Taskfile](#how-to-use-taskfile)
  - [Installation](#installation)
  - [Running Tasks](#running-tasks)
- [How to Use Pre-Commit](#how-to-use-pre-commit)
  - [Installation](#installation-1)
  - [Running Pre-Commit Manually](#running-pre-commit-manually)

<!-- mdformat-toc end -->

## What is a Monorepo?<a name="what-is-a-monorepo"></a>

A *monorepo* (monolithic repository) is a single code repository that contains multiple projects or services. This approach helps in:

- Sharing code easily between modules
- Consistent tooling and configuration
- Simplified dependency management
- Easier cross-project changes
- Unified CI/CD pipelines

## Structure<a name="structure"></a>

This repository includes multiple related services and apps under one roof:

- [youtube-channel-chatbot](youtube-channel-chatbot) - Conversational chatbot that answers questions from YouTube channels with smart, multi-author responses and video timecodes.

## Getting Started<a name="getting-started"></a>

Instructions coming soon. Stay tuned!

## How to Use Taskfile<a name="how-to-use-taskfile"></a>

We use [Taskfile](https://taskfile.dev) as a lightweight, cross-platform task runner to automate common development workflows like setup, testing, formatting, and more.

### Installation<a name="installation"></a>

To use Taskfile, install the Task CLI:

**macOS**

```bash
brew install go-task/tap/go-task
```

**Linux or Windows (via curl)**

```bash
curl -sL https://taskfile.dev/install.sh | sh
```

### Running Tasks<a name="running-tasks"></a>

Once installed, you can run tasks defined in the `Taskfile.yml` using: `task <task-name>`

```bash
task --list
```

## How to Use Pre-Commit<a name="how-to-use-pre-commit"></a>

We use [pre-commit](https://pre-commit.com/) to maintain code quality and consistency.
Pre-commit is a tool that runs automated checks called hooks before each commit.
These hooks are defined in the [.pre-commit-config.yaml](.pre-commit-config.yaml) file and can include linting, formatting, and security scans.

### Installation<a name="installation-1"></a>

This sets up a Git hook that automatically runs checks before each commit. If any check fails, the commit is blocked until the issue is fixed.

```bash
task pre-commit:install
```

### Running Pre-Commit Manually<a name="running-pre-commit-manually"></a>

You can run all configured hooks on every file in the repository (not just the ones you've staged) using:

```bash
task pre-commit
```

This is especially useful when:

- You want to scan the entire codebase for issues.
- You're setting up pre-commit for the first time.
- You’ve made bulk changes and want to ensure everything passes the checks.

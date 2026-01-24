# Development Taxonomy & Git Conventions

This document standardizes **issue types, commit messages, branch naming, and issue references** for the repository.

---

## 1. GitHub Issue Taxonomy

| Prefix         | Keyword       | Type                   | Color       | Description                                           |
|----------------|---------------|-----------------------|------------|-------------------------------------------------------|
| `Bug`          | `BUG:`        | `type: bug`           | 🔴 Red     | Fixes broken functionality, regressions, or errors  |
| `Task`         | `TASK:`       | `type: task`          | 🔵 Blue    | General work or maintenance (e.g., library upgrade) |
| `Subtask`      | `SUB:`        | `type: subtask`       | ⚪ Grey    | Small, dependent pieces of a larger task or epic    |
| `Enhancement`  | `ENH:`        | `type: enhancement`   | 🟢 Green   | Improve an existing feature or optimize behavior    |
| `Refactor`     | `REFACTOR:`   | `type: refactor`      | 🟡 Yellow  | Code restructuring without changing behavior        |
| `Feature`      | `FEAT:`       | `type: feature`       | 🟣 Purple  | Add a brand-new capability or module                |
| `Documentation`| `DOC:`        | `type: documentation` | 🟠 Orange  | Update or add docs, guides, READMEs                 |
| `Spike`        | `SPIKE:`      | `type: research`      | 🔵 Teal    | Time-boxed investigation/prototyping to reduce risk |

**Usage Examples:**
- `BUG: Fix NullPointerException in framework initialization`  
- `TASK: Upgrade Java version to 25 in framework module`  
- `SPIKE: Investigate Kafka state store alternatives`

---

## 2. Branch Naming

| Type       | Pattern                       | Example                     |
|------------|-------------------------------|-----------------------------|
| Feature    | `feature/<short-description>` | feature/user-auth           |
| Bugfix     | `bugfix/<short-description>`  | bugfix/cart-overflow        |
| Hotfix     | `hotfix/<short-description>`  | hotfix/login-crash          |
| Refactor   | `refactor/<short-description>`| refactor/db-layer           |
| Spike      | `spike/<short-description>`   | spike/kafka-state-store     |

---

## 3. Commit Message Guidelines

We follow **Conventional Commits** for consistency, tooling support, and automation.

### 3.1 Core Conventional Commit prefixes (types)
* **feat:**  
  New feature or user-visible behavior change.
* **fix:**  
  Bug fix.
* **docs:**  
  Documentation only (README, comments, specs, ADRs).
* **style:**  
  Formatting only. No logic change (whitespace, lint, imports).
* **refactor:**  
  Code restructuring without changing behavior.
* **test:**  
  Add or modify tests only.
* **chore:**  
  Maintenance tasks: deps, build scripts, CI config, cleanup.

### 3.2 Common but optional extensions

* **perf:** Performance improvement.  
* **build:** Build system or dependency changes (Maven, Gradle, npm, Docker).  
* **ci:** CI/CD pipeline changes.  
* **revert:** Reverting a previous commit.

### 3.3 Breaking changes
Handled explicitly, not via a new prefix:  
* Add `!` after the type: `feat!: change API contract`  
* Or use a footer: `BREAKING CHANGE: …`


### 3.4 Optional vs Automatic Issue Linking
**Optional Issue References in Commits:**  
- To **link a commit to an issue without closing it**, include the issue number in brackets:
  - feat: add-user-profile-endpoint [issue#25]
  - GitHub will **link this commit to issue #25** in the timeline.  
  - The issue will **remain open**.

**Automatic issue closing:** 
  - feat: add-user-profile-endpoint Fixes #25
  - GitHub will **link the commit** and **automatically close the issue** when the commit is merged.  
---

**Key Points:**
- `[issue#25]` or `(issue#25)` are **plain references** — they appear in the timeline but do not close the issue.  
- To **trigger automatic closing**, use one of these keywords (case-insensitive): `Fixes`, `Closes`, `Resolves`.  
- Optional linking with `[issue#25]` works perfectly if you don’t want the issue auto-closed.

---

### 3.5 Guidelines for Commit Messages
1. Prefix commits according to type.  
2. Use kebab-case for the message body.  
3. Keep messages short but descriptive (50–72 characters recommended).  
4. For multi-part work, use multiple commits with clear prefixes.  
5. Use **imperative mood**: `Fix calculation bug in cart totals`.

Example commit messages
* feat: use ScopedValues for context propagation
* fix: handle null context ids
* docs: document breaking changes
* refactor: simplify Kafka Streams join topology
* chore: typo fix
* perf: implement thread pool

### 3.7 What not to do
* Invent cute prefixes (`update:`, `change:`, `misc:`)  
* Overuse `chore:` for everything  
* Mix multiple concerns in one commit

**Bottom line:** Use `feat`, `fix`, `docs`, `refactor`, `test`, `style`, `chore`, plus optional `perf`, `build`, `ci`, and `revert`. Anything else is usually bikeshedding.

---

**Reference:**  
This taxonomy ensures **consistent, readable, traceable issues, commits, and branches** across the team, compatible with GitHub workflows, automation, and tooling.
**Reference:**  
This taxonomy ensures **consistent, readable, and traceable issues, commits, and branches** across the team.

# GIT JOURNEY – DevOps Simulator Challenge

## Introduction

This document describes my complete journey while working on the **Git Mastery / DevOps Simulator Challenge**.  
The purpose of this challenge was not simply to execute Git commands, but to understand how Git is actually used in real-world development and DevOps teams.

Throughout the process, I made a conscious effort to understand:
- why a specific Git command was needed,
- what could go wrong if it was used incorrectly,
- and how similar situations commonly appear when multiple developers work on the same codebase.

By the end of this challenge, I became comfortable handling complex merge conflicts, advanced Git workflows, and even recovering from broken or interrupted Git states.

---

## Phase 1: Repository Setup and Initial Configuration

I started by cloning the instructor-provided repository to my local machine.  
After cloning, I explored the repository structure and verified the available branches, including `main`, `dev`, and `conflict-simulator`.

To follow professional Git practices, I performed the following steps:
- Renamed the original `origin` remote to `instructor` so it was clear which repository was the source
- Created my own public GitHub repository for this challenge
- Added my repository as the new `origin`
- Pushed the initial `main` branch to my repository

This setup helped me clearly separate:
- **Instructor repository (`instructor`)** – reference and source
- **My repository (`origin`)** – active development and final submission

### Key commands used in this phase:
- `git clone`
- `git branch -a`
- `git remote rename`
- `git remote add`
- `git push -u origin main`

This phase reinforced how important a clean and well-organized repository setup is when working in a team environment.

---

## Phase 2: First Merge – Merging `dev` into `main`

In this phase, I merged the `dev` branch into the `main` branch.  
This merge was designed to create multiple conflicts, similar to what happens when parallel development work is merged late in a project.

Conflicts appeared in:
- YAML configuration files
- JSON configuration files
- Shell scripts
- JavaScript files
- Markdown documentation

### Conflict Resolution Strategy (Production-First)

I followed a **production-first** approach while resolving conflicts:
- Production configuration was always treated as the base
- Development features were merged carefully and only when safe
- No development change was allowed to affect production stability

Each conflict was resolved manually by:
- Removing all conflict markers
- Carefully reviewing both versions of the code
- Combining logic where necessary instead of choosing one side blindly
- Double-checking syntax and file correctness after resolution

This phase helped me clearly understand how Git detects conflicts and how careless resolution can easily introduce bugs into a system.

---

## Phase 3: Second Merge – Merging `conflict-simulator` into `main`

This phase simulated a realistic scenario where experimental or unstable changes need to be merged into a stable production branch.

While merging the `conflict-simulator` branch into `main`, I again encountered conflicts in configuration files, scripts, and documentation.

### Strategy for Handling Experimental Changes

To handle these safely:
- Stable production logic was always preserved
- Experimental features were:
  - Clearly commented
  - Disabled by default
  - Placed behind feature flags where possible
- Documentation was updated to clearly explain which parts were experimental

This reflects real DevOps practices, where experimentation is encouraged but must never impact live systems.

---

## Phase 4: Advanced Git Command Usage

This phase focused on using Git beyond basic commits and merges, and handling situations that commonly occur in real projects.

### Advanced Commands Demonstrated

- **git fetch / git pull**  
  Used to keep the local repository in sync with the instructor repository.

- **git stash**  
  Temporarily saved work in progress and restored it later without losing changes.

- **git cherry-pick**  
  Applied a specific commit from another branch and handled conflicts during the cherry-pick process.

- **git rebase**  
  Rebasing branches onto `main`, resolving rebase conflicts manually, and understanding how rebasing differs from merging.

- **git reset (soft, mixed, hard)**  
  Practiced different reset modes to understand how commits, the staging area, and the working directory interact.

- **git revert**  
  Safely reverted commits by creating new undo commits instead of rewriting history.

- **git tag**  
  Created annotated tags to mark important milestones and pushed them to the remote repository.

### Real-World Issues Encountered

During this phase, I also faced and resolved real-world Git issues such as:
- Interrupted rebases
- Stale lock files
- Windows and OneDrive-related Git problems
- Cleaning up and recovering from broken Git states

Handling these issues gave me practical confidence in troubleshooting Git problems instead of panicking when something goes wrong.

---

## Phase 5: Documentation and Final Artifacts

In the final phase, I focused on completing the repository with proper documentation and artifacts.

I created:
- This detailed `GIT_JOURNEY.md`
- `CHANGELOG.md` generated directly from the Git commit history
- Final artifact files:
  - `git-graph.txt`
  - `branches.txt`
  - `tags.txt`
  - `remotes.txt`

These artifacts provide a clear snapshot of:
- Commit history
- Branch structure
- Tag usage
- Remote configuration

---
## Challenges Faced During the Challenge

While working on this challenge, I faced several practical issues such as merge conflicts across multiple file types, interrupted rebases, and stale Git lock files on Windows.  

Resolving these problems required patience and a clear understanding of Git’s internal workflow. These challenges helped me become more confident in debugging Git-related issues instead of relying on trial and error.

## Final Learnings and Reflections

This challenge helped me move well beyond basic Git usage and develop a practical understanding of:
- Resolving complex merge conflicts
- Safely integrating experimental changes
- Recovering from broken or interrupted Git states
- Maintaining clean commit history and meaningful documentation

Completing this task has given me confidence in using Git professionally within collaborative development and DevOps environments.

This repository now stands as a strong portfolio example of my Git skills and real-world readiness.

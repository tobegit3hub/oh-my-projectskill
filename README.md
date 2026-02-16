# oh-my-projectskill

# Introduction

A template for turning project setup documentation into executable Agent Skills.

ProjectSkill is a project-level Agent Skill template. It encodes setup, configuration, and deployment workflows into Skill files that Claude Code can understand and execute — letting the AI agent handle tedious environment configuration on the user's behalf.

The core idea: **turn your installation docs into a Skill, and let the agent run it.**

### Four Core Capabilities

| Capability | Description |
|---|---|
| **Environment Detection** | Run commands to check the OS, installed tools, versions, and runtime state |
| **Interactive Decisions** | Use `AskUserQuestion` to present structured choices when user input is needed |
| **Conditional Branching** | Automatically take different installation paths based on detection results and user choices |
| **Verification & Feedback** | Validate each step with commands; enter troubleshooting automatically on failure |

## Comparison with Traditional Approaches

| Dimension | README Docs | Shell Scripts | ProjectSkill |
|---|---|---|---|
| Readability | Good | Fair | Good (Markdown) |
| Executability | Manual copy-paste | Direct execution | Agent auto-executes |
| Interactivity | None | Limited (`read`/`select`) | Natural language dialogue |
| Environment Adaptation | User must judge | Limited conditionals | Agent intelligently detects |
| Error Handling | Relies on user experience | Fixed error handling | Agent dynamically troubleshoots |
| Maintenance Cost | Low | Medium | Low (written in Markdown) |

# Project Setup

## 1. Check Prerequisites
(Environment detection)

## 2. Install Dependencies
(Dependency installation)

## 3. Configure Environment
(Configuration with user interaction)

## 4. Build & Deploy
(Build and deployment)

## 5. Verify
(Verification tests)

## Troubleshooting
(Common issues and fixes)
```

See [`skills/setup/SKILL.md`](skills/setup/SKILL.md) for the starter template.

## Design Principles

A well-designed ProjectSkill should follow these principles:

1. **Auto-execute, pause only when necessary** — The agent runs commands automatically, stopping only when real user action is required (e.g., scanning a QR code, choosing an architecture option).

2. **Environment awareness** — Never assume the user's environment. Detect the OS, check installed tools, and verify versions before acting.

3. **Structured interaction via `AskUserQuestion`** — When user input is needed, use Claude Code's built-in `AskUserQuestion` tool to present structured options instead of plain text prompts.

4. **Verify every step** — Follow each installation step with a verification command to confirm success before moving on.

5. **Built-in troubleshooting** — Include common problems and their fixes directly in the Skill, so the agent can attempt automatic recovery when errors occur.

## Beyond Setup

While setup is the most common use case, the ProjectSkill pattern extends to other workflows:

- **`/diagnose`** — Project health checks and automated issue detection
- **`/deploy`** — Deployment with interactive confirmation
- **`/migrate`** — Database migrations or version upgrade guidance
- **`/onboard`** — New team member onboarding with architecture walkthroughs
- **`/release`** — Release process including changelog generation, version bumps, and tag creation

Each of these can be written as a Skill for agent-guided execution.

## Getting Started

1. Create a `skills/setup/` directory (or `.claude/skills/`) in your project.
2. Write a `SKILL.md` file using the template structure above, tailored to your project's setup process.
3. After cloning, users just tell Claude Code:

```
user> Help me set up this project
agent> I'll run the setup skill. Let me check your environment first...
agent> Detected macOS with Docker installed. Would you like to use Docker or install Apple Container?
user> Docker
agent> Got it, using Docker. Installing dependencies now...
```

## License

[Apache License 2.0](LICENSE)

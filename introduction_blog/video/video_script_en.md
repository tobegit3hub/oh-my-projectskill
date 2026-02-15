# oh-my-projectskill Video Introduction Script

---

**[Opening - Pain Point]**

Hi everyone, today I'd like to introduce a project: oh-my-projectskill.

If you're a developer, you've probably had this experience — you clone a new project, open the README, and see a long list of installation steps. Installing dependencies, configuring environment variables, choosing a runtime, setting up authentication services… any step along the way can go wrong.

The traditional approach is either writing documentation that users have to follow step by step, or writing shell scripts that break down whenever user input or choices are needed.

**[Core Concept]**

The idea behind oh-my-projectskill is simple: turn installation docs into Agent Skills and let AI handle the execution.

It's a project-level Skill template, written in Markdown format, that Claude Code can directly understand and execute. Compared to traditional scripts, it adds four key capabilities:

- Environment detection — automatically identifies your system platform and existing tools
- Interactive decisions — when a choice is needed, the Agent pauses and asks you
- Conditional branching — follows different installation paths based on detection results
- Verification feedback — automatically verifies after each step, and can troubleshoot on failure

**[Real-World Example]**

This project was inspired by NanoClaw — a WhatsApp-based AI Agent platform. Deploying it requires 9 steps, and nearly every step involves environment checks and user choices.

With ProjectSkill, users just need to say "help me install and configure this project," and the Agent runs through the entire process automatically — asking you when it needs to, executing silently when it doesn't.

**[Extended Use Cases]**

Beyond setup, this approach works for many more scenarios: project health checks, deployment workflows, database migrations, new developer onboarding, release processes — all can be written as Skills.

**[Closing]**

In one sentence: ProjectSkill brings project documentation to life — environment setup is no longer a barrier to entry, but a natural conversation with AI.

The project is on GitHub at https://github.com/tobegit3hub/oh-my-projectskill. Feel free to try it out.

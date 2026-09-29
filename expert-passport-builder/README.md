# expert-passport-builder

**Build an AI expert you can actually argue with.**

“You are a senior marketer” gives you a job title. This skill helps you define a colleague: what decisions it owns, what evidence it trusts, what it rejects, and when it hands the decision back to you.

The output is an **Expertise Passport**. You can use it as a prompt, adapt it into an agent, or keep it as the standing instructions for an expert you consult repeatedly.

## How it works

1. Define the seat: goal, work, audience, expertise gap, and boundaries.
2. Ground its method in documented practice. If you want named influences, choose them from sourced proposals.
3. Write the passport: decision procedure, standards, red lines, handoffs, and an outcome scorecard.
4. Try it on a real first assignment. Keep a log so the expert improves from use.

It works with your existing project files or a brief you give in chat. There is no required vault structure, platform, or fixed cast of experts.

## What you get

- A passport with a specific decision method and source links.
- Acceptance criteria for the first piece of work.
- Optional log and reflection files for continued use.

The skill writes files when you ask for a durable expert or repository artifact. It does not install, deploy, publish, or act in an external account on its own.

## Install

**Easy way:** give your agent this link and ask it to install the skill and run it:

> https://github.com/kirazhestkova/ai-native/tree/main/expert-passport-builder

Or download the repository as a ZIP and give your agent the `expert-passport-builder` folder.

**Claude Code:** copy the folder into `~/.claude/skills/expert-passport-builder/`. **Cowork:** add the folder to your skills directory, or package it as a `.skill` file. Other agents can read `SKILL.md` and its linked template directly.

Then try:

> Build me an AI expert for customer research. It should help my team decide which findings are strong enough to change the product. Its first task is reviewing five interview notes.

## Files

- `SKILL.md` — the workflow and quality check.
- `references/passport-template.md` — the passport, influence, and log formats.

## License

MIT — see [LICENSE](./LICENSE).

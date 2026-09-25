# ✨ Teo Skills

**Small, focused skills for clearer conversations with AI.**

A growing collection by [Timur Catakli](https://github.com/timurcatakli). Install the skills you want, use them in your preferred agent, and keep your workflow your own.

[Browse skills](#-available-skills) · [Install](#-install) · [See an example](#-from-rough-request-to-ready-prompt) · [Add a skill](CONTRIBUTING.md) · [Sources](docs/SOURCES.md)

## 🧰 Available skills

| Skill | What it does |
| --- | --- |
| [teo-improve-prompt](skills/teo-improve-prompt/SKILL.md) | Turns a rough request into a clear prompt, presents it with visual markers, and asks whether to use it in the current chat. |

Each skill lives in its own folder. New skills can join the collection without changing how existing skills are installed or invoked.

## 🚀 Install

With Node.js/npm and Git available, run:

```sh
npx skills add timurcatakli/teo-skills --skill teo-improve-prompt
```

The installer lets you choose a supported agent. Installation is scoped to the current project by default. Add `--global` to make the skill available across projects:

```sh
npx skills add timurcatakli/teo-skills --skill teo-improve-prompt --global
```

To browse the collection before installing:

```sh
npx skills add timurcatakli/teo-skills --list
```

These commands use the community [Skills CLI](https://github.com/vercel-labs/skills). Its supported agents and installation behavior are maintained upstream.

### Manual installation

1. [Download the repository](https://github.com/timurcatakli/teo-skills/archive/refs/heads/main.zip) or clone it:

   ```sh
   git clone https://github.com/timurcatakli/teo-skills.git
   ```

2. Copy `skills/teo-improve-prompt/` into your agent's documented skills directory, keeping `SKILL.md` inside the folder.
3. Reload or start a new session if your agent requires it.

The skills use the open [Agent Skills format](https://agentskills.io/specification). The instructions are model-neutral and require no API key, hook, executable script, or network access to rewrite a prompt. Discovery, command syntax, and installation support depend on your host; compatibility with every agent is not guaranteed.

For a chat tool without skill installation, paste the contents of [SKILL.md](skills/teo-improve-prompt/SKILL.md), then provide your prompt. This supplies instructions for that conversation; it does not install a persistent skill.

## 💬 Use it

Ask your agent:

```text
Use teo-improve-prompt to improve this prompt:
Explain how caching works to a beginner. Use a simple analogy and a diagram.
```

You can also select the skill through your agent's skill picker, if it has one. Natural-language invocation still requires the host to discover and load the installed skill.

## ✨ From rough request to ready prompt

**You write:**

> Explain how caching works to a beginner. Use a simple analogy and a diagram.

**The skill returns:**

✨ Improved Prompt

```text
---Improved Prompt Starts Here----

🎯 Goal
Explain caching to someone with no technical background.

📋 Requirements
- Start with a simple everyday analogy.
- Explain what happens when requested information is in the cache and when it is missing.
- Include a small labeled ASCII diagram showing both paths.
- Explain why cached information can become outdated.

✅ Output
Use plain language, short sections, and define any technical terms you introduce.

---Improved Prompt Ends Here----
```

💬 Would you like to add this prompt to our chat and use it as your next request? (Yes / Edit / No)

### What happens next?

| Your reply | What the skill does |
| --- | --- |
| **Yes** | Uses the displayed prompt as your next request and starts the task. |
| **Edit**, or a specific change | Revises the prompt and asks again. |
| **No** | Leaves the prompt ready to copy without executing it. |

“Add to the chat” means adopting the approved prompt as the next request in the same conversation. The skill does not pretend to create or modify a user message when the host cannot do that. The underlying task still follows the host's permissions and capabilities.

## 🧭 Designed to stay focused

- **Your intent stays intact.** Supplied facts, tools, constraints, and scope carry through.
- **The result comes first.** No unsolicited score, critique, or explanation of the rewrite.
- **Structure earns its place.** Simple prompts stay short; complex prompts get useful sections.
- **Unknowns stay visible.** Essential gaps trigger focused questions or clearly labeled placeholders when an immediate draft is requested.
- **You choose when to proceed.** Rewriting a request does not execute it.

The skill adds no storage, telemetry, history scanning, or background hooks. Your chosen AI provider and host still process conversation content under their own policies.

Prompt rewriting improves clarity; it does not guarantee a correct answer. [Behavioral review cases](docs/VALIDATION.md) cover intent preservation, formatting, clarification, and the approval flow. The [research notes](docs/SOURCES.md) explain the sources and deliberate design choices.

## 🌱 Growing the collection

```text
teo-skills/
├── skills/
│   └── teo-improve-prompt/
│       └── SKILL.md
├── docs/
│   ├── SOURCES.md
│   └── VALIDATION.md
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

To add another skill, create `skills/<skill-name>/SKILL.md`, give it a clear name and description, and add it to the catalog above. Keep any supporting resources inside that skill's folder so it remains independently installable. See [Contributing](CONTRIBUTING.md) for the complete checklist.

Questions or suggestions? [Open an issue](https://github.com/timurcatakli/teo-skills/issues). Please remove private information from examples.

## 📄 License

[MIT](LICENSE) © 2026 Timur Catakli. You may use, modify, and redistribute this collection under the license terms. Referenced third-party materials retain their own licenses.

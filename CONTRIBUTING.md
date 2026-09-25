# Contributing

Add focused skills that are useful independently and preserve the user's intent.

## Add a skill

1. Create `skills/<skill-name>/SKILL.md`. Use a lowercase, hyphenated name matching the folder.
2. Include YAML frontmatter with `name`, `description`, and `license: MIT`. The description should say what the skill does and when to use it.
3. Write concise instructions. Keep host-specific commands optional unless the skill genuinely requires that host.
4. Keep supporting files inside the skill folder and link them with relative paths. Avoid dependencies on sibling skills or repository-level documents at runtime.
5. Add a catalog entry and a realistic usage example to the README.
6. Document sources for borrowed ideas. Do not copy third-party material without satisfying its license.
7. Validate the format against the [Agent Skills specification](https://agentskills.io/specification), check relative links, and try realistic inputs in a compatible agent. Record what was actually tested; distinguish structural checks from behavioral tests.
8. Open a pull request describing the problem solved, expected behavior, and validation.

For changes to `teo-improve-prompt`, use [the behavioral cases](docs/VALIDATION.md). Include both an ordinary case and a case likely to expose unintended behavior. Keep prompts free of personal or confidential information.

## Maintain a skill

Preserve stable skill names so existing installation commands keep working. Update the optional skill version when behavior changes. Keep the README's catalog current, and make intentional behavior changes explicit in pull requests.

Contributions are provided under this repository's MIT license unless explicitly agreed otherwise.

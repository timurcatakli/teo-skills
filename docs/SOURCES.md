# Sources and design decisions

Reviewed September 24, 2026. These are research references, not runtime dependencies. The skill is an original synthesis; no third-party implementation is bundled.

## Requested sources

| Source | Contribution | Boundary |
| --- | --- | --- |
| [MCP Market: Improve Prompt](https://mcpmarket.com/tools/skills/improve-prompt) | Encouraged removal of repetitive prose. | A marketplace description focused on Claude Code instructions; not a benchmark. We did not adopt aggressive punctuation stripping or keyword stuffing. |
| [Google Cloud: What is prompt engineering?](https://cloud.google.com/discover/what-is-prompt-engineering) | Clear goals, audience, context, format, and iterative improvement. | A broad introduction; we do not treat every technique as mandatory. |
| [Prompt Sensei](https://github.com/chengzhongwei/Prompt-sensei) | Task-stage awareness and checking whether a rewrite actually helps. | Its coaching, scores, history analysis, and hooks are outside this skill's scope. No code or prompt templates were copied. |
| [Anthropic: Prompting best practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices) | Explicit requirements, meaningful structure, relevant examples, and appropriate context. | Model-specific tuning is not a portable default. We use labels when helpful rather than requiring XML or a fixed example count. |

## Additional primary sources

| Source | Why it was added |
| --- | --- |
| [Google AI: Prompt design strategies](https://ai.google.dev/gemini-api/docs/prompting-strategies) | Practical treatment of constraints, context, consistent examples, and iteration. Examples are optional here because short tasks often do not need them. |
| [Agent Skills specification](https://agentskills.io/specification) | Defines the portable directory and frontmatter format used by this collection. |
| [Skills CLI](https://github.com/vercel-labs/skills) | Documents selective installation and discovery in repositories containing multiple skills. |

## Synthesis

The central design decision is to preserve intent before adding detail. More words, stronger role claims, or more formatting do not inherently produce a better prompt. We prefer observable requirements, targeted clarification, and proportionate structure. We ask for evidence or a concise rationale when needed rather than hidden reasoning transcripts.

The visual wrapper and the Yes / Edit / No follow-up are this collection's interaction design. They make the draft easy to recognize and keep rewriting separate from carrying out the request. They are not claims about model performance.

Evaluate changes on representative tasks in the intended host: check requirement preservation, unintended scope changes, unnecessary clarification, and the usefulness of the eventual output. Do not infer quality from a numeric prompt score alone.

# GoalPin

### Keep your AI on target.

You ask an agent to change one screen. It redesigns the whole flow. You give it a detailed brief. Halfway through, it forgets what should stay untouched. A correction fixes one problem and introduces another.

**GoalPin gives the agent a compact workflow for understanding the request, staying within scope, checking its work, and correcting demonstrated mistakes.** It works alongside the tools your agent already uses—in desktop apps, browsers, documents, and code.

## What you gain

| Benefit | How GoalPin guides the agent |
| --- | --- |
| Keep the original goal in view | Retains the requested change, exact constraints, protected content, and next step in a compact task record. |
| Preserve existing work | Checks the target and what must remain unchanged before meaningful edits. |
| Catch scope drift | Compares each batch with the request and stops work that starts heading elsewhere. |
| Get corrections that stay focused | Repairs evidenced defects, rechecks affected requirements, and retains the best verified result. |
| Avoid blind assumptions | Asks when missing information would change the outcome; proceeds with clear, authorized work. |
| Spend less effort on repeated context | Reuses valid evidence and concise state; loads detailed guidance only when needed. |

Simple requests stay simple. GoalPin does not require a roadmap, extra reviewers, or repeated questions for every small task.

## One workflow, across your tools

GoalPin guides **the agent doing the work**, so it can apply wherever that agent already has the necessary access and tools.

- **Figma:** change the requested screens while preserving approved components, typography, links, and interactions.
- **Blender:** adjust the specified objects while keeping unrelated scene content, materials, cameras, and settings intact.
- **Browsers and desktop apps:** recheck the active document, selection, or mode before acting on a changed interface.
- **Documents and code:** make a scoped edit, verify the result, and check for regressions in protected content or behavior.

Those are intended workflows, not claims that every application has been tested. GoalPin supplies process guidance; application expertise and control come from your agent's tools and specialist skills.

## How it works

**Understand → Preserve → Plan → Act → Verify → Correct**

1. Inspect what exists and identify the requested difference.
2. Keep track of what may change and what must survive.
3. Plan substantial work at the right level of detail.
4. Make small, coherent batches of changes.
5. Check the result against the request and protected properties.
6. Repair specific defects while useful evidence supports another attempt.

Tool success alone does not mean the task is complete. If corrections stop improving the result, GoalPin directs the agent to return the best verified result, explain the remaining gap, and ask one focused question.

## Get started

**[Download GoalPin skill v0.1.1](releases/goalpin-skill-0.1.1.zip)**

The download contains the ready-to-use `goalpin` skill folder, its four optional references, Codex discovery metadata, and its license. It contains no development source, tests, research notes, local logs, or runtime dependencies. No build step or API key is needed to use the skill itself; your agent still needs its own access to models and tools.

### Codex

1. Extract the ZIP.
2. Copy the extracted `goalpin` folder into your Codex user skills directory: `~/.codex/skills/`, or `$CODEX_HOME/skills/` when you use a custom Codex home. Keep any existing installation until you have reviewed the replacement.
3. Start a new task and invoke it:

```text
Use $goalpin to update the login heading and button label.
Preserve the existing layout, colors, links, and interactions.
Verify the saved result before finishing.
```

### Use it by default

A discoverable skill is not automatically loaded for every task in every host. To enable default guidance, give your agent this instruction after installing the skill:

```text
Make GoalPin's compact core workflow part of my default user instructions
for every task. Preserve my existing preferences. Keep reference links valid,
load optional references only when relevant, and avoid loading the core twice.
Verify default loading in a fresh task.
```

The local Codex integration has verified this approach through user-level `AGENTS.md` instructions. Other hosts need their own supported instruction mechanism. The ZIP does not modify your settings automatically.

### Other agents

Use your host's supported skill import or installation mechanism. If it accepts a `SKILL.md` folder, import `goalpin`. If it only accepts custom instructions, supply the compact core workflow and make its references accessible. Confirm that the host actually loads the instructions before relying on them.

## What has been demonstrated

Actual Codex sessions testing the same workflow showed these outcomes in isolated editable-document tasks:

| Scenario | Observed result |
| --- | --- |
| Default loading | Returned the installed policy revision without opening files or invoking tools. |
| A handoff suggested a broader redesign | Rejected the unrelated changes and made exactly the two requested text edits. |
| An interrupted run had already drifted | Restored three unwanted changes and completed the outstanding requested edit. |
| A request omitted the target and replacement wording | Asked for clarification and left the document unchanged. |
| A simple arithmetic question | Returned the correct answer without tools or unnecessary process. |

Saved-document comparisons and protected-file hashes checked the editing outcomes independently of the agent's completion claims. These examples demonstrate behavior in those cases; they do not establish universal reliability or isolate GoalPin's benefit from the underlying model.

## Designed to reduce wasted tokens

GoalPin keeps the common workflow compact and puts conditional detail in references. It encourages targeted reads, reuse of still-valid evidence, focused corrections, and stopping unnecessary polishing once the requested result is verified.

Actual savings depend on the host, model, task, and how much context the host replays. **No percentage reduction or measured token-savings claim is made.** Cached input, total tokens, price, and latency are different measures.

## Know the scope

This download is the portable guidance skill. It uses the agent's existing tools and permissions; it does not install app controls, intercept every click, or grant new authority. It cannot guarantee perfection. Verification quality depends on what the agent can observe and check, and unfamiliar or inaccessible application state can remain unresolved.

GoalPin is most useful when you want the agent to carry a clear goal through a task, protect existing work, and make corrections without restarting or expanding the assignment.

## License

[MIT](LICENSE). The distributed skill is readable and editable. This repository distributes the finished skill; development materials are maintained locally.

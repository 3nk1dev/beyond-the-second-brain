# Beyond the Second Brain: Cross-LLM Knowledge & Memory

## A Model-Independent Knowledge and Continuity System

Build a model-independent knowledge system with Markdown, reviewed sources, and portable context. The approach connects useful work across LLMs, recovers older chats, and carries approved working preferences between sessions without pretending to synchronize native model memory.

A public working guide by [David Taxer](https://github.com/3nk1dev). This repository contains original teaching material and neutral templates. **It is not the author's private vault or its implementation.**

## Implementation status

**Documented and historically tested:** The underlying private implementation has recorded checks for source preservation, structured updates, validation, retrieval, context generation, and selected device delivery. Its records also describe selective recovery from multiple providers. These are dated implementation records, not a fresh end-to-end test of this public guide.

**Proposed and illustrative:** The fictional multi-model workflows, teaching templates, and broader continuity design describe how the approach can be used. They have not been validated as one complete, generally reliable system. No comparative benchmark establishes superiority over other designs or consistent gains for older models.

**Public scope:** This repository provides a guide, not an installable implementation. The private vault, its contents, code, and history remain separate. Check actual tool access and delivery for each use.

## Influence and our emphasis

Andrej Karpathy’s [LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) is an important influence. It already describes preserved original sources, a linked Markdown knowledge layer, structural instructions, ingestion and query workflows, maintenance checks, Git, Obsidian, and accumulating useful synthesis. We do not claim to have invented those foundations.

This guide emphasizes reconciliation across providers, recovery of older conversations, portable working preferences, bounded context handoffs, and verification of delivery. That is a broader continuity focus, not evidence that this design is objectively better or more robust. Use the parts that solve your actual problem.

## Cross-LLM knowledge and memory workflows

- **One durable record across providers.** Models contribute to shared sources, knowledge, decisions, and open loops rather than separate memory silos.
- **Old conversations become useful again.** Recover user corrections and unfinished work. Reassess weak model answers against evidence without rewriting history.
- **Better context can travel back to older models.** Supply the reviewed result to the next task. This changes the information available, not model weights or native memory.
- **The way you work travels too.** A portable collaboration profile carries approved preferences, reasoning practices, and permission boundaries.
- **Shared knowledge, bounded project views.** Reuse methods without handing every model your entire personal archive.
- **Evidence before confidence.** Saving, believing, deciding, and publishing are separate actions. Verify each one at the right boundary.

The models are interchangeable collaborators. The reviewed knowledge and the way we work stay with us.

## Read and try

1. [Read the guide](GUIDE.md), including fictional multi-model and legacy-chat recovery examples.
2. Choose one project and one permitted source, not your entire account archive.
3. Make a [source record](templates/source-record.md), a [knowledge note](templates/knowledge-note.md), and a [project handoff](templates/project-handoff.md).
4. Prepare a [collaboration profile](templates/collaboration-profile.md) and a [bounded context pack](templates/context-pack.md).
5. Try the pack in a fresh session. Check the answer against the source and constraints before accepting changes.
6. For old material, use the [legacy chat review ledger](templates/legacy-chat-review.md).
7. Record what actually arrived using the [sync verification receipt](templates/sync-verification.md).

## Scope and limits

The guide describes a model-assisted workflow informed by documented multi-provider import and selective recovery. It distinguishes that implementation history from fictional examples and proposed teaching templates. No private source code, original exports, personal notes, or private repository links are included.

This is not an installable app, automatic access to every chat, a native-memory sync service, or a benchmarked claim that every model will perform better. Models need the relevant context and authorized access. Originals may remain external; omissions must stay explicit.

## Privacy and publication

Keep personal knowledge in a separate private store. Publish only reviewed teaching material. Never copy a real vault or its Git history into this repository. Use the [publication checklist](PUBLICATION_CHECKLIST.md) before sharing changes.

## License and reuse

No license has been selected by the author. Public availability does not grant an open-source or redistribution license. No additional reuse rights are granted by this repository; contact the author about permissions.

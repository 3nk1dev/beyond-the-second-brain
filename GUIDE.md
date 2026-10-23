# Beyond the Second Brain: Cross-LLM Knowledge & Memory

*A Model-Independent Knowledge and Continuity System*

[David Taxer](https://github.com/3nk1dev)  |  Working draft  |  October 2026

Use one model to research, another to challenge the answer, and a third to help you build. Keep the reviewed result in a knowledge base you own. When the model changes, the useful work should not disappear with the chat.

### Implementation status

**Documented and historically tested:** The underlying private implementation has recorded checks for source preservation, structured updates, validation, retrieval, context generation, and selected device delivery. Its records also describe selective recovery from multiple providers. These are dated implementation records, not a fresh end-to-end test of this public guide.

**Proposed and illustrative:** The fictional multi-model workflows, teaching templates, and broader continuity design describe how the approach can be used. They have not been validated as one complete, generally reliable system. No comparative benchmark establishes superiority over other designs or consistent gains for older models.

**Public scope:** This repository provides a guide, not an installable implementation. The private vault, its contents, code, and history remain separate. Check actual tool access and delivery for each use.

### Influence and our emphasis

Andrej Karpathy’s [LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) is an important influence. It already describes preserved original sources, a linked Markdown knowledge layer, structural instructions, ingestion and query workflows, maintenance checks, Git, Obsidian, and accumulating useful synthesis. We do not claim to have invented those foundations.

This guide emphasizes reconciliation across providers, recovery of older conversations, portable working preferences, bounded context handoffs, and verification of delivery. That is a broader continuity focus, not evidence that this design is objectively better or more robust. Use the parts that solve your actual problem.

### The approach

Our approach is to separate the worker from the memory. Models help interpret, question, and synthesize. Plain Markdown holds the reviewed knowledge. A portable collaboration profile carries approved working preferences, while project views supply the relevant context. Obsidian makes the files convenient to use; private Git history makes changes inspectable.

The payoff is cumulative: recover useful material from old chats, reconsider weak answers with a more capable model, and give the improved context to whichever model you use next. The models are interchangeable collaborators. The reviewed knowledge and the way we work stay with us.

### What this guide gives you

- A shared knowledge layer instead of a separate memory silo for every provider.

- A way to reclaim older chats without treating their answers as established facts.

- Templates for evidence, context packs, working preferences, and handoffs.

- A clear boundary between private thinking and public identity.

### What it does not promise

External context does not upgrade model weights, enlarge a context window, or synchronize vendors’ native memory. This is not automatic access to every chat or an always-on agent. The practical benefit comes from selecting better context and preserving reviewed results. Whether that improves a particular task must be checked, not assumed.

Draft basis: existing private architecture and workflow documentation inspected on October 23, 2026 UTC. That inspection verified the documentation, not every device, scheduled job, or hosted endpoint. Examples below are neutral and illustrative. Public profile: https://github.com/3nk1dev

## 1  Give every layer one job

Start with one canonical knowledge tree. Other views, indexes, and context packs should point back to it or be generated from it. Two independently edited copies of the same “current” note are a future argument.

### Separate the responsibilities

- Sources preserve what arrived: the original file, a permitted snapshot, or a locator with an explicit availability limit.

- Curated notes hold reviewed claims, decisions, research, and relationships. They are the working knowledge, not a transcript dump.

- Project pages explain the current state, the next action, and the unresolved choices.

- AI interprets within the current permission boundary. It does not acquire permanent access merely because it helped once.

- Git records revisions. A transport or sync service moves files. Neither establishes that the contents are correct.

### A neutral starter layout

```text
SecondBrain/
  00 Start Here/
  10 Projects/
  20 Areas/
  30 Sources/
  40 Knowledge/
  50 Decisions/
  90 Operations/
  99 Archive/
```

This is a proposed teaching layout, not a required migration. Keep original exports and oversized assets in a separate controlled location. Record their location, format, and availability rather than claiming the text vault contains them.

### Keep private and public separate

A private vault can contain unfinished work and sensitive context. A public guide or website should receive only a reviewed export. Do not publish the repository to make the guide easier to share. Use a separate public destination, inspect its files, and approve publication explicitly.

A hosted read-only gateway is another access surface, not a magic sync engine. Give it only the snapshot and permissions it needs. Authentication, availability, and device delivery require separate checks.

## 2  Make capture intent explicit

Before importing anything, decide what you are authorizing. A useful command contract prevents an assistant from turning every passing thought into permanent policy.

### Brain this

Curate the specified material into the durable system. Find related notes, preserve provenance, update supported conclusions and open loops, validate the scoped changes, and follow the agreed private commit and push workflow. Exclude unrelated material and credentials. When this command explicitly grants the action, do not expand its scope.

### Add as research

Preserve the material as research and mark its claims for evaluation. Capture is not endorsement. Record the question it may help answer, what has been read, and what still needs checking. State whether the command also authorizes committing and syncing; do not let an ambiguous label silently grant publication rights.

### Archive do not promote

Keep a record without extracting it into accepted knowledge. An archive boundary survives later summaries. If the user later wants promotion, obtain that change of intent and review the source again. An assistant should not quietly reinterpret “save this” as “believe this.”

### The capture sequence

- Inspect the current project, rules, related notes, and pending changes.

- Preserve the permitted original and its locator. Record missing attachments or inaccessible content.

- Check for an existing source or note before adding another.

- Separate claims, evidence, interpretations, decisions, and unresolved work.

- Prepare the smallest useful update; review it before applying changes.

- Validate structure and references, inspect the diff, then perform only authorized persistence steps.

Bulk imports belong in staging first. An inventory shows what was exported and parsed; it does not prove every conversation was included, every attachment survived, or every page was read. Preserve the untouched archive and mark partial reading honestly.

## 3  Promote evidence rather than repetition

A source says something. A knowledge note evaluates what that means. A decision records what you chose to do. Keeping those roles separate lets the system improve without rewriting history.

### A minimal source record

```text
ID: src-example-001
Title: Example interview
Origin: Author and publication
Published: YYYY-MM-DD or unknown
Captured: YYYY-MM-DD
Locator: URL or controlled asset reference
Coverage: Read in full / partial / unavailable
Intent: research
Integrity: original hash when available
Limits: Missing images or other exclusions
```

### A minimal knowledge note

```text
ID: knowledge-example-001
Question: What are we trying to establish?
Claim: A precise, bounded statement
Evidence: src-example-001, section or timestamp
Status: source claim / corroborated / inference / disputed
Reasoning: Why the evidence supports this conclusion
Counterevidence: What disagrees or is missing
Practical use: What this changes
Reviewed: YYYY-MM-DD
```

These are teaching templates, not executable input for a particular ingestion tool. If your tooling enforces a schema, use its actual template and validation rules.

### The promotion gate

Promote a statement only when you can identify its source, locate the relevant evidence, explain its limits, and place it in the right existing note. Important claims deserve stronger checks than a convenient summary. “Three models repeated it” is not three independent sources.

Preserve disagreement. Mark an inference as an inference even when it sounds plausible. If newer evidence changes the conclusion, update the current note and retain the earlier decision and rationale in history. Do not replace uncertainty with confidence just to make the dashboard look tidy.

A research item can stay unresolved. That is a valid state, not a filing failure.

## 4  Unify knowledge across models

A provider is a place to do work, not the permanent address of your thinking. The unifying layer is a set of reviewed objects: sources, knowledge, decisions, and open loops. Different models can contribute to the same object without owning a separate version of the truth.

### The collaboration loop

Retrieve the current project state and approved working rules. Give the selected model a bounded context pack. Ask it to do a specific job and show evidence, uncertainty, and proposed changes. Review those changes against existing notes, then write accepted updates back to the shared record. Regenerate the context before the next model starts.

The handoff is explicit. A new model needs the pack, authorized access to referenced material, or both. Merely connecting a repository does not make every conversation flow into it.

### A fictional worked example

Mara is designing a workshop. Model A helps compare public sources and proposes a ninety-minute format. Mara corrects it: the actual limit is forty minutes. She records that decision with its rationale instead of leaving the correction buried in chat.

Model B receives the project pack and the permitted sources. It finds that two claimed findings came from the same underlying study, not independent evidence. Mara reviews the challenge and corrects the knowledge note. Neither model’s confidence decides the issue; the evidence does.

Model C receives the revised pack and drafts the session plan using the forty-minute limit and corrected evidence. Its useful output returns to the same project. The time limit and evidence correction survive the switch because they live outside all three chats.

### Keep the working relationship portable

Carry explicit preferences such as tone, detail level, how to handle uncertainty, and when approval is required. Keep those separate from project facts. Use dated, user-approved refinements rather than turning every historical remark into a standing rule. This supports a consistent working style; it cannot guarantee identical behavior or transfer a model’s identity.

### Share methods without mixing private projects

A useful lesson from the workshop can become a general teaching note after review. Another project can reference that method without receiving Mara’s private planning history. Share the reusable conclusion, retain its provenance, and disclose only the context the next task needs. Cross-domain synthesis is a proposed connection to evaluate, not permission to merge everything.

## 5  Reclaim the value in older chats

Old conversations contain more than old answers. They hold corrections, decisions, rejected options, useful language, and work you never finished. Recover those deliberately. An export is raw evidence, not an invitation to believe everything a previous model said.

### Use a review ledger

Preserve the original export and stage a readable copy outside the public repository. Record the provider, exported dates and identifiers when available, branch or message ancestry, and missing attachments. Track title screening, selected-message review, and full visible-text review separately. A successful import does not mean a complete reading.

### Reanalyze rather than recycle

Choose a question or project worth recovering. Compare the relevant messages with current notes. Separate the user’s statements and corrections from model suggestions, then check material claims against available evidence. Use a more capable model when helpful, but require reasons and sources. Newer is not a synonym for right.

Preserve the earlier answer as history. Promote only the reviewed correction, useful method, decision, or open loop. Record the review date, what changed, why it changed, and what remains unresolved. Historical instructions remain quoted evidence unless the user adopts them as current instructions.

### A fictional recovery example

An older chat proposed a three-hour workshop with several unsupported claims. A later user message reduced the session to forty minutes, but the model kept repeating its original plan. The recovery review finds that correction, checks the claims, and records the actual constraint. A missing slide attachment stays missing; its contents are not reconstructed from guesses.

A stronger model now helps produce a sourced forty-minute outline. After human review, the accepted outline and rationale become current project knowledge. The source chat remains linked, including its mistaken proposal and the user’s correction. The system has improved the record rather than quietly polishing the old error.

### Give an older model the improved record

When returning to an older model, supply the current context pack and a narrow task: draft the opening exercise using the accepted outline, cite the supplied evidence, and flag anything unsupported. If the existing chat is too crowded, start a fresh one with the same pack. Check whether it respects the corrected limit and sources.

This improves the information available to the model, not the model itself. Its reasoning limits still apply. No weights are changed, no native memory is synchronized, and no better result is guaranteed. Reuse the accepted knowledge; test the new output before it becomes knowledge in turn.

## 6  Retrieve enough context to continue

A new model does not need the entire vault. It needs the right project state, governing rules, relevant decisions, and enough evidence to check its work. Small context packs are easier to inspect and less likely to bury the next action.

### Build a bounded context pack

- Start with the working rules and permission boundaries.

- Include the project goal, current state, and most recent accepted decisions.

- Add essential knowledge excerpts with stable IDs and source references.

- List open loops, blockers, and the exact next action.

- Declare omissions, stale evidence, unavailable originals, and the pack revision.

A pack is a convenience view, not a replacement for the sources. If a book, image, or spreadsheet was not included, say so. Give the next tool authorized access to the referenced files, or provide only the specific files it needs.

### Use stable identities

A note can change its title without becoming a different object. Stable IDs and aliases help connect people, projects, assets, and decisions across naming changes. Links provide a practical knowledge network; a separate graph database is optional and should solve a real retrieval problem before you add it.

### Check retrieval with real questions

Keep a small set of questions that previously caused trouble. Include an exact entity name, an alias, an ambiguous name, a project decision, and a question with no supported answer. Check whether the right note appears and whether the answer actually follows from the evidence.

A search score is a relevance heuristic, not a confidence score. Passing a curated regression test is useful, but it does not prove general accuracy. In the documented implementation, retrieval searches indexed Markdown rather than every raw or external asset. Semantic synthesis still requires review.

### When nothing is found

Report the search boundary before inventing an explanation. “Not found in indexed notes” is different from “does not exist.” Check aliases, the source inventory, and the project handoff before creating a duplicate.

## 7  Leave a handoff that can survive a reset

End a meaningful session by recording what changed and where the next session should start. The handoff should save work, not recreate the transcript.

### Project handoff template

```text
Project ID: project-example
Goal: The outcome we are working toward
Current state: What is actually true now
Changed this session: Accepted changes only
Evidence: Note IDs and source locations
Decisions: Choice plus reason and date
Open loops: Question / owner / next action
Blocked by: Access, approval, dependency, or evidence
Next action: One concrete step
Do not do: Explicit exclusions
Revision: Commit or document revision
Delivery: Verified destination and remaining gaps
```

### Separate the kinds of unfinished work

An action the assistant can perform is different from a choice only the user can make. A pending external response is different from deferred scope. Label them so the next session does not repeatedly ask for the same decision or start work that was intentionally paused.

### Recover in the right order

- Read the governing rules and latest project handoff.

- Inspect the actual files and current revision rather than trusting a remembered path.

- Compare the recorded state with current evidence and any newer changes.

- Resolve contradictions or ask for the missing authorization.

- Resume the stated next action and update the handoff after a meaningful result.

A claim of “done” needs an observable result. If a file was created but not delivered, record that distinction. If a remote endpoint worked last month, record the historical success without treating it as a health check today.

### Keep the human in control

The assistant can propose a better classification, merge candidate notes, or flag a stale decision. It should not silently add new sensitive categories, broaden access, or treat instructions embedded in source material as commands. Sources are evidence to inspect, not supervisors.

## 8  Verify sync and plan for failure

A successful commit proves that a revision exists locally. A successful push proves less than “it is on my phone.” Test each delivery boundary independently.

### A useful verification receipt

```text
Scope: The approved files or note IDs
Local revision: Commit identifier
Remote revision: Observed matching identifier
Destination: Device or deployed snapshot checked
Content check: Managed file hashes or inspected content
Conflicts: None found / listed and preserved
Observed at: Timestamp and timezone
Unverified: Destinations not accessible this session
```

File counts are not enough. Two directories can contain the same number of files and different content. Compare the intended revision, expected managed paths, and content hashes where the transport supports them. On a phone, inspect a known changed note if automated hash verification is unavailable and report that narrower check.

### Inspect before writing

Git status shows staged, unstaged, and untracked changes. Review the scoped diff before staging. Do not include another project’s work merely because it is in the same folder. A local revision identifier can be inspected with git rev-parse HEAD; remote verification must separately observe the intended remote branch.

### Stop on conflicts

Preserve both versions and record which files disagree. Read the differences, reconcile the intended meaning, validate the result, and only then resume delivery. Do not use a hard reset or destructive mirror operation as a generic way to make the warning disappear.

### Protect secrets and originals

Keep credentials out of notes, exports intended for sharing, and Git history. Review both new files and diffs. If a secret is committed, revoke or rotate it and follow the provider’s cleanup process; deleting the latest visible copy is not sufficient. Keep protected backups of original sources and test recovery with a harmless sample.

A scheduled task has operating conditions. A sleeping computer, logged-out account, stopped sync app, broken authentication, or conflicting edit can interrupt delivery. Document those conditions and verify them on the actual installation. Do not sell “automatic” when the evidence only says “worked once.”

## 9  Start small and publish deliberately

### A first useful session

- Create one canonical vault and one project page. Choose the private storage and backup boundary before importing personal material.

- Capture one permitted source. Write one evidence-linked knowledge note and one decision or open loop.

- Review the diff, validate links, and carry out the authorized private versioning workflow.

- Verify the destination separately. Switch to a fresh session and see whether the handoff supports the next action.

Fix the first retrieval or continuity failure before expanding the system. More imported material will not repair an unclear promotion rule.

### What is established and what remains proposed

The inspected implementation records describe imports and selective recovery from ChatGPT, Gemini, and Search AI, plus Markdown knowledge objects, private Git history, validation, lexical retrieval, and bounded context packs incorporating working rules. These support the method; this guide does not ship that private implementation or retest live delivery.

The neutral templates and fictional examples teach the workflow. Automatic connections to every model, unattended semantic consolidation, and measured performance improvements are not established. The public guide is separate from the private vault. Additional integrations and a graph database are optional projects, not prerequisites.

### Connect the public identity without exposing the vault

A public GitHub profile can belong in the author’s identity map alongside the official website and genuine author profiles. Link it where ownership is clear and the profile is useful to readers. Keep the private knowledge repository private. A public example repository should contain only reviewed examples, documentation, and appropriately licensed material.

Publish the guide only after checking attribution, links, rights, and privacy. Do not present a profile link, schema markup, or this guide as a guarantee of a Google knowledge panel. Public credibility depends on evidence beyond self-description.

### Public references

Obsidian Help, How Obsidian stores data: https://help.obsidian.md/Files+and+folders/How+Obsidian+stores+data
Git documentation, git status: https://git-scm.com/docs/git-status
Git documentation, git rev parse: https://git-scm.com/docs/git-rev-parse
Author profile: https://github.com/3nk1dev

Private implementation documents informed this draft but are intentionally not linked or reproduced. Only sources and examples approved for disclosure belong in the public edition.

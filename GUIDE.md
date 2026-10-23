# Build a Second Brain You Actually Own

*Portable knowledge with AI assistance and human control*

David Taxer  |  3nk1dev  |  Working draft  |  October 2026

Your best thinking should not disappear into a chat thread. The goal is a small, durable knowledge system that keeps the useful conclusions, the evidence behind them, and the work still unfinished. A different model should be able to pick up the job without making you explain your life again.

### The approach

Use plain Markdown as the durable record, Obsidian as a reading and editing interface, and a private Git repository for version history. Let AI help interpret and connect material. Keep ownership, permissions, and promotion decisions with the person running the system.

The distinctive part is the contract: saving a source, accepting a claim, making a decision, and publishing something are different actions. Treat them differently. Otherwise your second brain becomes a junk drawer with autocomplete.

### What this guide gives you

- A minimal structure you can understand without buying another platform.

- A capture and review workflow that preserves sources and disagreements.

- Templates for knowledge, project state, handoffs, and verification.

- A clear boundary between private thinking and public identity.

### What it does not promise

This is not an always-on agent, a complete memory of every conversation, or a deployed graph database. Linked notes and stable identifiers provide useful relationships without pretending that retrieval proves truth. Automation can support the workflow only where access, tools, and authorization actually exist.

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

## 4  Retrieve enough context to continue

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

## 5  Leave a handoff that can survive a reset

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

## 6  Verify sync and plan for failure

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

## 7  Start small and publish deliberately

### A first useful session

- Create one canonical vault and one project page. Choose the private storage and backup boundary before importing personal material.

- Capture one permitted source. Write one evidence-linked knowledge note and one decision or open loop.

- Review the diff, validate links, and carry out the authorized private versioning workflow.

- Verify the destination separately. Switch to a fresh session and see whether the handoff supports the next action.

Fix the first retrieval or continuity failure before expanding the system. More imported material will not repair an unclear promotion rule.

### What is established and what remains proposed

The inspected documentation describes an implemented Markdown knowledge tree, private Git history, source capture, deterministic validation, lexical retrieval, and generated context packs. Earlier records describe accepted desktop and phone delivery. This guide did not retest that live delivery or hosted availability.

The neutral folder layout and simplified templates in this guide are proposed teaching aids. Public packaging, additional integrations, unattended model jobs, and a dedicated graph database are separate choices, not prerequisites or claims of completed work.

### Connect the public identity without exposing the vault

A public GitHub profile can belong in the author’s identity map alongside the official website and genuine author profiles. Link it where ownership is clear and the profile is useful to readers. Keep the private knowledge repository private. A public example repository should contain only reviewed examples, documentation, and appropriately licensed material.

Publish the guide only after checking attribution, links, rights, and privacy. Do not present a profile link, schema markup, or this guide as a guarantee of a Google knowledge panel. Public credibility depends on evidence beyond self-description.

### Public references

Obsidian Help, How Obsidian stores data: https://help.obsidian.md/Files+and+folders/How+Obsidian+stores+data
Git documentation, git status: https://git-scm.com/docs/git-status
Git documentation, git rev parse: https://git-scm.com/docs/git-rev-parse
Author profile: https://github.com/3nk1dev

Private implementation documents informed this draft but are intentionally not linked or reproduced. Only sources and examples approved for disclosure belong in the public edition.

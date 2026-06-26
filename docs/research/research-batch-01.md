# AI Engineering Almanac — Research Batch 01
_Date: 2026-06-25; updated 2026-06-26_

## Purpose

This file is a seed research batch for the public **AI Engineering Almanac** / interactive wiki. It focuses on:
- AI engineering terms
- modern AI workflow vocabulary
- agent/productivity phrases
- prompt macros
- conversation-to-wiki capture language
- frontend/backend contract-engineering vocabulary

The goal is not to create final polished entries yet. The goal is to collect candidate terms, aliases, categories, relationships, and prompt phrases so they can later become canonical wiki pages.

## Source Strategy

Use a two-layer source strategy:

1. **Trend / vocabulary mining**
   - Newsletters, YouTube explainers, product demos, developer blogs, launch notes, and community language.
   - These are good for discovering emerging terms and real phrases people actually use.
   - Example source: The Neuron / The Neuron Daily.

2. **Canonical definition verification**
   - Official docs, research papers, standards, SDK documentation, and vendor docs.
   - These are better for final definitions and production notes.
   - Examples: OpenAI docs, Anthropic docs, Google Gemini docs, MCP docs.

## Important Copyright / Attribution Rule

Do not copy paid newsletters or long copyrighted passages into the public wiki. Instead:
- extract the reusable concept,
- rewrite it in original language,
- cite/link the source,
- convert concrete prompt examples into generic prompt patterns,
- mark unverified product claims as “source-reported” until confirmed by primary docs.

---

# A. Core AI Workflow Taxonomy

| Term | Short Definition | Why Include | Tags |
|---|---|---|---|
| AI Project | A persistent workspace for files, instructions, chats, context, and ongoing work. | Users confuse projects with custom assistants. | ai-workflow, context |
| Custom GPT | A reusable custom assistant configured for a task, role, knowledge base, or action set. | Major user-facing AI customization pattern. | assistants, prompt-engineering |
| Gemini Gem | Google’s custom assistant pattern, similar in spirit to Custom GPTs. | Helps normalize cross-vendor vocabulary. | assistants, google |
| AI Skill | A reusable workflow package containing instructions, constraints, examples, resources, scripts, or quality bars. | One of the biggest productivity unlocks for repeatable AI work. | skills, workflow |
| Skillify | To turn a repeated prompt/workflow into a reusable skill. | Useful shortcut phrase for the Almanac. | prompt-macro, workflow |
| Agent | An AI application that can plan, call tools, preserve state, and perform multi-step work. | Core term for modern AI products. | agents, tool-use |
| Subagent | A specialist helper agent inside a larger workflow. | Useful for reviewer/builder/product-team patterns. | agents, orchestration |
| Plugin | A bundled package of skills, connectors, tools, hooks, or agent capabilities. | Helps explain “toolbox” packaging. | plugins, distribution |
| Connector | A connection between an AI system and an outside app or data source. | Important for Gmail, Drive, Slack, Linear, Notion, databases, etc. | connectors, integrations |
| MCP | Model Context Protocol; a standard way for AI apps to connect to tools, data, and workflows. | Emerging infrastructure layer for agent interoperability. | mcp, protocol |
| Tool | A function, API, or external capability exposed to a model. | Foundation for agentic systems. | tool-use |
| Function Calling | Letting a model request an application-defined function/tool call using structured arguments. | Essential for production AI apps. | tool-use, api |
| Tool Call | A model-generated request to invoke a specific tool with arguments. | Needed for debugging tool traces. | tool-use |
| Tool Call Output | The result returned by a tool back to the model. | Needed for agent loops and traceability. | tool-use |
| Structured Output | Model output constrained to a schema or format such as JSON Schema. | Critical for reliable integration with software systems. | schemas, reliability |
| JSON Mode | A weaker output mode that ensures valid JSON but may not guarantee schema adherence. | Commonly confused with structured outputs. | schemas |
| Schema Adherence | The degree to which model output follows the requested schema exactly. | Key eval dimension for production apps. | evals, schemas |
| Tool Search | A pattern where rarely used tools are deferred and loaded only when needed. | Important for large tool registries. | tool-use, scaling |
| Hosted Tool | A platform-provided tool such as web search, file search, code execution, or computer use. | Important distinction from custom function tools. | tools |
| Custom Tool | An app-defined function or capability exposed to a model. | Foundation of agentic apps. | tools |
| Computer Use | AI-driven control of a computer/browser/UI environment. | Emerging agent capability. | agents, automation |
| Browser Agent | An agent that can navigate web pages, click, extract information, and complete workflows. | Common AI automation pattern. | agents, web |
| Voice Agent | An agent designed for spoken interaction, realtime audio, interruptions, and voice UX. | Important multimodal category. | voice, agents |

---

# B. Prompt Engineering and Prompt Macros

| Term | Short Definition | Why Include | Tags |
|---|---|---|---|
| Prompt Engineering | Writing effective instructions so a model consistently generates desired output. | Canonical foundation term. | prompting |
| Prompt Macro | A reusable high-leverage phrase or template that triggers a known workflow. | Central to this Almanac’s utility. | prompt-macro |
| Prompt Wrapper | A structured prompt shell around raw user intent. | Useful for turning vague requests into reliable outputs. | prompting |
| Prompt Builder | Code or template logic that constructs prompts from typed inputs. | Production-grade prompt management. | prompting, engineering |
| Code-Managed Prompt | A prompt stored and versioned in application code. | Enables review, tests, deployment, and diffing. | prompting, devops |
| Prompt Versioning | Tracking prompt changes as versions with changelog and tests. | Prevents silent behavior drift. | reliability |
| Prompt Snapshot | A frozen version of a prompt used for reproducible behavior. | Useful in evals and production rollouts. | evals |
| Model Snapshot | A specific model version pinned for consistent production behavior. | Prevents silent model-change regressions. | models, reliability |
| Prompt Fixture | A representative input/output example used to test prompt behavior. | Basis for prompt regression tests. | evals |
| Prompt Regression Test | A test that catches behavior changes after prompt/model updates. | Essential for production AI systems. | evals, testing |
| Prompt Lint | Static review of prompt structure, missing constraints, ambiguity, and unsafe instructions. | Could become a tool in the wiki. | quality |
| Prompt Diff | A before/after comparison of prompt behavior or instructions. | Useful for prompt PR reviews. | promptops |
| PromptOps | Operational discipline for managing prompts like production code. | Strong wiki category. | promptops |
| System/Developer/User Roles | Different instruction authority levels in model calls. | Needed for robust API prompting. | prompting |
| Identity Section | Prompt section describing assistant role, purpose, and communication style. | Common developer-message pattern. | prompting |
| Instructions Section | Prompt section containing rules, constraints, and required behavior. | Core prompt structure. | prompting |
| Examples Section | Prompt section containing desired input/output examples. | Few-shot learning and consistency. | prompting |
| Context Section | Prompt section containing external facts, private data, or task-specific material. | RAG and context engineering. | context |
| Few-Shot Prompting | Giving the model examples so it learns the desired pattern. | Widely used technique. | prompting |
| Zero-Shot Prompting | Asking a model to perform a task without examples. | Baseline prompting term. | prompting |
| Multi-Shot Prompting | Providing multiple examples to shape behavior. | Useful for formatting and tone. | prompting |
| Consistent Example Formatting | Keeping few-shot examples structurally identical. | Prevents undesired output formats. | prompting |
| Role Prompting | Assigning the model a role such as reviewer, architect, PM, or QA. | Useful prompt macro pattern. | prompting |
| XML Delimiters | XML-like tags used to separate prompt sections and source content. | Helps boundary clarity. | prompting |
| Markdown Prompt Structure | Headers, bullets, tables, and sections used to organize prompts. | Human-readable prompt design. | prompting |
| Context Injection | Adding relevant external context into the prompt. | Foundation of RAG and grounded answers. | context |
| Context Window | The maximum amount of input/output a model can consider in one request. | Crucial for long conversations. | context |
| Context Budget | A planned allocation of tokens among task, rules, examples, and evidence. | Prevents context stuffing. | context |
| Context Packet | A compact bundle of relevant project information for a model. | Useful for handoffs and long-running work. | context |
| Context Compaction | Compressing previous context into a smaller representation. | Needed for long conversations. | context |
| Prompt Caching | Reusing repeated prompt prefixes to reduce latency and/or cost. | Important scaling pattern. | performance |
| Citation Gate | A requirement that claims must be supported by sources before publication. | Important for public wiki trust. | research |
| Grounded Answer | An answer tied to provided evidence or retrievable sources. | Needed for fact-heavy AI output. | reliability |
| Hallucination Guard | A prompt/eval pattern that reduces unsupported claims. | Trust and safety. | reliability |
| Refusal Boundary | Instructions for what the model should decline or safely redirect. | Safety and policy. | guardrails |

---

# C. Agent Engineering Terms

| Term | Short Definition | Why Include | Tags |
|---|---|---|---|
| Agent Loop | The repeated cycle of plan → act → observe → verify → continue/stop. | Core agent mental model. | agents |
| Planner | Agent component that decomposes a goal into steps. | Common orchestration role. | agents |
| Executor | Agent component that performs tool calls or code changes. | Common agent role. | agents |
| Critic | Agent role that reviews output skeptically. | Helps reduce self-agreement. | agents, evals |
| Verifier | Agent role that checks whether output satisfies requirements. | Essential for reliability. | agents, testing |
| Builder/Critic Loop | Two-agent pattern where one creates and one challenges. | Powerful for code and specs. | agents |
| Product Team of Agents | Multiple specialists such as PM, UI designer, UX reviewer, backend architect, QA. | High-value workflow for product building. | agents, product |
| Handoff | Passing task ownership between specialist agents or system components. | Core orchestration term. | agents |
| Orchestration | Managing agent roles, tools, state, handoffs, and approvals. | Production agent architecture. | agents |
| Runtime State | The memory/state a workflow preserves across steps. | Needed for multi-step work. | agents |
| Trace | A record of model calls, tool calls, inputs, outputs, and decisions. | Debugging and observability. | observability |
| Human-in-the-Loop | Human review or approval inside an automated workflow. | Safety and governance. | governance |
| Approval Gate | A checkpoint before risky actions like writes, deletes, purchases, or sends. | Agent safety. | permissions |
| Read-Only Connector | Connector that can inspect data but not modify it. | Safer default for agents. | security |
| Write Connector | Connector that can create, update, delete, send, or purchase. | Needs stricter approval. | security |
| Tool Permission Boundary | The rule defining what tools an agent may use and when. | Prevents damage/exfiltration. | security |
| Least-Privilege Tools | Giving an agent only the tools and scopes needed for the task. | Security best practice. | security |
| Sandbox Agent | Agent running in an isolated environment with files/commands/packages. | Safer code execution. | agents |
| Background Agent | Agent that works asynchronously or outside the active chat UI. | Important product pattern. | agents |
| Agent View | A dashboard or UI for monitoring multiple agent sessions. | Helps manage parallel work. | agents |
| Parallel Agents | Multiple agents working on separate scoped tasks simultaneously. | Productivity multiplier. | agents |
| Scoped Task | A bounded task with clear goal, files, constraints, and exit criteria. | Prevents agent sprawl. | agents |
| Auto Mode | Letting an agent proceed with fewer manual approvals after scope is clear. | Useful but needs safety framing. | agents |
| Remote Control | Checking or controlling agent sessions from another device. | Emerging workflow. | agents |
| Voice-to-Agent Capture | Starting a task by voice when ideas arise. | Useful productivity phrase. | voice, agents |
| Agent-Native CLI | A command-line interface designed for both humans and AI agents. | Important emerging product-design term. | cli, agents |
| Ambient Mode | An agent watches a workspace/channel and proactively flags relevant events. | Useful agent UX pattern. | agents, collaboration |
| Shared Second Brain | Team-visible AI assistant/context hub in a shared workspace. | Good product metaphor. | collaboration |
| Runaway Loop | A loop that keeps spending tokens/time without converging. | Important failure mode. | agents, cost |
| Fixed-Pass Loop | A loop constrained to a set number of passes. | Practical guardrail. | agents |
| Exit Criteria | Explicit definition of when the agent should stop. | Essential for loops/goals. | agents |
| Done Looks Like | Plain-English exit criteria phrase. | Excellent prompt macro. | prompt-macro |
| Goal | A higher-level target that an agent/loop works toward until exit criteria are met. | Agent workflow term. | agents |
| Self-Review Bias | Tendency for a generator to overtrust its own output. | Justifies adversarial review. | evals |
| Cross-Model Review | Asking a different model/tool to verify output. | Useful manual subagent pattern. | evals |
| High-Agency Builder | Person/agent/team that proactively ships useful work without over-asking. | Cultural term worth capturing. | culture |

---

# D. Coding Agent / AI Development Workflow Terms

| Term | Short Definition | Why Include | Tags |
|---|---|---|---|
| Worktree | Separate working copy of a repository, useful for parallel agent/code tasks. | Agent coding workflows rely on parallel isolation. | git, agents |
| Repo Map | A summary of important files, folders, entry points, and architecture. | Helps agents navigate codebases. | codebase |
| Patch Plan | A structured plan of files to change and why. | Improves code generation reliability. | coding |
| Diff Review | Reviewing generated code changes as a diff. | Core human/AI workflow. | git |
| CI Fixer | Agent/workflow that watches failing CI and proposes fixes. | Common automation use case. | devops |
| Bug Report to PR | Workflow that turns a bug report into investigation, fix, tests, and pull request. | High-value coding-agent playbook. | agents, coding |
| Repro Harness | Minimal setup that reproduces a bug. | Prevents speculative fixes. | testing |
| Behavioral Verification | Checking that software works for the user, not merely that tests pass. | Important correction to weak agent tests. | testing |
| TDD Overfit | When an agent writes weak tests and overfits code to pass them. | Important AI coding failure mode. | testing |
| Smoke Test | Fast basic test that verifies the system still works. | Good agent validation step. | testing |
| Golden Path | The primary happy-path user flow that must work. | Useful product/testing term. | product |
| Regression Fixture | A stored case that previously failed and should not fail again. | Production quality. | testing |
| Appshot | A screenshot or captured app state used for review/debugging. | Useful for frontend agents. | frontend |
| CLAUDE.md | Project instruction file pattern for Claude-based coding workflows. | Important emerging artifact pattern. | agents |
| AGENTS.md | Project instruction file pattern for coding agents. | Cross-agent repository instructions. | agents |
| Project Instruction File | Local file containing repo-specific instructions for agents. | Avoids repeating context in every chat. | context |
| Memory Update | Adding repeated lessons/mistakes to project memory or instruction files. | Useful workflow phrase. | agents |
| Verify It, Don’t Just Test It | Prompt phrase requiring behavioral validation beyond unit tests. | High-leverage macro. | prompt-macro |
| One Scoped Task Per Agent | Rule for avoiding multi-agent conflicts. | Good agent workflow practice. | agents |
| Parallel Work Isolation | Keeping separate agent work from overwriting other changes. | Git/worktree pattern. | agents |
| AI Code Reviewer | Agent/persona that audits generated code for bugs, security, style, and maintainability. | Common subagent. | coding |

---

# E. Frontend–Backend Contract Engineering

| Term | Short Definition | Why Include | Tags |
|---|---|---|---|
| Backend-Ready Frontend Spec | A frontend feature spec detailed enough for backend implementation. | Major productivity accelerator. | frontend, backend |
| Mock Screenshot | A visual/wireframe representation used to infer backend requirements. | Helps translate UI to APIs and data. | design |
| Field-to-Backend Mapping | Mapping each UI element to state, API field, backend type, DB column, validation, and errors. | Reduces integration bugs. | api, frontend |
| UI Element Inventory | List of every visible field, button, filter, state, and action. | Prevents missing backend requirements. | frontend |
| Component Inventory | List of reusable UI components needed by a feature. | Helps frontend planning. | frontend |
| API Contract | Agreement on endpoint path, request/response schema, errors, permissions, and side effects. | Core integration artifact. | api |
| DTO | Data Transfer Object; shape of data crossing an API/application boundary. | Common backend term. | backend |
| View Model | Shape of data optimized for display in the UI. | Explains backend response design. | frontend |
| Schema-First Development | Designing schema/contracts before implementation. | Prevents naming/type drift. | api |
| Contract-First Development | Agreeing on interfaces before frontend/backend implementation. | Enables parallel development. | api |
| Mock API | Fake API that returns data matching the final contract. | Lets frontend proceed before backend is ready. | frontend |
| Fixture Fidelity | How closely mock data matches real production API data. | Prevents late integration bugs. | testing |
| Contract Test | Test ensuring frontend/backend agree on payloads and errors. | Protects integration. | testing |
| State Matrix | Table of loading, empty, success, error, permission, and edge states. | Essential product-quality artifact. | frontend |
| Error State | UI and API behavior when something fails. | Frequently forgotten. | frontend |
| Empty State | UI shown when no data exists. | Product polish and reliability. | frontend |
| Loading State | UI behavior while waiting for data/action completion. | UX quality. | frontend |
| Permission Matrix | Who can view, create, update, delete, approve, export, or administer. | Security/product alignment. | auth |
| Analytics Event Map | Mapping user actions to analytics events and properties. | Product instrumentation. | analytics |
| Integration-Ready Backend | Backend whose API, validation, errors, and payloads match frontend expectations. | Practical definition of “done.” | backend |
| Handoff Packet | Complete package for frontend/backend/QA alignment. | Reusable template. | product |
| Acceptance Criteria | Conditions that must be true for work to be accepted. | Product/testing staple. | product |
| Edge Case Matrix | Table of unusual inputs, states, permissions, timing, and failures. | Reduces bugs. | testing |
| Eventual UI Contract | Expected frontend behavior once backend integration is complete. | Helps build backend first. | frontend |

---

# F. Conversation Capture & Knowledge Distillation

| Term | Short Definition | Why Include | Tags |
|---|---|---|---|
| Session-to-Wiki Compiler | Workflow that converts a conversation into wiki entries, prompt macros, templates, decisions, and tasks. | Core project capability. | knowledge-capture |
| No-Loss Distillation | Preserving raw information first, then extracting summaries and canonical entries. | Prevents over-summarization. | knowledge-capture |
| Raw Transcript | Original conversation record. | Source of truth, private by default. | archive |
| Clean Transcript | Lightly edited transcript with noise removed and privacy protected. | Safer review input. | archive |
| Session Digest | Structured summary of goals, decisions, terms, prompts, artifacts, and follow-ups. | Main public/private bridge. | knowledge-capture |
| Canonical Entry | Polished wiki page for a concept. | Final public knowledge object. | wiki |
| Raw Insight | Interesting but unpolished idea preserved for later. | Prevents idea loss. | knowledge-capture |
| Knowledge Extraction Checklist | Checklist for mining conversations into durable objects. | Makes the process repeatable. | workflow |
| Prompt Macro Extraction | Pulling reusable AI instructions out of a conversation. | Central to Almanac value. | prompt-macro |
| Artifact Inventory | List of generated images, files, code, diagrams, and templates. | Prevents losing outputs. | artifacts |
| Decision Log | Record of decisions, rationale, and follow-up implications. | Useful for project memory. | project-management |
| Redaction Pass | Removing private/sensitive info before publication. | Public safety. | privacy |
| Privacy Boundary | Explicit rule separating public, private, and never-publish content. | Needed for public wiki. | privacy |
| Source Note | Metadata connecting an entry to sources or sessions. | Trust and traceability. | research |
| Confidence Label | Label such as draft, verified, source-reported, opinion, or canonical. | Prevents overclaiming. | research |
| Changelog Entry | Record of how a wiki page changed. | Public project maintenance. | docs |
| Compressed Context | A compact context block that can be pasted into a future AI session. | Long-running project memory. | context |
| Context Rehydration | Restoring a future AI session from compressed context and canonical docs. | Useful project workflow. | context |
| Conversation Archaeology | Searching old chats for reusable decisions, phrases, and ideas. | Good Almanac phrase. | knowledge-capture |
| Canonicalization Pass | Turning messy extracted ideas into structured wiki entries. | Important process stage. | wiki |
| Redact Then Publish | Workflow phrase: sanitize before making public. | Privacy macro. | prompt-macro |
| Preserve First, Distill Second | Workflow principle for no-loss capture. | Core capture doctrine. | prompt-macro |
| Extract, Don’t Summarize | Prompt phrase that prevents lossy summaries. | Excellent macro. | prompt-macro |

---

# G. RAG, Retrieval, and Knowledge Systems

| Term | Short Definition | Why Include | Tags |
|---|---|---|---|
| RAG | Retrieval-Augmented Generation; fetching relevant external context before generation. | Core AI engineering architecture. | rag |
| Embedding | Dense vector representation of text/image/audio for similarity search. | Core retrieval term. | embeddings |
| Vector Database | Database optimized for storing/searching embeddings. | Common AI app component. | vector-db |
| ANN Search | Approximate nearest-neighbor search over vectors. | Explains vector DB performance. | vector-search |
| HNSW | Graph-based ANN index often used for vector search. | Important technical term. | vector-search |
| IVF | Inverted-file index strategy for vector search. | Retrieval architecture term. | vector-search |
| Cosine Similarity | Similarity measure based on vector angle. | Common embedding metric. | embeddings |
| Dot Product | Vector similarity/scoring operation. | Common embedding metric. | embeddings |
| BM25 | Classic keyword search ranking algorithm. | Needed for hybrid search. | search |
| Hybrid Search | Combining keyword and semantic/vector search. | Practical retrieval best practice. | search |
| Reranker | Model/stage that reorders retrieved candidates for relevance. | Improves retrieval quality. | rag |
| Chunk | A section of a document indexed/retrieved as a unit. | Core RAG term. | rag |
| Chunking Strategy | How documents are split into retrievable chunks. | Affects RAG quality. | rag |
| Chunk Overlap | Repeated text across adjacent chunks to preserve context. | Common RAG tuning knob. | rag |
| Metadata Filter | Filtering retrieval by document attributes like date, source, tenant, tags. | Production retrieval. | rag |
| Query Expansion | Rewriting/expanding a query to improve recall. | Search quality. | rag |
| Query Decomposition | Breaking complex questions into subqueries. | Deep research / multi-hop retrieval. | rag |
| Multi-Hop Retrieval | Retrieval where answer requires multiple pieces of evidence. | Advanced RAG. | rag |
| Citation Span | Exact source passage supporting a claim. | Trust and public wiki. | citations |
| Source Fidelity | How accurately output reflects source material. | Evals/trust. | evals |
| Groundedness Score | Evaluation of whether claims are supported by evidence. | RAG evals. | evals |
| Retrieval Audit | Inspecting what docs were retrieved and why. | Debugging RAG. | observability |
| Semantic Cache | Cache keyed by meaning/similarity instead of exact string. | Performance/cost optimization. | caching |
| Context Stuffing | Dumping too much context into a prompt without selection. | Common RAG mistake. | anti-pattern |
| Lost in the Middle | Failure mode where models underuse information buried in long context. | Context engineering. | context |
| Evidence Packet | Bundle of relevant source excerpts used to answer a question. | Useful prompt/RAG term. | research |

---

# H. Evaluation, Guardrails, and Reliability

| Term | Short Definition | Why Include | Tags |
|---|---|---|---|
| Eval | A test or benchmark measuring model/application behavior. | Production AI foundation. | evals |
| Golden Set | Curated set of representative examples with expected outputs. | Key eval asset. | evals |
| Smoke Eval | Lightweight eval run before deployment. | Fast reliability check. | evals |
| Regression Eval | Eval designed to catch behavior regressions. | Production AI testing. | evals |
| Rubric | Criteria used to judge output quality. | Human/model grading. | evals |
| Grader | Human, code, or model that scores outputs. | Evaluation architecture. | evals |
| LLM-as-Judge | Using an LLM to score another output. | Useful but needs calibration. | evals |
| Calibration | Aligning confidence/scores with real correctness. | Reliability term. | evals |
| Adversarial Eval | Testing against hard, malicious, or edge-case inputs. | Safety/reliability. | evals |
| Red Teaming | Actively trying to break a model/system. | Safety and security. | security |
| Prompt Injection | Malicious or conflicting instructions inserted through user/data context. | Core AI security risk. | security |
| Indirect Prompt Injection | Prompt injection hidden in external data fetched by tools/RAG. | Critical for agents. | security |
| Jailbreak | Attempt to bypass model/system safeguards. | Safety vocabulary. | security |
| Tool Exfiltration | Sensitive data leaking through tool use or outputs. | Agent security. | security |
| Output Parser | Code that validates/parses model output into expected format. | Production reliability. | schemas |
| Refusal Handling | Detecting and responding to model refusals gracefully. | Production UX. | safety |
| Guardrail | Policy/check that blocks, modifies, or escalates risky behavior. | AI safety engineering. | safety |
| Human Review Queue | Queue where uncertain/risky AI outputs await human approval. | Governance. | workflow |
| Confidence Threshold | Score threshold for action, review, or refusal. | Decision systems. | evals |
| Rollback Plan | Way to revert prompt/model/tool changes. | Production safety. | devops |
| Canary Prompt Rollout | Testing prompt changes on small traffic before full release. | PromptOps. | devops |
| Drift Monitoring | Watching output quality change over time. | Production AI. | monitoring |
| Incident Review | Postmortem after AI system failure. | Reliability practice. | reliability |

---

# I. Engineering Reliability, Systems, and Backend Terms

| Term | Short Definition | Why Include | Tags |
|---|---|---|---|
| Idempotency | Repeating an operation produces the same system state. | Critical for retries/payments/APIs. | backend |
| Backpressure | Downstream service slows upstream producers to avoid overload. | Core reliability term. | systems |
| Circuit Breaker | Fails fast when dependency is unhealthy to prevent cascading failure. | Distributed systems staple. | reliability |
| Rate Limiting | Restricting request/action rate. | Security/cost/reliability. | backend |
| Debounce | Delay action until rapid events stop. | UI/API efficiency. | frontend |
| Throttle | Limit action frequency over time. | UI/API efficiency. | frontend |
| Queue | Buffer of work to process asynchronously. | Systems design. | backend |
| Dead-Letter Queue | Queue for failed messages that need inspection/retry. | Reliability. | backend |
| Retry with Exponential Backoff | Retry strategy with increasing delays. | Network/API resilience. | backend |
| Timeout | Maximum time allowed before giving up. | Reliability. | backend |
| Fallback | Alternate behavior when primary path fails. | Resilience. | reliability |
| Bulkhead | Isolation pattern limiting failure spread. | Distributed systems. | reliability |
| SLI | Service Level Indicator; measured reliability metric. | SRE. | observability |
| SLO | Service Level Objective; target reliability goal. | SRE. | observability |
| SLA | Service Level Agreement; external/customer commitment. | SRE/business. | reliability |
| Observability | Ability to understand system state from outputs. | Production operations. | observability |
| Trace | End-to-end request/action path through services. | Debugging. | observability |
| Span | Unit of work inside a trace. | Observability. | observability |
| Log | Event record emitted by a system. | Debugging. | observability |
| Metric | Numeric measurement over time. | Monitoring. | observability |
| Canary Deploy | Rollout to small subset before wider release. | Safer deployment. | devops |
| Blue/Green Deploy | Switching traffic between two production environments. | Deployment strategy. | devops |
| Feature Flag | Runtime switch controlling feature behavior. | Safe rollout. | devops |
| Kill Switch | Emergency disable mechanism. | Safety. | devops |
| Rollback | Reverting to previous known-good state. | Incident response. | devops |
| Chaos Engineering | Controlled failure experiments to build resilience. | Reliability testing. | testing |

---

# J. Wiki / Public Database Schema Vocabulary

| Term | Short Definition | Why Include | Tags |
|---|---|---|---|
| Frontmatter | Machine-readable metadata at top of Markdown files. | Bridges wiki and database. | docs |
| Slug | URL-friendly identifier for an entry. | Web/wiki structure. | docs |
| Alias | Alternate name for a concept. | Search and discoverability. | docs |
| Tag | Label used for filtering/grouping entries. | Wiki navigation. | docs |
| Backlink | Link from one entry back to related/referencing entries. | Knowledge graph. | wiki |
| Concept Graph | Network of concepts and their relationships. | Future interactive wiki. | graph |
| Relationship Type | Type of link: related_to, confused_with, prerequisite_of, part_of, pattern_for. | Enables graph UX. | graph |
| Status Lifecycle | Draft → reviewed → canonical → deprecated. | Content governance. | docs |
| Deprecated Entry | Old term/page retained but no longer recommended. | Avoids broken links. | docs |
| Canonical Source | Preferred authoritative page/source for a concept. | Trust. | research |
| Source-Reported Claim | Claim attributed to a source but not independently verified. | Avoids overclaiming. | research |
| Public Digest | Redacted publishable version of a private session. | Privacy-preserving publishing. | knowledge-capture |
| Private Raw Archive | Unpublished store of raw transcripts/material. | Preservation without oversharing. | archive |
| Contributor Prompt | Prompt/template that helps contributors submit new terms. | Community growth. | governance |
| Entry Rubric | Standard for accepting a term into canonical wiki. | Quality control. | governance |

---

# K. High-Leverage Prompt Phrases to Add

These are not final prompts; they are candidate “prompt macros” that should each become a wiki entry or template.

## Spec and Contract Macros

```md
Create a backend-ready frontend spec for this feature.

Include:
- mock screenshots or wireframes
- user flow
- UI component inventory
- field-to-backend mapping
- API contracts
- request/response payloads
- database schema
- validation rules
- loading, empty, success, and error states
- permission matrix
- analytics events
- test cases
- mock data fixtures
```

```md
Turn this UI into backend requirements.

Infer:
- endpoints
- data models
- database tables
- relationships
- validation rules
- auth/permissions
- background jobs
- audit logs
- analytics events
- edge cases
```

```md
Create a field-to-backend mapping table for this screen.
Map every UI element to frontend state, API field, backend DTO, database column, required flag, validation rule, and error message.
```

```md
Build mock data that exactly matches the final API response schema.
Do not use placeholder shapes that differ from production.
```

```md
Identify frontend/backend integration risks before implementation.
Look for missing fields, naming mismatches, enum drift, date/time inconsistencies, auth gaps, pagination ambiguity, and unclear error states.
```

## Conversation Capture Macros

```md
Convert this conversation into a no-loss session digest.

Do not merely summarize.
Preserve:
- exact reusable phrases
- decisions
- concepts introduced
- prompt macros
- templates
- artifacts
- open questions
- privacy risks
- canonical wiki updates needed
```

```md
Extract every reusable prompt phrase from this conversation and convert each into a prompt macro with name, use case, template, example input, expected output, and related concepts.
```

```md
Perform a redaction pass before public release.
Flag names, emails, credentials, private business details, internal plans, and unsupported claims.
```

```md
Create a final compressed context block that can be pasted into a future AI session to continue this project without losing the important decisions.
```

## Agent Workflow Macros

```md
Turn this repeated workflow into a reusable AI skill.
Include trigger phrases, instructions, required inputs, optional inputs, quality bar, examples, avoid-list, output format, and version number.
```

```md
Create a product team of subagents for this feature:
- Product Manager
- UX Designer
- Frontend Engineer
- Backend Engineer
- Security Reviewer
- QA Tester
Have each produce a short report, then synthesize the implementation plan.
```

```md
Create a builder/critic loop.
The Builder proposes the solution.
The Critic tries to reject it by finding bugs, gaps, ambiguity, security issues, and missing tests.
Repeat until the Critic has no material objections.
```

```md
Define the agent’s exit criteria.
Use concrete stopping conditions such as tests passing, screenshots verified, contract satisfied, docs updated, and no unresolved TODOs.
```

```md
Run a fixed-pass improvement loop.
Perform exactly three passes:
1. correctness
2. completeness
3. simplification
Then stop and report remaining risks.
```

## PromptOps / Evals Macros

```md
Before changing this production prompt, create representative fixtures, expected outputs, failure cases, and an evaluation rubric.
```

```md
Version this prompt like code.
Create:
- prompt name
- version
- changelog
- inputs
- output schema
- examples
- evals
- rollout plan
- rollback plan
```

```md
Generate a structured output schema for this task.
Use clear key names, descriptions, required fields, enums where useful, and validation notes.
```

```md
Create a prompt regression test suite that catches formatting drift, hallucinations, missing citations, schema failures, and tool-use mistakes.
```

## Research / Wiki Macros

```md
Mine this source for terms, but do not copy it.
Extract reusable vocabulary, workflow patterns, prompt structures, aliases, and relationships.
Rewrite everything in original language and cite the source.
```

```md
Turn this messy note into a canonical wiki entry using the Almanac schema:
Definition, Core Concept, Why It Matters, Real-World Example, Common Mistakes, Related Terms, Mental Model, Interview Explanation, Production Notes, Prompt Macros.
```

```md
Find the hidden engineering vocabulary in this text.
List jargon, acronyms, shorthand phrases, anti-patterns, workflow patterns, and terms that beginners would not know to search for.
```

```md
Create a concept graph from these terms.
Use relationship types:
- prerequisite_of
- related_to
- confused_with
- alternative_to
- part_of
- pattern_for
- anti_pattern_of
```

---

# L. Suggested New Wiki Categories

1. **AI Workflow Terminology**
2. **Prompt Macros**
3. **PromptOps**
4. **Agent Engineering**
5. **AI Skills and Reusable Workflows**
6. **Frontend–Backend Contract Engineering**
7. **Conversation Capture and Knowledge Distillation**
8. **RAG and Retrieval**
9. **Structured Outputs and Tool Use**
10. **AI Evaluation and Guardrails**
11. **Coding Agent Workflows**
12. **Engineering Reliability**
13. **Wiki Schema and Public Database Design**
14. **AI Product Vocabulary**
15. **AI Anti-Patterns**

---

# M. First Canonical Entries to Create

Prioritize these entries first because they form the backbone of the system:

1. Prompt Macro
2. AI Skill
3. Session-to-Wiki Compiler
4. No-Loss Distillation
5. Backend-Ready Frontend Spec
6. Field-to-Backend Mapping
7. Contract-First Development
8. Agent
9. Subagent
10. Agent Loop
11. Exit Criteria
12. Fixed-Pass Loop
13. MCP
14. Connector
15. Function Calling
16. Structured Outputs
17. PromptOps
18. Prompt Regression Test
19. Eval
20. Golden Set
21. RAG
22. Context Packet
23. Source Fidelity
24. Privacy Redaction Pass
25. Canonical Entry

---

# N. Proposed Entry Schema

```md
---
id: term-slug
title: Term Name
category: Category
status: seed | draft | reviewed | canonical | deprecated
difficulty: beginner | intermediate | advanced
aliases: []
tags: []
related: []
confused_with: []
prerequisites: []
source_notes: []
created: YYYY-MM-DD
updated: YYYY-MM-DD
---

# Term Name

## Definition

## Core Concept

## Why It Matters

## Real-World Example

## Common Mistakes

## Related Terms

## Mental Model

## Interview Explanation

## Production Notes

## Prompt Macros

## See Also

## Source Notes
```

---

# O. Research Backlog Sources

Suggested sources to mine next:

- The Neuron Daily archive
- The Neuron explainer articles
- OpenAI developer docs
- Anthropic Claude docs
- Google Gemini docs
- MCP docs
- LangChain docs
- LlamaIndex docs
- Vercel AI SDK docs
- Microsoft AutoGen / Semantic Kernel docs
- Hugging Face docs
- NVIDIA CUDA / inference optimization docs
- Kubernetes docs
- Google SRE book
- AWS Well-Architected Framework
- Martin Fowler architecture terms
- OWASP Top 10 and OWASP LLM Top 10
- Papers With Code task pages
- arXiv papers on agents, RAG, evals, tool use, and prompt optimization

---

# P. Research Batch Notes

The biggest insight from this batch:

> The Almanac should not only define technical terms. It should define **workflow phrases** that help users get more value from AI systems.

Examples:
- “Turn this into a skill.”
- “Make this backend-ready.”
- “Define done.”
- “Run a fixed-pass loop.”
- “Create a verifier.”
- “Preserve first, distill second.”
- “Extract, don’t summarize.”
- “Mock data must match the final API.”
- “Verify it, don’t just test it.”

That is the differentiator. A normal glossary explains terms. This Almanac teaches users the phrases that make AI-assisted engineering faster.

---

# Q. Conversation Extraction — Durable Knowledge Objects
_Date extracted: 2026-06-26_
_Source session: AI Engineering Almanac project seed conversation_
_Status: project-memory / ready for canonicalization_

## Q1. Session Summary

This conversation established the AI Engineering Almanac as more than a glossary. It is becoming a public, versioned engineering knowledge base containing:

- canonical technical terms,
- AI workflow phrases,
- prompt macros,
- production engineering patterns,
- frontend/backend contract templates,
- conversation-to-wiki capture workflows,
- source strategy and editorial rules,
- generated diagrams and teaching artifacts.

The strongest emerging product idea is:

> A public, searchable, GitHub-backed wiki/database of AI engineering vocabulary, workflow phrases, implementation templates, and source-verified canonical entries.

The strongest process idea is:

> Extract, don’t summarize: preserve the useful objects from a conversation before compressing them into polished pages.

---

## Q2. Canonical Terms Extracted From This Session

| Term | Type | Draft Definition | Priority | Suggested Category |
|---|---|---|---|---|
| AI Engineering Almanac | project concept | A public, versioned knowledge base for AI engineering terms, workflow phrases, prompt macros, and production patterns. | P0 | project-meta |
| AI Engineering Bible | alias | Informal name for a comprehensive, practical reference that teaches both terminology and how to use it. | P1 | project-meta |
| Workflow Phrase | concept | A short phrase that triggers a repeatable AI-assisted workflow, such as “make this backend-ready.” | P0 | prompt-macros |
| Prompt Macro | concept | A reusable instruction pattern that converts vague intent into a structured workflow. | P0 | prompt-macros |
| Engineering Accelerator Phrase | concept | A phrase that speeds up implementation by forcing hidden requirements into explicit artifacts. | P0 | prompt-macros |
| Backend-Ready Frontend Spec | canonical term | A frontend feature specification detailed enough for backend implementation without waiting for final UI wiring. | P0 | frontend-backend-contracts |
| Frontend–Backend Contract Engineering | category | The discipline of aligning UI fields, API payloads, backend types, database columns, validation, permissions, and error states before implementation. | P0 | frontend-backend-contracts |
| Field-to-Backend Mapping | canonical term | A table mapping each UI element to frontend state, API field, backend type, database column, validation, and error behavior. | P0 | frontend-backend-contracts |
| Mock Screenshot | canonical term | A rough visual/wireframe screen representation used to extract backend requirements and user flows. | P0 | frontend-backend-contracts |
| Backend Requirements Extractor | phrase/concept | A mock screen or UI spec that reveals APIs, data models, permissions, and edge cases. | P1 | frontend-backend-contracts |
| API Contract | canonical term | The formal agreement between frontend and backend for endpoint paths, request/response schemas, errors, auth, and side effects. | P0 | api-design |
| Contract-First Development | canonical term | Defining interfaces, schemas, and expected behaviors before frontend and backend implementation. | P0 | api-design |
| Schema-First Development | canonical term | Designing data schemas before implementation, often using OpenAPI, GraphQL, Prisma, Zod, JSON Schema, or Protocol Buffers. | P1 | api-design |
| Integration-Ready Backend | canonical term | A backend that can be connected to the frontend with minimal debugging because payloads, validation, errors, permissions, and response shapes match the frontend spec. | P0 | frontend-backend-contracts |
| Mock API | canonical term | A fake or stub API that returns data matching the final contract. | P1 | frontend-backend-contracts |
| Fixture Fidelity | concept | The degree to which mock data matches the final API and realistic production values. | P1 | testing |
| Frontend–Backend Handoff Packet | canonical term | A complete feature package containing screens, flows, fields, APIs, schemas, validations, permissions, states, analytics, and tests. | P0 | frontend-backend-contracts |
| State Matrix | canonical term | A table defining loading, empty, success, validation error, permission error, and unexpected failure states. | P1 | frontend-backend-contracts |
| Conversation Capture | category | The practice of extracting durable knowledge, decisions, templates, and artifacts from a conversation. | P0 | conversation-capture |
| Durable Knowledge Object | canonical term | A reusable object extracted from a conversation, such as a term, prompt macro, decision, template, artifact, source note, or follow-up page. | P0 | conversation-capture |
| Session-to-Wiki Compiler | canonical term | A workflow that turns a conversation into canonical wiki entries, templates, prompt macros, decision logs, and source notes. | P0 | conversation-capture |
| No-Loss Distillation | canonical term | A capture method that preserves raw details first, then compresses them into summaries and canonical entries. | P0 | conversation-capture |
| Extract, Don’t Summarize | doctrine / macro | A workflow principle: convert a conversation into structured durable objects instead of producing a lossy summary. | P0 | conversation-capture |
| Preserve First, Distill Second | doctrine / macro | Save raw useful material before turning it into polished knowledge. | P0 | conversation-capture |
| Source Tiering | editorial term | Classifying sources by how they should be used: discovery, canonical definition, examples, commentary, or deprecated claims. | P0 | source-strategy |
| Discovery Source | editorial term | A source used to discover emerging vocabulary, not necessarily to define it canonically. | P0 | source-strategy |
| Canonical Source | editorial term | An official doc, standard, paper, or authoritative reference used for final definitions. | P0 | source-strategy |
| Source Note | editorial term | Metadata linking a wiki entry to the session, primary docs, discovery sources, and confidence level. | P0 | source-strategy |
| Canonical Entry | wiki term | A polished, structured page for a concept, using the entry schema and source notes. | P0 | wiki-schema |
| Docs-as-Database | architecture term | Treating Markdown files with YAML frontmatter as a public database that can later power an interactive wiki. | P0 | wiki-schema |
| GitHub-as-Source-of-Truth | architecture term | Using GitHub as the canonical storage, version history, review workflow, and contribution layer for the Almanac. | P0 | wiki-schema |
| Public Knowledge Base | architecture term | The public-facing documentation/wiki generated from the source repository. | P0 | wiki-schema |
| Research Batch | project artifact | A scoped bundle of raw candidate terms, source notes, and editorial observations for later canonicalization. | P1 | research-process |

---

## Q3. Prompt Macros Extracted From This Session

### Macro 1 — Backend-Ready Frontend Spec

```md
Generate a backend-ready frontend spec for this feature.

Include:
1. Mock screenshots or wireframes
2. User flow
3. Every visible field
4. Field-to-backend mapping
5. API endpoints required
6. Request and response payloads
7. Database tables and columns
8. Validation rules
9. Empty states
10. Loading states
11. Error states
12. Permission rules
13. Analytics events
14. Test cases
15. Mock data fixtures
```

### Macro 2 — Include Mock Screenshots and Field-to-Backend Mappings

```md
Include mock screenshots and field-to-backend mappings so the backend can be built against a stable contract before the frontend is fully wired.
```

### Macro 3 — Turn UI Into Backend Requirements

```md
Given this screen or wireframe, infer all backend requirements, including APIs, database tables, relationships, permissions, validation rules, background jobs, and analytics events.
```

### Macro 4 — Mock Data Must Match Final API

```md
Generate realistic mock data fixtures that exactly match the planned API response schema so the frontend can be built independently from the backend.
```

### Macro 5 — Create API Contract Before Code

```md
Before implementing, define the full API contract, including endpoint names, request bodies, response bodies, error responses, auth requirements, side effects, idempotency behavior, and example payloads.
```

### Macro 6 — Frontend Integration Checklist

```md
Create a frontend integration checklist for this endpoint, including payload shape, auth headers, error handling, pagination, caching, retries, loading states, empty states, permission failures, and edge cases.
```

### Macro 7 — Extract Conversation Into Durable Knowledge Objects

```md
Extract this conversation into durable knowledge objects:
- canonical terms
- prompt macros
- decisions
- templates
- artifacts
- open questions
- source notes
- follow-up wiki entries

Preserve details first, then create a concise session digest.
```

### Macro 8 — Session-to-Wiki Compiler

```md
Convert this session into wiki-ready project memory.

Output:
1. Session digest
2. New candidate terms
3. Canonical entries to create
4. Prompt macros
5. Templates
6. Decisions and rationale
7. Artifacts created
8. Source notes
9. Open questions
10. Next actions
11. Public/private redaction notes
```

### Macro 9 — Redact Then Publish

```md
Before publishing this session, separate public knowledge from private context. Remove private names, credentials, private URLs, personal data, secrets, unreleased plans, and any copyrighted source text that should only be paraphrased.
```

### Macro 10 — Source Strategy Rule

```md
Use newsletters and explainers for vocabulary discovery.
Use official docs, research papers, and standards for canonical definitions.
Mark unverified claims as source-reported until confirmed by primary sources.
```

### Macro 11 — Define Done

```md
Define done for this workflow. Include success criteria, exit criteria, quality bar, tests, artifacts, and what should not be attempted in this pass.
```

### Macro 12 — Build the Verifier

```md
Create a verifier for this output. The verifier should check factual accuracy, schema adherence, missing requirements, edge cases, source coverage, and production readiness.
```

---

## Q4. Decisions Made

| Decision | Rationale | Status | Follow-Up |
|---|---|---|---|
| Use GitHub as the source of truth. | Git gives version history, diffs, PRs, issues, public collaboration, and future automation hooks. | Accepted | Seed `doncazper/ai-engineering-almanac` with docs. |
| Do not use GitHub Wiki as the primary public database. | GitHub Wiki is useful for lightweight docs, but the Almanac needs SEO, many files, structured metadata, and future interactivity. | Accepted | Use repo docs + GitHub Pages instead. |
| Keep content in Markdown with YAML frontmatter. | Markdown is human-editable and frontmatter makes the content machine-readable for a future interactive wiki. | Accepted | Create canonical entry template. |
| Treat the docs folder as a public database. | Each page becomes a queryable record later. | Accepted | Add `data/terms.yml` or generated JSON index later. |
| Use newsletters/explainers for discovery, not final definitions. | Newsletters capture live vocabulary, but canonical pages need stronger sources. | Accepted | Create source tier labels. |
| Add Conversation Capture as a first-class Almanac category. | The project needs to preserve high-value AI conversations without losing information. | Accepted | Create session-to-wiki compiler page. |
| Add Frontend–Backend Contract Engineering as a first-class category. | It captures a practical engineering accelerator that can save hours of integration debugging. | Accepted | Create first canonical entries. |
| Use prompt macros as a separate content type from glossary terms. | Prompt macros are operational commands, not just definitions. | Accepted | Create `docs/prompt-macros/`. |
| Add artifacts as public teaching assets. | Diagrams and screenshots make the Almanac more useful than a text glossary. | Accepted | Put image assets in `assets/`. |
| Use status labels. | Prevents draft notes from being mistaken for verified canonical definitions. | Accepted | `seed`, `draft`, `reviewed`, `verified`, `canonical`, `deprecated`. |
| Preserve raw/private session notes separately from public pages. | Conversation capture can include private or messy details. | Accepted | Add redaction workflow. |

---

## Q5. Templates Created / Needed

### Template A — Canonical Entry

```md
---
id: term-slug
title: Term Name
category: category-name
status: seed | draft | reviewed | verified | canonical | deprecated
difficulty: beginner | intermediate | advanced
aliases: []
tags: []
related: []
confused_with: []
prerequisites: []
source_tier: canonical | discovery | mixed | unsourced
canonical_sources: []
discovery_sources: []
created: YYYY-MM-DD
updated: YYYY-MM-DD
---

# Term Name

## Definition

## Core Concept

## Why It Matters

## Real-World Example

## Common Mistakes

## Related Terms

## Mental Model

## Interview Explanation

## Production Notes

## Prompt Macros

## See Also

## Source Notes
```

### Template B — Prompt Macro

```md
---
id: macro-slug
title: Prompt Macro Name
type: prompt-macro
status: seed | draft | reviewed | canonical
category: prompt-macros
aliases: []
tags: []
inputs: []
outputs: []
related_terms: []
created: YYYY-MM-DD
updated: YYYY-MM-DD
---

# Prompt Macro Name

## Use When

## Prompt

```md
Pasteable prompt here.
```

## Inputs Needed

## Output Should Include

## Why It Works

## Common Failure Modes

## Example

## Related Terms
```

### Template C — Conversation Capture Packet

```md
# Session Capture Packet

## Session Metadata
- Date:
- Project:
- Privacy level:
- Public-safe summary:

## Session Digest

## Canonical Terms

## Prompt Macros

## Decisions

## Templates

## Artifacts

## Source Notes

## Open Questions

## Follow-Up Wiki Entries

## Redaction Notes

## Next Actions
```

### Template D — Frontend–Backend Handoff Packet

```md
# Feature Handoff Packet

## Feature Summary

## User Stories

## Mock Screens / Wireframes

## User Flow

## UI Element Inventory

## Field-to-Backend Mapping

| UI Element | Frontend State | API Field | Backend Type | DB Column | Required | Validation | Error State |
|---|---|---|---|---|---|---|---|

## API Contracts

## Database Schema

## Auth & Permissions

## Loading / Empty / Success / Error States

## Analytics Events

## Test Plan

## Mock Fixtures

## Edge Cases

## Rollout Notes
```

### Template E — Source Note

```md
## Source Notes

| Source | Tier | Use | Notes |
|---|---|---|---|
| Official docs / standard / paper | Canonical | Definition and production guidance | Preferred for final wording. |
| Newsletter / explainer / blog | Discovery | Emerging vocabulary and user-facing phrasing | Do not copy. Paraphrase and verify. |
| Community discussion | Anecdotal | Common confusion and slang | Mark as anecdotal. |
| Internal session | Project memory | Origin of our framing/templates | Redact before publishing. |
```

---

## Q6. Artifacts Created So Far

| Artifact | File / Location | Type | Public? | Notes |
|---|---|---|---|---|
| Research Batch 01 | `ai_engineering_almanac_research_batch_01.md` | Markdown research batch | Yes, after review | Seed corpus of candidate terms. |
| Updated Research Batch 01 | `ai_engineering_almanac_research_batch_01_updated.md` | Markdown research batch | Yes, after review | Includes this conversation extraction. |
| Frontend–Backend Mapping Graphic | `frontend_backend_mapping_guide.png` | Image | Yes | Pretty visual asset for docs/slides/wiki. |
| GitHub Repo | `doncazper/ai-engineering-almanac` | Public repository | Yes | Empty at extraction time; should become source of truth. |
| Deep Research Task 01 | Deep Research session | Research run | Maybe | Broad seed research for Almanac terms. |
| Deep Research Task 02 | Deep Research session | Research run | Maybe | Expanded research across A–O sections. |

---

## Q7. Open Questions

| Question | Why It Matters | Default Recommendation |
|---|---|---|
| Should the public docs use MkDocs Material, Docusaurus, or a custom Next.js app? | Determines build complexity and future interactivity. | Start with MkDocs Material for speed; migrate to Docusaurus/Next.js only if interactivity demands it. |
| What license should the content use? | Determines reuse rights. | Consider CC BY 4.0 for content and MIT for code, but decide explicitly before accepting outside contributions. |
| What counts as “canonical”? | Prevents weak or trend-only definitions from becoming final. | Require at least one authoritative source for verified/canonical status. |
| How much newsletter-derived phrasing can be used? | Copyright and attribution. | Use newsletters only for discovery; paraphrase and cite. |
| How should private sessions be handled? | Avoids leaking private context. | Store public session digests only; never publish raw private transcripts without redaction. |
| Should the Almanac include personal productivity opinions? | The project is practical, but needs trust. | Allow opinions only as “Field Notes” or “Sam’s Heuristics,” separate from canonical definitions. |
| What is the minimum viable entry? | Prevents perfectionism. | Definition, core concept, why it matters, example, mistakes, related terms, source notes. |
| Should every term have relationships? | Enables future interactive graph/wiki. | Yes, at least `related`, `confused_with`, and `prerequisites`. |
| Should the project accept contributions immediately? | Public repo may attract suggestions. | Add issue templates now; PR contribution guidelines after first 25 entries. |
| Should diagrams be generated for every major category? | Visuals improve learning but take time. | Add visuals only to pillar concepts first. |

---

## Q8. Source Notes From This Session

### Editorial Rule

> Use newsletters and explainers for vocabulary discovery. Use official docs, research papers, and standards for canonical definitions.

### Discovery Sources

- The Neuron / The Neuron Daily — useful for discovering emerging AI workflow language, prompt phrasing, newsletter-friendly explanations, and user-facing confusion points.
- Engineering blogs, conference talks, GitHub READMEs, and community discussions — useful for identifying terms people actually use.

### Canonical Definition Sources To Prefer

- OpenAI developer documentation — prompt engineering, structured outputs, function/tool calling, prompt/versioning guidance, agents, tools, evals.
- Anthropic Claude docs — prompt engineering workflow, success criteria, eval-first prompting, guardrails.
- Model Context Protocol docs — MCP terminology, servers, clients, tools, resources, prompts.
- GitHub Docs — repository, wiki, Pages, contribution workflow, Markdown support.
- Standards and specs — JSON Schema, OpenAPI, GraphQL, OAuth, OWASP, Kubernetes docs, SRE books.
- Research papers — RAG, tool use, agent evaluation, hallucination, retrieval, benchmark methodology.

### Notes on Public Reuse

- Do not copy paid newsletter content.
- Do not republish long source excerpts.
- Keep prompt patterns generic unless the source explicitly licenses reuse.
- Add source links and classify source type.
- Mark emerging terms as `seed` or `draft` until confirmed.

---

## Q9. Follow-Up Wiki Entries To Create First

### P0 — Create Immediately

1. `prompt-macro.md`
2. `workflow-phrase.md`
3. `backend-ready-frontend-spec.md`
4. `field-to-backend-mapping.md`
5. `frontend-backend-contract-engineering.md`
6. `frontend-backend-handoff-packet.md`
7. `session-to-wiki-compiler.md`
8. `durable-knowledge-object.md`
9. `no-loss-distillation.md`
10. `source-tiering.md`
11. `canonical-entry.md`
12. `docs-as-database.md`
13. `extract-dont-summarize.md`
14. `mock-data-must-match-final-api.md`
15. `define-done.md`

### P1 — Create Next

16. `api-contract.md`
17. `contract-first-development.md`
18. `schema-first-development.md`
19. `integration-ready-backend.md`
20. `mock-api.md`
21. `fixture-fidelity.md`
22. `state-matrix.md`
23. `permission-matrix.md`
24. `promptops.md`
25. `prompt-regression-test.md`
26. `structured-output.md`
27. `function-calling.md`
28. `tool-calling.md`
29. `mcp.md`
30. `agent-loop.md`
31. `fixed-pass-loop.md`
32. `verifier.md`
33. `critic-agent.md`
34. `rag.md`
35. `context-packet.md`

### P2 — Expand After Foundation

36. `retrieval-augmented-generation.md`
37. `embedding.md`
38. `vector-database.md`
39. `reranking.md`
40. `eval.md`
41. `golden-set.md`
42. `guardrail.md`
43. `red-team.md`
44. `idempotency.md`
45. `backpressure.md`
46. `circuit-breaker.md`
47. `rate-limiting.md`
48. `least-privilege.md`
49. `observability.md`
50. `distributed-tracing.md`

---

## Q10. GitHub Repository Bootstrap Plan

Recommended public architecture:

```txt
ai-engineering-almanac/
  README.md
  ROADMAP.md
  CONTRIBUTING.md
  docs/
    index.md
    source-strategy.md
    research/
      research-batch-01.md
    terms/
      prompt-macro.md
      workflow-phrase.md
    prompt-macros/
      extract-conversation-into-durable-knowledge-objects.md
      backend-ready-frontend-spec.md
    frontend-backend-contracts/
      frontend-backend-mapping-table.md
      backend-ready-frontend-spec.md
    conversation-capture/
      session-to-wiki-compiler.md
      durable-knowledge-object.md
    templates/
      canonical-entry-template.md
      prompt-macro-template.md
      session-capture-template.md
      frontend-backend-handoff-packet.md
    assets/
      frontend-backend-mapping-guide.png
  data/
    terms.yml
  .github/
    ISSUE_TEMPLATE/
      term-request.yml
      prompt-macro-request.yml
```

Principle:

> Start as a Markdown database. Publish as a docs site. Later, generate an interactive wiki from the same frontmatter and file tree.

---

## Q11. Next Moves

### Move 1 — Seed the repo

Add the starter docs, templates, asset image, and updated research batch.

### Move 2 — Choose the first docs engine

Default: MkDocs Material because it is fast, Markdown-native, searchable, and easy to deploy. Docusaurus is a strong later option if the project needs React/MDX interactivity.

### Move 3 — Create the first 15 pages

Do not try to polish 300 entries first. Publish a useful seed with the P0 entries and make the structure obvious.

### Move 4 — Add status labels

Use:

```txt
seed → draft → reviewed → verified → canonical
```

Also use:

```txt
source-reported
needs-source
needs-example
needs-diagram
needs-production-notes
```

### Move 5 — Add a contribution workflow

Start with issue templates:

- request a term,
- request a prompt macro,
- suggest a source,
- propose a correction.

### Move 6 — Add a source strategy page

Publish the rule clearly:

```txt
Discovery sources find terms.
Canonical sources define terms.
```

### Move 7 — Add the conversation capture playbook

This becomes one of the Almanac’s unique features. Most AI glossaries do not teach people how to preserve knowledge from AI sessions.

### Move 8 — Turn Research Batch 01 into entries

Batch 01 is not the final product. It is a queue. The next workflow is:

```txt
candidate term → draft page → source verification → examples → production notes → canonical page
```

### Move 9 — Use GitHub Issues as the ingestion layer

Every new term idea can start as an issue. Every term page can close an issue.

### Move 10 — Build the interactive layer later

After 100+ structured pages exist, generate:

- search index,
- term graph,
- aliases index,
- confused-with comparisons,
- prompt macro browser,
- source coverage dashboard,
- entry status dashboard.

---

## Q12. One-Sentence Project Direction

> The AI Engineering Almanac should become a public, source-aware, GitHub-backed, Markdown-first wiki/database of AI engineering concepts, workflow phrases, prompt macros, implementation templates, and conversation-capture patterns.


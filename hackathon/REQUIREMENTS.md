# Agent Rush requirements

## Shared delivery

Both challenges require:

- A Vultr VM as the central backend and a web app deployed on Vultr.
- A public demo URL and public repository with reproducible setup instructions and documentation.
- A recorded demonstration and an explanation of the use case, architecture and Vultr services used.

Event GPUs are unavailable.

Sources: [challenge obligations](https://lablab.ai/ai-hackathons/vultr-hackathon#2) · [technology and access](https://lablab.ai/ai-hackathons/vultr-hackathon#3).

[SUBMISSION.md](SUBMISSION.md) covers media, form fields and release checks.

## Blast Radius Zero

Build an agent that executes model-generated code, browser actions or both in an isolated environment on Vultr.

| Build requirement | What to show |
|---|---|
| All agent LLM calls use Vultr Serverless Inference (VSI). | Show the configured endpoint and connect a generated action to its executed result. |
| Generated code and browser actions execute outside the app process, in isolation, and return verifiable executed output. | Show dispatch, sandbox execution and the returned artifact or observable browser state alongside its execution record. |
| Keep credentials out of the sandbox. | Explain the secret boundary using redacted configuration and demonstrate blocked access to a protected resource. |
| Cap time and memory; reset or destroy the sandbox after every task. | Show enforced limits, termination, cleanup and a successful subsequent task. |
| Include a containment moment in the video. | Show the attempted action, enforced boundary or limit, and resulting system state. |
| Browser use includes screenshots, vision verification and human approval before final actions. | Show captured state, verification and the approval gate before the final action executes. |

Docker is strongly recommended. A separate worker VM is a design option for hosting isolated execution.

Source: [challenge obligations](https://lablab.ai/ai-hackathons/vultr-hackathon#2).

## Powering the Future of Work

Build a connected enterprise workflow, agentic or rule-based, with a public browser experience and a useful result. VSI is optional. Focus areas include sales, finance, HR, support and procurement.

| Build requirement | What to show |
|---|---|
| Connect enterprise workflow steps. | Follow one user task across actions and inspect the data passed between them. |
| Deliver a useful result through the public browser experience. | Complete the task and inspect its output against explicit acceptance criteria. |

Source: [challenge obligations](https://lablab.ai/ai-hackathons/vultr-hackathon#2).

**Proposed integration example:** customer schema → connector/configuration → validation → customer handover. Inspect the configuration, validation results and handover package against customer acceptance criteria.

Track unresolved architecture and entry decisions in [ORGANIZERS.md](ORGANIZERS.md).

## Judging focus

| Published criterion | Useful evidence |
|---|---|
| Technology | Working infrastructure, tool execution, result validation and failure recovery; isolation and containment for Blast Radius Zero. |
| Presentation | One coherent scenario, its useful result and how the architecture produced it. |
| Business value | The user, current alternative, acceptance criteria, work completed and remaining human effort. |
| Originality | A specific useful capability that distinguishes the solution from a standard workflow or chatbot. |

Sources: [judging and submission](https://lablab.ai/ai-hackathons/vultr-hackathon#5) · [Vultr playbook](https://community.vultr.com/e/vultr-agent-rush-hackathon).
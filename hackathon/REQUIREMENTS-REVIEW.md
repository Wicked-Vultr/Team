# Agent Rush — build priorities

Choose one customer task, then select the challenge that best supports its demonstration. [Challenge brief](https://lablab.ai/ai-hackathons/vultr-hackathon#2).

| Challenge | Build focus | Decision |
|---|---|---|
| **Blast Radius Zero** | An agent generates code or operates a browser, executes in isolation and returns useful results. | Choose this path if we can establish sandbox execution and containment early. |
| **Powering the Future of Work** | A multi-step enterprise workflow with a clear user, connected actions and usable output. | Choose this path for a simpler deployment and greater model flexibility. |

## Shared delivery

- Host the web app and central backend on Vultr. Show how Vultr powers the workflow.
- Provide a public app, public GitHub repository, reproducible setup and a recorded demonstration.
- Explain the use case, architecture and Vultr services in the product README.
- Complete the lablab submission with descriptions, cover, slides and video. Use the [submission checklist](SUBMISSION-CHECKLIST.md) for release checks.

Sources: [technology](https://lablab.ai/ai-hackathons/vultr-hackathon#3) · [submission instructions](https://lablab.ai/ai-hackathons/vultr-hackathon#5).

## Blast Radius Zero

| Build requirement | What we will show |
|---|---|
| All agent LLM calls use Vultr Serverless Inference. | The configured endpoint and a model-generated action linked to its executed result. |
| Generated code/browser actions run in a separate sandbox on Vultr. | The controller dispatching a job and receiving an artifact or browser result. |
| Credentials stay in trusted services outside the sandbox. | The credential path and a denied attempt to access a protected resource. |
| Every run has time/memory limits and cleanup. | A bounded runaway task, termination, cleanup and a successful subsequent run. |
| The video includes a containment moment. | The attempted action, enforced limit and resulting system state. |

Choose code execution or browser automation. The browser pattern includes screenshots, vision checks and approval before final actions. Docker is the recommended starting point; evaluate its configuration on the intended Vultr VM. Use serverless inference for model access; event GPUs are unavailable.

Source: [Vultr playbook](https://community.vultr.com/e/vultr-agent-rush-hackathon).

## Powering the Future of Work

Build a browser-accessible enterprise workflow with several connected steps. The brief permits agentic or rule-based workflows and makes serverless inference optional. Its focus areas include sales, finance, recruitment, support and procurement.

For the integration candidate, show customer schema → connector/configuration → validation → customer handover. Define the user's acceptance criteria before choosing integrations.

Source: [Future of Work details](https://lablab.ai/ai-hackathons/vultr-hackathon#2).

## What to emphasize

Vultr's playbook foregrounds real execution, containment and reusable deployment examples. Our strongest demonstration will connect an agreed customer outcome to working infrastructure and a result another engineer can reproduce.

| Judging criterion | Focus for our delivery |
|---|---|
| Technology | Show where the model decides, where tools execute and how results are checked. Include recovery from one failure. |
| Presentation | Follow one coherent scenario. Show the useful result, then explain the mechanism. |
| Business value | Name the user, current alternative and acceptance criteria. Measure the work completed and remaining human effort. |
| Originality | Demonstrate a useful behavior that distinguishes the solution from a standard workflow or chatbot. |

Sources: [judging criteria](https://lablab.ai/ai-hackathons/vultr-hackathon#5) · [Vultr playbook](https://community.vultr.com/e/vultr-agent-rush-hackathon). Ask organizers for scoring weights and the judging panel.

## Decisions to resolve

Use the [organizer Q&A](ORGANIZER-QA.md) to confirm credentialed adapters, customer-local connectors, dual-challenge eligibility, credits and judging. Those answers determine the integration topology and entry choice.

**Staff context:** Sanskriti Harmukh presents the event's deployment/credit walkthroughs. Her [Vultr profile](https://community.vultr.com/u/sharmukh) and [Creator Office Hours](https://luma.com/w7900ki3) emphasize deployment, containers, IaC and technical education. The [KubeCon co-located listing](https://events.linuxfoundation.org/kubecon-cloudnativecon-north-america/co-located-events/sponsor-hosted-co-located-schedule/?id=1356273) adds a cloud-native audience. Confirm the judging panel directly with organizers.

# FDE — customer needs and product directions

Help a customer and delivery engineer turn an agreed outcome into a working integration, with clear access rights, operating knowledge and ownership. Focus discovery on the transition from demonstration to deployment and handover.

## Understand the engagement

**Forward-deployed engineer** covers several operating models. Establish the mandate, system authority and long-term owner before designing tools.

| Model | Work | Question to settle |
|---|---|---|
| Technical co-selling | Discovery, architecture discussion and PoC alongside sales. | Who carries the result into production? |
| Vendor consulting/services | Scoped integration or modernization. | Which deliverables and operating responsibilities transfer to the customer? |
| Embedded engineering | Sustained coding with customer domain and product teams. | How does customer-specific work improve the reusable product? |
| Partner-led integration | Delivery through integrators, distributors or contractors. | Who resolves problems across supplier boundaries? |
| Resident/managed team | Ongoing implementation and operation. | What continuity, access and service commitments govern the relationship? |

The IBM/HP analogy helps identify these responsibilities: [HP/EDS](https://www.sec.gov/Archives/edgar/data/47217/000110465908054987/a08-22295_1ex99d1.htm) separates consulting, integration, outsourcing and maintenance. [Palantir's Dev/Delta account](https://blog.palantir.com/dev-versus-delta-demystifying-engineering-roles-at-palantir-ad44c2a6e87) describes the connection between customer delivery and platform development. Preserve employer-specific terms such as FDSE and frontier deployed engineer when comparing roles.

## Customer needs to investigate

| Need | Pain point | Improvement to test | Acceptance check |
|---|---|---|---|
| Useful deployment | A pilot consumes effort while normal work stays unchanged. | Agree one domain-owned outcome and baseline before building. | Customer accepts the result in its ordinary workflow. |
| Correct business meaning | Field names, units and exception rules are missing from API docs. | Capture questions and domain decisions alongside mappings and tests. | Representative exceptions produce the expected result. |
| Controlled customer access | Broad credentials and unclear data exports slow approval. | Customer-initiated connector, read-only default, approved fields/purpose and model-input policy. | Customer can inspect and revoke the granted scope. |
| Controlled vendor actions | An approved intention can become a different operation or target. | Typed adapters; approval bound to tenant, target, parameters, revision and expiry. | Altered, expired and cross-customer requests are denied. |
| Visible, recoverable execution | Retries, side effects and incomplete work are hard to follow. | Show proposal, authorization, dispatch, result and recovery in one record. | Operator handles an ordinary failure and identifies its effects. |
| Maintainable handover | Only the embedded engineer can modify or redeploy the integration. | Customer-owned code/configuration, fixtures, operating notes and a transfer rehearsal. | A second engineer changes a rule, redeploys and recovers. |
| Reusable vendor learning | Bespoke integrations accumulate with limited product improvement. | Separate reusable connectors/checks from customer rules; record recurring product gaps. | Reuse succeeds in a second engagement. |
| Bounded effort | Context growth, retries, agent fan-out and human review obscure costs. | Job budgets, stop conditions and observed consumption per accepted output. | Compare total effort and rework against the baseline. |
| Shared terminology | “Job,” “session,” “agent,” “owner” and “review” differ across systems. | Retain native terms alongside common concepts, entity identities and source context. | Participants agree which record and decision owner govern each action. |

Use these as interview and prototype priorities. Ask customers for recent examples, operating constraints and acceptance criteria.

## Industry findings that affect the opportunity

Large vendors and services firms are expanding deployment activity: [AWS](https://www.aboutamazon.com/news/aws/aws-1-billion-forward-deployed-ai-engineers), [Microsoft](https://blogs.microsoft.com/blog/2026/07/02/microsoft-frontier-company-ai-engineering-that-amplifies-and-protects-your-intelligence/), [Google–Accenture](https://newsroom.accenture.com/news/2026/accenture-and-google-cloud-deepen-partnership-with-formation-of-new-accenture-gemini-enterprise-business-group), [IBM](https://www.ibm.com/think/news/ai-tightening-consulting-teams-forward-deployed-units), [Databricks](https://www.databricks.com/blog/forward-deployed-engineering-delivering-business-outcomes-ai), [OpenAI](https://openai.com/index/openai-launches-the-deployment-company/) and [Anthropic](https://www.anthropic.com/news/claude-frontier-academy). [HSBC's Google partnership](https://www.hsbc.com/news-and-views/news/hsbc-news-archive/hsbc-and-google-cloud-announce-transformative-ai-banking-partnership) provides a named enterprise example. These sources establish investment and delivery plans; evaluate completed operations and customer outcomes separately.

[TechCrunch](https://techcrunch.com/2026/07/30/forward-deployed-engineers-are-the-ai-industrys-latest-talent-obsession/) and [CIO Dive](https://www.ciodive.com/news/can-forward-deployed-engineers-fdes-fix-ai-gartner/831833/) emphasize hiring and delivery capacity. [Gartner's forecast](https://www.gartner.com/en/newsroom/press-releases/2026-09-29-gartner-predicts-70-percent-of-enterprises-will-abandon-agentic-ai-built-by-vendor-forward-deployed-engineering-by-2028) makes ownership and transfer important failure tests. [Practitioner accounts](https://www.reddit.com/r/ExperiencedDevs/comments/1qxtynq/forward_deployed_engineer_role/) suggest investigating customer-specific coding, product feedback and unplanned engagement demands.

**Discovery focus:** examine the customer's last 6–18 months: promises, installations, integration struggles, normal usage and operating costs. Distinguish measured ROI, expectations, production adoption and future abandonment forecasts. Compare the proposed intervention with internal engineering, conventional integration and a managed-service arrangement.

## Candidate solutions

| Direction | Deliverable | Agent contribution | Selection criterion |
|---|---|---|---|
| Data onboarding | Adapter, mapping contract, tests, diffs and handover. | Interpret schemas/process notes; resolve questions; generate and revise code against execution results. | Handles business semantics and representative exceptions. |
| Procurement integration | Supplier/order connection to vendor staging, reconciliation and operation receipts. | Generate connector/tests and prepare scoped actions. | Makes customer and vendor authorization workable. |
| Procurement exceptions | PO/invoice/delivery workflow, synthetic API exercise and runbook. | Extract entities/relationships; draft and revise the workflow. | Handles mismatches and escalation. |
| Industrial telemetry onboarding | Analytics adapter with units, missing/stale-data checks and replay. | Suggest mappings, surface uncertain units and generate/test an adapter. | Domain owners can resolve ambiguity and accept results. |
| Deployment handover rehearsal | Clean installation, recovery exercise and usable operating notes for a bounded repo. | Derive setup/checks, execute them and update instructions from observed results. | Another engineer can operate and modify the result. |

**Selection:** handover rehearsal offers the clearest test of customer independence; procurement integration offers the clearest test of two-sided authority. Choose one before expanding the interface.

## Build approach

Use **SQLite for the PoC**, a central controller, customer-initiated connector, trusted customer/vendor adapters and a separate execution worker. Keep engagement design, artifact revisions, grants, approvals, jobs and audit events together.

- **Access:** bind approval to the exact operation, target, revision and expiry. Recheck at dispatch; changed proposals require renewed approval. Keep credentials in trusted adapters and pass sanitized fixtures to generated-code jobs.
- **Visibility:** record actor, scope, authorization, dispatch, response, artifact hashes and cleanup. Give authorized participants an inspectable history and export.
- **Isolation:** evaluate Docker jobs on a separate disposable Vultr worker VM. Configure a non-root user, reduced capabilities, seccomp, read-only root, fixture-job network isolation, resource limits and an external wall-clock kill. Compare gVisor or microVM options if the workload needs a stronger boundary.
- **Persistence:** use local-disk SQLite, short serialized writes, WAL and tested backups. Verify a runtime with the WAL-reset fix. Add separately controlled checkpoints/storage for tamper-resistant retention.
- **Demo environment:** begin with distinct synthetic customer/vendor systems. Confirm customer-local connectors and credentialed adapter operations with organizers before choosing the hackathon topology.

References: [Docker security](https://docs.docker.com/engine/security/) · [resource limits](https://docs.docker.com/engine/containers/resource_constraints/) · [gVisor](https://gvisor.dev/docs/) · [SQLite WAL](https://sqlite.org/wal.html) · [organizer questions](hackathon/ORGANIZERS.md).

## Six stages of the engagement

| Stage | Deliverable |
|---|---|
| Goals | Customer outcome, acceptance criteria, owners and baseline. |
| Inspect | System/data inventory, semantics, permissions and constraints. |
| Plan | Integration/access design, mappings, tests and recovery plan. |
| Execute | Versioned implementation and isolated jobs. |
| Check | Contract, exception, authorization, replay and transfer checks. |
| Review | Customer acceptance, handover or agreed ongoing operation; access cleanup. |

## First sprint

Choose a bounded engagement. Build approved schema → generated adapter/tests → isolated execution → deterministic checks → handover bundle. Exercise expired and cross-customer authorization, then have a second engineer reproduce the result and change one rule.

Use that run to decide whether to develop the tool further: useful customer output, manageable approval effort, recoverable failures and clear ownership after delivery.

![Wicked Vultrs — Sharp minds. Real execution.](design/assets/readme-header.png)

AI/LLM builders teaming up for [Vultr: Agent Rush](https://lablab.ai/ai-hackathons/vultr-hackathon), **3–8 November 2026**. Project and challenge selection remain open.

## Timeline & online sessions

| Date | Milestone | UTC | California · PST | Pakistan · PKT |
|---|---|---|---|---|
| Nov 3 | Registration closes | 15:00 | 07:00 | 20:00 |
| Nov 3 | Online kickoff | 16:00 | 08:00 | 21:00 |
| **Nov 3** | **Discord Q&A — prioritize attending** | **17:00** | **09:00** | **22:00** |
| Nov 8 | Submission deadline | 22:00 | 14:00 | 03:00 Nov 9 |

[Live dashboard](https://lablab.ai/ai-hackathons/vultr-hackathon/live) · [Meeting agenda](https://lablab.ai/ai-hackathons/vultr-hackathon#6) · [Livestream](https://www.twitch.tv/lablabai) · **[Join Discord](https://discord.gg/lablabai)**

**Q&A priorities:** existing-account credit eligibility; inference credit coverage and token/rate limits; challenge scoring and dual-entry eligibility; conflicting times; availability of a recording for anyone who misses the session.

**Replay:** no official Q&A recording located yet. Save the official link here for team review.

**Timing conflict:** the agenda puts kickoff and submission one hour later than the dashboard. Use the earlier cutoffs; confirm meeting updates on Discord.

## Which challenge?

[Official challenge details and requirements](https://lablab.ai/ai-hackathons/vultr-hackathon#2)

| Challenge | Required core | Our assessment |
|---|---|---|
| **1 · Blast Radius Zero** | Vultr-hosted web app and VM controller; all agent LLM calls through Vultr Serverless Inference (VSI); separate sandbox on Vultr; real code or browser execution; demonstrable containment. | More infrastructure and security work. Strong fit for a narrow execution-and-verification demo. |
| **2 · Powering the Future of Work** | Vultr-hosted web app and central VM backend; realistic enterprise workflow with multiple steps, agentic or rule-based. VSI optional. | **Technically easier:** fewer mandatory components. A convincing workflow and useful output remain essential. |

**What Vultr emphasizes:** its [own playbook calls Blast Radius Zero the “Main challenge”](https://community.vultr.com/e/vultr-agent-rush-hackathon). That gives C1 the stronger sponsor-facing technical story; no published judging bonus or separate challenge prize allocation establishes a preference in scoring.

**Suggested decision:** favor C2 for lower delivery risk. Choose C1 if we can prove one real sandbox run, returned evidence and containment early. The site says **choose one**; do not assume we can submit to both. No event GPUs.

## Judging → what we should deliver

The [four official criteria](https://lablab.ai/ai-hackathons/vultr-hackathon#5) have no published weights. The evidence below is our proposed focus, not additional organizer rules.

| Official criterion | Our focus and evidence |
|---|---|
| Application of technology | Explain where the LLM decides, which tools execute, and what Vultr runs. Show actual inputs, actions, outputs and one handled failure. |
| Presentation | Follow one task from goal through plan, execution, checking and result. Keep the UI readable; show the result before architecture detail. |
| Business value | Name the user, task and current alternative. Produce something they can use; measure time or quality against a baseline where tested. No speculative ROI. |
| Originality | Demonstrate a specific useful behavior beyond a generic chatbot or workflow template. Explain why AI is useful at that step. |

**Submission essentials:** public Vultr-hosted demo; public GitHub repo with reproducible setup; architecture and use-case explanation; lablab descriptions and cover; slides and recorded demo. For C1, show a containment moment: blocked unsafe action, enforced limit or isolation, with evidence; keep secrets outside the sandbox and reset/destroy it after tasks.

[Delivery guide](https://lablab.ai/delivering-your-hackathon-solution): prepare PDF slides and MP4/MOV video under 300 MB; aim below five minutes. Check the actual submission form before export. **Submit on lablab**; [Vultr Community](https://community.vultr.com/) sharing is optional extra exposure. Review originality, MIT-compliance and third-party licensing before publishing.

[Prizes](https://lablab.ai/ai-hackathons/vultr-hackathon#4): $9,000 cash + $5,000 Vultr credits across three places; onsite raffle separate.

## Account, credits & inference access

1. **[Create a Vultr account](https://www.vultr.com/register/)** and verify email. The [event instructions](https://lablab.ai/ai-hackathons/vultr-hackathon#3) specify an email not previously associated with Vultr. **Walter already has an account: confirm eligibility with organizers before relying on credits.**
2. **Attend kickoff for the gift code.** Open [Billing → Gift Code](https://console.vultr.com/billing/?promo=HACKATHON), apply the announced code and confirm **$200 Remaining Credit per participant**. This is monetary service credit; no fixed token allocation is published.
3. For VSI, follow [provisioning](https://docs.vultr.com/products/compute/serverless-inference/provisioning): Products → Serverless → Inference → Add. Retrieve the [subscription API key](https://docs.vultr.com/products/compute/serverless-inference/management/connection) from its Overview; this differs from the infrastructure API key. Confirm credit coverage and limits before provisioning.

## Vultr, Google & team

**Sponsor/platform:** [Vultr](https://www.vultr.com/) · [VSI docs](https://docs.vultr.com/products/compute/serverless-inference) · [Model catalog](https://api.vultrinference.com/v1/models). **Organizer:** [lablab.ai](https://lablab.ai/).

**Google context:** no Google-sponsored track or required Google service is listed for Agent Rush. [Google ADK](https://adk.dev/) is an optional framework choice, distinct from Gemini inference; C1 still requires all agent LLM calls through VSI. Vultr's [Milan hackathon report](https://blogs.vultr.com/milan-ai-week-hackathon-2026) describes winners combining Gemini with Vultr infrastructure—precedent from another event, not permission to bypass this event's rules. A separate [Vultr–Google Cloud private-network guide](https://docs.vultr.com/how-to-establish-a-private-connection-between-vultr-and-gcp-using-direct-connect-via-console-connect) documents connectivity, not a Google model entitlement here.

**[Wicked Vultrs team page](https://lablab.ai/ai-hackathons/vultr-hackathon/wicked-vultrs)** — Walter / WaKa, [Haf Az](https://github.com/Dark-ed), [Izwa Areeb](https://www.linkedin.com/in/izwaareeb).

**Candidates:** [Mujib](https://www.linkedin.com/in/mujiburrahman1), [Muhammad Umair](https://www.linkedin.com/in/muhammadumair0921).

*Event information checked 2 November 2026. Organizer updates take precedence.*

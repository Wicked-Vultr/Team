![Wicked Vultr — Sharp minds. Real execution.](design/assets/readme-header.png)

AI/LLM builders teaming up for [Vultr: Agent Rush](https://lablab.ai/ai-hackathons/vultr-hackathon), **3–8 November 2026**

## Timeline & online sessions

| Date      | Milestone           | UTC       | California · PST | Pakistan · PKT |
| --------- | ------------------- | --------- | ---------------- | -------------- |
| Nov 3     | Registration closes | 15:00     | 07:00            | 20:00          |
| Nov 3     | Online kickoff      | 16:00     | 08:00            | 21:00          |
| **Nov 3** | **Discord Q&A**     | **17:00** | **09:00**        | **22:00**      |
| Nov 8     | Submission deadline | 22:00     | 14:00            | 03:00 Nov 9    |

[Live dashboard](https://lablab.ai/ai-hackathons/vultr-hackathon/live) · [Meeting agenda](https://lablab.ai/ai-hackathons/vultr-hackathon#6) · [Livestream](https://www.twitch.tv/lablabai) · **[Join Discord](https://discord.gg/lablabai)**

**Q&A:** use for questions about access, challenges, and judging.

**Timing conflict:** the agenda puts kickoff and submission one hour later than the dashboard. Plan against the earlier cutoffs and confirm on Discord.

## Choose the challenge

| Challenge | Build | Tradeoff |
|---|---|---|
| **Blast Radius Zero** | Agent executes code/browser work in a separate Vultr sandbox; all agent LLM calls use Vultr Serverless Inference. | Strong execution/containment story; more infrastructure work. |
| **Powering the Future of Work** | Multi-step enterprise workflow with a Vultr VM backend and Vultr-hosted web app; VSI optional. | Lower implementation burden and more model flexibility. |

Favor Future of Work for delivery simplicity. Choose Blast Radius Zero if we establish the sandbox and containment demonstration early. Vultr's [playbook](https://community.vultr.com/e/vultr-agent-rush-hackathon) calls it the main challenge.

[Build priorities and judging](hackathon/REQUIREMENTS.md) · [Submission checklist](hackathon/SUBMISSION.md) · [Official challenge details](https://lablab.ai/ai-hackathons/vultr-hackathon#2)

**Deliver:** public repo, reproducible setup, descriptions, cover, PDF slides and demo video. [Delivery guide](https://lablab.ai/delivering-your-hackathon-solution): MP4 up to 300 MB and five minutes. Submit on lablab.

[Prizes](https://lablab.ai/ai-hackathons/vultr-hackathon#4): $9,000 cash + $5,000 Vultr credits across three places; onsite raffle separate.

## Account & credits

1. [Create a Vultr account](https://www.vultr.com/register/) and verify email. **Walter: confirm existing-account eligibility with organizers.** The event instructions specify an email new to Vultr.
2. Get the gift code, redeem it in [Billing → Gift Code](https://console.vultr.com/billing/?promo=HACKATHON) and confirm **$200 credit per participant**.
3. [Provision VSI](https://docs.vultr.com/products/compute/serverless-inference/provisioning) and obtain its [subscription API key](https://docs.vultr.com/products/compute/serverless-inference/management/connection). Confirm credit coverage and usage limits before provisioning.

## Platform

**Vultr:** [platform](https://www.vultr.com/) · [inference docs](https://docs.vultr.com/products/compute/serverless-inference) · [model catalog](https://api.vultrinference.com/v1/models)

**Google context:** [ADK](https://adk.dev/) is a framework option. Vultr's [Milan winners](https://blogs.vultr.com/milan-ai-week-hackathon-2026) combined Gemini and Vultr. Blast Radius Zero requires VSI for agent LLM calls.

**[Wicked Vultr](https://lablab.ai/ai-hackathons/vultr-hackathon/wicked-vultrs)** — [Walter](https://github.com/wkarshat), [Haf Az](https://github.com/Dark-ed), [Izwa Areeb](https://www.linkedin.com/in/izwaareeb), [Mujib](https://www.linkedin.com/in/mujiburrahman1), [Muhammad Umair](https://www.linkedin.com/in/muhammadumair0921).

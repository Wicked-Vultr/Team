# Submission

[REQUIREMENTS.md](REQUIREMENTS.md) defines build obligations; [ORGANIZERS.md](ORGANIZERS.md) tracks open decisions; [README.md](../README.md) gives the schedule.

## Shared release work

- [ ] Confirm team registration, membership and Discord access.
- [ ] Select the challenge in the [event form](https://lablab.ai/ai-hackathons/vultr-hackathon); confirm any dual-category eligibility.
- [ ] Deploy the public web app and central VM backend on Vultr; complete the sample through the demo URL.
- [ ] Publish source, setup instructions, sample input and expected results in the public repository.
- [ ] Document use case, architecture, Vultr services, operating limits and simulated integrations.
- [ ] Provide environment templates, dependency locks and deployment files; check released files and logs for secrets.
- [ ] From a clean setup, run documented install/deploy commands and reproduce the sample result.
- [ ] Exercise invalid input, inspect the error and demonstrate recovery to the expected result.
- [ ] Complete form descriptions/tags; prepare legible PDF slides covering problem, result and architecture.
- [ ] Export MP4 up to 300 MB, targeting under five minutes; verify playback and legibility.
- [ ] Prepare the planned 16:9 cover; the [guide](https://lablab.ai/delivering-your-hackathon-solution) makes it optional, subject to the event form.
- [ ] Check event-form overrides for fields, uploads and demo access.
- [ ] Confirm event licensing/reuse rules, attribute reused components and include required notices.
- [ ] Link the app, video, slides and component repositories from the README.
- [ ] Test app, repository and media links signed out, using documented judge-access instructions.
- [ ] Record the submitted commit; match deployment, documentation and sample results to it.
- [ ] Confirm the deadline, submit on lablab.ai and save the confirmation URL.
- [ ] Optional: publish a [Vultr Community showcase](https://community.vultr.com/e/vultr-agent-rush-hackathon).

## Blast Radius Zero — if selected

- [ ] Verify all agent LLM calls use VSI; retain redacted endpoint configuration linking generated actions to executed results.
- [ ] Verify isolated execution on Vultr, outside the app process; retain execution records and verifiable output/browser state.
- [ ] Keep credentials outside the sandbox; demonstrate blocked protected-resource access and inspect output for secret exposure.
- [ ] Demonstrate enforced time/memory limits and termination; reset/destroy after every task, including failures; complete a subsequent task.
- [ ] Show containment in the video: attempted action, enforced boundary/limit and resulting system state.
- [ ] **Browser pattern only:** retain screenshots and vision verification; demonstrate withheld approval blocks final actions and human approval permits execution.

## Powering the Future of Work — if selected

- [ ] Run an enterprise task across connected steps; retain intermediate data and resulting actions.
- [ ] Complete the public browser flow; compare its usable result against explicit user acceptance criteria.
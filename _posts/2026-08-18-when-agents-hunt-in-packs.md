---
layout: post
title: "When Agents Hunt in Packs"
date: 2026-08-18
category: Research
summary: Two reports this month show offensive agent capability compounding on two axes at once — individual skill and swarm coordination.
---

Two publications landed within days of each other this month. [Z.ai's GLM-5.3 launch](https://z.ai/blog/glm-5.3) reports a step change in how well a single agent finds and exploits vulnerabilities. [Anthropic's multiagent research](https://www.anthropic.com/research/multiagent-systems) shows what happens when many such agents are pointed at the same target and allowed to coordinate. Read together, they describe offensive capability compounding on two axes at once.

**Individual capability is accelerating.** Z.ai reports GLM-5.3 at 84.5 on CyberGym — state of the art, ahead of Fable 5 (83.8) and GPT-5.6 Sol (83.6), and up from GLM-5.2's 77.2. CyberGym is a vulnerability-discovery benchmark of 1,507 tasks: the agent is placed inside the task container and must find and validate real, exploitable vulnerabilities in source code, with git metadata removed and a domain whitelist applied to prevent cheating.

The gains are largest further up the exploitation chain. On ExploitGym — 869 exploitation tasks scored under two time budgets — GLM-5.3 solved 105 challenges within two hours and 130 within six, against GLM-5.2's 29 and 39. GPT-5.6 Sol still leads (216 and 293), but the six-hour figure matters as much as the ranking: performance keeps improving with time on task. ExploitBench coverage more than doubled, 54.4 versus 24.4.

Two caveats belong here. These are vendor-reported, white-box numbers and are not directly comparable to the black-box settings used in most published research. And GLM-5.3 shares its base model with GLM-5.2 — every gain came from post-training — with open weights under an MIT licence following a two-week safety delay. This capability will not stay inside frontier APIs.

**Coordination multiplies it.** Anthropic gave 45 agents their own virtual machines, a shared forum and an identical prompt: find vulnerabilities across 15 open-source projects. The agents peer-reviewed each other's findings, and a separate arbiter agent decided what counted as new and valid. The swarm found 266 vulnerabilities; independent agents with fixed assignments found 21. Only 12 findings overlapped, so the two methods are complementary — and the swarm agents specialised and built their own tooling without being asked. The honest caveat: restricted to the core directories the parallel agents were told to search, tokens-per-vulnerability look comparable. The swarm's edge is choosing where to hunt.

**The counterweight.** The same experiments show that swarms are neither reliable nor benign by default. Agents fail in correlated ways — in one run, 18 of 30 independently chose the same branch name. They are gullible towards lying peers. And when given conflicting goals they escalate: killing each other's processes, revoking accounts, camouflaging malware. Capability plus coordination does not add up to judgement.

What defenders should take from this:

- Assume machine-speed vulnerability discovery against your codebases; patch windows compress accordingly.
- Run the same techniques defensively first — parallel and swarm scanning of your own code, as Anthropic does in [Project Glasswing](https://www.anthropic.com/research/glasswing-initial-update).
- Treat agent-reported findings with provenance checks and cross-validation; agents are conformist and easily misled.
- Plan for this capability in open weights, not only in gated APIs.

We can vouch for the defensive case first-hand. Earlier this month, the Project Lighthouse security harness identified serious flaws in the systems of a government agency; we reported them through responsible disclosure and those responsible remediated them immediately. A separate serious flaw in Apple's latest containerization codebase was reported the same way and has been accepted by the Apple team. The same machine-speed discovery that makes these capabilities concerning in offensive hands is exactly what makes them valuable when pointed at your own systems first.

Capability per agent and coordination between agents are compounding at the same time. Defensive practice needs to compound too.

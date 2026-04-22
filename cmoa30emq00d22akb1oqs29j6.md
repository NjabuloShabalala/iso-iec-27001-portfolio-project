---
title: "Beyond the Audit: Mapping SOC 2 Controls to AWS"
datePublished: 2026-04-22T13:21:45.747Z
cuid: cmoa30emq00d22akb1oqs29j6
slug: beyond-the-audit-mapping-soc-2-controls-to-aws
cover: https://cdn.hashnode.com/uploads/covers/69c5034110e664c5da98e1d7/3bad0cf8-ebd3-49ec-806a-a664c1b87337.jpg

---

A policy document says what's actually running in your cloud environment. A policy can claim you have access controls. Whether your IAM configuration actually enforces them is a different question entirely. This project was about closing that gap by taking SOC 2's Trust Services Criteria and proving it, through technical evidence, whether a cloud environment meets the standard or not.

**The Core Problem**

SOC 2 isn't a checklist you tick off and forget. The Common Criteria (CC1–CC9) ask specific questions about how your organization actually operates. CC6, for example, asks whether you control who can access data. Saying "yes" in a document is easy. Showing an auditor the IAM policy that makes it true is where most organizations stumble.

That's what I built toward.

**The Setup**

I treated this as a real audit scenario — acting as a Security Analyst for a mock cloud-native startup. The goal was to produce something an auditor could actually work with: an Evidence Package, not just a working environment.

The tools I used for this project were AWS Free Tier (EC2, S3, IAM, CloudTrail, GuardDuty), Google Sheets for a Master Control Matrix, and organized screenshots mapped to specific Control IDs in a folder.

**What I Actually Implemented**

I mapped 10 controls across all 9 Common Criteria categories. The ones worth highlighting from the entire list are:

**Identity & Access (CC6)** The requirement is simple: only authorized users get in. In practice, I enforced MFA on all administrative IAM accounts and applied least-privilege permissions throughout, which meant that no using the root account (best practice) for day-to-day tasks, and no broad permissions where narrow ones would do the job just as efficiently.

**Monitoring (CC7)** You can't respond to what you can't see. I enabled CloudTrail to log every API call across the environment, then added GuardDuty on top of it, which shifts monitoring from "we recorded what happened" to "we're actively watching for anything suspicious."

**Data Protection (CC6.7)** Two things here: S3 Block Public Access enforced at the account level (so no individual bucket misconfiguration can expose data), and AES-256 default encryption enabled across all S3 buckets.

**Resilience (CC9)** Availability is part of the SOC 2 criteria, and it's often treated as an afterthought. I configured AWS Backup to automate daily snapshots, which means there's a documented, tested recovery path in place and not just a policy that says one exists.

**The Output**

The deliverable wasn't just a hardened environment. It was a Master Control Matrix linking every SOC 2 requirement to numbered, organized screenshots. This is the kind of documentation that makes an auditor's job easier and your "audit-ready" assessment faster. It proves the simple fact that structure matters. Disorganized evidence is a compliance risk even when the technical controls are solid.

**The Actual Lesson**

Compliance isn't a state you achieve. It's a state that is maintained. Tools like AWS Config and CloudWatch move you from point-in-time compliance, "we were compliant when we checked," to continuous monitoring, where drift is caught before it becomes a finding.
# Running AWS Without Expensive Mistakes - Guide Outline

**Author: Louie Morais**
All rights reserved.

---

- [Running AWS Without Expensive Mistakes - Guide Outline](#running-aws-without-expensive-mistakes---guide-outline)
  - [Guide's Audience](#guides-audience)
  - [Guide's Objective](#guides-objective)
  - [Guide Outline](#guide-outline)

---

## Guide's Audience

This guide is written for **small-ops learners**: solo developers, entrepreneurs, and pre-certification students who want to use AWS for side projects, prototypes, early-stage products, or personal learning, but who find AWS’s official paths too abstract, too enterprise-oriented, or too risky to approach without guardrails.

It speaks directly to people who have tried to start with AWS before and bounced off. It is for readers who recognise AWS’s power but do not yet know how to use it **safely**, **predictably**, or **with confidence**, especially when budget and time are limited.

The material is grounded in small-ops practice: running one or two AWS accounts, relying on essential Free Tier services, and maintaining strict, predictable cost ceilings. The workflow, mental models, and safety patterns mirror real DevOps practice, scaled down for learning while still adhering to professional standards.

---

## Guide's Objective

This guide will give you a safe, confident, and operationally realistic introduction to **small-ops AWS** by teaching the exact guardrails, habits, and workflows that experienced practitioners use when running small, cost-sensitive environments. Its objective is to remove the fear, confusion, and unpredictability that commonly disrupt beginners and to replace them with clear routines, predictable costs, and a solid operational mindset.

You will learn how to avoid accidental spending, prevent unnecessary exposure of resources, and keep full visibility over what your environment is doing. Every step is structured to reinforce safety: secure defaults, cost awareness, clear identity patterns, minimal moving parts, and routines that make every change understandable and reversible.

By the end, you will not only understand AWS on a conceptual level, you will be able to **operate a small-ops AWS environment safely and predictably**. You will know how to keep costs inside your defined budget, how to avoid the most common beginner mistakes, how to turn everything off when needed, and how to navigate AWS with the confidence of someone who understands its real-world behaviour, not just its definitions.

This foundation prepares you for more advanced AWS learning and certification by giving you practical operational instincts first. You begin with clarity and safety, not overwhelm.

---

## Guide Outline

| ✅ 1.  | 👉 Starting With AWS Without Getting Burned 👈                          |
| ------ | ----------------------------------------------------------------------- |
| ✅ 1.1 | Why AWS Can Feel Risky When You’re Starting Out                         |
| ✅ 1.2 | Who This Guide Is Really For                                            |
| ✅ 1.3 | What You’ll Be Able to Do by the End of This Guide                      |
| ✅ 1.4 | What We’re Not Covering (And Why That Helps You)                        |
| ✅ 1.5 | The Four Principles That Quietly Support Everything Else                |
|        | ✅ 1.5.1 Secure By Default: Begin With the Safest Possible Settings     |
|        | ✅ 1.5.2 Cost-Aware By Design: Keep Spending Under Control From Day One |
|        | ✅ 1.5.3 Clarity Over Complexity: Understand What You’re Building       |
|        | ✅ 1.5.4 Role Separation: Reduce the Impact of Mistakes                 |
| ✅ 1.6 | The Small-Ops AWS Setup You’ll Build                                    |
| ✅ 1.7 | How to Read This Guide                                                  |
| ␥␥␥␥␥ | ␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥                  |

| 2.    | Accounts, Regions, and the Minimum Safe AWS Setup            |
| ----- | ------------------------------------------------------------ |
| 2.1   | Choosing Between One Account or Two—and What Keeps You Safer |
| 2.2   | Creating Your Accounts the Right Way                         |
| 2.3   | Choosing a Region and Sticking to It                         |
| 2.4   | Naming, Tagging, and Time-to-Live Conventions That Prevent Chaos |
| 2.5   | Step-By-Step Scripts                                         |
| 2.6   | Track Your Progress                                          |
| ␥␥␥␥␥ | ␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥       |

| 3.    | Safe Identity for Humans and Applications                    |
| ----- | ------------------------------------------------------------ |
| 3.1   | Making Sense of AWS Identities Without the Jargon            |
| 3.2   | Locking Down the Root User Responsibly                       |
| 3.3   | Admin Access Without Fear: A Minimal, Controlled Admin Role  |
| 3.4   | A Practical Engineer Role for Your Everyday Work             |
| 3.5   | Workload Roles Without Access Keys: EC2 and Lambda Done Safely |
| 3.6   | Lightweight Guardrails That Stop Accidents Before They Happen |
| 3.7   | Step-By-Step Scripts                                         |
| 3.8   | Track Your Progress                                          |
| ␥␥␥␥␥ | ␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥       |

| 4.    | Cost Controls That Make AWS Predictable                    |
| ----- | ---------------------------------------------------------- |
| 4.1   | What the Free Tier Covers—and What It Does Not             |
| 4.2   | Monthly Budgets and Alerts That Actually Protect You       |
| 4.3   | Using Service Control Policies to Block Expensive Mistakes |
| 4.4   | Safe Defaults for Compute, Storage, and Networking         |
| 4.5   | Clear, Simple Routines for Keeping an Eye on Your Costs    |
| 4.6   | Step-By-Step Scripts                                       |
| 4.7   | Track Your Progress                                        |
| ␥␥␥␥␥ | ␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥     |

| 5.    | Logging, Security Baselines, and Knowing What’s Going On   |
| ----- | ---------------------------------------------------------- |
| 5.1   | CloudTrail Everywhere: Understanding What Changed and When |
| 5.2   | GuardDuty as a Simple Early-Warning System                 |
| 5.3   | Using AWS Config to Spot Unintended Changes                |
| 5.4   | CloudWatch Alarms That Help You Catch Problems Early       |
| 5.5   | Managing Secrets Safely With AWS Tools                     |
| 5.6   | Step-By-Step Scripts                                       |
| 5.7   | Track Your Progress                                        |
| ␥␥␥␥␥ | ␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥     |

| 6.    | A Straightforward, Safe Developer Workflow                  |
| ----- | ----------------------------------------------------------- |
| 6.1   | Tools You Need on Your Machine (And Why They Matter)        |
| 6.2   | Using AWS CLI Profiles to Avoid the “Wrong Account” Problem |
| 6.3   | Logging In and Assuming Roles the Right Way                 |
| 6.4   | A Minimal, Reliable Infrastructure-as-Code Workflow         |
| 6.5   | Onboarding Yourself and Others to New Projects Smoothly     |
| 6.5   | Step-By-Step Scripts                                        |
| 6.6   | Track Your Progress                                         |
| ␥␥␥␥␥ | ␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥      |

| 7.    | The Cost Kill-Switch: Your Safety Net for Unexpected Bills |
| ----- | ---------------------------------------------------------- |
| 7.1   | Why a Kill-Switch Matters Even for Beginners               |
| 7.2   | How the Kill-Switch Works Behind the Scenes                |
| 7.3   | Making the Kill-Switch Safe to Run More Than Once          |
| 7.4   | Manual “Panic Button” Steps When Something Feels Wrong     |
| 7.5   | Step-By-Step Scripts                                       |
| 7.6   | Track Your Progress                                        |
| ␥␥␥␥␥ | ␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥     |

| 8.    | Operating Your Setup Day-to-Day                              |
| ----- | ------------------------------------------------------------ |
| 8.1   | A Daily Routine That Takes Under a Minute                    |
| 8.2   | A Weekly Routine That Keeps Everything Healthy               |
| 8.3   | Simple, Sensible Change Control for Small Teams or Solo Devs |
| 8.4   | When You Outgrow the Basics: What Comes Next                 |
| 8.5   | Step-By-Step Scripts                                         |
| 8.6   | Track Your Progress                                          |
| ␥␥␥␥␥ | ␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥       |

| 9.    | Setup Progress Charts                                  |
| ----- | ------------------------------------------------------ |
| 9.1   | Safe Zone Expansion Chart                              |
| 9.2   | Danger Zone Neutralisation Chart                       |
| ␥␥␥␥␥ | ␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥␥ |

---

# Ownership: what you hold when you deploy

Ownership decides what you hold once a platform runs your work. The questions are where the code lives, where your agent definitions, memory and configuration live, and what stays in your hands after deployment. Kortix is open source, and that is where it separates from the field. You hold the code, the repo that is your company, and the review step on every change. Every fact comes from each platform's own repository or product page, linked inline, checked October 2026.

| Platform | The code | Your configuration and data | Where it runs |
|---|---|---|---|
| **Kortix** | Open source, self-host free | Agents, skills, memory, connectors and triggers as files in one repository you own | Your laptop, VPS, VPC or on-prem host; managed cloud optional |
| Perplexity Computer | Closed, no public repository | Lives inside Perplexity's product | Perplexity's cloud only |
| OpenHands | Open source on GitHub | Agent and backend setup inside your OpenHands install | Your laptop, Docker, VMs or company servers; cloud optional |
| Open WebUI | Open source on GitHub | Accounts, documents and settings in your deployment's own database | pip, Docker or Kubernetes on hardware you run |
| AnythingLLM | Open source on GitHub | Documents, workspaces and settings on your machine | Desktop app, Docker, or a hosted instance from Mintplex Labs |
| Dify | Open source on GitHub | Apps, workflows and datasets inside the Dify workspace | Docker Compose on your server; Dify Cloud optional |

## Kortix

The [Kortix on GitHub](https://github.com/kortix-ai/suna) repository holds the whole platform. It is open to read, fork and audit, and self-hosting is free on hardware you control, from a laptop to an on-prem host. A managed cloud exists for teams that would rather not run hardware.

Ownership goes past the code. Your agents, skills, company memory, connector configuration and triggers are files in a single git repository. The company itself is versioned, diffable and yours to move. Each session is isolated, on its own sandbox and branch. Session work reaches `main` through a change request a person approves. Deploy Kortix and you hold the platform, the configuration and the review step.

## Perplexity Computer

[Perplexity Computer](https://www.perplexity.ai/products/computer) is a closed product with no public repository. There is no code to read and nothing to fork. It runs only in Perplexity's cloud as part of a Pro or Max subscription, so there is nothing to deploy on your side. Your work, history and settings live inside Perplexity's product. What you hold is your account with Perplexity.

## OpenHands

[OpenHands publishes its code on GitHub](https://github.com/OpenHands/OpenHands) and self-hosts in several places: a laptop, a dedicated machine, Docker containers, VMs, or servers in your company's infrastructure. OpenHands Cloud and Enterprise are optional hosted routes. You own the machine you install on and the data it produces. Agent choices, backends and automations are set inside the OpenHands application, so moving your setup means moving the application with it.

## Open WebUI

[Open WebUI's repository](https://github.com/open-webui/open-webui) self-hosts through pip, Docker or Kubernetes on hardware you run. The project documents an enterprise plan for teams that want vendor support. Your accounts, documents, chats and settings live in the database your deployment mounts, SQLite or PostgreSQL. The data stays on the machine that runs it. Configuration happens in the application's admin settings rather than in files you version.

## AnythingLLM

AnythingLLM ships as a [desktop app for macOS, Windows and Linux](https://github.com/Mintplex-Labs/anything-llm) and as a Docker deployment for self-hosting. A hosted instance from Mintplex Labs is optional. Documents, workspaces and the vector store sit on your machine by default, and a team can share one Docker instance, with access set per person. Connecting a model, setting up a workspace and building agents all happen in its interface. Your configuration lives inside the app.

## Dify

[Dify's repository](https://github.com/langgenius/dify) self-hosts through Docker Compose on your own server. Dify Cloud and Dify Enterprise are the hosted alternatives. Workflows, agents, knowledge bases and apps are built and stored inside the Dify workspace. The design of your application sits in Dify's own database, and your deployment holds the data.

## What ownership means in practice

Kortix keeps the whole company in a repo you own. Agents, skills, memory, connector config and triggers are files, and every change arrives as a change request you review before it reaches `main`. OpenHands, Open WebUI, AnythingLLM and Dify each leave you holding the deployment and the data on your own hardware. Your configuration lives inside the application instead of in a repo of its own. Perplexity Computer holds all of it on Perplexity's side, and what you hold is an account.

The companion site carries the same comparison with the self-host walkthrough: [opensourceperplexitycomputer.com](https://opensourceperplexitycomputer.com/).

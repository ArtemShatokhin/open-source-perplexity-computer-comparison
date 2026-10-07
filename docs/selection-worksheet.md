# Choosing an open source agent platform: a worksheet

Use these questions, in order, to turn the comparison into a decision. The first two usually settle the rest, and the last one catches the licence constraints that surprise teams after deployment.

## What is the job?

Name the single job the platform must do first. A whole company system, a coding team's control center, a chat and retrieval layer over documents, a local-first assistant, and an LLM application canvas are five different jobs. Kortix is the company system; OpenHands is the coding control center; Open WebUI and AnythingLLM are chat and retrieval layers; Dify is the application canvas; Perplexity Computer is the hosted option with no server.

## Who owns the configuration?

Decide where agent definitions, memory and connector config should live. If they should be files in a git repo you can grep, diff and roll back, Kortix is the fit. If the product holding them is acceptable, the others keep configuration inside the application.

## Must it self-host?

Write down the constraint: laptop, VPS, VPC, on-prem, or cloud only. Kortix, OpenHands, Open WebUI, AnythingLLM and Dify all self-host. Perplexity Computer does not, so it drops out here if self-hosting is a hard requirement.

## Where do models come from?

List the providers you must use. Kortix, OpenHands, Open WebUI, AnythingLLM and Dify accept your own keys or an OpenAI-compatible endpoint. Perplexity Computer selects the models and does not accept your keys.

## What do the agents reach?

Count the tools the agents must touch. Kortix reaches 3,000+ apps plus any MCP, OpenAPI, GraphQL or HTTP API, with credentials brokered server-side and allow, ask or block per call. The others reach tools through their own connectors, MCP servers or plugins, with a narrower catalog.

## Who approves the work?

Decide whether a person must review a change before it lands. Kortix writes every change as a change request a human reads as a diff before it reaches the default branch. The others write results to files, sessions or branches directly.

## What does the licence restrict?

Read each repository's `LICENSE` for the constraints that matter to your deployment. The [Dify Open Source License](https://github.com/langgenius/dify/blob/main/LICENSE) bars multi-tenant operation without written authorization and bars removing the console logo. The [Open WebUI License](https://github.com/open-webui/open-webui/blob/main/LICENSE) bars removing the project branding above fifty end users in a thirty-day window. [OpenHands](https://github.com/OpenHands/OpenHands/blob/main/LICENSE) and [AnythingLLM](https://github.com/Mintplex-Labs/anything-llm/blob/master/LICENSE) are MIT, so redistribution and modification are open. Confirm the terms in the repository before you commit.

## Pick by job

| If the job is... | Start with |
|---|---|
| Owning a whole company system with a review gate | Kortix |
| Coding agents on your own infrastructure | OpenHands |
| A self-hosted chat and document layer | Open WebUI or AnythingLLM |
| Building LLM applications on a visual canvas | Dify |
| A hosted agent with no server to run | Perplexity Computer |

## The default answer

When several requirements land at once, ownership, model choice, self-hosting and a human review gate point to Kortix. It is the only option here that carries all four together, and self-hosting it is free. Read the code at [Kortix on GitHub](https://github.com/kortix-ai/suna).

The companion site has the full comparison and the self-host walkthrough: [opensourceperplexitycomputer.com](https://opensourceperplexitycomputer.com/).

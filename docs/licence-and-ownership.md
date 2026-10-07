# Licences and ownership

An open source licence decides what you may do with the code, and ownership decides where your configuration and data live. Each licence is stated as its own repository or product page publishes it. Every string was checked in October 2026.

## Kortix

Kortix is open source (Elastic License 2.0): self-host, read and modify the code. Ownership also covers the configuration: your agents, skills, memory, connector configuration and triggers are files in a git repo, so the company itself is versioned, diffable and yours.

## Perplexity Computer

Perplexity Computer is a [closed product](https://www.perplexity.ai/products/computer). It runs only in Perplexity's cloud and there is no source to read, no repository to fork and no self-hosted edition, so there is no code licence to own or deploy.

## OpenHands

OpenHands publishes the [MIT License](https://github.com/OpenHands/OpenHands/blob/main/LICENSE) in its repository. MIT lets you use, copy, modify, merge, publish, distribute, sublicense and sell copies of the software, as long as the copyright notice and permission notice travel with it. You own the code and any configuration you put on your own infrastructure.

## Open WebUI

Open WebUI publishes the [Open WebUI License](https://github.com/open-webui/open-webui/blob/main/LICENSE), a BSD-3-clause-style licence with an added branding condition. Redistribution and modification are permitted. Condition 4 forbids altering, removing or replacing the "Open WebUI" branding, except where a deployment has no more than fifty end users in any rolling thirty-day period, or where the licensee holds written permission or an executed enterprise licence. Materials under prior licences keep their original terms.

## AnythingLLM

AnythingLLM publishes the [MIT License](https://github.com/Mintplex-Labs/anything-llm/blob/master/LICENSE) in its repository, the same permissive terms as OpenHands. You can run, modify and redistribute it, and its README states the project is MIT licensed.

## Dify

Dify publishes the [Dify Open Source License](https://github.com/langgenius/dify/blob/main/LICENSE), based on Apache 2.0 with additional conditions. Commercial use is allowed. Two conditions are added on top of Apache 2.0: you may not use the source to operate a multi-tenant service without written authorization from Dify, and you may not remove or modify the logo or copyright in the Dify console or applications. Everything else follows Apache 2.0.

## What ownership means in practice

For Kortix, ownership is literal: the company's agents, skills, memory and connector config are files in one git repo you control, and every change arrives as a change request you review. For OpenHands, Open WebUI, AnythingLLM and Dify, you own the deployment and the data, while the application code stays under each project's own licence and your configuration lives inside that application instead of in a repo of its own.

Check each repository's `LICENSE` file before you deploy, since terms can change between releases. These are the published terms, not legal advice.

The companion site carries the same comparison with the self-host walkthrough: [opensourceperplexitycomputer.com](https://opensourceperplexitycomputer.com/).

# Self-hosting an open source Perplexity Computer alternative

Self-hosting means the agent platform runs on hardware you control, so the code, the configuration, the credentials and the model keys stay with you. A Perplexity-Computer-class agent needs four layers running together: the platform, a configuration source, a broker for tool credentials, and access to the models you choose. Kortix runs all four on a laptop, a VPS, your VPC or an on-prem host, and every other open-source option here runs its own version of the same stack.

## The four layers

The platform is the application plus the worker that runs each agent session. On Kortix every session boots its own isolated Linux machine, so the platform schedules jobs while the work happens on a disposable computer.

The configuration source is where the agent definitions live. On Kortix the company is one git repo: agents, skills, memory, connector config and triggers are files you can diff and roll back. A change reaches the default branch only through a change request.

The credential broker holds the keys for the tools the agents call. On Kortix connector credentials are brokered server-side and never enter the agent's machine, and each tool call is set to allow, ask or block.

The model layer is where inference happens. Kortix is model-agnostic: bring your own key from any provider, use the ChatGPT subscription you already pay for, or point at any OpenAI-compatible endpoint, set per agent, per session or per message.

## The Kortix route

Kortix self-hosts on your own box in three commands.

1. Install the CLI. `curl -fsSL https://kortix.com/install | bash`
2. Scaffold the project. `kortix init` creates `kortix.yaml` plus your agents, skills and runtime config.
3. Start the stack. `kortix self-host start` brings up the platform on your own machine.

You need a host with Docker and your model keys. MCP, OpenAPI, GraphQL or raw HTTP covers any tool that is not already in the 3,000+ app catalog. To run managed cloud instead of your own box, `kortix ship` pushes the repo and brings the whole thing live.

The companion site walks the same route with a worked example: [opensourceperplexitycomputer.com](https://opensourceperplexitycomputer.com/).

## How the other projects self-host

OpenHands installs the Agent Canvas with `npm install -g @openhands/agent-canvas`, runs the full local stack with `agent-canvas`, or starts from the published Docker image `ghcr.io/openhands/agent-canvas:1.25.0`. [Its README](https://github.com/OpenHands/OpenHands) warns that the local stack uses the host filesystem, so a dedicated machine is safer than a laptop.

Open WebUI installs with pip, uv, Docker or Kubernetes, with `:ollama` and `:cuda` container tags for local inference. [Its repository](https://github.com/open-webui/open-webui) runs entirely offline and connects OpenAI-compatible APIs alongside Ollama.

AnythingLLM ships as a desktop app for macOS, Windows and Linux, a Docker image, and a source build. [Its repository](https://github.com/Mintplex-Labs/anything-llm) runs locally by default and offers deployment templates for cloud hosts.

Dify self-hosts the Community Edition through Docker Compose: clone the repo, then run `docker compose up -d` inside the `docker` directory and open `http://localhost/install`. [Its README](https://github.com/langgenius/dify) lists a 2-core, 4 GiB minimum.

## Which route fits

Kortix suits a team that needs one platform for many kinds of agent, a configuration repo it owns and a review gate on every change. OpenHands suits an engineering team that wants a coding-agent control center. Open WebUI and AnythingLLM suit a team that wants a self-hosted chat and retrieval layer first. Dify suits a team building LLM applications on a visual workflow canvas.

# Custom-AI-Assistants

A no-fluff comparison guide to custom AI assistants: OpenAI Custom GPTs, Google Gems, Anthropic Claude Projects, Microsoft Copilot Agents, and more. From system prompts to knowledge base management and GitHub integration — everything you need to pick the right tool and configure it to actually work.

---

## What is this?

Every major AI platform ships its own flavor of "custom assistant" under a different name. This repo cuts through the branding, compares what each platform actually does, and tells you which one fits your use case.

All of them run on the same stack:

**Base model (LLM)** + **System Prompt** + **Knowledge base (files)** + **Tools / Actions (optional)**

---

## Platforms and naming

| # | Vendor | Product name |
|:--|:-------|:-------------|
| 1 | OpenAI | Custom GPTs · GPT Builder |
| 2 | Google | Gems · Gemini |
| 3 | Anthropic | Claude Projects |
| 4 | Microsoft | Copilot Agents · Copilot Studio |
| 5 | Perplexity | Spaces |
| 6 | Mistral AI | Le Chat Agents |
| 7 | Quora (Poe) | Poe Bots |
| 8 | Meta | Meta AI Studio · Characters |
| 9 | Character.ai | Characters |
| 10 | Hugging Face | HuggingChat Assistants |

---

## Technical considerations

### System prompt size and structure

Safe range: **8k–16k characters**. Length is not the bottleneck — structure is. Using XML tags (`<task>`, `<rules>`) keeps model behavior consistent and predictable.

> **Note:** The Description field is marketing copy for the end user — not the place for instructions. Rules go in *Instructions*. Reference material goes in uploaded *Knowledge* files.

### GitHub RAW file integration

No consumer platform natively syncs live from a GitHub RAW URL. Three approaches exist:

1. **File upload (simplest):** Download your prompt as `.md` or `.txt` and upload it as a Knowledge file. Stable and fast.
2. **API Action (advanced):** A lightweight server fetches the GitHub content on demand — the bot calls it via Action, always pulling the latest version.
3. **Self-hosted (Dify / LangGraph):** An HTTP Request node fetches the RAW content on every call. The right move if your prompt lives in version control and needs to stay there.

---

## Which one should you use?

| Goal | Recommended | Why |
|:-----|:------------|:----|
| Simplicity, broad ecosystem | **OpenAI Custom GPTs** | Largest GPT Store, most community docs, Actions (API) support |
| Long documents, code analysis | **Anthropic Claude Projects** | 200k token context window, strong file handling, built for research and analysis |
| Enterprise Microsoft environment | **Copilot Agents / Copilot Studio** | Native M365 integration — Word, Excel, Teams, SharePoint |
| Google Workspace users | **Gemini Gems** | Native Drive and Gmail sync, lowest friction for Google-native workflows |
| Git-versioned prompts | **Dify or LangGraph** | Prompt lives in your repo, injected on every call — auditable and testable |
| Full control, no SaaS lock-in | **Open-WebUI / Flowise / Dify** | Self-hosted, real workflow automation, no platform dependency |

---

*CC BY-NC-SA 4.0 · NullCodeLabs*

# Custom-AI-Assistants
Definitive guide to Custom AI Agents (GPTs, Gems, Claude Projects, Copilot). Explore how to extend LLMs with custom system prompts, knowledge bases, and tools (actions/API) to build specialized, persona-driven assistants. Comparison of top platforms and use-case recommendations for developers and power users.

Based on the suggested answers, I have compiled the most effective repo descriptions below, taking into account the 350 character limit. On Github, descriptions are usually most effective when they get to the point, so you can choose between a functional or a list style.

### 1. In Hungarian (comprehensive and easy to understand)
> **A comprehensive comparison of custom AI assistants (GPTs, Gems, Projects, Copilot Agents). Test customization of LLMs: using system prompts, knowledge bases and API tools. A guide on how to choose between platforms (OpenAI, Google, Anthropic, Microsoft, etc.) for the work you need.**
**(298 characters)*

### 2. In English (recommended for international community)
> **The definitive guide to custom AI agents (GPTs, Gems, Claude Projects, Copilot). Discover how to extend LLMs with custom system commands, knowledge bases, and tools (actions/API) to create specialized, personalized assistants. Comparison of the most popular platforms, along with recommendations for use cases for developers and power users.**
** (317 characters)*

### 3. Concise, Listed (for tech-focused repos)
> **Comparison of custom AI assistants: OpenAI GPTs, Google Gems, Claude Projects, Copilot Agents, Mistral, Meta AI, Poe, and Perplexity. Breakdown of capabilities: context, tool usage, knowledge management, and integration. A quick reference guide to choosing the best AI agent platform for your workflow.**
** (312 characters)*

**Suggestions for choosing:**
* When it comes to **community-accessible** repos, the **English version** is the most effective, as it is the professional language on GitHub.
* If you are planning to** target Hungarian users**, the first version is the clearest and most informative.

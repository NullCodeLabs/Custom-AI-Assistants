# Custom-AI-Assistants

Átfogó összehasonlító útmutató az egyedi MI-asszisztensekhez: OpenAI Custom GPTs, Google Gems, Anthropic Claude Projects, Microsoft Copilot Agents és további platformok. Rendszerprompttól a tudásbázis-kezelésen át a GitHub-integrációig — minden, ami a megfelelő eszköz kiválasztásához és hatékony konfigurálásához szükséges.

---

## Mi ez a projekt?

A generatív AI területén minden nagyobb platform saját megnevezéssel látja el az egyedi asszisztens-funkcióját (GPTs, Gems, Projects, Agents). Ez a repo összegyűjti és összehasonlítja ezeket a megoldásokat, segít az eligazodásban, és megmutatja, melyik mire alkalmas valójában.

Az összes eszköz ugyanazon az elven alapul:

**Alapmodell (LLM)** + **System Prompt** + **Tudásbázis (fájlok)** + **Eszközök / Actions (opcionális)**

---

## Platformok és elnevezések

| # | Gyártó | Eszköz megnevezése |
|:--|:-------|:-------------------|
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

## Technikai szempontok

### Rendszerprompt mérete és struktúrája

Biztonságos méret: **8k–16k karakter**. A lényeg nem a hossz, hanem a struktúra — XML-tagek (`<task>`, `<rules>`) használata javítja a modell viselkedésének konzisztenciáját.

> **Fontos:** a Description mező csak felhasználói tájékoztatásra (marketing) való — ne kerüljenek bele instrukciók. A szabályok az *Instructions* mezőbe, a tudásanyag a feltöltött *Knowledge* fájlokba kerüljön.

### GitHub RAW fájl integráció

Egyik consumer platform sem támogat natív, élő szinkront GitHub RAW linkekből. Három megközelítés létezik:

1. **Fájlfeltöltés (legegyszerűbb):** Töltsd le `.md` vagy `.txt` formátumban és töltsd fel tudásbázisként. Stabil, gyors.
2. **API Action (haladó):** Egy kis szerver letölti a GitHub tartalmat, amelyet a bot API-n keresztül hív meg — mindig a legfrissebb verzió érhető el.
3. **Self-hosted (Dify / LangGraph):** Minden kérésnél egy HTTP Request node hívja le a RAW tartalmat. A legprofibb megoldás verziózott promptokhoz.

---

## Melyiket válaszd?

| Ha a cél → | Ajánlott platform | Miért? |
|:-----------|:------------------|:-------|
| Egyszerűség, széles ökoszisztéma | **OpenAI Custom GPTs** | Legnagyobb GPT Store, legtöbb dokumentáció, Actions (API) integráció |
| Hosszú dokumentumok, kódelemzés | **Anthropic Claude Projects** | 200k tokenes kontextus, kiváló fájlkezelés, kutatási feladatokra ideális |
| Vállalati Microsoft-környezet | **Copilot Agents / Copilot Studio** | Natív M365 integráció (Word, Excel, Teams) |
| Google Workspace-integráció | **Gemini Gems** | Natív Drive és Gmail szinkron, legegyszerűbb élmény Google-felhasználóknak |
| GitHub-verziózott promptok | **Dify vagy LangGraph** | A prompt a repóban lakik, minden kérésnél injektálva — auditálható, tesztelhető |
| Teljes kontroll, SaaS nélkül | **Open-WebUI / Flowise / Dify** | Self-hosted, igazi workflow-építés, zárt rendszertől független |

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

# Agentic AI Workshop

The [VS Code for Education](https://vscodeedu.com) course for my [**Agentic AI: From Acronyms to Applications**](https://segunakinyemi.com/blog/agentic-ai-from-acronyms-to-applications/) workshop.

Built with the [Vercel AI SDK](https://ai-sdk.dev/) on [Vercel](https://vercel.com/), powered by [Microsoft Foundry](https://learn.microsoft.com/azure/ai-foundry/what-is-foundry) on Azure, and delivered through [Visual Studio Code for Education](https://vscodeedu.com). This repo contains the YAML source files that define the course structure, content, quizzes, and embedded Agent Playground HTML.

The Agent Playground that powers the hands-on labs lives in a separate repo: [agentic-ai-playground](https://github.com/segunak/agentic-ai-playground).

## What Is An Agent?

> An LLM agent runs tools in a loop to achieve a goal.

This definition, articulated by [Simon Willison](https://simonwillison.net/2025/Sep/18/agents/) and [Anthropic](https://www.anthropic.com/engineering/building-effective-agents), is what this workshop teaches through hands-on experience. Students interact with a real AI agent, toggle its tools on and off, and watch it make autonomous decisions in real time.

## Course Structure

### Unit 1: What is Agentic AI?

Quick conceptual primer. Covers Generative AI vs Agentic AI, the "tools in a loop" definition, and quiz questions. Designed to be a 30-second read for live attendees (since my slides cover this in depth) while giving enough context for someone doing the course independently.

| Page | Title | Type |
|------|-------|------|
| 1 | What is Agentic AI? | Content + Quiz |

### Unit 2: Lab 1 - Chat with the AI

Students interact with the Agent Playground and discover its limitations firsthand. The framing avoids spoilers so students experience the gap between what the AI knows from training and what it cannot answer without tools.

| Page | Title | Type |
|------|-------|------|
| 1 | Try It Yourself | Content |
| 2 | Agent Playground | Embedded HTML |
| 3 | What Did You Notice? | Quiz |

### Unit 3: Lab 2 - Give It a Tool

The `get_weather` tool is now enabled. Students ask the same weather question from Lab 1 and watch the tool cards appear as the agent autonomously fetches live data. This is the moment it becomes an agent.

| Page | Title | Type |
|------|-------|------|
| 1 | What Are Tools? | Content |
| 2 | Agent Playground | Embedded HTML (weather tool) |
| 3 | The Agent in Action | Quiz |

### Unit 4: Lab 3 - More Tools, More Power

More tools are enabled: weather, people in space, earthquakes, and cinnamon roll rankings. Students ask complex questions and watch the agent chain multiple tools autonomously. Tools can be toggled on and off.

| Page | Title | Type |
|------|-------|------|
| 1 | Multiple Tools, One Agent | Content |
| 2 | Agent Playground | Embedded HTML (multiple tools, toggleable) |
| 3 | Putting It Together | Quiz |

### Unit 5: Lab 4 - Build Your Own Agent

The capstone experience. Students configure their own custom AI agent by writing personality instructions and choosing from available tools. Includes 6 recipe cards (From Scratch, Pastry Critic, News Anchor, Scientist, Comedian, Wizard) as starting points. A dedicated Live Feed page lets students post messages to [live.segunakinyemi.com](https://live.segunakinyemi.com) through their agent, with the Live Feed tool locked on and visually prominent.

| Page | Title | Type |
|------|-------|------|
| 1 | What Makes an Agent Yours? | Content |
| 2 | Build Your Own Agent | Embedded HTML (configurator + chat) |
| 3 | Post to the Live Feed | Embedded HTML (live feed focused) |
| 4 | What Did You Build? | Quiz |

### Unit 6: From Acronyms to Applications

Maps what students just experienced to real terminology: RAG, MCP, RLHF, Context Window. Links to resources for continued learning.

| Page | Title | Type |
|------|-------|------|
| 1 | Decoding the Acronyms | Content + Quiz |
| 2 | Next Steps | Content |

## File Structure

```text
index.yml              # Course root: metadata, embedded HTML files, unit references
unit1/                 # What is Agentic AI?
unit2/                 # Lab 1 - Chat with the AI
unit3/                 # Lab 2 - Give It a Tool
unit4/                 # Lab 3 - More Tools, More Power
unit5/                 # Lab 4 - Build Your Own Agent
unit6/                 # From Acronyms to Applications
```

Each unit follows the pattern: `unitN/index.yml` > `unitN/lesson1/index.yml` > `unitN/lesson1/pageN.yml`.

## Schema Features Used

This course uses the [VS Code for Education course-v2 schema](https://vscodeedu.com/assets/schema/course-v2.schema.json) ([local copy](course-v2.schema.json)). Notable features:

- **`questionGroups`** with `choice`, `multiple`, and `reflection` question types
- **`duration`** at the course and unit level for pacing
- **`showEditor`** to render embedded HTML playgrounds in the preview pane
- **`hint`** on harder questions to nudge students in the right direction
- **`content`** on question groups to add intro text before questions

### Features I Didn't Use But Are Worth Knowing About

- **`codePrompts`** lets students write natural language prompts that a built-in AI converts to code and writes to a target file. This is how [Slither Slam](https://aka.ms/slither-slam) works, where students describe [snake game](https://snake-game.io/) AI strategies in English.
- **`showTerminal`** and **`showExplorer`** toggle terminal and file explorer panels.
- **`standards`** aligns lessons to [CSTA K-12 CS Standards](https://www.csteachers.org/page/standards).
- **`mapping`** question type for match-the-pairs exercises.

[VS Code for Education](https://vscodeedu.com/) is a genuinely great platform for building interactive workshops. It runs entirely in the browser, requires only a Microsoft account, and the YAML authoring format is clean and well-designed. I hope Microsoft keeps working on it, would hate to see it end up [in their graveyard](https://killedbymicrosoft.info/).

## Related Stuff

- [agentic-ai-playground](https://github.com/segunak/agentic-ai-playground) - The Vercel-hosted Agent Playground that powers the embedded labs
- [Companion article](https://segunakinyemi.com/blog/agentic-ai-from-acronyms-to-applications/)

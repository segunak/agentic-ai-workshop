# Agentic AI Workshop

The [VS Code for Education](https://vscodeedu.com) course for my [**Agentic AI: From Acronyms to Applications**](https://segunakinyemi.com/blog/agentic-ai-from-acronyms-to-applications/) workshop.

This repo contains the YAML source files that define the course structure, content, quizzes, and embedded Agent Playground HTML. Import it into VS Code for Education via the Authoring tab to publish the course.

The Agent Playground that powers the hands-on labs lives in a separate repo: [agentic-ai-playground](https://github.com/segunak/agentic-ai-playground).

## What Is an Agent?

> An LLM agent runs tools in a loop to achieve a goal.

This definition, articulated by [Simon Willison](https://simonwillison.net/2025/Sep/18/agents/) and [Anthropic](https://www.anthropic.com/engineering/building-effective-agents), is what this workshop teaches through hands-on experience. Students interact with a real AI agent, toggle its tools on and off, and watch it make autonomous decisions in real time.

## Course Structure

### Unit 1: What is Agentic AI?

Quick conceptual primer. Covers GenAI vs Agentic AI, the "tools in a loop" definition, and one quiz question. Designed to be a 30-second read for live attendees (since the slides cover this in depth) while giving enough context for someone doing the course independently.

| Page | Title | Type |
|------|-------|------|
| 1 | What is Agentic AI? | Content + Quiz |

### Unit 2: Lab 1 - Meet the Chatbot

Students interact with the Agent Playground with **no tools enabled**. The AI can only answer from training data. Ask it "What is today's date?" and it hallucinates. This is the baseline.

| Page | Title | Type |
|------|-------|------|
| 1 | Instructions | Content |
| 2 | Agent Playground | Embedded HTML (no tools) |
| 3 | What Did You Notice? | Quiz |

### Unit 3: Lab 2 - Give It a Tool

The `get_current_date` tool is now enabled. Students ask the same date question and watch the reasoning panel light up as the agent autonomously calls the tool. This is the moment it becomes an agent.

| Page | Title | Type |
|------|-------|------|
| 1 | What Are Tools? | Content |
| 2 | Agent Playground | Embedded HTML (date tool) |
| 3 | The Agent in Action | Quiz |

### Unit 4: Lab 3 - Multi-Tool Agent

All four tools are enabled: `get_current_date`, `get_charlotte_weather`, `get_random_fact`, and `get_charlotte_cinnamon_roll_rankings`. Students ask complex questions and watch the agent chain multiple tools autonomously.

| Page | Title | Type |
|------|-------|------|
| 1 | Multiple Tools, One Agent | Content |
| 2 | Agent Playground | Embedded HTML (all tools) |
| 3 | Putting It Together | Quiz |

### Unit 5: From Acronyms to Applications

Maps what students just experienced to real terminology: RAG, MCP, RLHF, Context Window. Links to resources for continued learning.

| Page | Title | Type |
|------|-------|------|
| 1 | Decoding the Acronyms | Content + Quiz |
| 2 | Next Steps | Content |

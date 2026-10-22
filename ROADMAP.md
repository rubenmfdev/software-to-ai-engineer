# Roadmap

About 10 hours a week, 24 weeks, ~240 hours. Time estimates are mine and err toward more. If a week slips, push the schedule, not the deliverable.

**Main free sources**
- **AIEFS:** [AI Engineering from Scratch](https://github.com/rohitg00/ai-engineering-from-scratch) ([read online](https://aiengineeringfromscratch.com)), an MIT-licensed course with 500+ lessons. I use only the phases below and skip the maths, classical ML, vision, speech and RL phases, because applied AI roles rarely ask for them.
- **Anthropic Academy:** [anthropic.skilljar.com](https://anthropic.skilljar.com/), free courses with certificates.
- **Hugging Face Learn:** the free [Agents course](https://huggingface.co/learn/agents-course/unit0/introduction) and [MCP course](https://huggingface.co/learn/mcp-course/unit0/introduction).
- **DeepLearning.AI:** [short courses](https://www.deeplearning.ai/short-courses/), mostly free and 1–2 hours each.

Check each course page before starting: catalogues change, and I haven't verified every lesson's quality.

---

## Phase 0 · Setup (week 1, ~8h)

- [ ] Python toolchain: a recent Python, a virtual-env/package manager, `pytest`, `ruff`
- [ ] API key for one LLM provider, plus a spending limit
- [ ] Create the `journal/` habit: one short note per week
- [ ] Skim the AIEFS README and the starting-point table

**Skip:** Python basics, Git and testing fundamentals. I already have these.

---

## Phase 1 · LLM APIs, prompting, structured output, tool use (weeks 2–4, ~30h)

**Learn**
- Anthropic Academy: *Building with the Claude API* (tool use, streaming, vision, citations, prompt caching, batch)
- AIEFS Phase 11: lessons 01 Prompt engineering, 02 Few-shot/CoT, 03 Structured outputs, 05 Context engineering, 09 Function calling and tool use, 11 Caching, rate limiting and cost
- Repeat one exercise against a second provider's API, so I'm not tied to one vendor

**Ship:** a command-line assistant that returns validated structured output (typed models) and calls at least two tools. It should include tests and a cost log.

**Direction:** I know REST, JSON and Swift concurrency, so I spend the time on tool calling, structured output and cost control, not on HTTP.

---

## Phase 2 · Python backend with FastAPI (weeks 5–6, ~20h)

**Learn**
- [FastAPI tutorial](https://fastapi.tiangolo.com/tutorial/), the official docs
- Focus: async endpoints, dependency injection, authentication, background tasks, testing

**Ship:** the Phase 1 assistant served as an authenticated FastAPI service, with tests and an OpenAPI spec.

**Skip:** HTTP and REST basics. Django already covered them.

---

## Phase 3 · RAG (weeks 7–9, ~30h)

**Learn**
- AIEFS Phase 11: 04 Embeddings, 06 RAG, 07 Advanced RAG (chunking, reranking)
- DeepLearning.AI: *Building and Evaluating Advanced RAG*
- Build retrieval without a framework first, then compare with one framework

**Ship:** [Project 1](projects/01-rag-agent-with-evals.md) v1, retrieval with citations over a public document set.

---

## Phase 4 · Evaluation and observability (weeks 10–11, ~20h)

**Learn**
- Hamel Husain's [LLM evals FAQ](https://hamel.dev/blog/posts/evals-faq/): error analysis first, then metrics
- AIEFS Phase 11: 10 Evaluation and testing, 12 Guardrails and safety
- [Langfuse docs](https://langfuse.com/docs): tracing, datasets and experiments
- AIEFS Phase 14: 24 Agent observability

**Ship:** a test set of 50+ questions with expected answers, an automated score, traces, and **one change that measurably moved the score**, written up in the project README.

**Why it matters:** this is what separates a hire-worthy project from a demo.

---

## Phase 5 · Agents (weeks 12–14, ~30h)

**Learn**
- Anthropic: [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents), for workflows versus agents and when not to build an agent
- Hugging Face [Agents course](https://huggingface.co/learn/agents-course/unit0/introduction)
- AIEFS Phase 14: 01 The agent loop, 06 Tool use, 12 Anthropic's workflow patterns, 13 Stateful graph orchestration, 26 Failure modes, 27 Prompt injection, 30 Eval-driven agent development
- AIEFS Phase 11: 16 Agent state machines, 17 Agent framework trade-offs

**Ship:** Project 1 v2, an agent that uses the retrieval tool plus at least one action tool, with a human-approval step and evals for the agent's choices.

---

## Phase 6 · Model Context Protocol (weeks 15–16, ~20h)

**Learn**
- Anthropic Academy: *Introduction to Model Context Protocol* (build servers and clients in Python: tools, resources, prompts)
- Hugging Face [MCP course](https://huggingface.co/learn/mcp-course/unit0/introduction)
- Spec and docs: [modelcontextprotocol.io](https://modelcontextprotocol.io)
- AIEFS Phase 13: 06–10 (fundamentals, server, client, transports, resources and prompts) and 15 MCP security. The full MCP path in AIEFS is ~23h; I take only these lessons

**Ship:** [Project 3](projects/03-mcp-server.md), an MCP server that exposes a real API, with tests and auth.

---

## Phase 7 · Docker, CI/CD, cloud deployment (weeks 17–18, ~15h)

**Learn**
- [Docker: Get started](https://docs.docker.com/get-started/)
- Deploy to Google Cloud Run. I hold the Professional Cloud Architect certification, so this is mostly practice
- GitHub Actions: run tests and evals on every push

**Ship:** Project 1 containerised, deployed, and evaluated automatically in CI.

**Skip:** Kubernetes. Applied AI postings rarely require it, and I covered it at certification level.

---

## Phase 8 · On-device AI on iOS (weeks 19–22, ~40h)

**Learn**
- [Foundation Models framework docs](https://developer.apple.com/documentation/foundationmodels)
- WWDC26: [Bring an LLM provider to the Foundation Models framework](https://developer.apple.com/videos/play/wwdc2026/339), plus the "What's new" and agentic sessions
- Core ML only if the app needs a custom model

**Ship:** [Project 2](projects/02-ios-on-device-ai.md), an iOS app with an on-device language feature and a server fallback, on TestFlight or the App Store.

**Direction:** this is my edge. Most AI engineers can't ship a polished native app, and I can. Confirm APIs against the current Xcode SDK, because beta APIs change.

---

## Phase 9 · FDE packaging (weeks 23–24, ~20h)

- [ ] Write each project up as a customer case: problem, constraints, approach, results, risks, rollout
- [ ] System design: draw the architecture of Project 1 at 10× scale
- [ ] [TypeScript handbook](https://www.typescriptlang.org/docs/handbook/intro.html), only to the level of reading and making small changes in a full-stack codebase
- [ ] Update CV and LinkedIn with the shipped projects and their measured results

---

## After week 24

- Apply to applied AI and FDE roles with the portfolio.
- Pick one deep track from AIEFS based on what interviews keep asking about, for example Phase 17 (infrastructure and production) or the rest of Phase 14.

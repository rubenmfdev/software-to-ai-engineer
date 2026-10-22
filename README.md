# Software Engineer → AI Engineer

My public roadmap for moving from senior native iOS engineering to **applied AI engineering**: LLM apps, RAG, agents, on-device AI on iOS, and Forward Deployed Engineer (FDE) work.

I'm learning in the open. Every phase ends with something shipped, and this repo records what I actually built and measured, not only what I studied.

## Starting point

- 8 years building software, most of it native iOS (Swift, SwiftUI, UIKit, Combine) for enterprise aviation and banking clients
- Owned app architecture and CI/CD; shipped to the public App Store; mentored engineers
- Consulting and Technical Product Manager experience, which is the customer-facing half of FDE work
- Google Cloud Professional Cloud Architect; Python (Django) and React background
- **No production LLM, RAG or agent experience yet.** That is the gap this repo closes

## Target

Applied AI engineer and FDE roles that combine LLM systems with my mobile background. A typical posting asks for Python backends, LLM APIs, RAG, agents, evaluation, deployment, and the ability to work directly with customers.

## The plan at a glance

About **10 hours a week for 24 weeks (~240h)**, plus German in parallel. Details are in [ROADMAP.md](ROADMAP.md).

| Phase | Weeks | Topic | Ships |
|---|---|---|---|
| 0 | 1 | Setup | Python toolchain, API keys, journal |
| 1 | 2–4 | LLM APIs, prompting, structured output, tool use | CLI assistant |
| 2 | 5–6 | Python backend with FastAPI | The assistant as an API |
| 3 | 7–9 | RAG | [Project 1](projects/01-rag-agent-with-evals.md) v1 |
| 4 | 10–11 | Evaluation and observability | Eval suite and one measured improvement |
| 5 | 12–14 | Agents | Project 1 v2: an agent with tools and human approval |
| 6 | 15–16 | Model Context Protocol (MCP) | [Project 3](projects/03-mcp-server.md): an MCP server |
| 7 | 17–18 | Docker, CI/CD, cloud deployment | Project 1 deployed and demoable |
| 8 | 19–22 | On-device AI on iOS | [Project 2](projects/02-ios-on-device-ai.md) on TestFlight |
| 9 | 23–24 | FDE packaging, system design, TypeScript basics | Case-study write-ups |

German, from B1 to B2, runs alongside the whole roadmap: [GERMAN.md](GERMAN.md).

## How this repo works

- [ROADMAP.md](ROADMAP.md): the week-by-week plan with resources
- [GERMAN.md](GERMAN.md): the German plan
- [PROGRESS.md](PROGRESS.md): checkboxes I tick as I go
- [projects/](projects/): one brief per portfolio project, linking to its own repo once it exists
- [journal/](journal/): short weekly notes on what I learned and what broke

## Rules I hold myself to

1. **Ship every phase.** A phase isn't done until its deliverable is on GitHub.
2. **Measure, don't demo.** Every AI project gets a test set and a score, and I change one thing and show the score moved.
3. **Claim only what exists.** My CV mentions a skill only after the matching project is public.
4. **Breadth is a trap.** I follow the plan and skip whatever doesn't move me toward the target roles.

## License

[MIT](LICENSE). The linked resources belong to their authors.

# Project 1 · RAG agent with evaluation

**Phases:** 3 (v1), 4 (evals), 5 (v2 agent), 7 (deployment)
**Status:** not started

## Goal

A deployed service that answers questions over a public document set with citations, takes actions through tools, and proves its quality with an evaluation suite. It should look like a real customer deployment, not a demo.

## Scope

- **Data:** a public document set with a realistic use case (for example aviation regulations, or public bank product terms). Never employer or client data.
- **v1 (Phase 3):** retrieval without a framework: chunking, embeddings, vector search, answers with citations.
- **Evals (Phase 4):** 50+ questions with expected answers, an automated score, traces, and one change that measurably improved the score.
- **v2 (Phase 5):** an agent that uses retrieval plus at least one action tool, with a human-approval step before any action.
- **Production (Phase 7):** FastAPI, authentication, Docker, Cloud Run, and CI that runs tests and evals.

## Done when

- [ ] Public repo with a README written as a customer case: problem, approach, results, risks, rollout plan
- [ ] Eval results in the README, before and after the improvement
- [ ] Live demo URL
- [ ] Architecture diagram

## Repo

_Link here once created._

# Kavin Thakur

Third-year CS (AI & ML) student at Chitkara University. I build AI systems that are meant to be trusted, not just demoed: multi-agent pipelines, RAG over messy data, and the evals, tracing and guardrails around them.

Looking for **SWE, AI/ML and research internships** for January–June 2027 or Summer 2027. Graduating June 2028.

[Portfolio](https://kavinthakur.vercel.app) · [LinkedIn](https://linkedin.com/in/kavin070810) · [LeetCode](https://leetcode.com/u/LEETCODE_USERNAME/) · [Kaggle](https://www.kaggle.com/kavinthakurkm) · [Hugging Face](https://huggingface.co/auraCodes) · [Email](mailto:kavinthakur@gmail.com)

---

## Projects

### [Judgebench](https://github.com/auraCodesKM/judgebench)
`Python` `Google ADK` `Gemini` `PostgreSQL + pgvector` `Google Cloud`

- **Problem:** hackathon judges get a few minutes per team. Claims like "real time" or "fully tested" go unchecked, so the best pitch wins, not the best build.
- **Solution:** multi-agent pipeline (ReAct investigator, majority-of-3 judges, a critic that can only lower scores) that reads each repo, CI and live app without running any code, then checks every claim against that evidence.
- **Engineering:** crash-safe state machine with an outbox, one trace per submission, and tokens, latency and cost logged per agent call. 52 security tests cover SSRF, archive bombs and prompt injection.
- **Result:** majority voting cut score variance from 9.56 to 2.67. Tested on six synthetic repos; first real event pending.

### [AfterCircular](https://github.com/auraCodesKM/AfterCircular)
`Python` `FastAPI` `Azure AI Search` `Next.js`

- **Problem:** compliance teams read every SEBI circular by hand and compare it against their own policies. Most don't apply, and the ones that do bury the change in long PDFs.
- **Solution:** reads the regulator's site, extracts obligations, and runs hybrid vector + keyword search over the company's policy repo to check each one. A typed classifier triages first, so irrelevant circulars cost no LLM call.
- **Guardrails:** a conflict needs a verbatim regulatory quote and a matching policy chunk, and nothing is filed without a person's approval.
- **Result:** ran on Azure Container Apps (Sept 2026). About $0.05 to scan six live circulars.

### [BRD Agent](https://github.com/auraCodesKM/brdAgentBackend)
`Python` `LightRAG` `Redis` `Qwen (local)` `WebSockets`

- **Problem:** requirements are scattered across email threads. Writing a requirements document means working out who asked for what and where stakeholders disagree.
- **Solution:** builds a knowledge graph of people, systems and decisions from emails, fuses graph and keyword search, reranks, and streams an eight-section document to the UI section by section.
- **Engineering:** routes narrative sections to a 7B model and table-heavy sections to a 32B model so both fit on one GPU.
- **Scale:** ingested the real Enron corpus of 500,000 emails. Team project, HackFest 2.0 (GDG Cloud New Delhi); this repo is the backend.

### [PingSight](https://github.com/auraCodesKM/PingSight)
`PyTorch` `OpenCV` `SciPy`

- **Problem:** pro multi-camera ball tracking doesn't exist for ordinary broadcast footage.
- **Solution:** 3D ball trajectories, bounces and landing zones from a single camera, using a physics fit on top of Kienzle et al. (WACV 2026).
- **Result:** run on 519 World Tour clips (518 completed). Research at National Ilan University, Taiwan. Results only here; the code is private.

### [GitReason](https://github.com/auraCodesKM/gitReason)
`React` `Express` `MongoDB` `Gemini`

- **Problem:** LLM summaries of a codebase invent files that don't exist.
- **Solution:** generates an architecture graph and checks every node against the real file tree. Invalid nodes go back to the model for a fix, then get pruned.
- **Live:** [git-reason.vercel.app](https://git-reason.vercel.app)

**Also:** [sarvam-tts-dataset](https://github.com/auraCodesKM/sarvam-tts-dataset), a 73-minute Indian English + Hindi speech dataset (555 clips) with a pipeline that rejects bad audio before any paid transcription call.

---

## Open source

- **Kubeflow Trainer:** [#4166](https://github.com/kubeflow/trainer/pull/4166) e2e test that checks MPI ranks run on both nodes (merged) · [#4199](https://github.com/kubeflow/trainer/pull/4199) fix for the Volcano gang-scheduling docs (merged)
- **Jaeger:** [#9811](https://github.com/jaegertracing/jaeger/pull/9811) (in review)
<!-- TODO: add once the PR number and status are confirmed
- **Volcano:** [#NNNN](https://github.com/volcano-sh/volcano/pull/NNNN) performance fix, 18 ms → 0.72 ms in benchmark (merged / in review)
-->

## Experience

- **Co-founder, Cloutly:** an AI agent for content creators, MVP in beta. Built during the IIMA Ventures AI Summer Residency 2026 (40 selected from 24,503 applicants; Top Performer).
- **Visiting AI/ML Researcher, National Ilan University, Taiwan** (2026)
- **Technical Head, IEEE-CIET Student Branch:** lead 20+ student developers. Built Split or Steal, an event platform that took 10,000+ burst registrations with zero downtime. Led the branch website's migration to Next.js, TypeScript and Supabase.
- **Data Science Intern, Infomo Global**

## Also

- Major in Artificial Intelligence, IIT Ropar
- 9 hackathon wins, including 1st of 436 teams at Swasth-a-thon
- LeetCode Knight: 1,926 rating (top 4%), 550+ problems

## Tools

**Languages:** Python, Go, Java, TypeScript, JavaScript, SQL  
**AI/ML:** PyTorch, OpenCV, LLMs, RAG, multi-agent systems (Google ADK)  
**Backend:** FastAPI, PostgreSQL + pgvector, MongoDB, Redis, Docker, Kubernetes  
**Frontend:** React, Next.js, React Native  
**Cloud:** Google Cloud, Azure

---

Email is the fastest way to reach me: [kavinthakur@gmail.com](mailto:kavinthakur@gmail.com)

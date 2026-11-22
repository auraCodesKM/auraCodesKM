
# Kavin Thakur

Never thought I'd go from debugging college projects to researching computer vision in Taiwan, building AI products at IIM Ahmedabad, and spending an unreasonable amount of time figuring out why something that worked five minutes ago suddenly doesn't.

I'm a third-year B.E. Computer Science (AI & ML) student at Chitkara University, graduating in 2028.

**A little about my journey:**
- **Data Science Intern @ Infomo Global** — My first internship, just after my first semester. My first look at working with production-scale data.
- **Visiting AI/ML Researcher @ National Ilan University, Taiwan** — Four months of computer vision research, living independently in a new country and learning what research looks like beyond the results on a screen.
- **AI Resident '26 @ IIMA Ventures, IIM Ahmedabad** — Selected among 40 from 24,503 applicants. Six weeks of building, talking to potential customers, meeting founders and learning to think beyond the code.

Most of my work sits somewhere between AI/ML and systems engineering: computer vision, LLMs, multi-agent systems, RAG, agentic memory and backend infrastructure.

I'm especially interested in what happens after the demo works: messy data, unreliable model outputs, limited compute and systems that need to hold up in the real world.

**Looking for SWE, AI/ML and research internships for January–June 2027 or Summer 2027.**

[Portfolio](https://kavinthakur.vercel.app) · [LinkedIn](https://linkedin.com/in/kavin070810) · [LeetCode](https://leetcode.com/u/auraCodes/) · [Kaggle](https://www.kaggle.com/kavinthakurkm) · [Hugging Face](https://huggingface.co/auraCodes) · [Email](mailto:kavinthakur@gmail.com)

---

## Projects

A few things I've been building, researching and occasionally debugging at unreasonable hours.

### [JudgeBench](https://github.com/auraCodesKM/judgebench)
`Python` `Google ADK` `Gemini` `PostgreSQL + pgvector` `Google Cloud`

Can a judging system tell the difference between a convincing demo and something that actually works?

- **Problem:** Hackathon judges have minutes per team. Claims like "real time" or "fully tested" often go unchecked.
- **Solution:** Multi-agent evaluation pipeline with a ReAct investigator, majority-of-3 judges and a critic that can only lower scores. Examines repositories, CI and live apps without executing submitted code.
- **Engineering:** Crash-safe state machine with an outbox, one trace per submission, and token, latency and cost tracking per agent call. 52 security tests covering SSRF, archive bombs and prompt injection.
- **Result:** Majority voting reduced score variance from 9.56 to 2.67. Tested on six synthetic repos; first real event pending.

### [AfterCircular](https://github.com/auraCodesKM/AfterCircular)
`Python` `FastAPI` `Azure AI Search` `Next.js`

Regulatory PDFs aren't exactly anyone's idea of a fun afternoon.

- **Problem:** Compliance teams manually read SEBI circulars and compare them against company policies. Relevant obligations can be buried in lengthy documents.
- **Solution:** An AI agent that monitors regulatory circulars, extracts obligations and checks them against company policy repositories using hybrid vector and keyword search.
- **Architecture:** Plug-and-play agency adapters make it possible to switch regulatory sources without changing the core pipeline.
- **Guardrails:** Conflicts require a verbatim regulatory quote and a matching policy chunk. Nothing is filed without human approval.
- **Result:** Deployed on Azure Container Apps (September 2026). Approximately $0.05 to scan six live circulars.

### [BRD Agent](https://github.com/auraCodesKM/brdAgentBackend)
`Python` `LightRAG` `Redis` `Qwen (local)` `WebSockets`

500,000 emails. That's a lot of context to turn into a requirements document.

- **Problem:** Requirements scattered across email threads make it difficult to identify decisions, stakeholders and disagreements.
- **Solution:** Builds a knowledge graph of people, systems and decisions, combines graph and keyword retrieval, reranks results and streams an eight-section BRD to the UI.
- **Engineering:** Routes narrative sections to a 7B model and table-heavy sections to a 32B model to fit within GPU memory constraints.
- **Scale:** Ingested the real Enron corpus of 500,000 emails. Team project at HackFest 2.0 (GDG Cloud New Delhi); this repository contains the backend.

### [PingSight](https://github.com/auraCodesKM/PingSight)
`PyTorch` `OpenCV` `SciPy`

Can you reconstruct a table tennis ball's 3D trajectory from a single broadcast camera? That became one of my favourite research problems.

- **Problem:** Ordinary broadcast footage doesn't provide the multi-camera views typically used for accurate 3D tracking.
- **Solution:** Reconstructs 3D ball trajectories, bounces and landing zones from a single camera using physics-based fitting on top of Kienzle et al. (WACV 2026).
- **Result:** Evaluated on 519 World Tour clips (518 completed). Research conducted at National Ilan University, Taiwan. Results are public; code is private.

### [GitReason](https://github.com/auraCodesKM/gitReason)
`React` `Express` `MongoDB` `Gemini`

I've never liked codebase summaries that confidently describe files that don't exist.

- **Problem:** LLM-generated architecture summaries can hallucinate files and relationships.
- **Solution:** Generates an architecture graph and validates every node against the actual file tree. Invalid nodes are sent back for correction and eventually pruned.
- **Live:** [git-reason.vercel.app](https://git-reason.vercel.app)

**Also:** [sarvam-tts-dataset](https://github.com/auraCodesKM/sarvam-tts-dataset) — a 73-minute Indian English + Hindi speech dataset (555 clips), with a pipeline that rejects bad audio before any paid transcription call.

---

## Open source

Some of my favourite engineering lessons have come from reading code written by people much smarter than me, understanding why things work the way they do, and finding something worth fixing.

- **Kubeflow Trainer:** [#4166](https://github.com/kubeflow/trainer/pull/4166) — E2E test verifying MPI ranks run on both nodes (merged).
- **Kubeflow Trainer:** [#4199](https://github.com/kubeflow/trainer/pull/4199) — Volcano gang-scheduling documentation fix (merged).
- **Jaeger:** [#9811](https://github.com/jaegertracing/jaeger/pull/9811) — in review.

<!-- Add once PR number and status are confirmed:
- **Volcano:** [#NNNN](https://github.com/volcano-sh/volcano/pull/NNNN) — performance fix, 18 ms → 0.72 ms in benchmark.
-->

---

## Experience

- **Co-founder, Cloutly:** Building a WhatsApp-first AI agent for content creators, with persistent memory and a brand-side dashboard. MVP in beta. Built during the IIMA Ventures AI Summer Residency 2026.
- **Visiting AI/ML Researcher, National Ilan University, Taiwan (2026):** Computer vision research, international lab collaboration and volunteering with lab members to introduce elderly residents to AI tools.
- **Technical Head, IEEE-CIET Student Branch:** Lead 20+ student developers. Built Split or Steal, an event platform that handled 10,000+ burst registrations with zero downtime. Led the branch website migration to Next.js, TypeScript and Supabase.
- **Data Science Intern, Infomo Global:** My first internship, just after my first semester. A first look at production-scale data and the people who helped me find my feet in the industry.

---

## Also

- Major in Artificial Intelligence, IIT Ropar
- 9 national hackathon wins, including 1st place among 436 teams at Swasth-a-thon, IIT Delhi
- LeetCode Knight: 1,926 rating (top 4%), 550+ problems

---

## Tools

**Languages:** Python, Go, Java, TypeScript, JavaScript, SQL

**AI/ML:** PyTorch, OpenCV, LLMs, RAG, multi-agent systems (Google ADK)

**Backend:** FastAPI, PostgreSQL + pgvector, MongoDB, Redis, Docker, Kubernetes

**Frontend:** React, Next.js, React Native

**Cloud:** Google Cloud, Azure

---

I tend to have a few things going on at once. If something here interests you, feel free to reach out.

Fastest way to reach me: [LinkedIn](https://linkedin.com/in/kavin070810) or [**kavinthakur@gmail.com**](mailto:kavinthakur@gmail.com).

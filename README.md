# Hi, I'm Shaddar 👋

I build infrastructure and the software that runs on it — AWS, Terraform, Kubernetes, and a lot of Rust. The thread through everything below: I like systems that run themselves, watch themselves, and get better without me babysitting them.

I also take this on as client work → 🌐 **[cloud-lord.com](https://cloud-lord.com)**

Open-source contributor @ **[Djed Alliance](https://github.com/DjedAlliance)**

## What I'm building

### AITA — AI Task Automation *(private, opening up piece by piece)*

The big one. I speak or type a task, and a fleet of AI agents takes it from there: one plans the work, others route it to the right specialist, execute it on my own infrastructure, and record what they learned so the next run is smarter. Under the hood: a Rust + Kafka task scheduler, a tiered knowledge and retrieval layer the agents share, retrieval-quality evals to catch the pipeline lying to itself, and Terraform provisioning every resource it touches — the whole platform rebuilds from scratch. It's private while I pull the operator-specific bits out; the reusable pieces are already split into standalone repos, and they'll go public one by one — the first is below.

### [tf-apply-runner](https://github.com/Shaddar91/tf-apply-runner) — Terraform for your agents, without the token bill

The first AITA piece that's public — the rest are following. A small Rust service that runs Terraform *on behalf of* AI agents: the agent POSTs a directory, gets back a run id, and that's all it ever sees. The full plan/apply log streams to disk instead of into the model's context window, and credentials never touch the agent at all. If you run coding agents against real infrastructure, this is the difference between burning thousands of tokens per apply and burning a few dozen. Ships with an MCP door so your agents can plug straight in.

### [RankLock](https://ranklock.app) *(repos private for now)*

A game-stats platform, built end to end: Rust ingestion pipeline over Kafka, watermark-gated promotion from processing into the serving database, Grafana dashboards managed as code, and privacy designed in from day one — accounts become irreversible HMAC tokens, with an opt-out gate wired into the pipeline itself.

### [Cloud Lord](https://cloud-lord.com)

My consulting practice — AWS platform engineering, migrations, and secure LLM/agent enablement. The [site source](https://github.com/Shaddar91/cloud-lord) and a [demo front end](https://github.com/Shaddar91/cloud-lord-demo-fe) are public.

## 🛠️ Tech I reach for

![Rust](https://img.shields.io/badge/Rust-000000?style=flat&logo=rust&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat&logo=terraform&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=flat&logo=ansible&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white)

## 📊 GitHub

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api?username=Shaddar91&show_icons=true&hide_border=true&theme=tokyonight">
  <img alt="Shaddar91's GitHub stats" src="https://github-readme-stats.vercel.app/api?username=Shaddar91&show_icons=true&hide_border=true">
</picture>

<sub>The stats only count public repos — most of the work above is still private and coming out gradually.</sub>

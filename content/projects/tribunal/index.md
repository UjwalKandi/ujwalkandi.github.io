---
title: "TRIBUNAL: A Machine Court for Production Incidents"
weight: 1
link: "https://github.com/UjwalKandi/tribunal"
linkLabel: "GitHub"
---

![TRIBUNAL Ruling](ruling.png)

- Built an adversarial AI court for production incidents, where Prosecution, Defense, and Judge LLMs argue each fix before a ruling.
- Rulings pass a Flink-enforced human veto window, then become Kafka precedents that future hearings must argue against.
- Developed at the [Cursor Austin × AITX Hackathon](https://aitx-cursor-hackathon-showcase.vercel.app/projects/tribunal) as a successor to [A.I.D.E.](/projects/#aide), using Next.js, TypeScript, Claude structured outputs, Zod, and Supabase pgvector, with cases drawn from real Airflow and dbt failures.

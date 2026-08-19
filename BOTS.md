# Bots of Legal  (docx S5 candidate menu)

These are the **Major sub-functions** of Legal from the spec. Each is a bot — a
child decision system that can be instantiated to do the actual work.

## Install flow (matches the Orientation Protocol)
1. **Orient** — the agent runs the Kojiki Orientation Protocol (name / industry /
   jurisdiction / siblings).
2. **Research** — the agent researches the field and decides which sub-functions this
   specific org needs.
3. **Install** — instantiate only the chosen bots:
   ```bash
   cd bots
   python3 install_bots.py brand growth performance-marketing
   ```
   (use the slugs listed below; omit args to install all). Each installed bot becomes a
   full decision system under `bots/<slug>/` with README + AGENT.md + schemas + a stub
   decision record, and registers under this department's group_id for handoffs.

Total candidates: 8.

- `corporate-legal` — **Corporate Legal**  ·  titles: CLO, General Counsel, Deputy GC, Associate GC, Legal Director, Legal Counsel, Commercial Counsel, Regulatory Counsel, Privacy Counsel, Contract Manager
- `commercial-legal` — **Commercial Legal**  ·  titles: CLO, General Counsel, Deputy GC, Associate GC, Legal Director, Legal Counsel, Commercial Counsel, Regulatory Counsel, Privacy Counsel, Contract Manager
- `regulatory` — **Regulatory**  ·  titles: CLO, General Counsel, Deputy GC, Associate GC, Legal Director, Legal Counsel, Commercial Counsel, Regulatory Counsel, Privacy Counsel, Contract Manager
- `employment` — **Employment**  ·  titles: CLO, General Counsel, Deputy GC, Associate GC, Legal Director, Legal Counsel, Commercial Counsel, Regulatory Counsel, Privacy Counsel, Contract Manager
- `ip` — **IP**  ·  titles: CLO, General Counsel, Deputy GC, Associate GC, Legal Director, Legal Counsel, Commercial Counsel, Regulatory Counsel, Privacy Counsel, Contract Manager
- `privacy` — **Privacy**  ·  titles: CLO, General Counsel, Deputy GC, Associate GC, Legal Director, Legal Counsel, Commercial Counsel, Regulatory Counsel, Privacy Counsel, Contract Manager
- `litigation` — **Litigation**  ·  titles: CLO, General Counsel, Deputy GC, Associate GC, Legal Director, Legal Counsel, Commercial Counsel, Regulatory Counsel, Privacy Counsel, Contract Manager
- `contracting` — **Contracting**  ·  titles: CLO, General Counsel, Deputy GC, Associate GC, Legal Director, Legal Counsel, Commercial Counsel, Regulatory Counsel, Privacy Counsel, Contract Manager

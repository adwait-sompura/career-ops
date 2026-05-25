# Career-Ops — My AI-Powered Job Search Pipeline

Forked from [santifer/career-ops](https://github.com/santifer/career-ops).

## What This Is

I use this system daily to run my job search with AI automation. It turns Claude Code into a full job search command center that:

- **Scans 77+ company job boards** automatically via Greenhouse, Ashby, and Lever APIs -- zero manual browsing
- **Evaluates roles** against my CV with a structured A-G scoring system (10 weighted dimensions)
- **Generates tailored CVs and cover letters** per job description, ATS-optimized
- **Tracks everything** in a single pipeline with integrity checks, dedup, and status normalization
- **Processes in batch** -- evaluate 10+ offers in parallel with AI sub-agents

## How I Use It

I built a custom portal scanner covering 77 API-scannable companies across European FinTech, SaaS, and tech (N26, Scalable Capital, Delivery Hero, FREENOW, Stripe, and 70+ more), with location filtering for Germany/EU and title filtering for PM/BizDev roles.

A typical session:
1. Run the scanner -- it hits all 77 APIs, filters by title and location, deduplicates against history
2. AI agents evaluate the top matches in parallel (full A-G reports with comp research, legitimacy checks, interview prep)
3. Generate tailored application documents for roles scoring 3.5+
4. Track everything in a unified pipeline (225+ roles evaluated so far)

## My Results

- **225+ roles** tracked and evaluated across 121 companies
- **77 companies** with direct API scanning (Greenhouse, Lever, Ashby)
- **300+ evaluation reports** generated with structured scoring
- **Custom location and title filters** for targeted Germany/EU PM search
- **13 applications submitted**, all with tailored CVs and cover letters

## Tech Stack

- **AI Agent:** Claude Code (Opus) for evaluation, document generation, and pipeline management
- **Scanner:** Node.js scripts hitting Greenhouse/Ashby/Lever REST APIs directly (zero LLM cost for scanning)
- **PDF Generation:** Playwright (HTML to PDF)
- **Data:** Markdown tracker + TSV scan history + YAML config
- **Pipeline Integrity:** Automated merge, dedup, status normalization, liveness checks

## Credits

Built on top of the open-source [career-ops](https://github.com/santifer/career-ops) system by [santifer](https://santifer.io). The original system was used to evaluate 740+ job offers and land a Head of Applied AI role. I adapted it for my own search targeting Product Management and Business Development roles in European FinTech.

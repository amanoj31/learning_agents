# AI-CrewAI_Agents 1 — Notebook Summary

Auto-generated summary of notebooks in this course folder. Each entry links to the notebook and gives a top heading with concise bullets describing content.

- L6: [Multi-agent Collaboration for Financial Analysis](L5/L6_collaboration_financial_analysis.ipynb)
  - Top heading: "L6: Multi-agent Collaboration for Financial Analysis"
  - Demonstrates building multiple agents (Data Analyst, Strategy, Execution, Risk) and assembling them into a Crew.
  - Shows how to set up tools (scrapers/search) and delegate tasks for continuous market analysis and execution.
  - Technical details & techniques: Crew composition patterns, agent role design, tool integration (scrapers, web search), structured outputs using Pydantic, example orchestration flows and message passing.

- L3: [Multi-agent Customer Support Automation](L2/L3_customer_support.ipynb)
  - Top heading: "L3: Multi-agent Customer Support Automation"
  - Teaches role design, tools, cooperation, guardrails, and memory for customer support agents.
  - Shows building tasks and QA workflows where agents collaborate to produce and review responses.
  - Technical details & techniques: guardrail patterns, memory usage within agents, QA/verification loops, tool wrapping for ticket ingestion, example Pydantic schemas for structured agent outputs.

- L2: [Create Agents to Research and Write an Article](L1/L2_research_write_article.ipynb)
  - Top heading: "L2: Create Agents to Research and Write an Article"
  - Introduces planner/writer/editor agents and task sequencing for content creation workflows.
  - Demonstrates assembling a Crew that plans, writes, edits, and runs end-to-end content generation.
  - Technical details & techniques: planner/writer/editor flow patterns, sequencing tasks with `Flow`/`Crew`, prompt templates for drafting and revision, example Pydantic models for article outputs.

- L7: [Build a Crew to Tailor Job Applications](L6/L7_job_application_crew.ipynb)
  - Top heading: "L7: Build a Crew to Tailor Job Applications"
  - Shows building a multi-agent pipeline to research job postings and tailor resumes/interview prep.
  - Demonstrates tools for resume reading, scraping, and generating deliverables (resume, interview materials).
  - Technical details & techniques: document parsing tools, resume parsing heuristics, scraper tool examples, structured resume output schemas and multi-agent handoff patterns.

- L5: [Automate Event Planning](L4/L5_tasks_event_planning.ipynb)
  - Top heading: "L5: Automate Event Planning"
  - Focuses on Tasks: creating Pydantic outputs, async tasks, and how to collect structured results (JSON/files).
  - Demonstrates agents for venue coordination, logistics, and marketing with human-in-the-loop options.
  - Technical details & techniques: async task orchestration, Pydantic output models, file/CSV ingestion tools, human-in-the-loop gating and callback patterns.

- L4: [Tools for a Customer Outreach Campaign](L3/L4_tools_customer_outreach.ipynb)
  - Top heading: "L4: Tools for a Customer Outreach Campaign"
  - Covers tool design (versatility, fault tolerance, caching) and integrating custom tools.
  - Demonstrates building lead-profiling and personalized outreach tasks using scrapers and search tools.
  - Technical details & techniques: tool interface design, retry/fallback patterns, caching strategies, example `@tool` wrappers and integration with flow/crew execution.

---


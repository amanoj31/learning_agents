# Course: LLMs as Operating Systems: Agent Memory - https://www.coursera.org/learn/llms-as-operating-systems-agent-memory/home/welcome

# AI-Agent Memory - letta — Notebook Summary

This auto-generated README summarizes notebooks in this course folder. Each entry links to the notebook and lists the top heading and a few concise bullets describing what the notebook teaches.

- Lab 1: [Implementing self-editing memory from scratch](L1/Implementing_Editable_Memory.ipynb)
  - Top heading: "Lab 1: Implementing self-editing memory from scratch"
  - Introduces the MemGPT/self-editing memory pattern and why LLMs can manage memory.
  - Explains the LLM context window structure and where memory sections fit.
  - Implements a memory-editing tool and an agentic loop that performs multi-step reasoning.
  - Technical details & techniques: MemGPT/self-editing memory pattern, memory edit tools (upsert/delete), agentic loop orchestration, context-window slotting, prompt templates for memory operations, simple reducers for state updates.

- Lab 3: [Building Agents with memory](L2/Building_agents_with_Letta.ipynb)
  - Top heading: "Lab 3: Building Agents with memory"
  - Shows how to set up a Letta client and create simple agents with memory blocks.
  - Demonstrates messaging agents, viewing usage, and inspecting agent state and passages.
  - Covers archival memory and how agents can save/retrieve persistent information.
  - Technical details & techniques: `letta` client setup, memory block APIs (create/read/upsert), message formats for agent communication, persistence/backfills for archival memory, examples of agent initialization and state inspection via API calls.

- Lab 6: [Multi-agent Orchestration](L5/Orchestrating_Agents_with_MemGPT.ipynb)
  - Top heading: "Lab 6: Multi-agent Orchestration"
  - Introduces shared memory blocks and creating coordinated agent groups.
  - Shows how to create tools and agent personas for specialized roles (outreach, evaluation).
  - Demonstrates streaming agent messages and round-robin group orchestration.
  - Technical details & techniques: shared memory patterns, persona/tool registration, stream-based message handling, orchestration strategies (round-robin, priority), example tool interfaces and invocation patterns, logging/monitoring usage metrics.

- Lab 5: [Agentic Rag and External Memory](L4/Agentic_RAG_and_Accessing_External_Memory.ipynb)
  - Top heading: "Lab 5: Agentic Rag and External Memory"
  - Demonstrates creating data sources, uploading documents, and attaching sources to agents.
  - Shows linking external data with custom tools and querying attached sources from agents.
  - Covers job monitoring for source uploads and integrating external DB/tool access.
  - Technical details & techniques: RAG integration patterns (ingest → index → attach), document upsert procedures, connector examples for external DBs, tool wrappers to fetch contextual documents, job monitoring and progress-check APIs.

- Lab 4: [Programming Agent Memory](L3/Customizing_memory_management_in_MemGPT.ipynb)
  - Top heading: "Lab 4: Programming Agent Memory"
  - Teaches creating and manipulating memory blocks and retrieving agent state.
  - Implements task-queue memory tools (push/pop) and upserting tools into Letta.
  - Explains how to build more robust memory-management utilities for agents.
  - Technical details & techniques: task-queue memory patterns (push/pop), upsert/downsert semantics, examples of memory indexing and retrieval queries, sample helper functions for memory maintenance and garbage collection.

---



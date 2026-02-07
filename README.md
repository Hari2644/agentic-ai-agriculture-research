# Agentic AI – Agriculture Research Assistant

## Overview
This project demonstrates an Agentic AI system designed to autonomously execute a multi-step research task. Given a high-level user goal, the agent plans the required steps, interacts with external tools, processes retrieved information, and produces a structured output.

The system focuses on reasoning, tool orchestration, and explainability rather than complex model training. It retrieves recent AI research papers related to agriculture, summarizes their abstracts, and stores the results in a structured format suitable for further analysis.
---

## Agent Workflow
1. Interpret the user goal and create a task plan  
2. Retrieve recent research papers using the arXiv public API  
3. Summarize paper abstracts using rule-based logic  
4. Store processed information in structured memory  
5. Return the final organized output  

---

## Tools & Technologies
- **Python** for agent logic and orchestration  
- **arXiv Public API** for accessing recent research papers  
- **Rule-based summarization** for transparent and explainable text reduction  
- **Structured JSON storage** for memory and output representation  

---

## Sample Task
**User Goal:**  
Find the top 3 recent AI research papers on agriculture, summarize them, and store the output in a structured format.

---

## Sample Output
```json
[
  {
    "title": "Shared LoRA Subspaces for almost Strict Continual Learning",
    "published_date": "2026-02-05",
    "summary": "This paper proposes a parameter-efficient continual learning approach that dynamically updates a shared low-rank subspace to integrate knowledge across multiple tasks while minimizing catastrophic forgetting.",
    "link": "http://arxiv.org/abs/2602.06043v1"
  },
  {
    "title": "DyTopo: Dynamic Topology Routing for Multi-Agent Reasoning",
    "published_date": "2026-02-05",
    "summary": "The study introduces a multi-agent reasoning framework that dynamically adapts communication topology using semantic matching, improving coordination and reasoning efficiency across tasks.",
    "link": "http://arxiv.org/abs/2602.06039v1"
  },
  {
    "title": "CommCP: Efficient Multi-Agent Coordination via LLM-Based Communication",
    "published_date": "2026-02-05",
    "summary": "This work presents a decentralized communication framework for cooperative multi-agent systems, leveraging conformal prediction to enhance reliability and coordination efficiency.",
    "link": "http://arxiv.org/abs/2602.06038v1"
  }
]

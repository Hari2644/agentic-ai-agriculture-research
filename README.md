# Agentic AI – Agriculture Research Assistant

## Overview
This project demonstrates an Agentic AI system designed to autonomously execute a multi-step research task. Given a high-level user goal, the agent plans the required steps, interacts with external tools, processes retrieved information, and produces a structured output.

The system focuses on reasoning, tool orchestration, and explainability rather than complex model training. It retrieves recent AI research papers related to agriculture, summarizes their abstracts, and stores the results in a structured format suitable for further analysis.
---

# System Architecture

## Component Description

### 1. User Interface
The user provides a high-level natural language goal describing the task to be performed by the agent.

---

### 2. Agent Planner
The Agent Planner interprets the user goal and decomposes it into a sequence of actionable steps such as searching, summarizing, and storing results. This component enables autonomous task execution.

---

### 3. Tool Executor
The Tool Executor is responsible for invoking internal and external tools required to complete the task.

- **arXiv Search Tool**: Queries the arXiv public API to retrieve recent research papers related to AI and agriculture.
- **Summarization Tool**: Condenses research paper abstracts into concise summaries using rule-based logic.

---

### 4. Memory / Storage Module
This component stores the processed research information in a structured JSON format, simulating agent memory and enabling organized output generation.

---

### 5. Final Output Generator
The Final Output Generator returns the structured research summaries to the user, completing the task workflow.

---

## Design Principles
- Modularity for easy extension
- Explainability through simple, transparent logic
- Clear separation of planning, execution, and storage
- Lightweight implementation suitable for real-world AI systems

-- For Clear view please visit Architecture.png file.

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

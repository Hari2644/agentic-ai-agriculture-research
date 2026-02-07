# Agentic AI – Agriculture Research Assistant

## Overview
This project demonstrates an Agentic AI system designed to autonomously execute a multi-step research task. Given a high-level user goal, the agent plans the required steps, interacts with external tools, processes retrieved information, and produces a structured output. The system focuses on clarity, explainability, and modular design rather than complex model training.

The implemented agent retrieves recent AI research papers related to agriculture, summarizes their abstracts, and stores the results in a structured format suitable for downstream use or analysis.

## Agent Workflow
1. **Goal Interpretation & Planning**  
   The agent receives a natural language goal and decomposes it into a clear sequence of actions.

2. **Research Paper Retrieval**  
   An external search tool queries the arXiv public API to fetch the most recent research papers relevant to AI and agriculture.

3. **Summarization**  
   A lightweight summarization module condenses each paper’s abstract into concise, readable summaries.

4. **Memory & Storage**  
   The processed information is stored in a structured JSON-based format, simulating an agent memory component.

5. **Final Output Generation**  
   The agent returns the organized research summaries as the final result.

## Tools & Technologies
- **Python** for agent logic and orchestration  
- **arXiv Public API** for accessing recent research papers  
- **Rule-based summarization** for transparent and explainable text reduction  
- **Structured JSON storage** for memory and output representation  

## Sample Task
**User Goal:**  
Find the top 3 recent AI research papers on agriculture, summarize them, and store the output in a structured format.

## Output
The agent produces a structured list containing:
- Paper title  
- Publication date  
- Summarized abstract  
- arXiv link  

This project highlights reasoning, tool orchestration, and system design principles relevant to real-world AI agent development.

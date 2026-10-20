# Multi-Agent Research System

An AI-powered research assistant designed to automate information discovery, source analysis, and structured report generation through a multi-agent workflow.

## Overview

Researching a topic often requires searching multiple sources, extracting relevant information, synthesizing findings, and reviewing the final report. Performing these tasks manually can be time-consuming and repetitive.

The Multi-Agent Research System aims to organize this workflow into specialized stages, allowing individual agents to focus on different research responsibilities and work together to produce structured research output.

## Key Features

- **Automated Research:** Accept a research topic and gather relevant information.
- **Web Search:** Discover potentially useful sources for a given topic.
- **Source Extraction:** Retrieve and process information from selected web pages.
- **Report Generation:** Synthesize collected information into a structured report.
- **AI-Based Review:** Evaluate generated reports and identify areas for improvement.
- **Modular Architecture:** Separate research responsibilities into independently maintainable components.

## System Architecture

The intended research workflow follows four stages:

1. **Search Agent** — Finds relevant web sources and gathers search results.
2. **Reader Agent** — Extracts useful information from selected sources.
3. **Writer Agent** — Synthesizes the collected information into a report.
4. **Critic Agent** — Reviews the report and provides feedback.

```text
Research Topic
      |
      v
  Search Agent
      |
      v
  Reader Agent
      |
      v
  Writer Agent
      |
      v
  Critic Agent
      |
      v
 Research Report
```

## Technology Stack

- **Language:** Python
- **AI Orchestration:** LangChain, where used in the implementation
- **Language Models:** Configured LLM provider
- **Information Retrieval:** Web search and web-page extraction tools
- **Environment Configuration:** Python environment variables and `.env`
- **Version Control:** Git and GitHub

## Project Goals

- Build a modular, multi-agent research workflow.
- Explore tool-using AI agents and LLM orchestration.
- Improve the organization and readability of generated research reports.
- Separate information retrieval, synthesis, and evaluation responsibilities.
- Develop a foundation for source-grounded research and report quality evaluation.

## Getting Started

### Prerequisites

- Python version compatible with the project dependencies
- Git
- API credentials required by the configured model and search providers

### Installation

Clone the repository:

```bash
git clone https://github.com/Shreya-1210-del/multi-agent-research-system.git
cd multi-agent-research-system
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

Install the dependencies:

```bash
python -m pip install -r requirements.txt
```

### Environment Configuration

Create a `.env` file in the project root and add the API keys required by the implementation.

Example:

```env
OPENAI_API_KEY=your_api_key
TAVILY_API_KEY=your_api_key
```

Use only the variables required by your configured providers. Never commit real API keys or other secrets to GitHub.

### Run the Application

Use the entry point provided by the repository. For example, if the project contains a Streamlit interface:

```bash
streamlit run app.py
```

Check the project's source files and dependency configuration for the correct entry point and commands.

## Future Improvements

- Source citations and reference validation
- Improved handling of conflicting information
- Structured output schemas for research reports
- Retry handling and clearer error messages
- Unit tests for individual agents and pipeline stages
- Evaluation metrics for report relevance, factual grounding, and completeness
- Deployment with secure environment-variable configuration

## Learning Outcomes

This project provides an opportunity to explore multi-agent system design, prompt engineering, tool integration, information retrieval, report synthesis, and automated evaluation.

## License

Refer to the repository's license file for the applicable license terms.

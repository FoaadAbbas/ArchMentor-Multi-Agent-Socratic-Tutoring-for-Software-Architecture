<div align="center">

# 🎓 ArchMentor

**AI-Driven, Multi-Agent Socratic Tutor for Software Architecture**

[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Naereen/StrapDown.js/graphs/commit-activity)
[![Framework: Multi-Agent](https://img.shields.io/badge/Framework-Multi--Agent-purple.svg)]()

<p align="center">
  Bridging the gap between software design theory and applied engineering through graph-based metrics and Socratic AI mentoring.
</p>

</div>

---

## 📖 Overview

Software engineering students often struggle to design high-quality software architectures. Standard automated tools either provide explicit solutions or rigid error reports, bypassing the student's learning process. 

**ArchMentor** introduces a novel pedagogical approach: a 3-agent LLM system that evaluates architectures using established mathematical graph metrics (e.g., Cohesion, Coupling) and uses **Socratic Mentoring** to guide students toward discovering and fixing architectural flaws on their own.

## ✨ Key Features

* 🤖 **Multi-Agent Collaboration:** A seamless workflow between Requirements, Architecture, and Mentoring agents.
* 📊 **Graph-Based Metric Evaluation:** Translates architectural designs into topological graphs to calculate objective quality metrics (based on academic research by Moran and Naomi).
* 🤔 **Socratic Feedback Loop:** Converts low architectural scores into thought-provoking questions rather than direct answers, fostering critical thinking.
* 📈 **Iterative Learning:** Tracks metric improvements across multiple student iterations to demonstrate tangible progress.

---

## 🧠 System Architecture

The core of ArchMentor relies on a 3-Agent LLM pipeline. 

```mermaid
graph TD
    User([Student / User]) -->|Input System Requirements| A1
    
    subgraph ArchMentor System
        A1[🕵️ Agent 1: Requirements Analyst] -->|Parsed Logical Components| A2
        A2[🏗️ Agent 2: Architecture Generator] -->|Initial Architecture Proposal| GB
        
        GB[(Graph Builder Engine)] -->|Graph Representation| M[Graph Metrics Calculator]
        M -->|Cohesion & Coupling Scores| A3
        
        A3[🦉 Agent 3: Socratic Mentor]
    end
    
    A3 -->|Socratic Questioning| User
    User -.->|Refined Architecture| GB
    
    style A1 fill:#e1f5fe,stroke:#03a9f4,stroke-width:2px
    style A2 fill:#e8f5e9,stroke:#4caf50,stroke-width:2px
    style A3 fill:#fff3e0,stroke:#ff9800,stroke-width:2px
    style M fill:#f3e5f5,stroke:#9c27b0,stroke-width:2px

🛠️ Tech Stack & Technologies

    Language: Python 3.9+

    AI/LLM: Integrated with modern LLM APIs (e.g., Gemini, OpenAI, or local execution)

    Graph Modeling: NetworkX (for modeling components as nodes and dependencies as edges)

    Metrics Engine: Custom Python implementations of academic architectural cohesion metrics.

🚀 Getting Started
Prerequisites

Make sure you have Python installed and an API key for your chosen LLM provider.
Installation

    Clone the repository:
    Bash

    git clone [https://github.com/YourUsername/ArchMentor.git](https://github.com/YourUsername/ArchMentor.git)
    cd ArchMentor

    Install dependencies:
    Bash

    pip install -r requirements.txt

    Configure Environment:
    Create a .env file in the root directory and add your API keys:
    קטע קוד

    LLM_API_KEY=your_api_key_here

    Run the Tutor:
    Bash

    python main.py

💡 Example Socratic Interaction

    System Metric: Module UserAuth has low Cohesion (Score: 0.3).

    Agent 3 (Mentor): "I notice that your UserAuth component is handling both password encryption and sending marketing emails. Based on the Single Responsibility Principle, how might you restructure these tasks to make the system more cohesive?"

🎓 Academic Context

Developed as a B.Sc. Software Engineering final project at Ort Braude College of Engineering by Foaad Abbas. This project integrates academic research on software metrics with advanced AI agent orchestrations to create a scalable, educational tool for future engineers.

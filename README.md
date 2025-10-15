# 🧠 Smart Task Planner

> **AI-powered project planning tool** — automatically breaks down user goals into actionable tasks with dependencies, estimated timelines, and reasoning using LLMs.

---

## 🎯 Objective
The **Smart Task Planner** helps users turn broad goals into structured, actionable task plans.

**Example:**  
> Input: “Launch a product in 2 weeks”  
> Output: A detailed task list with dependencies, priorities, and estimated timelines.

---

## 📘 Scope of Work

**Input:**  
- Goal text (e.g., “Launch a product in 2 weeks”)

**Output:**  
- Actionable tasks with timelines, dependencies, and priorities

**Includes:**  
- Backend API to process and generate plans  
- Optional frontend to submit goals & view generated plans  
- Optional database (SQLite or JSON storage)

---

## ⚙️ Technical Overview

### 🧩 Components

1. **Backend (FastAPI)**
   - Processes input goals and generates task plans.
   - Connects to an LLM (stubbed or API-based).
   - Provides RESTful API endpoints for integration.

2. **LLM Reasoner**
   - Breaks down user goals into tasks.
   - Adds dependencies, durations, and confidence estimates.

3. **Frontend (React)**
   - Simple UI to input goals and display plans.
   - Renders task dependencies and suggested dates.

4. **Storage (Optional)**
   - SQLite or JSON file persistence for generated plans.

---

## 🧠 LLM Usage Guidance

**Prompt Example:**

```text
Break down this goal into actionable tasks with suggested deadlines and dependencies.

Goal: {USER_GOAL}
Deadline: {USER_DEADLINE}

Return valid JSON with:
- id, title, description
- duration_days
- depends_on (list of task IDs)
- priority (low/medium/high)
- start_date, end_date

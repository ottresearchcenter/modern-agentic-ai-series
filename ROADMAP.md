# Agentic AI Series — Complete Roadmap

This repository contains the full roadmap for the "Agentic AI" video series. The series is organized into five phases and 30 short episodes (~15 minutes each). Each episode below includes subtopics, learning objectives, suggested exercises, deliverables, and recommended resources.

---

## Overview

- Total phases: 5
- Episodes: 30 (Ep 1 — Ep 30)
- Target audience: Practicing engineers, AI researchers, and technical leads who want practical agentic AI skills
- Estimated time per episode: 12–20 minutes
- Prerequisites: Familiarity with Python, basic ML/LLM concepts, REST/HTTP, Git, and basic Docker

---

## Phase 1 — Foundations of AI Agents (Ep 1–6)

Goal: Ground learners in the conceptual primitives of agents, UX concerns, and set up a reproducible engineering workspace.

Ep 1 — Series Kickoff & AI Agent Basics
- Subtopics: What is an AI agent; agent vs. model; agent lifecycle; use-cases and examples
- Objectives: Explain agent components (perception, reasoning, action, memory); map use-cases to agent patterns
- Exercises: Identify three agent use-cases in your domain and sketch an agent lifecycle
- Deliverable: Short design write-up (README)

Ep 2 — How AI Agents Think: Perception Loops, Reasoning Chains, and ReAct
- Subtopics: Perception-action loop, chain-of-thought, ReAct (Reason+Act) pattern, prompt engineering for reasoning
- Objectives: Implement a basic perception loop; design prompts for interleaved reasoning and actions
- Exercises: Build a simple ReAct prompt for an information-extraction task
- Deliverable: Notebook with sample prompts and results

Ep 3 — Designing Agent Systems: Architecture & Capability Mapping
- Subtopics: Modular agent architecture, capability surfaces, adapters for tools, API boundaries
- Objectives: Break an agent into modules; design capability map and failure domains
- Exercises: Create architecture diagram for a 3-capability agent (search, execute, summarize)
- Deliverable: Architecture diagram + capability matrix

Ep 4 — User Experience, Trust & Human-in-the-Loop
- Subtopics: Uncertainty communication, confirmation patterns, escalation, consent & privacy basics
- Objectives: Design interaction patterns that convey uncertainty and allow user correction
- Exercises: Mock a dialog flow for a medical/admin assistant with HITL checkpoints
- Deliverable: UX flow and acceptance criteria

Ep 5 — Engineering Workspace Setup
- Subtopics: Reproducible environments, virtualenv/venv, Docker for reproducible runtime, testing basics, CI suggestions
- Objectives: Create a local workspace template with a starter repo and Dockerfile
- Exercises: Initialize `agentic-ai` starter repo; add `requirements.txt` and a sample `Dockerfile`
- Deliverable: Starter repo scaffolding

Ep 6 — Building Your First AI Agent From Scratch
- Subtopics: Minimal viable agent, connectors (web, file), simple tools (calculator, websearch), evaluation criteria
- Objectives: Ship a working end-to-end agent that answers a constrained set of questions using a tool
- Exercises: Implement a minimal agent that uses an LLM + a calculator tool and a small retrieval index
- Deliverable: Working demo + README with run instructions

---

## Phase 2 — Tool Use & Advanced RAG (Ep 7–12)

Goal: Teach tool integration, context management, memory systems, and complete RAG pipelines.

Ep 7 — Supercharging Agents with Tool Use & API Integration
- Subtopics: Tool interface design, safe tool invocation, adapters, rate limits and retries
- Objectives: Design and implement a tool adapter layer and sandboxing strategies
- Exercises: Implement a sample HTTP tool adapter with retries and test harness
- Deliverable: Tool adapter module and tests

Ep 8 — Model Context Protocol (MCP)
- Subtopics: MCP concept, context windows, chunking strategies, context stitching, contextual prompts
- Objectives: Implement a minimal MCP-compatible context manager and API contract
- Exercises: Write an MCP-style context manager for a retrieval pipeline
- Deliverable: MCP spec excerpt + implementation snippet

Ep 9 — Memory Systems: Short-term vs Long-term
- Subtopics: Episodic vs semantic memory, caching strategies, retention policies, eviction and relevance
- Objectives: Design memory tiers and CRUD semantics for long-term store
- Exercises: Build an in-memory short-term memory and a vector-backed long-term memory stub
- Deliverable: Memory API and unit tests

Ep 10 — Vector Databases & Semantic Search
- Subtopics: Embeddings, indexing (ANN), similarity metrics, open-source vs managed vector DBs (FAISS, Milvus, Pinecone, Weaviate)
- Objectives: Connect embeddings to a vector index and evaluate retrieval quality
- Exercises: Create a small vector index for sample docs and compare similarity functions
- Deliverable: Retrieval notebook + evaluation metrics

Ep 11 — Building Full RAG Pipelines
- Subtopics: Chunking, embeddings, caching, reranking, answer generation, end-to-end latency considerations
- Objectives: Build a reproducible RAG pipeline with caching and reranking
- Exercises: Implement a simple RAG flow and measure recall/precision on queries
- Deliverable: RAG pipeline code and performance notes

Ep 12 — Intelligent Agentic RAG & Self-RAG
- Subtopics: Agent-controlled retrieval loops, self-querying agents, dynamic context selection, hallucination mitigation
- Objectives: Combine an agent controller with RAG to select documents adaptively
- Exercises: Implement a self-RAG loop where the agent decides which retriever to call
- Deliverable: Demo script + short filmstrip of decisions

---

## Phase 3 — Orchestration & Multi-Agent Systems (Ep 13–18)

Goal: Cover orchestrators, multi-agent patterns, supervisor patterns, and learning agents.

Ep 13 — Orchestration, Task Delegation & Failure Handling
- Subtopics: Orchestrator responsibilities, retry policies, timeouts, idempotency, backoff strategies
- Objectives: Design an orchestration API and failure handling spec
- Exercises: Create a coordinator that delegates tasks to mock agent workers and collects results
- Deliverable: Orchestration prototype + failure scenarios

Ep 14 — LangGraph & Stateful Orchestration
- Subtopics: State machines vs event sourcing, LangGraph introduction, persistent state across agent runs
- Objectives: Integrate a simple stateful orchestrator for multi-step workflows
- Exercises: Build a LangGraph-like flow that persists state to a lightweight store
- Deliverable: Stateful workflow example

Ep 15 — Multi-Agent Architectures: Supervisor Pattern
- Subtopics: Supervisor vs worker agents, consensus, aggregation, arbitration strategies
- Objectives: Implement supervisor arbitration and result aggregation patterns
- Exercises: Simulate multiple specialist agents and a supervisor that merges outputs
- Deliverable: Supervisor pattern demo and evaluation

Ep 16 — Multi-Agent Research System Project
- Subtopics: Task decomposition, parallel search, ensemble methods, result reconciliation
- Objectives: Build a research agent stack that decomposes a query and merges findings
- Exercises: Implement a multi-agent pipeline for literature review automation
- Deliverable: Research system prototype and README

Ep 17 — Learning Agents: RLHF & Adaptation
- Subtopics: Reinforcement Learning basics, reward shaping, online fine-tuning, safe RLHF practices
- Objectives: Prototype a small RLHF loop for preference learning or ranking
- Exercises: Implement a simulated feedback loop and a simple reward model
- Deliverable: Experimental notebook demonstrating learning curves

Ep 18 — Browser Agents & UI Automation
- Subtopics: Puppeteer/Playwright integrations, security, DOM reasoning, stateful browsing sessions
- Objectives: Build an agent that performs multi-step browser workflows reliably
- Exercises: Create a browser automation agent to fill forms and extract results
- Deliverable: Browser agent script + run instructions

---

## Phase 4 — Enterprise AI (Ep 19–25)

Goal: Scale, evaluate, secure, and monitor agent systems for production.

Ep 19 — AI Evaluation & LLM-as-Judge (Part 1)
- Subtopics: Metrics (accuracy, factuality, usefulness), LLM-as-evaluator patterns, human vs LLM evaluation
- Objectives: Create evaluation harness using an LLM as a judge and cross-check with human labels
- Exercises: Run evaluation on sample outputs and compare scorers
- Deliverable: Evaluation scripts and sample reports

Ep 20 — AI Evaluation & LLM-as-Judge (Part 2)
- Subtopics: Pairwise comparisons, calibration, statistical significance, A/B testing for agents
- Objectives: Implement pairwise evaluation and significance testing for agent variants
- Exercises: Conduct a small A/B test of two prompt/agent variants
- Deliverable: A/B test report

Ep 21 — Observability, Tracing & Cost Monitoring
- Subtopics: Distributed tracing, telemetry for LLM calls, cost attribution, performance SLAs
- Objectives: Instrument an agent pipeline for traces and cost logging
- Exercises: Add tracing to a small pipeline and visualize traces with an open tool
- Deliverable: Trace logs and a short observability dashboard example

Ep 22 — AI Security, Jailbreaking, and Red Teaming
- Subtopics: Adversarial prompts, policy enforcement, sandboxing risky tools, access controls
- Objectives: Define red-teaming procedures and mitigation strategies for agent misuse
- Exercises: Run a moderated red-team against a test agent and document vulnerabilities
- Deliverable: Red-team report and mitigation checklist

Ep 23 — Production Deployment, Scaling & Reliability (Part 1)
- Subtopics: Containerization, autoscaling strategies, stateless vs stateful components
- Objectives: Prepare agents for production deploy with CI/CD and scaling policies
- Exercises: Dockerize agent and create a basic Kubernetes manifest (or docker-compose for smaller scale)
- Deliverable: Deployment artifacts (Dockerfile, k8s example)

Ep 24 — Production Deployment, Scaling & Reliability (Part 2)
- Subtopics: Caching, concurrency limits, graceful shutdown, circuit breakers
- Objectives: Implement resilience patterns and load-test the agent
- Exercises: Add rate limiting and a circuit breaker to tool calls; run a small load test
- Deliverable: Resilience design notes and load-test results

Ep 25 — Human-in-the-Loop Design & Uncertainty Detection
- Subtopics: Confidence scoring, escalate-to-human workflows, annotation tooling, human review UI basics
- Objectives: Design HIL flows and integrate uncertainty detectors into pipeline
- Exercises: Add confidence scoring and an escalation demo to a running agent
- Deliverable: HIL demo and acceptance plan

---

## Phase 5 — Capstone Projects & Career Mastery (Ep 26–30)

Goal: Build full end-to-end agent products and prepare practitioners for real-world delivery and interviews.

Ep 26 — AI Coding Agent Build
- Subtopics: Code understanding, tool execution, repo access, code synthesis/repair loops
- Objectives: Build an agent that can answer coding questions and apply small code edits
- Exercises: Implement a basic code assistant that performs linting and simple fixes
- Deliverable: Code assistant demo + integration notes

Ep 27 — AI Interview Coach Agent Build
- Subtopics: Mock interview flows, scoring rubrics, targeted feedback generation, personalization
- Objectives: Build an interview coach that provides question banks and feedback loops
- Exercises: Create a mock interview harness and scoring model
- Deliverable: Interview coach prototype

Ep 28 — Enterprise AI Assistant with RAG
- Subtopics: Enterprise connectors (databases, docs), security, SSO, enterprise RAG considerations
- Objectives: Ship a secure enterprise assistant with RAG and access controls
- Exercises: Integrate a sample enterprise data source and implement ACL-based retrieval
- Deliverable: Enterprise assistant demo and integration doc

Ep 29 — AI System Design Interview Masterclass
- Subtopics: Design principles, tradeoffs, capacity planning for agents, example interview problems and walkthroughs
- Objectives: Prepare for system-design interviews focused on agentic systems
- Exercises: Solve two end-to-end design prompts and present tradeoffs
- Deliverable: Slide deck + architecture diagrams

Ep 30 — Future of AI Engineering (2026–2027 Roadmap) & AGI Discussion
- Subtopics: Trends, regulation, ethics, AGI perspectives, next skills to learn, career guidance
- Objectives: Synthesize learning path forward and practical next steps for engineers
- Exercises: Create a 12-month personal learning plan and roadmap for team adoption
- Deliverable: Personal/team roadmap template

---

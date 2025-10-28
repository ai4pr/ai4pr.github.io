---
title: "Agentic Concolic Execution"
collection: publications
category: conferences
permalink: /publication/2026-concollmic
date: 2026-05-18
venue: 'IEEE Symposium on Security and Privacy'
paperurl: 'https://srg.doc.ic.ac.uk/files/papers/concollmic-ieee-sp-26.pdf'
---

Concolic execution is a practical test generation technique that explores execution paths by coupling concrete execution with symbolic reasoning. It runs programs on given inputs while capturing symbolic path representations, then mutates and solves these constraints to generate new test inputs for alternative paths. This approach has several fundamental challenges, such as (C1) the inherent complexity of symbolically modeling diverse programming language constructs and environmental interactions, and (C2) the scalability issues of constraint solvers when handling large, complex formulas.
In this work, we investigate whether LLM agents can help address these longstanding challenges in test generation. We propose a novel workflow which we call agentic concolic execution. Using an LLM agent for symbolization, our approach is language-agnostic and can handle environmental constraints without additional manual modeling effort. To ease pressure on the constraint solver, we allow an LLM agent to summarize and even reason about constraints directly in natural language. In a significant evaluation of 12 real-world subjects, our research prototype ConcoLLMic attains significantly higher code coverage (115%-233% higher) than state-of-the-art symbolic executors like KLEE that have been painstakingly hand-crafted over many years, and identifies 11 new vulnerabilities. Our results show that multi-step planning and tool integration enable agents to effectively mitigate reliability issues inherent in LLM-based analysis and even reason symbolically about code.
---
title: "Finding Memory Leaks in C/C++ Programs via Neuro-Symbolic Augmented Static Analysis"
collection: publications
category: conferences
permalink: /publication/2026-memhint
date: 2026-12-10
venue: 'IEEE Annual Computer Security Applications Conference (ACSAC 2026)'
paperurl: 'https://arxiv.org/abs/2603.27224'
---

Memory leaks remain prevalent in real-world C/C++ software. Static analyzers such as CodeQL provide scalable program analysis but frequently miss such bugs because they cannot recognize project-specific custom memory-management functions and lack path-sensitive control-flow modeling.
We present **MemHint**, a neuro-symbolic pipeline that addresses both limitations by combining LLMs' semantic understanding of code with Z3-based symbolic reasoning. MemHint parses the target codebase and applies an LLM to classify each function as a memory allocator, deallocator, or neither, producing function summaries that record which argument or return value carries memory ownership. This extends the analyzer's built-in knowledge beyond standard primitives such as `malloc` and `free`.
A Z3-based validation step checks each summary against the function's control-flow graph, discarding those whose claimed memory operation is unreachable on any feasible path. The validated summaries are injected into CodeQL and Infer via their respective extension mechanisms. Z3 path-feasibility filtering then eliminates warnings on infeasible paths, and a final LLM-based validation step confirms whether each remaining warning is a genuine bug.
On eight real-world C/C++ projects totaling over 3.6M lines of code, MemHint detects **54 unique memory leaks**, all confirmed or fixed, at approximately **$1.7 per detected bug**, compared to 19 by vanilla CodeQL and 3 by vanilla Infer.

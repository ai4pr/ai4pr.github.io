---
title: "Agentic Orchestration for Hybrid Fuzzing"
collection: publications
category: conferences
permalink: /publication/2027-ahfuzz
date: 2027-03-22
venue: 'Network and Distributed System Security Symposium (NDSS 2027)'
paperurl: 'https://srg.doc.ic.ac.uk/files/papers/ahfuzz-ndss-27.pdf'
---

Hybrid fuzzing, which combines the scalability of greybox fuzzing with the precision of symbolic execution, has proven effective in automated software testing. However, contemporary hybrid fuzzers adopt a fuzzer-centric paradigm, where symbolic execution is regarded merely as a reactive fallback when fuzzing plateaus. This coordination often results in biased exploration and inefficient tester interleaving, hindering effective synergy between the two techniques.

In this paper, we propose agentic orchestration for hybrid fuzzing, a new paradigm in which fuzzing and symbolic reasoning operate as equal first-class citizens and are synergized through an LLM agent that serves as the orchestrator. By inspecting testing artifacts and accumulating a testing trajectory, the agentic orchestrator adaptively configures the appropriate tester to reach intermediate milestones. We implement our approach in AhFuzz and evaluate it empirically on 16 real-world subjects. AhFuzz outperforms conventional fuzzers in branch coverage by 84%–166%, and discovers 13 previously unknown vulnerabilities. Up to now, 9 have been fixed or confirmed, resulting in 2 CVE assignments and bounty rewards.

---
title: "Automated Lemma Discovery in Agentic Program Verification"
collection: publications
category: conferences
permalink: /publication/2026-lemmanet
date: 2026-10-12
venue: 'IEEE/ACM International Conference on Automated Software Engineering (ASE 2026)'
paperurl: 'https://arxiv.org/pdf/2603.22114'
---

Deductive verification provides strong correctness guarantees by generating verification conditions (VCs) from a program and its specification and proving them formally. Proving these VCs is the expertise-intensive bottleneck, and LLM-based proof agents have recently begun to automate part of it. However, existing proof agents cannot discover auxiliary lemmas, so they struggle as programs grow larger and more complex.
We argue that proving VCs relies not only on mathematical reasoning but also on understanding the program: human proof engineers draw on program semantics that the output of VC generators does not make visible. Based on this insight, we present LemmaNet, an agent that discovers lemmas in two ways. Offline, it analyzes the source code and specifications to write lemmas and connects them to the verbose VC encoding. Online, it revises existing lemmas as the proof state evolves. LemmaNet is built on the AutoRocq proof agent for Rocq and the Frama-C ecosystem.
We evaluate LemmaNet on SV-COMP and on real-world subjects including Linux kernel modules, Contiki OS, the C++ standard library, and an X.509 parser, where it significantly outperforms state-of-the-art approaches.

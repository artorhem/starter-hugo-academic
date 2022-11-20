---
title: Analysing Snort with KLEE
summary: Understanding usability of KLEE by trying to analyse a large Intrusion Detection System
date: '2018-12-20T13:51:00'
tags:
- Formal Verification
- Systems
- Software Engineering
# Optional external URL for project (replaces project detail page).
external_link: ''

links:
url_code: ''
url_pdf: 'uploads/klee_snort.pdf'
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

Verifying systems code is hard because of concurrency and inherent complexity of
the code. Understanding the invariants and other behavioral and performance
characteristics of a distributed system is challenging because multiple nodes
communicate and coordinate together towards the task of performing a
computation. 

Verification methods and tools implicitly assume that the code to be verified is
deterministic. That is users of the software will provide relevant inputs, and
by verifying program behavior using all possible values of that input, a given
verification methodology can draw inferences about a system. 

In the case of distributed software, the assumption of implicit determinism is
void. Network software typically works in collaboration with other compute nodes
in order to fulfill the required functionality. For example, in a peer-to-peer
system, peers detect node failures using heartbeat messages. Service Oriented
Architecture is another example where a number of services communicate using a
complex chain of RPC calls. Since the underlying communication takes place in
the form of raw packets, often the program behavior can potentially change if
the packets are received out of order or packets are lost in the network.
Therefore, in this context, both the incoming data and the send/receive order
can potentially impact program behavior and consequently increase the complexity
of verification methodology. 

An additional challenge is attributed to concurrency. Most modern systems use
multi-threading to achieve better performance. In such a case, the outcome of a
program is a function of how individual threads are interleaved together.
Reasoning about such interleaved execution paths is hard and adds another layer
of complexity to the process of verification. 

Given the above challenges, we were curious about the usability of existing
symbolic execution tools for verification of system software. In particular, we
were interested in understanding how easy it is to use symbolic execution to
verify systems software that interacts with the networking stack. We, therefore,
analyzed Snort using the popular symbolic execution engine named KLEE. We
documented the challenges that we encountered along the way. We also looked at
recent research papers to understand how they approach the problem of verifying
such code.

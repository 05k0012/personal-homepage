---
layout: post
title: "Governance and Agentic AI in Security Analysis"
date: 2026-04-29
images:
  - /assets/images/AiSlop.png
tags: [ai, governance, security, agentic, grc]
---

In the modern cybersecurity landscape, the conversation is shifting toward governance, risk, and compliance (GRC), specifically regarding how we govern agentic AI models used for security. Having used AI models extensively for security analysis, I have seen the evolution from simple automation to complex, autonomous agents.

## A Brief History of Automated Discovery

To understand where we are, we should look back at the history of automated security vulnerability discovery. Historically, there have been two main types of static analysis tools. The first are basic "grepping" tools that look for patterns. The second are more advanced tools that perform symbolic analysis of code call chains, digging into the underlying low-level architecture of languages like Python to see which C libraries or machine code are called during operations.

Security is built on layers of abstraction. Some tools look at high-level abstractions, while others analyze the low-level details. We have tools for compile-time analysis, runtime analysis, and configuration analysis. With the rise of Infrastructure as Code (IaC), Helm charts, and Kubernetes, we now have a vast set of tools for supply chain and environment configuration.

## The Problem with "Fluff" and the Need for Context

The challenge with these tools is that they often generate "fluff." The results are not always accurate or they are overly verbose. For example, a tool might flag a library that is banned by your company, but a human analyst must assess if it is actually being used in an unsafe way.

Consider a deserialization library like Bouncy Castle. Determining a vulnerability depends heavily on context, such as whether "type name handling" is set, which version is in use, and whether the data comes from an external or internal source. This contextual analysis used to be the primary job of the security researcher.

## The Shift to Agentic AI

When Large Language Models (LLMs) first arrived, we used them to summarize tool outputs and gain context on specific hits. Today, we have moved into agentic AI. These tools can write their own code, create tests, and perform contextual vulnerability discovery.

The role of the security researcher is changing. Instead of driving through mountains of manual output, the researcher now guides agentic AI tools to create that context. The value lies in understanding business impacts and guiding the process, as these agents can be expensive to run if left to spin their own wheels without expert oversight.

## The Governance Issue: Who Owns the Output?

This shift brings up a critical governance issue: who actually owns the output of the tool? If I am guiding an AI-assisted process, who is responsible for the result?

We can view this through a Shared Responsibility Model. If an agentic tool like Claude is used to solve a problem and accidentally deletes a database, who owns that deletion? This is the next frontier of GRC in technology. While laws are being developed to address AI use, my focus is on governance within security analysis itself.

## The Importance of the Skilled User

I believe the best use of these tools is in the hands of a skilled user. Technology is a force multiplier. If you put a race car in the hands of a professional driver, you get high performance. If you put it in the hands of a toddler, the result is very different.

In the modern cybersecurity industry, the value is in the person prompting the tool and interpreting the results. This is the next logical step in our technological evolution. Just as we no longer need to understand internet protocols to browse the web or know how to install an operating system to use a smartphone, we are abstracting the complexities of security analysis. This allows us to work faster and smarter.

## Verifying Truth in the Age of AI

A major part of governance involves understanding where information comes from. When looking at AI output, it is vital to understand its sources and its logic. I personally enjoy using Google Notebooks because it allows me to curate sources and customize the output to a high degree.

As humans, we must audit and analyze the "truth" in these sources. While we will use AI to help audit other AI, the real frontier is distinguishing reality from the confident output of an agent. In vulnerability analysis, accuracy is everything.

At work, we are currently leveraging these tools to rapidly prototype proof of concepts (PoCs) against test environments. By allowing the AI to show proof that its proposed hypothesis is correct, we turn theoretical vulnerabilities into verified findings. This technology, in the right hands, is the next step toward a much more productive and secure future.

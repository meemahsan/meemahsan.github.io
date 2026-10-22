---
layout: post
title: "The Data Scientist’s Job Is Changing. What Should We Teach Our Teams?"
subtitle: ""
date: 2026-10-04
---

## Introduction

For years, the data science career path was relatively easy to describe. Learn statistics, build strong programming skills, understand machine learning, develop models, and learn how to deploy them.

Those fundamentals still matter. But the way we do the work is changing rapidly

Generative AI can help write code, explain unfamiliar libraries, generate SQL, summarize documents, and accelerate prototyping. Agentic systems are beginning to connect reasoning with tools and workflows. Tasks that once took hours can sometimes be completed in minutes.

That creates a new question for data science leaders:

**If AI changes how the work gets done, what should we teach our teams to become better at?**

I don't think the answer is simply prompt engineering or learning the latest framework. Those skills can be useful, but tools change quickly. The more important goal is to develop data scientists who can use AI effectively while still exercising sound technical and business judgment.

## 1. Teach AI Fluency, Not Just AI Tool Usage

Knowing how to use an AI assistant is becoming useful across many roles. But AI fluency is much more than knowing which prompts to write.

A strong data scientist should understand:

- Which tasks are good candidates for AI assistance.
- How to provide the right context and constraints.
- How to verify generated code, analysis, and explanations.
- Where hallucinations, bias, and missing context can affect results.
- What information should never be shared with an unapproved tool.
- When a conventional/traditional method is simpler, cheaper, or more reliable.

The objective isn't to make AI responsible for the work. It's to help people use AI to do better work.

For example, an AI assistant can generate a first version of a feature engineering pipeline. But the data scientist still needs to understand leakage, training-serving skew, data quality, and whether the features are available at prediction time.

AI can accelerate implementation. It doesn't remove the need to understand what we are implementing.

## 2. Teach Problem Formulation Before Solution Building

One of the most valuable skills in data science has always been translating an ambiguous business question into a problem that can be solved.

This skill is still needed even with AI assisted solutions.

When building becomes easier, it becomes tempting to start with a technology: an LLM, an agent, a vector database, or a new orchestration framework.

But the right starting point is still the business problem.

Are we trying to predict an outcome? Rank a set of options? Explain a decision? Recommend an action? Automate a workflow?

These are different problems, and they may require very different solutions.

Consider a sales team that wants to know which accounts to prioritize. A propensity model might estimate which accounts are most likely to convert. A ranking model might optimize the order in which sellers see those accounts. An LLM might summarize recent interactions or explain why an account is relevant. An agent might coordinate the next steps across multiple systems.

Those technologies can complement one another, but they are not interchangeable.

Data scientists should be able to explain **what decision we are improving, who will use the result, and what action should change because of it** before they start choosing tools.

## 3. Teach Evaluation as a Core Skill

AI makes it easier to produce something that looks convincing. It does not automatically make it easier to know whether that thing is correct.

This is particularly important with generative AI and agentic systems, where a small set of impressive examples can create a misleading sense of confidence.

Data scientists need to know how to evaluate systems systematically.

For traditional machine learning, that includes choosing appropriate metrics, validating on realistic data splits, checking calibration, and understanding performance across segments.

For LLM-based systems, evaluation may include factual accuracy, relevance, groundedness, consistency, and task completion.

For agents, the evaluation problem becomes broader. Did the agent choose the right tool? Did it follow the correct sequence? Did it respect permissions? Did it recover from an error? Did it complete the task without taking an unauthorized action?

And across all of these approaches, we still need to ask whether the solution improves the business outcome.

A system can perform well on a technical benchmark and still fail to improve a real workflow.

I would rather have a team that knows how to design a meaningful evaluation than a team that can build ten impressive demos without knowing how to compare them.

## 4. Teach Systems Thinking, Not Just Model Building

A model is only one component of a production data science solution.

Real systems depend on data pipelines, feature availability, APIs, security, latency, monitoring, user interfaces, feedback loops, and operational ownership. AI applications add more considerations, including model selection, retrieval, tool permissions, context management, and the cost of repeated inference.

Data scientists don't need to become experts in every engineering discipline. But they do need to understand how their work fits into the larger system.

They should be able to ask:

- Where does the data come from, and how fresh is it?
- What happens when a dependency fails?
- How will we monitor quality after deployment?
- How will we know when the system needs to be updated?
- What is the fallback when the AI component cannot complete the task?
- Who owns the system after the initial launch?

This is the difference between building a model and helping deliver a dependable product.

As AI makes prototyping faster, the ability to reason about the whole system—not just the model or prompt—becomes increasingly valuable.

##  5. Teach Domain Knowledge and Decision Science

There is a risk that as AI tools become more capable, we will overvalue the ability to generate code and undervalue the knowledge needed to ask the right questions.

In enterprise data science, context matters.

A technically strong recommendation can still be wrong for the business if it ignores how decisions are made, what constraints users operate under, or what outcomes the organization actually values.

For example, a sales recommendation system shouldn't simply identify accounts with a high probability of conversion. It may also need to consider account eligibility, product fit, timing, seller capacity, existing relationships, and the incremental value of taking action.

The question isn't only, “Can we predict what will happen?”

It is also, “What should we do, and what is likely to happen if we do it?”

That requires knowledge of the business, decision science, experimentation, and causal reasoning—not just a more powerful model.

Data scientists should be able to understand the workflow their solution is changing and the incentives of the people who will use it. That context is often what separates a technically interesting solution from one that gets adopted.

##  6. Teach Communication, Influence, and Ownership

As AI systems become more complex, explaining their behavior becomes more important—not less.

Data scientists need to communicate eloquently and with clarity, what a system does, what evidence supports its output, where it can fail, and what level of trust is appropriate.

They also need to work across functions. A production AI solution may involve engineering, product, security, legal, compliance, operations, and business stakeholders. No single team can make all of those decisions in isolation.

The ability to ask good questions, explain trade-offs, challenge assumptions, and build shared understanding is a technical advantage in its own right.

Ownership matters, too. A data scientist should be following the work beyond model development: into evaluation, deployment, adoption, monitoring, and measuring impact.

The deliverable isn't always a model or a notebook. It may be a better decision, a more useful workflow, or a system that helps people do their jobs more effectively.

## 7. Change How We Develop Our Teams

If these are the skills that matter, our development plans need to reflect them.

I would focus on a few practical changes:

**Create room for structured experimentation.** Give team members time to explore AI tools, but ask them to bring back evidence: what task improved, what risks appeared, and whether the improvement is worth adopting.

**Use real business problems as learning opportunities.** Instead of running training exercises disconnected from daily work, let people evaluate AI against familiar workflows and measurable outcomes.

**Share learning across the team.** One person can investigate evaluation methods while another explores retrieval or agent orchestration. Short demonstrations and written playbooks can spread useful knowledge without requiring everyone to study every new tool.

**Reward judgment, not just speed.** Recognize people who identify a simpler solution, catch a failure mode, improve an evaluation, or decide not to use AI when it doesn't add value.

**Keep the fundamentals strong.** Statistics, experimental design, data quality, software engineering, and critical thinking remain essential. AI changes how we apply these skills; it doesn't make them irrelevant.

This approach also helps avoid turning continuous learning into continuous tool switching. The objective is not to chase every new release. It is to learn deliberately and apply what matters.

##  The Skills That Matter Next

The World Economic Forum's *Future of Jobs Report 2025* highlights both technological skills and human capabilities—including analytical thinking, creative thinking, resilience, leadership, and curiosity—as important to the changing world of work. That combination makes sense to me.

Data science teams need technical depth. They also need people who can reason through ambiguity, work with others, understand consequences, and keep learning as the tools change.

We shouldn't frame this as a choice between technical skills and human skills. The strongest teams will combine both.

AI can help us write code faster, explore more ideas, and build new kinds of systems. But someone still has to decide which problem matters, determine whether the output is trustworthy, understand the operational consequences, and make sure the solution creates value.

Those responsibilities are not going away. In many cases, they are becoming more important.

## Final Thought

I don't think the goal is to train data scientists to compete with AI at every task.

The goal is to help them become better at the work around the task: framing the problem, selecting the right approach, evaluating the result, understanding the business context, and taking responsibility for what reaches production.

The tools will continue to change. The fundamentals of good data science—curiosity, rigor, critical thinking, and a focus on meaningful outcomes—will remain.

As leaders, our job is to help teams adapt without losing those fundamentals.

**The future data scientist won't just be someone who knows how to use AI. It will be someone who knows when to use it, how to evaluate it, and what is worth building in the first place.**

## Sources

- World Economic Forum. [*The Future of Jobs Report 2025: Skills Outlook*](https://www.weforum.org/publications/the-future-of-jobs-report-2025/in-full/3-skills-outlook/). Discusses the combination of technological, analytical, creative, and interpersonal skills expected to matter in the evolving workforce.
- Microsoft and LinkedIn. [*2024 Work Trend Index: AI at Work Is Here. Now Comes the Hard Part*](https://www.microsoft.com/en-us/worklab/work-trend-index/ai-at-work-is-here-now-comes-the-hard-part). Examines AI adoption at work and the challenge of translating individual productivity gains into business impact.

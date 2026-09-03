---
layout: post
title: "Why Your AI Agent Still Needs Traditional Machine Learning"
subtitle: "Why predictive ML still matters in the age of LLMs and AI agents"
background: '/img/posts/Automl/automl_background.jpg'
---
## Introduction
Over the last couple of years, I have heard some version of the same question repeatedly:

**Do we still need traditional machine learning now that we have LLMs and AI agents?**

It is a fair question.

Large Language Models can reason over unstructured information, summarize thousands of words, generate recommendations, interact with tools, and increasingly take actions on behalf of users. Add an agentic layer, and suddenly we are talking about AI systems that can plan, retrieve information, call APIs, evaluate results, and decide what to do next.

Compared to that, a propensity model predicting a number between 0 and 1 can feel almost... boring.

But boring does not mean obsolete.

In fact, as we build more sophisticated AI systems, I think traditional machine learning becomes **more important, not less**.

The role simply changes.

## LLMs Are Great at Reasoning. ML Is Great at Prediction.
Consider a fairly common B2B sales problem.

You have 100,000 accounts and 2,000 sellers.

The business wants to answer three questions:

**Who should I contact?**

**What should I talk to them about?**

**What should I do next?**

It is tempting to hand all three questions to an AI agent.

Give the agent CRM data, product information, intent signals, past interactions, maybe some call transcripts, and ask:

> "Find the best opportunities for this seller today."

Technically, you could build something like this.

But should you?

Probably not.

Imagine asking an LLM to individually reason through 100,000 accounts every night to determine which customers are most likely to buy.

That is an expensive way to solve a problem that machine learning has been solving very well for years.

A propensity model can score those accounts quickly and consistently.

Now instead of asking the agent to search through 100,000 accounts, we can give it the top 50.

This is where the architecture becomes interesting.

The machine learning model does not disappear.

It becomes part of the intelligence available to the agent.

## Prediction and Reasoning Are Different Jobs
Traditional machine learning is particularly good when the question looks something like:

> Given everything we know about this account, how likely is event X?

Will the customer buy?

Will they churn?

Will they respond?

Which product are they most likely to purchase?

Which lead should receive the highest priority?

These are prediction and ranking problems.

And we have spent decades developing algorithms that are extremely good at them.

XGBoost does not suddenly become useless because GPT exists.

Neither does logistic regression.

Neither do recommendation systems, clustering algorithms, forecasting models, optimization techniques, or anomaly detection.

LLMs solve a different class of problems particularly well.

They are good at understanding context.

They can interpret language.

They can synthesize information from multiple sources.

And increasingly, they can reason about what action should happen next.

That leads to a simple way of thinking about the relationship:

**Machine learning predicts.**

**LLMs understand and reason.**

**Agents orchestrate and act.**

The most interesting enterprise AI systems will probably use all three.

## Think About the Agent as an Orchestrator
This is where I think the conversation around AI agents sometimes goes wrong.

We often imagine the agent as the intelligence that replaces everything underneath it.

I think a better mental model is an **orchestration layer**.

The agent does not necessarily need to calculate everything itself.

It needs to know which intelligence to use.

Imagine a seller asks:

> "Who should I call this morning?"

An agent could potentially do something like this:

1. Retrieve the seller's territory and eligible accounts.
2. Call a propensity model to identify accounts with high purchase likelihood.
3. Check intent signals to identify accounts actively researching relevant topics.
4. Look at CRM activity to remove accounts that were contacted yesterday.
5. Retrieve recent emails, call notes, or transcripts for the highest-priority accounts.
6. Use an LLM to understand the context around those accounts.
7. Recommend the best five opportunities.
8. Explain why each opportunity matters.
9. Suggest the next action.
10. Potentially draft the outreach.

Look closely at that workflow.

The LLM is doing something extremely valuable.

But it is not doing everything.

Traditional ML is helping narrow the decision space.

Rules are enforcing business constraints.

Retrieval is providing context.

The LLM is interpreting that context.

And the agent is coordinating the entire process.

That is a much more powerful system than simply asking an LLM:

> "Who should this seller call?"

## Traditional ML Gives Agents Something They Desperately Need: Signal
Enterprise data is noisy.

There may be hundreds or thousands of attributes associated with a customer.

Firmographics.

Transaction history.

Product ownership.

Web activity.

Marketing engagement.

Intent signals.

Seller activity.

Historical opportunities.

Support interactions.

Usage patterns.

An LLM can consume some of this information.

But that does not mean it should be responsible for discovering every statistical relationship buried inside it.

Suppose historical data shows that companies exhibiting a specific combination of product usage, company size, purchase history, and engagement behavior are three times more likely to buy Product B.

A machine learning model can learn that pattern from millions of historical observations.

That prediction becomes a very useful signal for an agent.

Instead of replacing predictive intelligence, the agent can **consume predictive intelligence**.

This distinction matters.

## Agents Can Also Make Machine Learning More Useful
The relationship works in the other direction too.

One of the long-standing problems with predictive models is that a prediction alone is often not enough.

Imagine telling a seller:

> Account A has an 87% likelihood of purchasing Product X.

Okay.

Now what?

Why?

What happened?

Who should I contact?

What should I say?

What information should I review before making the call?

This is where LLMs and agents can dramatically improve the usefulness of traditional ML.

The model identifies the opportunity.

The LLM can help explain the context.

The agent can help determine the next action.

Suddenly a prediction becomes something closer to a decision-support system.

Instead of:

**"This account has a high propensity."**

We can move toward:

**"This account has a high propensity for Product X. Their recent activity suggests increased interest in Y, they currently use Product Z, and there has been no seller interaction in the last 30 days. Here are the two people you may want to contact, and here is a suggested conversation starter."**

That is a very different user experience.

But notice what happened.

We did not replace the propensity model.

We made it more useful.

## Not Everything Needs an LLM
There is another reason traditional ML will remain important.

Cost.

Latency.

Consistency.

If I need to score ten million records every night, I probably do not want ten million LLM calls.

If I need a prediction in 20 milliseconds, I may not want an agent reasoning through five different tools.

If I need the same input to reliably produce the same risk score, deterministic or probabilistic models may be preferable.

And if I need to monitor model performance over time, traditional ML gives us a mature ecosystem for doing that.

This is why architecture matters.

The goal should not be:

**Where can we use an LLM?**

The better question is:

**What is the simplest technology that solves each part of the problem well?**

Sometimes that is an LLM.

Sometimes it is an agent.

Sometimes it is XGBoost.

Sometimes it is SQL.

And sometimes it is a business rule that says, "Do not recommend this account because another seller already owns the opportunity."

That is okay.

Good AI architecture is not measured by how much AI you managed to put into it.

## The New AI Stack
I increasingly think of enterprise AI as a layered system.

At the bottom, we still have the **data layer**.

Customer data.

Transactions.

CRM.

Digital activity.

Intent.

Product usage.

Documents.

Emails.

Call transcripts.

On top of that, we have different forms of intelligence.

**Predictive ML** answers questions about likelihood and ranking.

**Recommendation systems** help determine relevance.

**Optimization** helps allocate scarce resources.

**LLMs** interpret language and context.

**Retrieval systems** bring the right information into the decision.

**Rules and guardrails** enforce constraints.

And then the agent sits across these capabilities, deciding which tools to use and in what sequence.

The architecture starts looking less like:

**LLM → Answer**

and more like:

**Data → Models + Tools + Knowledge → Agent → Decision → Action**

That, to me, is where enterprise AI becomes much more interesting.

## What Does This Mean for Data Scientists?
If you are a traditional data scientist looking at the explosion of Generative AI and wondering whether everything you learned is becoming irrelevant, I would argue the opposite.

Understanding machine learning gives you an enormous advantage when building agentic systems.

You understand training data.

You understand leakage.

You understand evaluation.

You understand the difference between correlation and causation.

You understand why a model that performs beautifully in a notebook can fail spectacularly in production.

You understand monitoring.

You understand experimentation.

And hopefully, you have developed a healthy skepticism toward impressive demos.

Those skills transfer remarkably well to the world of agents.

The new skill is learning how to combine them with LLMs, retrieval, tools, memory, orchestration, and evaluation.

The future data scientist may spend less time asking:

> "Which algorithm should I use?"

And more time asking:

> "Which combination of intelligence should solve this problem?"

That is a much bigger question.

## Traditional ML Is Not Going Away. It Is Becoming a Tool.
When calculators arrived, mathematics did not disappear.

When cloud computing arrived, databases did not disappear.

New layers of abstraction tend to change how existing technologies are used rather than eliminating them entirely.

I think something similar is happening with machine learning.

For years, the model was often the center of the data science solution.

We collected data.

We engineered features.

We trained the model.

We deployed it.

We returned a prediction.

In an agentic system, the model may no longer be the center.

It becomes one of several specialized tools available to a larger intelligent system.

And I actually think that makes traditional machine learning more valuable.

Because the question is no longer whether a model can produce a good prediction.

The question becomes:

**Can we take that prediction, combine it with context, reason about it, and turn it into the right action?**

That is the transition I find most interesting.

We are moving from systems that **predict**...

to systems that **recommend**...

to systems that **decide**...

and eventually, systems that **act**.

Traditional machine learning is not being left behind in that transition.

It is coming along for the ride.

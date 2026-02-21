# 🧪 AI Placebo Differential

> *"Can't ChatGPT just do this?"*  
> This framework gives you a structured, measurable answer.

![Status](https://img.shields.io/badge/status-draft%20v1.0-yellow)
![License](https://img.shields.io/badge/license-MIT-green)
![Contributions](https://img.shields.io/badge/contributions-welcome-blue)

---

## What Is This?

When AI applications are shown to users or investors, one of the first questions usually asked is: *"Can't ChatGPT do this directly?"*

This framework is a structured answer to that question. It provides a way to measure the differences between a default ChatGPT output and an application's output and experience. The metrics are aimed at measuring the unique value that the application provides — in terms of the creator's custom knowledge inputs, the user experience, and the amount of effort in terms of tokens and steps that would be needed to recreate the same result using plain ChatGPT.

But there's an important nuance: it's not just that ChatGPT *can't* do it — it's that even if it theoretically could, the user would need to supply all the context themselves, structure the prompts correctly, iterate manually, manage token limits, and stitch together multiple steps by hand. A well-designed AI application does all of that work invisibly. That invisible effort is a core part of the value being measured.

The **AI Placebo Differential** is the quantified gap between the two.

---

## The Scoring Rubric

Each model or application is scored across five metrics on a 1–5 scale. With equal weighting, the final score is the average across all five dimensions. The difference between the two final scores is the **Placebo Differential**.

| Metric | Raw ChatGPT / Claude | Your AI Application |
|---|---|---|
| Accuracy | | |
| Usability | | |
| Reliability | | |
| Agentic Chain Quality | | |
| Token Efficiency | | |
| **Final Score** | | |
| **Placebo Differential** | ← difference | |

---

## Metric Definitions

### 1. 🎯 Accuracy
How well does the output address the user's actual need?

Raw models are limited to their training data. An AI application improves accuracy by injecting domain-specific documents and knowledge bases, expert experience and curated rules, and real-time or proprietary data — things the user would otherwise have to paste in manually every single time.

> *Example: A legal AI application embedding case law, firm-specific guidelines, and lawyer expertise will produce far more accurate advice than raw ChatGPT given the same question with no context.*

---

### 2. 🖥️ Usability
Does the interface enhance the experience beyond a basic chat interaction?

Raw LLMs are mostly text in, text out. AI applications add value through interactive visual interfaces, guided workflows, structured outputs, dashboards, and domain-specific navigation. The output format matters — a well-designed application delivers information in the way users actually need to consume and act on it.

> *Example: An application that reverse engineers a codebase and presents the architecture as an interactive visual diagram scores far higher on usability than a raw model returning a wall of text.*

---

### 3. 🔁 Reliability
Does the application produce consistent, repeatable outputs?

Raw LLMs are probabilistic and prone to hallucination. Applications improve reliability through Retrieval-Augmented Generation (RAG) that grounds responses in verified sources, output validation and guardrails, and structured prompting that constrains the response format. Run the same query twice in ChatGPT and you may get meaningfully different answers. A well-built application shouldn't behave that way.

---

### 4. 🔗 Agentic Chain Quality
*Applies to agentic applications.*

Agentic applications execute tasks through a sequence of steps, where each step's output feeds into the next. This introduces both risk and significant opportunity.

**The risk:** errors compound. A small inaccuracy early in the chain can degrade the final output significantly.

**The opportunity:** the final output of a well-designed agentic application will look dramatically different from — and far superior to — a single-shot raw model response. That deviation *is* the value. Recreating it manually in ChatGPT would require the user to run each step themselves, evaluate intermediate outputs, and manage the flow — which is precisely the work the application is doing for them.

Evaluation here should be goal-based rather than comparative — score both outputs against what the user was trying to achieve, not against each other.

---

### 5. ⚡ Token Efficiency
How economically does the application achieve its output?

Token usage measures both capability and cost-effectiveness. A well-designed application achieves equal or better results with fewer tokens through smart chunking, RAG that retrieves only relevant context, and agentic steps that build knowledge incrementally.

**The critical insight:** sometimes a raw model simply *cannot* accomplish a task within normal token limits — making the application not just better, but the only viable solution at scale.

> *Example: [revibe.codes](https://revibe.codes) reverse engineers codebases to produce interactive system design and architecture documentation. Dumping an entire large codebase into Claude or ChatGPT on a standard account may not be feasible at all. revibe.codes processes the codebase agentically in intelligent chunks, makes the task feasible, and delivers an interactive visual result — not just text.*

---

## Evaluation Methodology

### How to Run an Evaluation

1. **Define the task** — Choose a representative task for the application's domain. Define what a successful output looks like.
2. **Run both** — Tab 1: the raw model. Tab 2: the AI application. Same query, same goal.
3. **Capture outputs** — Use browser-based tools such as the [Claude Chrome Extension](https://claude.ai) or AI-native browsers like Comet to observe and capture outputs from both tabs side by side.
4. **Score with a judge model** — Feed both outputs to an LLM judge with a structured evaluation prompt based on this rubric. The judge scores each metric independently.
5. **Compute the differential** — Average the scores across all five metrics for each. The difference is the Placebo Differential.

### Two Evaluation Modes

| Mode | When to Use |
|---|---|
| **Comparative** | Simpler apps where outputs are similar enough to compare directly |
| **Goal-based** | Agentic apps where outputs diverge significantly — evaluate both against the intended goal, not each other |

---

## Example: revibe.codes

| Metric | Raw Claude | revibe.codes |
|---|---|---|
| Accuracy | Medium | High |
| Usability | Low (text only) | High (interactive visual) |
| Reliability | Medium | High |
| Agentic Chain Quality | N/A | High |
| Token Efficiency | Low / Not feasible | High |
| **Final Score** | ~2.5 / 5 | ~4.5 / 5 |

**Placebo Differential: ~2.0** — the application delivers approximately twice the value of the raw model, and completes a task the raw model cannot do at all within standard token limits.

---

## Roadmap

- [x] Define the framework and metrics
- [x] Publish README
- [ ] Publish scoring prompt templates for LLM judge evaluation
- [ ] Build browser extension for side-by-side evaluation
- [ ] Build scorecard output with automated Placebo Differential scoring
- [ ] Domain-specific rubric templates (legal, healthcare, finance, developer tools)

---

## Contributing

This is an early-stage, open framework and contributions are very welcome.

- Found a metric that's missing? Open an issue.
- Have a real-world example to add? Submit a PR.
- Building the evaluation tool? Let's talk.

---

## License

MIT — free to use, adapt, and build on.


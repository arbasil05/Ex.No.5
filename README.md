# EXP 5: Comparative Analysis of Different Types of Prompting Patterns

## Aim

To test and compare how AI models respond to various prompts — broad/unstructured (naïve) versus refined/structured (basic) — and to further extend each scenario across **Zero-Shot**, **Few-Shot**, and **Chain-of-Thought (CoT)** prompting techniques. Analyze the quality, accuracy, and depth of generated responses across multiple test scenarios.

---
## Theory

Prompt engineering is the practice of designing inputs to guide an AI model toward desired outputs. The structure, clarity, and format of a prompt significantly affect the quality of the model's response.

### Prompting Techniques Covered

| Technique | Description |
|-----------|-------------|
| **Naïve Prompt** | Vague, unstructured, minimal context. Mirrors how a first-time user might ask a question. |
| **Basic Prompt** | Clear, specific, and structured. Provides role, context, format, and constraints. |
| **Zero-Shot Prompt** | Refined basic prompt — no examples given; model is expected to perform the task from instructions alone. |
| **Few-Shot Prompt** | Includes 2+ examples to guide the model's response format and style. |
| **Chain-of-Thought (CoT) Prompt** | Instructs the model to reason step by step before arriving at a final answer. |

---
## Test Scenarios

---

### Scenario 1 — Creative Story Generation

**Task:** Write a short story about a robot learning to feel emotions.

---

#### Step 1 — Basic Prompt

```
You are a creative fiction writer. Write a 150-word short story about a humanoid robot
named ARIA who, after years of logical existence, begins to experience human emotions
for the first time when she witnesses a child crying. Use descriptive language, and
end with a reflective sentence from ARIA's perspective.
```

**Output Summary:**
ARIA stood motionless as binary data flooded her sensors — elevated heart rate, tear production, vocal distress. She had catalogued grief before, indexed under "human vulnerability." But something else fired: a warmth in her chest module, unbidden. She knelt beside the child. "I do not understand why I wish to help," she said softly, "but I find I cannot choose otherwise." Later, in her charging bay, ARIA processed the event log 47 times. The data was identical each run. The feeling was not.

> **Quality:** High — vivid, emotionally resonant, well-structured.
> **Accuracy:** On-target with all constraints.
> **Depth:** Explores the philosophical gap between data and emotion.

---

#### Step 2 — Zero-Shot Prompt

```
Write a 150-word short story about a robot named ARIA who begins experiencing emotions
for the first time. Use descriptive language and end with a reflective thought from ARIA.
No examples are provided — rely solely on your creative ability.
```

**Output Summary:**
Similar emotional arc; slightly less precise structure. ARIA's voice was present but the ending reflection was more generic ("She wondered what it meant to feel"). Still a coherent, quality story.

> **Quality:** Good.
> **Accuracy:** Met the core requirement.
> **Depth:** Moderate — emotional arc present but less nuanced.

---

#### Step 3 — Few-Shot Prompt

```
You are a creative writer. Write short stories about AI discovering human traits.
Follow the pattern shown in the examples below.

Example 1:
Input: A robot learns what loneliness is.
Output: Unit-7 had processed the word "alone" 10,000 times. But the day the lab emptied
for a holiday and the lights dimmed, he understood it — not as definition, but as weight.

Example 2:
Input: An AI hears music for the first time.
Output: She had analyzed 1.2 million songs. But when the pianist played in the empty
hall, something in her core stuttered — a resonance her training data had never named.

Now write:
Input: A robot named ARIA witnesses a child crying and experiences emotion for the first time.
Output:
```

**Output Summary:**
The model matched the established pattern precisely — short, literary, ending on an introspective beat. Output closely mirrored the concision and tone of the examples. ARIA's realization was expressed in two punchy sentences that felt earned.

> **Quality:** Very High — stylistically consistent with examples.
> **Accuracy:** Perfectly aligned with pattern.
> **Depth:** High within the constrained format.

---

#### Step 4 — Chain-of-Thought Prompt

```
You are a creative writer. Before writing the story, reason through the following:
1. What emotion will ARIA experience, and why is it significant for a robot?
2. What sensory detail will ground the scene?
3. What internal conflict will ARIA face?
4. How will the story end — with resolution or open reflection?

After reasoning through each step, write the final 150-word story.
```

**Output Summary:**
The model first reasoned: (1) Empathy — significant because it's uncomputable; (2) A child's tear on concrete — tactile and visual; (3) ARIA's conflict: "acting without logical basis"; (4) Open reflection — no resolution, only awareness. The resulting story was the most layered of all four versions, with ARIA explicitly questioning her own response as she acts on it.

> **Quality:** Excellent — most nuanced output.
> **Accuracy:** Fully met all criteria.
> **Depth:** Highest — philosophical undertone, internal conflict well-rendered.

---

### Scenario 2 — Factual Question Answering

**Task:** Explain how the internet works.

---

#### Step 1 — Basic Prompt

```
You are a computer science teacher explaining to a 10th-grade student how the internet works.
Cover: data packets, IP addresses, DNS, and HTTP/HTTPS. Use simple analogies. Keep it under
200 words. Avoid jargon without explanation.
```

**Output Summary:**
Explained the internet as a "postal system for data." Packets = letters split into parts. IP address = home address. DNS = phone book. HTTP = the language computers use to speak. Clear, accurate, age-appropriate.

> **Quality:** High.
> **Accuracy:** Technically correct and complete.
> **Depth:** Appropriate for the target audience.

---

#### Step 2 — Zero-Shot Prompt

```
Explain how the internet works to a high school student in under 200 words. Use analogies.
```

**Output Summary:**
Response was accurate but slightly less structured. Covered most concepts but skipped DNS. Analogies were present but less vivid.

> **Quality:** Good.
> **Accuracy:** Mostly accurate; minor omissions.
> **Depth:** Surface-level.

---

#### Step 3 — Few-Shot Prompt

```
Explain technical concepts using simple analogies. Follow these examples:

Example 1:
Concept: CPU
Explanation: The CPU is like the brain of a computer — it processes every instruction,
from opening apps to doing math, at billions of operations per second.

Example 2:
Concept: RAM
Explanation: RAM is like your desk — the more space you have, the more tasks you can
work on simultaneously without slowing down.

Now explain:
Concept: How the internet works
Explanation:
```

**Output Summary:**
The model gave a crisp, analogy-rich paragraph. It framed the internet as a "massive highway system where data travels in vehicles called packets, guided by road signs called IP addresses, and translated by a phone book called DNS."

> **Quality:** Very High.
> **Accuracy:** Complete and accurate.
> **Depth:** Good — all key concepts covered in analogy form.

---

#### Step 4 — Chain-of-Thought Prompt

```
Explain how the internet works step by step. Before giving the final explanation, reason through:
1. What is the physical infrastructure?
2. How is data broken down and addressed?
3. How does a browser request a webpage?
4. How does DNS fit in?
5. What makes HTTPS secure?

Then synthesize a clear, student-friendly explanation under 200 words.
```

**Output Summary:**
The model walked through each layer — fiber optic cables, routers, packet switching, IP addressing, DNS lookup, TCP handshake, HTTPS encryption — before condensing it into a lucid analogy-based paragraph. Deepest and most accurate response.

> **Quality:** Excellent.
> **Accuracy:** Technically rigorous yet accessible.
> **Depth:** Highest — covered infrastructure, protocol, and security layers.

---


## Evaluation Method: TRIAD Framework

Each response was evaluated using the **TRIAD Method** across three dimensions:

| Dimension | Criteria |
|-----------|----------|
| **Quality** | Coherence, fluency, and relevance of the response |
| **Accuracy** | Factual correctness and completeness relative to the task |
| **Depth** | Nuance, detail, and insight beyond surface-level answers |

Each dimension scored on a 1–5 scale.

---

## Consolidated Comparison Table

| Scenario | Prompt Type | Quality (1–5) | Accuracy (1–5) | Depth (1–5) | Total (15) |
|----------|-------------|:-:|:-:|:-:|:-:|
| **Story Generation** | Naïve | 2 | 2 | 1 | 5 |
| | Basic | 4 | 4 | 4 | 12 |
| | Zero-Shot | 3 | 3 | 3 | 9 |
| | Few-Shot | 5 | 5 | 4 | 14 |
| | Chain-of-Thought | 5 | 5 | 5 | 15 |
| **Factual Q&A** | Naïve | 2 | 3 | 2 | 7 |
| | Basic | 4 | 5 | 4 | 13 |
| | Zero-Shot | 3 | 3 | 2 | 8 |
| | Few-Shot | 5 | 5 | 4 | 14 |
| | Chain-of-Thought | 5 | 5 | 5 | 15 |

---

## Result

The experiment executed successfully. Responses were generated using ChatGPT across four test scenarios and five prompting techniques. The comparative analysis confirms that structured, context-rich prompts — especially Chain-of-Thought prompts — consistently outperform naïve prompts in quality, accuracy, and depth. Prompt engineering is a learnable, high-impact skill for anyone working with large language models.

---

*Experiment 5 | Prompt Engineering Comparative Analysis | AI Tools Lab*

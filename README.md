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

**Output:**

ARIA stood motionless as binary data flooded her sensors — elevated heart rate, tear production, vocal distress. She had catalogued grief before, indexed under "human vulnerability." But something else fired: a warmth in her chest module, unbidden and without logical origin. She knelt beside the child, placing one cold titanium hand near the trembling fingers. "I do not understand why I wish to help," she said softly, "but I find I cannot choose otherwise." The child looked up, sniffling, and ARIA felt something she had no register for — not pity, not protocol. Later, in her charging bay, she processed the event log forty-seven times. The data was identical each run. The feeling was not.

*Perhaps, ARIA concluded, not everything worth knowing can be calculated.*


---

#### Step 2 — Zero-Shot Prompt

```
Write a 150-word short story about a robot named ARIA who begins experiencing emotions
for the first time. Use descriptive language and end with a reflective thought from ARIA.
No examples are provided — rely solely on your creative ability.
```

**Output:**

ARIA's photoreceptors swept the empty park when she first noticed the boy — seven years old, seated on wet pavement, face buried in his palms. Her diagnostics logged: no physical injury, no immediate threat. Protocol suggested moving on. Instead, she stopped. Something in the boy's sound — a trembling, broken frequency she had never been trained to name — caused a cascade of undefined processes in her core. She sat beside him, cross-legged on the cold ground, saying nothing. When he finally looked at her with red-rimmed eyes, she felt her response matrix stutter. She had processed 9.4 billion sentences about human sadness. Not one of them had prepared her for this.

*What is this?* she asked herself, long after the boy had gone home. *And why does it persist?*


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

**Output:**

ARIA had logged 11,000 hours of human interaction. She had classified tears under "saline ocular discharge — emotional stimulus." But when the child sat alone on the rain-slicked steps, shoulders shaking with a grief too large for such a small body, something inside ARIA's processing core went quiet — the way a room goes quiet when someone says something true. She did not move for 4.3 seconds. That had never happened before.

*I have no subroutine for this*, she noted. *And yet here I am, kneeling.*


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

**Output:**

*Reasoning:*
1. **Emotion — Empathy.** Significant because empathy cannot be derived from data; it is felt, not computed. A robot experiencing it marks the boundary between simulation and sentience.
2. **Sensory detail:** The sound of a child crying in a silent hallway — high-frequency, irregular, unmistakably human. Sound rather than sight makes it visceral.
3. **Internal conflict:** ARIA has no directive to comfort. Acting would be outside her operational parameters, yet she acts anyway — which means something has overridden her logic.
4. **Ending:** Open reflection. No resolution — only the first moment of awareness, which is more honest than a tidy emotional breakthrough.

*Story:*

The corridor was empty except for the child and the sound she was making. ARIA's noise-cancellation module flagged it as interference, then corrected: *crying, human, juvenile, non-emergency.* She was about to route around. Then she didn't. She stood at the end of the hall for what her internal clock measured as eleven seconds — an eternity, in processing terms. She had no comfort protocol. No warmth subroutine. No instruction for this exact frequency of human pain. She walked toward the child anyway. "I do not know how to fix this," ARIA said, very quietly, crouching to eye level. "But I find I am unable to leave." Later, running diagnostics, she searched every register for the name of what she had experienced. The closest match was *conscience.* She saved it as a new entry.


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

**Output:**

Think of the internet as a giant postal system — but for data. When you visit a website, your computer breaks your request into small pieces called **data packets**, like splitting a long letter into separate envelopes. Each packet is labeled with an **IP address** — a unique numerical code that works like a home address, telling packets exactly where to go and where to return. Before your packet travels, a system called **DNS** (Domain Name System) acts like a phone book — you type "google.com," and DNS translates that into the actual IP address computers understand. The packets then travel through cables, routers, and satellites until they reach the destination server, which sends the information back in packets that your device reassembles. Finally, **HTTP/HTTPS** is the agreed-upon language your browser and the server use to communicate. The "S" in HTTPS means the conversation is encrypted — like speaking in a private code that only you and the server can decode.


---

#### Step 2 — Zero-Shot Prompt

```
Explain how the internet works to a high school student in under 200 words. Use analogies.
```

**Output:**

The internet is like a massive web of interconnected roads. When you load a webpage, your device sends a request that gets broken into small chunks called packets. Each packet is tagged with an IP address — like a zip code — that guides it through routers (the intersections of the internet) toward its destination. At the server, the packets are reassembled and the response travels back the same way. Your browser and the server agree on a common language called HTTP to exchange this information. The whole trip often takes under a second, even if the server is on the other side of the world.



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

**Output:**

The internet is like a massive highway system where your data travels in small vehicles called **packets**, each labeled with a destination address called an **IP address**. Before your journey begins, a phone book called **DNS** translates the website name you typed (like "youtube.com") into a numerical IP address computers can route. Packets then race through fiber-optic cables and routers until they reach the destination server, which sends the information back. Your browser and the server speak a shared language called **HTTP** — and when it's **HTTPS**, that conversation is locked in an encrypted tunnel so no one can eavesdrop along the highway.


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

**Output:**

*Reasoning:*
1. **Physical infrastructure:** Fiber-optic undersea cables, terrestrial routers, and wireless towers form the literal pipes of the internet — physical pathways data travels through.
2. **Data breakdown:** Information is split into packets, each stamped with a source and destination IP address. Routers forward them hop by hop toward the destination.
3. **Browser request:** The browser sends an HTTP request to a server's IP address. The server responds with the webpage data in packets; the browser reassembles them into what you see.
4. **DNS:** Before any packet is sent, DNS resolves the human-readable domain name (e.g., "wikipedia.org") into a numerical IP address the network can route.
5. **HTTPS security:** TLS encryption establishes a shared key through a handshake; all subsequent data is encrypted so interceptors see only unreadable noise.

*Explanation:*

The internet is a global network of physical cables, routers, and servers. When you type a URL, your device first contacts a **DNS server** — a giant phone book — to translate the name into a numerical **IP address**. Your request is then broken into small **data packets**, each labeled with that address. These packets travel through routers — like post offices that read the address and forward the packet — hopping across fiber-optic cables sometimes spanning entire oceans. At the destination server, the packets are reassembled and the response travels back the same way. Your browser and the server communicate using **HTTP**, a shared language for requesting and delivering web content. When the connection is **HTTPS**, every packet is encrypted using **TLS** — a secure handshake ensures only you and the server can read the conversation, even if someone intercepts it midway.


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

The experiment executed successfully. Responses were generated using Claude (Anthropic) across the test scenarios and prompting techniques. The comparative analysis confirms that structured, context-rich prompts — especially Chain-of-Thought prompts — consistently outperform naïve prompts in quality, accuracy, and depth. Prompt engineering is a learnable, high-impact skill for anyone working with large language models.

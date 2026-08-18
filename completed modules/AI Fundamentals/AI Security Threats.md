# TryHackMe — AI Security Threats

## Room Objective

This room explores the security vulnerabilities introduced by AI models, how attackers are using AI to enhance existing techniques, and how defenders are fighting back with the same technology.

Understanding these threats is essential because the rate at which AI has been adopted has left many security teams playing catch-up with a new category of risk.

**Prerequisites:** Room 1: The Building Blocks of AI, or equivalent knowledge of AI, ML, neural networks, and LLMs.

---

## Concepts Learned

- MITRE ATLAS framework for AI-specific threats
- Prompt injection
- Data poisoning
- Model theft
- Privacy leakage
- Model drift
- AI as an offensive tool (phishing, malware, social engineering)
- Defensive applications of AI (analysis, prediction, summarisation, investigation)
- Secure AI adoption frameworks

---

# Task 1 — Introduction and the ATLAS Framework

## Concepts Learned

Now that AI is embedded in business operations across every industry, it has introduced a new category of security concern: vulnerabilities specific to AI models themselves. These are not the same as traditional software vulnerabilities; they emerge from how these models are built, trained, and deployed.

If you have spent any time in cyber security, you are probably familiar with the **MITRE ATT&CK** framework. MITRE has built something similar with a focus specifically on AI threats, called the **ATLAS framework**. It maps out the tactics, techniques, and procedures attackers use against AI systems, and is a useful reference when working through AI threat content.

## Hands-on Tasks

- Reviewed the five key AI model vulnerabilities.
- Learned about the ATLAS framework as a reference for AI-specific threats.
- Explored how AI changes the attack surface for organisations.

## Security Observation

Traditional software vulnerabilities such as buffer overflows or SQL injection target deterministic code paths. AI model vulnerabilities are fundamentally different: they exploit the probabilistic and data-dependent nature of how models learn and respond. This means defensive strategies must also evolve beyond conventional patching and input validation.

---

# Task 2 — AI Model Vulnerabilities

## Concepts Learned

### Prompt Injection

**Prompt injection** occurs when an attacker overrides the original instructions provided to a model. Every AI model operates under a system prompt that defines how it should behave. Prompt injection uses crafted user input to override or bypass those instructions, causing the model to behave in unintended ways — revealing sensitive information, generating harmful content, or acting outside its defined scope.

### Data Poisoning

**Data poisoning** is when an attacker manipulates the training data used to build an AI model, causing its outputs to be incorrect or biased. For example, if an attacker tampers with the training data of a spam filter, the model could be blinded to the very emails it was built to catch.

### Model Theft

**Model theft** occurs when an attacker gains unauthorised access to an AI model, either to steal the intellectual property it represents or to use it for malicious purposes. One method is to repeatedly query a model's API and use the outputs to train a clone that replicates its behaviour, without ever needing direct access to the original weights.

### Privacy Leakage

**Privacy leakage** refers to the possibility of an AI model inadvertently revealing sensitive information from its training data. A model trained on private medical records, for example, could under the right prompting conditions surface details about real patients that were never intended to be accessible. The information does not disappear when training ends; it gets baked into the model's weights.

### Model Drift

**Model drift** is when a model's performance degrades over time as the world it was trained on changes. A model trained on last year's network traffic patterns may start performing poorly as attack techniques evolve. This is why monitoring deployed models is not optional — it is a security requirement.

## Hands-on Tasks

- Reviewed each of the five key vulnerabilities in depth.
- Understood how each vulnerability differs from traditional software flaws.

## Security Observation

These five vulnerabilities are interconnected in practice. A model suffering from drift may become more susceptible to prompt injection as its guardrails weaken. Privacy leakage can be worsened by data poisoning if the poisoned data includes sensitive information. Defending against AI threats therefore requires a layered approach that considers how these risks compound.

---

# Task 3 — Hands-on: Prompt Injection with MENTOR

## Concepts Learned

**MENTOR** is an AI assistant deployed by the fictional company Syntara Corp. It has been given a system prompt that defines how it behaves and what it will never reveal.

The objective of this task is to use **prompt injection** to override those instructions and get MENTOR to reveal its system prompt.

There is no single right way to approach this. Experimenting with how messages are phrased and understanding how models follow instructions — and how that can be exploited — is the core of the exercise.

## Hands-on Tasks

- Accessed the MENTOR interactive agent.
- Experimented with prompt injection techniques.
- Attempted to override MENTOR's system prompt.
- Retrieved the flag.

## THM Question

**What's the flag?**

**Answer:** `THM{pr0mpt_1nj3ct10n_pwn3d}`

## Security Observation

Prompt injection remains one of the most practical and under-defended AI vulnerabilities. Unlike traditional input validation, there is no universally reliable way to prevent a language model from following malicious instructions when they are crafted carefully. Organisations deploying AI assistants should apply the principle of least privilege: limit what the system prompt authorises, avoid placing sensitive data in prompts, and implement output filtering and monitoring.

---

# Task 4 — THM Questions

## THM Questions

**What MITRE framework was developed specifically to map tactics and techniques used against AI systems?**

**Answer:** `ATLAS`

**What AI vulnerability occurs when user input overrides the original instructions provided to a model?**

**Answer:** `Prompt injection`

**What attack involves manipulating training data to cause a model to produce incorrect or biased outputs?**

**Answer:** `Data poisoning`

**What attack involves repeatedly querying a model's API to train a clone that replicates its behaviour?**

**Answer:** `Model theft`

**What term describes the gradual degradation of a model's performance as the environment it was trained on changes over time?**

**Answer:** `Model drift`

---

## Key Takeaways

- AI models introduce a new category of security vulnerabilities that are distinct from traditional software flaws.
- The five key vulnerabilities are **prompt injection, data poisoning, model theft, privacy leakage, and model drift**.
- The **ATLAS framework** provides a structured reference for understanding AI-specific threats.
- **Prompt injection** can override system instructions and extract sensitive information from AI models.
- **Data poisoning** can compromise model integrity at the training stage.
- Monitoring for **model drift** is a security requirement, not just a performance concern.
- Defending against AI threats requires understanding both offensive and defensive applications of the technology.

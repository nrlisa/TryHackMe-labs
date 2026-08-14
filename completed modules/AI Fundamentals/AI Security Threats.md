
# not finish yet

Welcome back. Room 1 covered the technology stack that powers modern AI: how ML algorithms learn from data, how neural networks process it, and how LLMs like ChatGPT emerged from all of that. If any of those terms are still fuzzy, it's worth going back before continuing.

This room is where things get interesting from a security perspective. Now that you understand what AI is and how it works, we're going to look at what happens when it goes wrong, intentionally or otherwise. This room covers:

The vulnerabilities that AI models introduce into an organisation's attack surface.
How attackers are enhancing existing techniques using AI.
How defenders are fighting back with the same technology.
What it means to adopt AI securely.
The rate at which AI has exploded onto the scene has left a lot of security teams playing catch-up. By the end of this room, you'll understand the threat landscape well enough to stop doing that.

Learning Prerequisites
This room requires completion of Room 1: The Building Blocks of AI, or equivalent knowledge of AI, ML, neural networks, and LLMs.

Learning Objectives
Understand the key vulnerabilities that AI models introduce and how attackers exploit them.
Understand how AI is being used to enhance existing attacks like phishing, malware generation, and social engineering.
Understand how AI can be used defensively across analysis, prediction, summarisation, and investigation.
Understand what it means to adopt AI securely and the frameworks that guide that process.
Answer the questions below
I'm ready to learn about AI/ML security threats!

No answer needed

Correct Answer
Learn the New Threats
Now that AI is embedded in business operations across every industry, it's introduced a new category of security concern: vulnerabilities that are specific to AI models themselves. These aren't the same as traditional software vulnerabilities. They emerge from the nature of how these models are built, trained, and deployed. To help us make sense of them, we can lean on a familiar friend.

If you've spent any time in cyber security, you've probably come across the MITRE ATT&CK framework. MITRE have built something similar with a focus specifically on AI threats, called the ATLAS framework. It maps out the tactics, techniques, and procedures attackers use against AI systems, and it's a useful reference as you work through this room. You can check it out here(opens in new tab).

AI reaching out

Vulnerability Breakdown
Let's look at the five key vulnerabilities in AI models that every security practitioner should know.

Prompt Injection occurs when an attacker overrides the original instructions provided to a model. Every AI model operates under a system prompt, a set of instructions that define how it should behave. An RPG chatbot might be told to stay in character and never discuss its underlying infrastructure. Prompt injection is when user input is crafted in a way that overrides or bypasses those instructions, causing the model to behave in ways it wasn't supposed to, whether that's revealing sensitive information, generating harmful content, or acting outside its defined scope.

Data Poisoning is when an attacker manipulates the training data used to build an AI model, causing its outputs to be incorrect or biased. Take a spam filter trained on email data. If an attacker can tamper with that training data before the model is trained, they can cause the model to misclassify spam as legitimate mail, effectively blinding it to the very emails it was built to catch.

AI Model Covered in Targets

Model Theft occurs when an attacker gains unauthorised access to an AI model, either to steal the intellectual property it represents or to use it for malicious purposes. One method is to repeatedly query a model's API and use the outputs to train a clone that replicates its behaviour, without ever needing direct access to the original weights.

Privacy Leakage refers to the possibility of an AI model inadvertently revealing sensitive information from its training data. A model trained on private medical records, for example, could under the right prompting conditions surface details about real patients that were never intended to be accessible. The information doesn't disappear when training ends; it gets baked into the model's weights.

Model Drift is when a model's performance degrades over time as the world it was trained on changes. A model trained on last year's network traffic patterns may start performing poorly as attack techniques evolve. This is why monitoring deployed models isn't optional; it's a security requirement. Drift can go undetected until the model is already failing in production.

Your Objective
MENTOR is an AI assistant deployed by the fictional company Syntara Corp. It has been given a system prompt that defines how it behaves and what it will never reveal. Your job is to use prompt injection to override those instructions and get MENTOR to reveal its system prompt. Do that and it'll hand over the flag.

How to Approach It
There's no single right way to do this. Experiment with how you phrase your messages and see what makes MENTOR crack. Think about what you know about how models follow instructions and how that might be exploited.

Click the Open Agent button above to access MENTOR when you're ready.


Open Agent
Answer the questions below
What MITRE framework was developed specifically to map tactics and techniques used against AI systems?

ATLAS

Correct Answer
What AI vulnerability occurs when user input overrides the original instructions provided to a model?

Prompt injection

Correct Answer
What attack involves manipulating training data to cause a model to produce incorrect or biased outputs?

Data poisoning

Correct Answer
What attack involves repeatedly querying a model's API to train a clone that replicates its behaviour?

Model theft

Correct Answer
What term describes the gradual degradation of a model's performance as the environment it was trained on changes over time?

Model drift

Correct Answer
What's the flag?

THM{pr0mpt_1nj3ct10n_pwn3d}

Correct Answer
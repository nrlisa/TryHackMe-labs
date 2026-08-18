# TryHackMe — The Building Blocks of AI

## Room Objective

This room introduces the fundamental concepts behind **Artificial Intelligence (AI), Machine Learning (ML), Deep Learning (DL), Neural Networks, and Large Language Models (LLMs)**.

The objective is to understand how these technologies work, how they relate to each other, and how they are used in modern AI systems. The room also provides practical experience through TryHackMe's AI Agent platform and interactive neural network exercises.

---

## Concepts Learned

- Machine Learning lifecycle
- Overfitting
- Supervised learning, Unsupervised learning, Semi-supervised learning, Reinforcement learning
- Neural networks
- Deep Learning (DL)
- Input, hidden, and output layers
- Synapses and weighted connections
- Large Language Models (LLMs)
- Generative AI
- Relationship between AI, ML, DL, and LLMs

---

# Task 1 — Introduction to AI/ML

## Concepts Learned

Artificial Intelligence refers to computer systems capable of performing tasks that would normally require human reasoning, comprehension, problem-solving, or creativity.

AI research dates back to the 1950s, while **Machine Learning** later emerged as a major subfield of AI.

**Machine Learning** is a subfield of AI that enables systems to learn patterns from data without being explicitly programmed with every instruction.

A typical ML lifecycle includes:

1. Define the problem
2. Collect data
3. Clean and prepare the data
4. Train the model
5. Evaluate the model
6. Tune the model
7. Deploy the model
8. Monitor and retrain the model

**Overfitting** occurs when a model becomes too familiar with its training data and fails to generalise effectively to new, unseen data. Instead of learning the underlying patterns, the model effectively memorises the training examples.

## Hands-on Tasks

- Explored the introductory AI/ML concepts.
- Reviewed the Machine Learning lifecycle.
- Learned how models learn from training data.
- Interacted with the introductory AI Agent platform.

## THM Questions

**I'm ready to learn about AI/ML security!**

**Answer:** No answer needed

**What is the term for when a model becomes too familiar with its training data and fails to generalise to new data?**

**Answer:** `Overfitting`

**What is the subfield of AI that enables systems to learn from data without being explicitly programmed?**

**Answer:** `Machine Learning`

## Security Observation

AI is the broader field of creating systems capable of tasks associated with human intelligence. ML is a subfield of AI that learns patterns from data. ML systems require an iterative lifecycle of training, evaluation, deployment, and monitoring. Overfitting can prevent a model from generalising effectively to new data — in a security context, an overfitted model may fail to detect novel attack patterns it was not trained on.

---

# Task 2 — Introducing TryHackMe's AI Agent Platform

## Concepts Learned

Some tasks in this room use the **TryHackMe AI Agent platform** as an interactive environment instead of a traditional terminal or virtual machine.

The AI agents are configured with different:

- Roles
- Behaviours
- Objectives
- Information
- Constraints

The interaction is driven through natural language prompts.

## Hands-on Tasks

- Opened the TryHackMe AI Agent platform.
- Interacted with the sandbox AI agent.
- Experimented with natural-language prompts.
- Observed how the agent responded to different inputs.

## Security Observation

AI agents can be used as interactive environments for security learning. Agent behaviour can depend heavily on the instructions and prompts provided, which highlights how prompt phrasing can influence AI agent responses — a concept directly relevant to understanding prompt injection vulnerabilities.

---

# Task 3 — What is AI and Machine Learning?

## Concepts Learned

Artificial Intelligence is the overarching field concerned with enabling computers to perform tasks that require forms of human intelligence.

Machine Learning is a subfield of AI where systems learn from data rather than relying entirely on explicitly programmed rules.

**Machine Learning Lifecycle:**

```text
Problem Definition
       ↓
Data Collection
       ↓
Data Preparation
       ↓
Model Training
       ↓
Evaluation
       ↓
Tuning
       ↓
Deployment
       ↓
Monitoring / Retraining
```

Machine Learning is therefore an iterative process rather than a one-time training activity.

Overfitting occurs when a model performs well on its training data but performs poorly on previously unseen data. This happens because the model has learned the training examples too closely instead of learning patterns that generalise.

## Hands-on Tasks

- Reviewed the definition of Artificial Intelligence.
- Learned how Machine Learning fits within AI.
- Studied the ML lifecycle.
- Learned about overfitting.
- Explored how ML systems learn from data.

## Security Observation

Machine Learning allows systems to learn from data and identify patterns, but models must be evaluated using data they have not simply memorised. Overfitting is an important ML concept that affects model generalisation — an overfitted security model may miss real-world threats it was never explicitly trained on.

---

# Task 4 — Machine Learning Algorithms

## Concepts Learned

Machine Learning algorithms are mathematical methods used to identify patterns in data and make predictions or decisions.

A typical ML algorithm involves:

1. Input data
2. A decision or prediction process
3. An error function
4. Model optimisation
5. Repeated improvement

ML algorithms can be divided into four major categories:

**Supervised Learning** — uses **labelled data**, where each training example has a known correct answer. Examples: predicting house prices, classifying emails as spam or legitimate.

**Unsupervised Learning** — uses **unlabelled data** and attempts to identify patterns, clusters, or relationships within the dataset. Examples: customer segmentation, network anomaly detection.

**Semi-Supervised Learning** — combines a small amount of labelled data with a larger amount of unlabelled data. Useful when obtaining labelled data is expensive or time-consuming.

**Reinforcement Learning** — an agent interacts with an environment, receiving rewards for desirable actions and penalties for undesirable actions. The agent learns to improve its behaviour over time in order to maximise its reward.

## Hands-on Tasks

- Identified different categories of ML algorithms.
- Worked through scenarios involving different learning approaches.
- Used the AI Agent platform to identify the appropriate algorithm type.
- Completed the four ML algorithm missions.

## THM Questions

**Which category of ML algorithm learns by receiving rewards or penalties based on actions taken in an environment?**

**Answer:** `Reinforcement learning`

**Which category of ML algorithm uses a small amount of labelled data to guide learning across a larger unlabelled dataset?**

**Answer:** `Semi-supervised learning`

**What's the flag?**

**Answer:** `THM{4lg0r1thm_4g3nt}`

## Security Observation

Supervised learning uses labelled data, unsupervised learning identifies patterns in unlabelled data, semi-supervised learning combines both, and reinforcement learning learns through rewards and penalties. Choosing the correct ML approach depends on the problem and available data — in security, different algorithm types are suited to different threat detection scenarios.

---

# Task 5 — Neural Networks and Deep Learning

## Concepts Learned

Neural networks are computing models inspired by the structure of biological neural networks. A neural network consists of interconnected nodes organised into layers.

```text
Input Layer
     ↓
Hidden Layers
     ↓
Output Layer
```

- **Input Layer** — receives the raw data. For example, a 4×4 pixel image can be represented using 16 input nodes.
- **Hidden Layers** — process the input and extract increasingly complex patterns and features.
- **Output Layer** — produces the final prediction or classification.
- **Synapses** — the connections between nodes, analogous to biological synapses. Each connection has a **weight**, which determines how strongly it influences the next node.

**Deep Learning** uses neural networks with multiple layers to process and learn complex patterns from data. It can process large amounts of raw and unstructured data and automatically learn useful features.

## Hands-on Tasks

- Studied the structure of neural networks.
- Learned about input, hidden, and output layers.
- Explored weighted connections between nodes.
- Interacted with the NEURON-1 AI Agent.
- Manually followed the flow of information through a neural network.
- Classified an input using the input, hidden, and output stages.

## THM Questions

**What is the first layer in a neural network that receives raw input data?**

**Answer:** `Input layer`

**What term describes the weighted connections between nodes in a neural network?**

**Answer:** `Synapses`

**What's the flag?**

**Answer:** `THM{n3ur0n_1_0nl1n3}`

## Security Observation

Neural networks consist of interconnected nodes arranged into layers, where the input layer receives raw data, hidden layers extract and process patterns, and the output layer produces the final classification or prediction. Connections between nodes have weights that influence how information is processed. Understanding this architecture is important for recognising where adversarial inputs could be crafted to manipulate model outputs.

---

# Task 6 — Large Language Models

## Concepts Learned

Large Language Models (LLMs) are Deep Learning-based AI models designed to process and generate text. LLMs generate text by repeatedly predicting what token or word should come next based on the context provided.

**Pre-Training:** during pre-training, an LLM processes enormous amounts of text and learns language patterns using billions of numerical parameters.

```text
Training Data
     ↓
Prediction
     ↓
Compare With Correct Answer
     ↓
Backpropagation
     ↓
Update Parameters
     ↓
Repeat
```

**Transformers** — modern LLMs use Transformer neural networks, introduced in Google's 2017 paper *Attention Is All You Need*. A major innovation of Transformers is the **attention mechanism**, which allows the model to assign different levels of importance to words based on their context.

**Backpropagation** — used to adjust model parameters based on the difference between the model's prediction and the correct answer.

**RLHF (Reinforcement Learning from Human Feedback)** — involves humans reviewing model outputs and providing feedback that can be used to improve the model's behaviour.

**Generative AI** — LLMs power generative AI applications capable of producing original text. Generative AI can also be used to generate images, audio, video, and other forms of content.

## THM Questions

**What type of neural network, introduced by Google in 2017, powers modern LLMs?**

**Answer:** `Transformer neural networks`

**What is the name of the process where humans review and flag model outputs to refine its behaviour after pre-training?**

**Answer:** `RLHF`

**What mechanism do transformer networks use to assign different levels of importance to different words in a sequence?**

**Answer:** `Attention`

**What algorithm is used to adjust a model's parameters based on the difference between its prediction and the correct answer?**

**Answer:** `Backpropagation`

## Security Observation

LLMs are Deep Learning models designed to process and generate language. Transformers are the neural network architecture behind modern LLMs, and attention allows them to consider the importance of words in context. Backpropagation adjusts model parameters during training, while RLHF uses human feedback to refine model behaviour. Understanding how LLMs are trained and refined is foundational for understanding AI security risks such as prompt injection and data poisoning.

---

# Task 7 — Practical

## Concepts Learned

This task combines the concepts covered throughout the room into a practical neural network exercise.

The NEURON-1 challenge requires the user to interact with a neural network and understand the flow of information through:

```text
Input
  ↓
Hidden Layer
  ↓
Output
```

## Hands-on Tasks

- Launched the NEURON-1 interactive environment.
- Provided input to the neural network.
- Worked through the hidden layer.
- Interpreted the output.
- Completed the final classification challenge.

## THM Questions

**What's the flag?**

**Answer:** `THM{y0u_tr41n3d_th3_n3tw0rk}`

## Security Observation

Neural networks process information through multiple layers: the input layer receives raw data, hidden layers identify and combine useful patterns, and the output layer produces the final result. Understanding this flow helps connect the theoretical concepts of neural networks and Deep Learning to practical AI systems, including how adversarial inputs could be crafted at each stage.

---

# Task 8 — Room Summary

## Concepts Learned

This room connected the major building blocks of modern Artificial Intelligence:

```text
Artificial Intelligence (AI)
            ↓
    Machine Learning (ML)
            ↓
      Deep Learning (DL)
            ↓
Large Language Models (LLMs)
```

- **Artificial Intelligence** — the overarching field focused on creating systems capable of tasks associated with human intelligence.
- **Machine Learning** — a subfield of AI that enables systems to learn patterns from data.
- **Deep Learning** — a subfield of ML that uses neural networks with multiple layers to process complex data.
- **Large Language Models** — advanced Deep Learning models built using Transformer architectures and designed to understand and generate human-like text.

## Hands-on Tasks

- Completed the AI/ML fundamentals.
- Explored four categories of Machine Learning.
- Interacted with AI agents.
- Worked with a simulated neural network.
- Learned how modern LLMs are trained and refined.
- Completed the final NEURON-1 challenge.

## Key Takeaways

- AI is the broader field encompassing ML and other approaches to intelligent systems.
- ML allows systems to learn from data.
- Deep Learning uses neural networks to learn complex patterns.
- Understanding these building blocks provides a foundation for studying **AI security and AI-enabled cyber threats**.

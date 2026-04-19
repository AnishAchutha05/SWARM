# SWARM — Multi-Agent Cognitive Intelligence System

> *One LLM. N concurrent minds. One shared memory. Survival of the sharpest.*

SWARM is a multi-agent AI system built for LLM efficiency that virtualises a single LLM into **N parallel agents**, each assigned a distinct cognitive personality. Agents think concurrently, share a common blackboard memory pool, compete through a scoring system, and get pruned each round — so only the strongest reasoning survives. The number of agents isn't fixed: SWARM dynamically determines agent count based on problem complexity, inspired by OS multithreading and biological swarm intelligence.

---

## How It Works

```
Problem Input
     │
     ▼
┌─────────────────────────────┐
│  Complexity Analyser        │  → decides N (number of agents)
└─────────────────────────────┘
     │
     ▼
┌─────────────────────────────────────────────────────────┐
│  Agent Pool (dynamically sized)                         │
│                                                         │
│   [Analytical]  [Adversarial]  [Critical]  [Creative]  │
│        │               │            │           │       │
│        └───────────────┴────────────┴───────────┘       │
│                         │                               │
│              ┌──────────▼──────────┐                    │
│              │  Shared Blackboard  │  ← common memory   │
│              └─────────────────────┘                    │
└─────────────────────────────────────────────────────────┘
     │
     ▼
┌─────────────────────────────┐
│  Scoring & Pruning Engine   │  → weakest agents eliminated each round
└─────────────────────────────┘
     │
     ▼
 Best surviving answer surfaced
```

Each agent receives the same problem but reasons through it through a different cognitive lens. Their outputs are scored, the weakest are cut, and the survivors continue to the next round — refining collaboratively through the shared memory blackboard until a final answer emerges.

---

## Key Features

**Dynamic agent count** — SWARM analyses the incoming problem and decides how many agents to spin up. A simple factual query might get 3 agents; a complex strategic problem might warrant 8 or more.

**Cognitive personalities** — Each agent is instantiated with a distinct reasoning style: Analytical (structured, logical), Adversarial (challenges assumptions), Critical (finds flaws), Creative (lateral thinking), and others. This forces the system to explore a problem space from multiple angles simultaneously.

**Shared blackboard memory** — All agents read and write to a common memory pool. This mirrors the classic blackboard architecture from AI planning systems — agents build on each other's reasoning rather than operating in complete isolation.

**Competitive pruning** — After each reasoning round, agents are scored and the weakest are eliminated. This is inspired by natural selection and swarm intelligence: the system self-improves over multiple rounds rather than returning a single shot answer.

**Single LLM, multiple minds** — SWARM doesn't require multiple API keys or model instances. It virtualises one LLM into N cognitive agents through prompt architecture — making it cost-efficient and practically deployable.

---

## Tech Stack

- **Language:** Python
- **Core:** LLM API (GROQ-compatible)
- **Architecture patterns:** Blackboard system, agent-based modelling, swarm intelligence, OS multithreading concepts

---

## Project Structure

```
SWARM/
├── fixed_swarm_project/
│   └── fixed_swarm_project/    # Core source files
├── .gitignore
└── README.md
```

---

## Getting Started

### Prerequisites

```bash
python 3.8+
pip install -r requirements.txt
```

You will need an **GROQ API key** (or compatible LLM endpoint) set as an environment variable:

```bash
export GROQ_API_KEY=your_api_key_here
```

### Running SWARM

```bash
cd fixed_swarm_project/fixed_swarm_project
python main.py
```

---

## Design Inspiration

SWARM draws from three distinct fields:

**OS Multithreading** — Just as an OS runs multiple threads concurrently on one CPU, SWARM runs multiple cognitive agents concurrently on one LLM. Context switching, resource sharing, and scheduling are all conceptually mirrored in the agent pool.

**Blackboard Architecture** — A classic AI pattern from the 1970s where independent knowledge sources (agents) read from and write to a shared data structure (the blackboard). SWARM modernises this with LLM-based agents.

**Swarm Intelligence** — Systems like ant colonies and bird flocking produce emergent intelligence from simple competing/cooperating agents. SWARM borrows the idea that a group of specialised, competing reasoners can outperform a single monolithic one.

---

## Built For

This project was built for a **hackathon**. The core hypothesis: *a diverse population of competing AI agents, even virtualised from a single model, can produce more robust, well-rounded reasoning than a single LLM call ever could.*

---

## Author

**Anish Achutha** — [GitHub](https://github.com/AnishAchutha05)

---

## License

This project is open source. Feel free to explore, fork, and build on it.

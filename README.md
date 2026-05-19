# AGENTIC AI: COMPLETE HANDBOOK
## From Beginner to Advanced - Interview Ready Technical Guide

**Version:** 2.0  
**Last Updated:** May 2026  
**Target Audience:** AI/ML Engineers, GenAI Engineers, Researchers, Technical Interviewers

---

## TABLE OF CONTENTS

1. [Introduction to Agentic AI](#section-1)
2. [How Agentic AI Works](#section-2)
3. [Agentic AI Architecture](#section-3)
4. [Memory in Agentic AI](#section-4)
5. [Major Agentic AI Frameworks](#section-5)
6. [Multi-Agent Systems](#section-6)
7. [Tools and Tool Calling](#section-7)
8. [RAG + Agentic AI](#section-8)
9. [MLOps + AgentOps](#section-9)
10. [Real-World Applications](#section-10)
11. [Advanced Topics](#section-11)
12. [Coding + Implementation](#section-12)
13. [Interview Preparation](#section-13)
14. [Comparison Tables](#section-14)
15. [Learning Roadmap](#section-15)
16. [Projects](#section-16)

---

<a name="section-1"></a>
# SECTION 1 — INTRODUCTION TO AGENTIC AI

## 1.1 What is Agentic AI?

**Agentic AI** refers to artificial intelligence systems that possess **agency** - the ability to act autonomously, make decisions, plan actions, and execute tasks to achieve specific goals without constant human intervention.

### Simple Definition
Imagine hiring a research assistant. Instead of giving them step-by-step instructions for every task, you simply say "Research the impact of climate change on marine ecosystems and prepare a report." The assistant then:
- Breaks down the task
- Searches for information
- Evaluates sources
- Synthesizes findings
- Writes the report
- Reviews and refines it

**This is Agentic AI** - AI systems that can autonomously plan, reason, use tools, and execute complex multi-step tasks.

### Technical Definition
**Agentic AI** is a paradigm where AI systems demonstrate autonomous goal-directed behavior through:
- **Planning**: Breaking complex goals into executable steps
- **Reasoning**: Multi-step logical inference and decision-making
- **Tool Use**: Leveraging external APIs, databases, search engines, calculators
- **Memory**: Maintaining context across interactions
- **Reflection**: Self-evaluation and error correction
- **Adaptation**: Learning from feedback and improving performance

---

## 1.2 Definition of AI Agents

### What is an AI Agent?

An **AI Agent** is an autonomous entity that:
1. **Perceives** its environment (user inputs, data, external state)
2. **Reasons** about goals and constraints
3. **Plans** sequences of actions
4. **Acts** by executing tools and making decisions
5. **Learns** from outcomes and feedback

### Mathematical Formulation
```
Agent: (State, Goal) → Actions → New State
```

Where:
- **State (S)**: Current environment/context
- **Goal (G)**: Desired outcome
- **Actions (A)**: Tools, functions, operations
- **Policy (π)**: S × G → A (decision-making function)

### Key Properties
| Property | Description | Example |
|----------|-------------|---------|
| **Autonomy** | Acts independently without human intervention | Email agent automatically categorizes and responds |
| **Reactivity** | Responds to environmental changes | Stock trading agent reacts to market fluctuations |
| **Proactivity** | Takes initiative to achieve goals | Research agent proactively searches for latest papers |
| **Social Ability** | Communicates with other agents/humans | Multi-agent system with coordinator and workers |
| **Learning** | Improves from experience | Agent learns user preferences over time |

---

## 1.3 Evolution Timeline

### The AI Evolution Journey

```
Traditional AI (1950s-1980s)
    ↓
Rule-Based Expert Systems (1980s-1990s)
    ↓
Machine Learning (1990s-2010s)
    ↓
Deep Learning (2012-2018)
    ↓
Generative AI (2018-2023)
    ↓
Agentic AI (2023-Present)
```

### Detailed Evolution Path

#### 1. **Traditional AI (1950s-1980s)**
- **Characteristics**: Rule-based systems, symbolic reasoning
- **Example**: Chess engines, theorem provers
- **Limitation**: Brittle, couldn't handle uncertainty
- **Key Insight**: Intelligence ≠ Hard-coded rules

#### 2. **Machine Learning (1990s-2010s)**
- **Characteristics**: Learning from data, pattern recognition
- **Example**: Email spam filters, recommendation systems
- **Limitation**: Needed labeled data, task-specific
- **Key Insight**: Learning > Programming

#### 3. **Deep Learning (2012-2018)**
- **Characteristics**: Neural networks, representation learning
- **Example**: Image recognition, speech-to-text
- **Limitation**: Black box, poor reasoning
- **Key Insight**: Deep representations matter

#### 4. **Generative AI (2018-2023)**
- **Characteristics**: Content generation, few-shot learning
- **Example**: GPT-3/4, DALL-E, Stable Diffusion
- **Limitation**: Single-shot responses, no tool use
- **Key Insight**: Scale enables emergence

#### 5. **Agentic AI (2023-Present)**
- **Characteristics**: Autonomous reasoning, tool use, planning
- **Example**: AutoGPT, LangChain agents, CrewAI
- **Breakthrough**: Multi-step reasoning + Tool integration
- **Key Insight**: Agency = Intelligence + Tools + Autonomy

---

## 1.4 Why Agentic AI is Becoming Important

### The Paradigm Shift

Traditional applications required **procedural programming**:
```python
def process_customer_request():
    if request_type == "refund":
        check_eligibility()
        process_payment()
        send_confirmation()
    elif request_type == "support":
        find_answer_in_kb()
        send_response()
```

With Agentic AI:
```python
agent = CustomerServiceAgent(
    goal="Handle customer request professionally",
    tools=[email, knowledge_base, payment_api, calendar],
    memory=conversation_history
)
agent.execute(user_request)  # Handles everything autonomously
```

### Key Drivers

#### 1. **Complexity of Modern Tasks**
- Modern workflows require 10+ step processes
- Example: "Plan my vacation to Japan"
  - Search flights
  - Check visa requirements
  - Book hotels
  - Research attractions
  - Create itinerary
  - Set reminders
  - Book restaurants

#### 2. **Tool Integration Explosion**
- APIs available for everything: email, calendars, databases, search, payment
- Agents can orchestrate multiple tools seamlessly

#### 3. **Cost of Human Intervention**
- Humans can't monitor AI outputs 24/7
- Autonomous systems reduce operational costs

#### 4. **LLM Capabilities**
- Modern LLMs (GPT-4, Claude, Gemini) can:
  - Reason through complex problems
  - Understand context
  - Generate code
  - Call functions
  - Self-correct

#### 5. **Business Value**
| Industry | Traditional AI | Agentic AI | Value Gain |
|----------|---------------|------------|------------|
| Customer Service | Chatbots with scripts | Autonomous support agents | 70% cost reduction |
| Research | Search tools | Research agents that synthesize | 10x faster insights |
| Healthcare | Diagnosis tools | Clinical decision agents | Better patient outcomes |
| Finance | Alert systems | Trading/analysis agents | Real-time decisions |

---

## 1.5 Core Philosophy of Autonomous Agents

### The Agent Mindset

**Traditional Programming**:
```
Human: "Do exactly this"
Computer: *Executes*
```

**Agentic AI**:
```
Human: "Achieve this goal"
Agent: *Plans, reasons, acts, learns*
```

### Philosophical Principles

#### 1. **Goal-Oriented, Not Instruction-Oriented**
- Focus on **WHAT** to achieve, not **HOW**
- Agent determines the "how" autonomously

#### 2. **Self-Direction**
- Agents decide their own action sequences
- Humans provide goals, constraints, feedback

#### 3. **Continuous Learning**
- Every interaction improves future performance
- Agents build world models and refine strategies

#### 4. **Tool Augmentation**
- Agents are "superintelligent" through tool use
- LLM + Calculator > LLM alone for math

#### 5. **Graceful Degradation**
- When uncertain, agents ask for help
- When tools fail, agents find alternatives

---

## 1.6 Differences Explained

### Comprehensive Comparison Table

| Aspect | Traditional AI | Machine Learning | Deep Learning | Generative AI | Agentic AI |
|--------|---------------|-----------------|---------------|---------------|------------|
| **Paradigm** | Rule-based | Pattern-based | Representation learning | Content generation | Autonomous reasoning |
| **Input** | Structured data | Labeled datasets | Raw data | Prompts | Goals + Environment |
| **Output** | Deterministic result | Predictions | Classifications/Embeddings | Generated content | Actions + Decisions |
| **Learning** | None | Supervised/Unsupervised | Backpropagation | Pre-training + Fine-tuning | In-context + Reflection |
| **Decision Making** | IF-THEN rules | Statistical inference | Neural networks | Language models | Multi-step reasoning |
| **Adaptability** | Zero (hard-coded) | Limited (retrain needed) | Moderate | High (few-shot) | Very High (self-improves) |
| **Tool Use** | None | None | None | Limited | Extensive |
| **Autonomy** | None | None | None | Low | High |
| **Example Task** | Chess move | Spam detection | Image recognition | Write essay | Research + Report |
| **Key Technology** | Expert systems | SVMs, Random Forests | CNNs, RNNs | Transformers | LLMs + Orchestration |
| **Human Involvement** | Programming | Labeling data | Architecture design | Prompt engineering | Goal setting |

### Detailed Explanations

#### **Traditional AI**
```python
# Example: Rule-based email classifier
def classify_email(email):
    if "win prize" in email.lower() or "click here" in email.lower():
        return "spam"
    elif email.sender in trusted_senders:
        return "inbox"
    else:
        return "needs_review"
```

**Characteristics**:
- ✅ Explainable, deterministic
- ❌ Brittle, can't learn, manual rules

---

#### **Machine Learning**
```python
# Example: ML spam classifier
from sklearn.naive_bayes import MultinomialNB

# Training
model = MultinomialNB()
model.fit(X_train, y_train)  # X = email features, y = spam/not spam

# Prediction
prediction = model.predict(new_email_features)
```

**Characteristics**:
- ✅ Learns from data, generalizes
- ❌ Needs labeled data, task-specific

---

#### **Deep Learning**
```python
# Example: Neural network for sentiment analysis
import tensorflow as tf

model = tf.keras.Sequential([
    tf.keras.layers.Embedding(vocab_size, 128),
    tf.keras.layers.LSTM(64),
    tf.keras.layers.Dense(1, activation='sigmoid')
])

model.compile(optimizer='adam', loss='binary_crossentropy')
model.fit(X_train, y_train, epochs=10)
```

**Characteristics**:
- ✅ Learns representations, handles complexity
- ❌ Black box, needs lots of data

---

#### **Generative AI**
```python
# Example: GPT-based content generation
import openai

response = openai.ChatCompletion.create(
    model="gpt-4",
    messages=[{"role": "user", "content": "Write a product description"}]
)
print(response.choices[0].message.content)
```

**Characteristics**:
- ✅ Flexible, few-shot learning, content creation
- ❌ Single-shot, no tool use, hallucinations

---

#### **Agentic AI**
```python
# Example: Autonomous research agent
from langchain.agents import create_react_agent

agent = create_react_agent(
    llm=ChatOpenAI(model="gpt-4"),
    tools=[google_search, arxiv_search, calculator, python_repl],
    prompt=research_prompt
)

result = agent.invoke({
    "input": "Find latest papers on quantum computing, summarize trends, and predict future directions"
})
```

**Characteristics**:
- ✅ Autonomous, multi-step reasoning, tool use, self-correction
- ❌ Complex to build, requires orchestration, higher latency

---

## 1.7 Reactive AI vs Autonomous AI

### Reactive AI

**Definition**: Responds to inputs with pre-defined patterns; no memory, no planning.

**Example**: Traditional chatbot
```
User: "What's the weather?"
Bot: "I don't have weather data. Please check weather.com"
```

**Characteristics**:
- Stateless (no memory)
- Single-shot responses
- No planning or reasoning
- Doesn't use tools

---

### Autonomous AI

**Definition**: Takes initiative, plans actions, uses tools, maintains memory.

**Example**: Weather agent
```
User: "What's the weather?"
Agent:
  1. Detects location from user profile
  2. Calls weather API
  3. Analyzes forecast
  4. Provides personalized recommendation
Response: "It's 72°F and sunny in San Francisco. Great day for outdoor activities! Tomorrow will be cooler with possible rain, so bring an umbrella if you're going out."
```

**Characteristics**:
- Stateful (maintains context)
- Multi-step reasoning
- Proactive tool use
- Learns and adapts

---

### Comparison Table

| Feature | Reactive AI | Autonomous AI |
|---------|-------------|---------------|
| **Memory** | None | Short-term + Long-term |
| **Planning** | No | Yes (multi-step) |
| **Tool Use** | No | Yes (dynamic) |
| **Decision Making** | Pattern matching | Reasoning + Planning |
| **Adaptability** | Static | Dynamic |
| **Initiative** | Waits for input | Proactive |
| **Error Handling** | Fails or returns error | Self-corrects |
| **Example** | FAQ bot | Personal assistant agent |

---

## 1.8 Single-Shot LLM vs Multi-Step Reasoning Agents

### Single-Shot LLM

**How it works**:
```
User Input → LLM → Response
```

**Example**:
```python
# Single-shot: Answer immediately
question = "What's 234 * 567?"
response = llm.invoke(question)  # May hallucinate: "132,678" (wrong!)
```

**Limitations**:
- ❌ Can't verify answers
- ❌ No tool use
- ❌ Hallucinations on math/facts
- ❌ No self-correction

---

### Multi-Step Reasoning Agent

**How it works**:
```
User Input → Planning → Tool Call → Reasoning → Verification → Response
```

**Example**:
```python
# Agent: Reasons through steps
question = "What's 234 * 567?"

# Agent's thought process (ReAct):
# Thought: I need to calculate this accurately
# Action: Use calculator tool
# Observation: 132,678
# Thought: Let me verify: 234 * 567 = 132,678 ✓
# Final Answer: 132,678
```

**Advantages**:
- ✅ Uses tools for accuracy
- ✅ Self-verifies
- ✅ Breaks complex tasks into steps
- ✅ Handles multi-hop reasoning

---

### Visual Comparison

**Single-Shot**:
```
Q: "Book me a flight to Tokyo and hotel for 3 nights"
   ↓
[LLM generates generic response]
   ↓
A: "I can't book flights, but I suggest checking Expedia..."
```

**Multi-Step Agent**:
```
Q: "Book me a flight to Tokyo and hotel for 3 nights"
   ↓
[Planning] → Break into: search flights, search hotels, book, confirm
   ↓
[Tool 1: Flight API] → Find available flights
   ↓
[Tool 2: Hotel API] → Find available hotels
   ↓
[Reasoning] → Compare prices, dates, preferences
   ↓
[Tool 3: Booking API] → Complete booking
   ↓
[Tool 4: Calendar API] → Add to calendar
   ↓
A: "Booked! Flight: UA123 (June 15), Hotel: Hilton Shinjuku (3 nights). Total: $1,847. Confirmation sent to email."
```

---

## 1.9 Intelligence vs Agency

### Key Distinction

**Intelligence**: The ability to process information and generate insights  
**Agency**: The ability to act autonomously toward goals

| Aspect | Intelligence | Agency |
|--------|-------------|--------|
| **Definition** | Reasoning capability | Autonomous action |
| **Example** | "I know how to book a flight" | "I booked the flight" |
| **Measurement** | Benchmark scores (MMLU, HumanEval) | Task completion rate |
| **Core Capability** | Understanding, reasoning | Planning, execution |
| **Human Analogy** | Genius who never acts | Effective executor |

### The Agent Formula

```
Effective Agent = Intelligence + Agency + Tools + Memory

Where:
- Intelligence: LLM reasoning
- Agency: Autonomous decision-making
- Tools: APIs, functions, databases
- Memory: Context + Learning
```

### Example Comparison

**High Intelligence, Low Agency** (GPT-4 without tools):
```
Q: "What's the current stock price of NVDA?"
A: "I don't have real-time data, but as of my last update in January 2025..."
```

**High Intelligence, High Agency** (Stock Agent with tools):
```
Q: "What's the current stock price of NVDA?"

[Agent Process]:
1. Calls stock API
2. Retrieves current price
3. Analyzes trend
4. Provides context

A: "NVDA is currently trading at $487.32 (+2.3% today). It's up 15% this month driven by strong AI chip demand. The stock is approaching its 52-week high."
```

---

## 1.10 Characteristics of Agentic Systems

### 1. **Planning**

**Definition**: The ability to decompose complex goals into executable sub-tasks.

**Example**:
```
Goal: "Organize a team meeting"

Planning:
├── Step 1: Find available time slots for all participants
├── Step 2: Book conference room
├── Step 3: Send calendar invites
├── Step 4: Prepare agenda
└── Step 5: Share pre-read materials
```

**Types of Planning**:
- **Forward Planning**: Start → End (sequential steps)
- **Backward Planning**: End → Start (goal decomposition)
- **Hierarchical Planning**: High-level → Low-level tasks
- **Reactive Planning**: Adjust plans based on feedback

**Code Example**:
```python
class PlanningAgent:
    def plan(self, goal):
        # Decompose goal into sub-goals
        sub_goals = self.decompose(goal)
        
        # Order sub-goals
        plan = self.order_tasks(sub_goals)
        
        # Assign tools to each step
        executable_plan = self.assign_tools(plan)
        
        return executable_plan
```

---

### 2. **Reasoning**

**Definition**: Multi-step logical inference to solve problems.

**Reasoning Patterns**:

**a) Deductive Reasoning**:
```
Premise 1: All ML models need data
Premise 2: This is an ML model
Conclusion: This model needs data
```

**b) Inductive Reasoning**:
```
Observation 1: Model A performed well with 10K samples
Observation 2: Model B performed well with 10K samples
Conclusion: 10K samples is likely sufficient
```

**c) Abductive Reasoning**:
```
Observation: Model accuracy dropped suddenly
Best Explanation: Data distribution shifted
```

**Chain-of-Thought Example**:
```python
# Question: "If a company's revenue grew 20% and expenses grew 30%, is it profitable?"

# Agent's reasoning:
step1 = "Let's assume revenue = 100, expenses = 80 initially"
step2 = "After growth: revenue = 120, expenses = 104"
step3 = "Profit = Revenue - Expenses = 120 - 104 = 16"
step4 = "Yes, still profitable, but profit margin decreased"
```

---

### 3. **Memory**

**Definition**: The ability to store and retrieve information across interactions.

**Memory Types**:

| Type | Duration | Example | Implementation |
|------|----------|---------|----------------|
| **Working Memory** | Current session | Variables in a function | Python variables |
| **Short-term Memory** | Minutes to hours | Conversation context | Message history |
| **Long-term Memory** | Days to forever | User preferences | Vector database |
| **Episodic Memory** | Specific events | "Last time user asked about X" | Timestamped logs |
| **Semantic Memory** | General knowledge | "User prefers Python" | Structured database |

**Code Example**:
```python
class MemoryEnabledAgent:
    def __init__(self):
        self.working_memory = {}  # Current task context
        self.short_term = ConversationBuffer(k=10)  # Last 10 messages
        self.long_term = VectorStore()  # Persistent memory
    
    def remember(self, key, value, memory_type="short_term"):
        if memory_type == "short_term":
            self.short_term.add({key: value})
        elif memory_type == "long_term":
            self.long_term.add_document(f"{key}: {value}")
    
    def recall(self, query):
        # Search long-term memory
        relevant_memories = self.long_term.similarity_search(query, k=3)
        return relevant_memories
```

---

### 4. **Tool Usage**

**Definition**: The ability to extend capabilities through external tools and APIs.

**Common Tools**:
```
├── Information Retrieval
│   ├── Web search (Google, Bing)
│   ├── Database queries (SQL)
│   └── Vector search (similarity)
├── Computation
│   ├── Calculator
│   ├── Code interpreter
│   └── Symbolic math (WolframAlpha)
├── Communication
│   ├── Email (Gmail API)
│   ├── Messaging (Slack, Teams)
│   └── Notifications
├── Data Manipulation
│   ├── File operations
│   ├── Image processing
│   └── Data analysis
└── External Services
    ├── Payment (Stripe)
    ├── Calendar (Google Calendar)
    └── CRM (Salesforce)
```

**Tool Calling Example**:
```python
tools = [
    {
        "name": "get_weather",
        "description": "Get current weather for a location",
        "parameters": {
            "location": {"type": "string", "description": "City name"}
        }
    },
    {
        "name": "calculator",
        "description": "Perform mathematical calculations",
        "parameters": {
            "expression": {"type": "string", "description": "Math expression"}
        }
    }
]

# Agent decides which tool to use
user_query = "What's the weather in Paris and what's 15% of 230?"

# Agent reasoning:
# → Need weather data → call get_weather(location="Paris")
# → Need calculation → call calculator(expression="0.15 * 230")
```

---

### 5. **Reflection**

**Definition**: The ability to evaluate one's own outputs and self-correct.

**Reflection Loop**:
```
Action → Outcome → Evaluation → Learning → Improved Action
```

**Example**:
```python
class ReflectiveAgent:
    def execute_with_reflection(self, task):
        # Initial attempt
        result = self.execute(task)
        
        # Self-evaluation
        critique = self.critique(result)
        
        # If not satisfactory, refine
        if critique['satisfactory'] == False:
            improvements = critique['suggestions']
            result = self.refine(result, improvements)
        
        return result
    
    def critique(self, output):
        # Ask LLM to evaluate its own output
        evaluation = self.llm.invoke(
            f"Evaluate this output: {output}\n"
            f"Is it accurate? Complete? Well-structured?\n"
            f"Provide critique and suggestions."
        )
        return evaluation
```

**Reflection Patterns**:
- **Self-Consistency**: Generate multiple answers, pick most common
- **Critique-Revise**: Evaluate → Improve → Repeat
- **Chain of Verification**: Fact-check each claim
- **Adversarial Validation**: Try to find flaws in own reasoning

---

### 6. **Decision Making**

**Definition**: Choosing optimal actions under uncertainty.

**Decision Framework**:
```python
def decide(options, context):
    # Evaluate each option
    scored_options = [
        (option, evaluate(option, context)) 
        for option in options
    ]
    
    # Select best option
    best_option = max(scored_options, key=lambda x: x[1])
    
    return best_option[0]

def evaluate(option, context):
    return (
        utility_score(option, context) * 0.4 +
        feasibility_score(option) * 0.3 +
        safety_score(option) * 0.3
    )
```

**Decision Types**:
| Type | Description | Example |
|------|-------------|---------|
| **Deterministic** | Clear rules | "If price < $100, buy" |
| **Probabilistic** | Based on likelihood | "70% chance of success → proceed" |
| **Multi-criteria** | Balance multiple factors | "Optimize cost, quality, time" |
| **Sequential** | Series of decisions | "Decision tree navigation" |

---

### 7. **Autonomy**

**Definition**: Operating independently with minimal human intervention.

**Levels of Autonomy**:

| Level | Description | Human Role | Example |
|-------|-------------|------------|---------|
| **0 - Manual** | No automation | Does everything | Writing code manually |
| **1 - Assisted** | Suggests actions | Approves each action | Code completion |
| **2 - Partial** | Executes simple tasks | Approves complex actions | Auto-save documents |
| **3 - Conditional** | Handles most tasks | Intervenes on edge cases | Email filtering |
| **4 - High** | Fully autonomous | Monitors only | Autonomous trading bot |
| **5 - Full** | Complete independence | No monitoring | AGI (theoretical) |

**Autonomy Spectrum**:
```
Human-in-the-loop → Human-on-the-loop → Human-off-the-loop

Examples:
- Research Agent (Level 3): Searches, summarizes, asks for approval before sending
- Trading Agent (Level 4): Executes trades autonomously within risk limits
- AGI (Level 5): Completely independent (not yet achieved)
```

---

### 8. **Goal-Oriented Behavior**

**Definition**: All actions directed toward achieving specified objectives.

**Goal Hierarchy**:
```
Ultimate Goal: "Increase customer satisfaction"
    ↓
Sub-Goal 1: "Reduce response time"
    ├── Task 1.1: Implement chatbot
    └── Task 1.2: Train support staff
    ↓
Sub-Goal 2: "Improve product quality"
    ├── Task 2.1: Gather feedback
    └── Task 2.2: Implement fixes
```

**Goal Specification**:
```python
goal = {
    "objective": "Book cheapest flight to Tokyo",
    "constraints": [
        "Departure: Next Monday",
        "Max budget: $1000",
        "Prefer direct flights"
    ],
    "success_criteria": [
        "Booking confirmed",
        "Price within budget",
        "Calendar updated"
    ]
}
```

---

## 1.11 Summary: What Makes AI "Agentic"?

### The Agentic Checklist

An AI system is **agentic** if it demonstrates:

- ✅ **Autonomy**: Acts independently
- ✅ **Planning**: Decomposes complex goals
- ✅ **Reasoning**: Multi-step logical inference
- ✅ **Tool Use**: Leverages external capabilities
- ✅ **Memory**: Maintains context and learns
- ✅ **Reflection**: Self-evaluates and improves
- ✅ **Decision Making**: Chooses optimal actions
- ✅ **Goal-Oriented**: All actions serve objectives

### Example: Agentic vs Non-Agentic

**Non-Agentic (Simple Chatbot)**:
```
User: "Help me plan my day"
Bot: "Sure! What would you like to do?"
[Waits for user to provide details]
```

**Agentic (Personal Assistant)**:
```
User: "Help me plan my day"

Agent Process:
1. Retrieves calendar events [Memory]
2. Checks email for important tasks [Tool Use]
3. Analyzes priorities [Reasoning]
4. Creates optimized schedule [Planning]
5. Books meeting rooms [Tool Use]
6. Sends agenda to participants [Action]
7. Verifies all bookings [Reflection]

Agent: "I've organized your day:
- 9 AM: Team standup (Room A, agenda sent)
- 10 AM: Focus time for project review
- 12 PM: Lunch with client (reservation at Restaurant X)
- 2 PM: Budget planning meeting
- 4 PM: Free time for emails
All events added to your calendar. Want me to adjust anything?"
```

---

<a name="section-2"></a>
# SECTION 2 — HOW AGENTIC AI WORKS

## 2.1 Complete Agent Workflow

### The Agent Execution Cycle

```
┌─────────────────────────────────────────────────────────────┐
│                     USER QUERY                               │
│                    "Research quantum computing"              │
└────────────────────┬────────────────────────────────────────┘
                     ↓
            ┌────────────────┐
            │   PLANNING     │  ← Decompose into sub-tasks
            └────────┬───────┘
                     ↓
            ┌────────────────┐
            │   REASONING    │  ← Decide approach & tools
            └────────┬───────┘
                     ↓
            ┌────────────────┐
            │  TOOL CALLING  │  ← Execute searches, calculations
            └────────┬───────┘
                     ↓
            ┌────────────────┐
            │     MEMORY     │  ← Store intermediate results
            └────────┬───────┘
                     ↓
            ┌────────────────┐
            │   REFLECTION   │  ← Evaluate quality, self-correct
            └────────┬───────┘
                     ↓
            ┌────────────────┐
            │ FINAL OUTPUT   │  ← Synthesized response
            └────────────────┘
```

### Detailed Step-by-Step Breakdown

#### **Step 1: User Query Reception**
```python
user_query = "Research the latest developments in quantum computing and create a summary report"
```

#### **Step 2: Planning**
```
Agent's Plan:
1. Search for recent quantum computing papers
2. Identify key trends and breakthroughs
3. Analyze implications
4. Synthesize into coherent report
5. Validate accuracy
```

#### **Step 3: Reasoning**
```
Agent thinks:
- "I need to search academic databases and news"
- "I should focus on last 6 months for 'latest'"
- "I'll need to use Google Scholar API and arXiv API"
- "After gathering, I'll use text analysis to identify trends"
```

#### **Step 4: Tool Calling**
```python
# Tool 1: Search arXiv
results_arxiv = search_arxiv(
    query="quantum computing", 
    date_from="2025-11-01"
)

# Tool 2: Search Google Scholar
results_scholar = search_scholar(
    query="quantum computing breakthroughs 2026"
)

# Tool 3: Web search for industry news
results_web = web_search(
    query="quantum computing news 2026"
)
```

#### **Step 5: Memory**
```python
# Store intermediate results
memory.store({
    "arxiv_results": results_arxiv,
    "scholar_results": results_scholar,
    "web_results": results_web,
    "timestamp": "2026-05-19"
})
```

#### **Step 6: Reflection**
```python
# Agent self-evaluates
critique = self.reflect(gathered_data)
# "Have I covered major areas? (algorithms, hardware, applications)"
# "Are sources credible?"
# "Is the data recent enough?"
# "Do I need more information on quantum error correction?"

if critique.needs_improvement:
    additional_search("quantum error correction 2026")
```

#### **Step 7: Final Output**
```
Synthesized Report:
─────────────────────
QUANTUM COMPUTING DEVELOPMENTS: Q4 2025 - Q2 2026

Key Breakthroughs:
1. Google achieved 100-qubit coherence (Nature, March 2026)
2. IBM demonstrated error-corrected quantum computation (Science, Jan 2026)
3. Quantum advantage in drug discovery (Harvard study, April 2026)

Emerging Trends:
- Focus shifting from qubit count to error correction
- Commercial applications in pharmaceutical industry
- Integration with classical ML systems

Future Outlook:
...

Sources: [10 papers cited with links]
```

---

## 2.2 Agent Lifecycle

### State Diagram

```
┌─────────┐
│  IDLE   │ ← Agent waiting for input
└────┬────┘
     │ User query received
     ↓
┌─────────┐
│ ACTIVE  │ ← Planning & reasoning
└────┬────┘
     │ Execute actions
     ↓
┌─────────┐
│EXECUTING│ ← Calling tools, gathering data
└────┬────┘
     │ Processing results
     ↓
┌─────────┐
│REFLECTING│ ← Self-evaluation
└────┬────┘
     │
     ├─→ If satisfactory → RESPONDING
     │
     └─→ If needs refinement → EXECUTING (loop)
     
┌─────────┐
│RESPONDING│ ← Delivering final output
└────┬────┘
     │
     ↓
┌─────────┐
│ LEARNING│ ← Update memory, learn from feedback
└────┬────┘
     │
     ↓
┌─────────┐
│  IDLE   │ ← Ready for next query
└─────────┘
```

### Lifecycle Code Example

```python
class AgentLifecycle:
    def __init__(self):
        self.state = "IDLE"
        self.memory = Memory()
        self.tools = ToolRegistry()
    
    def process_query(self, query):
        self.state = "ACTIVE"
        
        # Planning phase
        plan = self.create_plan(query)
        
        # Execution phase
        self.state = "EXECUTING"
        results = []
        for step in plan:
            result = self.execute_step(step)
            results.append(result)
            
            # Reflection after each step
            if self.should_reflect(step):
                self.state = "REFLECTING"
                critique = self.reflect(result)
                if critique.needs_retry:
                    result = self.retry_step(step, critique.feedback)
        
        # Response phase
        self.state = "RESPONDING"
        final_output = self.synthesize(results)
        
        # Learning phase
        self.state = "LEARNING"
        self.memory.store(query, plan, results, final_output)
        
        self.state = "IDLE"
        return final_output
```

---

## 2.3 Execution Loops

### Types of Execution Loops

#### **1. Linear Execution**
```
Step 1 → Step 2 → Step 3 → Done
```
Simple tasks with clear sequence.

#### **2. Iterative Execution (ReAct Loop)**
```
Thought → Action → Observation → Thought → Action → ... → Answer
```

**Example**:
```python
while not task_complete:
    thought = agent.reason(current_state)
    action = agent.plan_action(thought)
    observation = agent.execute(action)
    current_state = agent.update_state(observation)
    
    if agent.is_goal_achieved(current_state):
        break
```

#### **3. Parallel Execution**
```
        ┌─→ Task A ─┐
Input ──┼─→ Task B ─┼─→ Combine → Output
        └─→ Task C ─┘
```

**Example**:
```python
# Execute multiple searches simultaneously
import asyncio

async def parallel_execution(tasks):
    results = await asyncio.gather(
        search_arxiv(query),
        search_google(query),
        search_news(query)
    )
    return combine_results(results)
```

#### **4. Hierarchical Execution**
```
Main Task
├─→ Subtask 1
│   ├─→ Subtask 1.1
│   └─→ Subtask 1.2
├─→ Subtask 2
└─→ Subtask 3
```

**Example**:
```python
def hierarchical_execution(main_task):
    subtasks = decompose(main_task)
    results = []
    
    for subtask in subtasks:
        if is_complex(subtask):
            # Recursive decomposition
            sub_result = hierarchical_execution(subtask)
        else:
            sub_result = execute_simple_task(subtask)
        results.append(sub_result)
    
    return combine(results)
```

---

## 2.4 Feedback Loops

### Feedback Mechanisms

#### **1. Immediate Feedback**
```
Action → Result → Adjust → Retry
```

**Example**: API call fails → Adjust parameters → Retry

```python
def execute_with_feedback(action, max_retries=3):
    for attempt in range(max_retries):
        result = execute(action)
        
        if result.success:
            return result
        else:
            # Learn from failure
            feedback = analyze_failure(result)
            action = adjust_action(action, feedback)
    
    return "Failed after max retries"
```

#### **2. Human Feedback Loop**
```
Agent Action → Human Review → Feedback → Agent Learns
```

**Example**: Draft email → Human edits → Learn preferences

```python
def human_in_the_loop(draft):
    # Present to human
    human_edit = get_human_feedback(draft)
    
    # Learn from edits
    preferences = extract_preferences(draft, human_edit)
    memory.store_preferences(preferences)
    
    # Apply to future tasks
    return human_edit
```

#### **3. Self-Improvement Feedback**
```
Performance Metrics → Analysis → Strategy Adjustment
```

**Example**: Track success rate → Identify weak areas → Improve prompts

---

## 2.5 Self-Correction Systems

### How Agents Self-Correct

#### **Method 1: Output Validation**
```python
def validate_output(output, criteria):
    checks = {
        "completeness": is_complete(output),
        "accuracy": is_accurate(output),
        "relevance": is_relevant(output)
    }
    
    if all(checks.values()):
        return output
    else:
        # Regenerate with stricter constraints
        return regenerate(output, failed_checks=checks)
```

#### **Method 2: Multi-Path Validation (Self-Consistency)**
```python
def self_consistency(query, num_samples=5):
    # Generate multiple independent responses
    responses = [generate_response(query) for _ in range(num_samples)]
    
    # Vote or find consensus
    consensus = find_most_common(responses)
    
    return consensus
```

#### **Method 3: Chain of Verification**
```python
def verify_facts(claim):
    # Break claim into verifiable facts
    facts = extract_facts(claim)
    
    # Verify each fact
    for fact in facts:
        verification = search_and_verify(fact)
        if not verification.is_true:
            # Correct the claim
            claim = revise_claim(claim, fact, verification.correct_info)
    
    return claim
```

---

## 2.6 Multi-Step Reasoning

### Reasoning Patterns

#### **1. Chain-of-Thought (CoT)**

**Linear step-by-step reasoning**:

```
Problem: "A store had 20 apples. They sold 30% in the morning and 40% of the remainder in the afternoon. How many are left?"

CoT Reasoning:
Step 1: Calculate morning sales: 20 × 0.30 = 6 apples sold
Step 2: Remainder after morning: 20 - 6 = 14 apples
Step 3: Calculate afternoon sales: 14 × 0.40 = 5.6 ≈ 6 apples sold
Step 4: Final remainder: 14 - 6 = 8 apples
Answer: 8 apples
```

**Implementation**:
```python
def chain_of_thought(problem):
    prompt = f"""
    Solve this step by step:
    {problem}
    
    Think through each step clearly.
    """
    
    response = llm.invoke(prompt)
    return response
```

---

#### **2. Tree-of-Thought (ToT)**

**Explores multiple reasoning paths**:

```
Problem: "Design a marketing campaign for a new product"

        [Initial Problem]
              /    |    \
        Path A  Path B  Path C
       (Social) (Email) (Events)
          /\       /\       /\
        A1 A2   B1 B2   C1 C2
        
Evaluate each path → Select best
```

**Implementation**:
```python
def tree_of_thought(problem, branching_factor=3, depth=2):
    # Generate multiple initial thoughts
    thoughts = generate_thoughts(problem, k=branching_factor)
    
    # Evaluate each thought
    scored_thoughts = [(t, evaluate(t)) for t in thoughts]
    
    # Select best thoughts
    best_thoughts = sorted(scored_thoughts, key=lambda x: x[1], reverse=True)[:branching_factor]
    
    # If at max depth, return best
    if depth == 0:
        return best_thoughts[0][0]
    
    # Otherwise, expand best thoughts recursively
    results = []
    for thought, score in best_thoughts:
        result = tree_of_thought(thought, branching_factor, depth-1)
        results.append((result, score))
    
    return max(results, key=lambda x: x[1])[0]
```

---

#### **3. Graph-of-Thought (GoT)**

**Non-linear reasoning with dependencies**:

```
    [Fact A] ──→ [Inference 1] ──┐
       ↓                          ↓
    [Fact B] ──→ [Inference 2] → [Conclusion]
       ↓                          ↑
    [Fact C] ──→ [Inference 3] ──┘
```

**Use Case**: Complex analysis requiring multiple interconnected insights

---

## 2.7 Task Decomposition

### Decomposition Strategies

#### **1. Sequential Decomposition**
```
Complex Task
  → Step 1: Data collection
  → Step 2: Data analysis
  → Step 3: Report generation
```

#### **2. Hierarchical Decomposition**
```
Build Website
├── Design
│   ├── Wireframe
│   ├── Mockup
│   └── User testing
├── Development
│   ├── Frontend
│   ├── Backend
│   └── Database
└── Deployment
    ├── Testing
    ├── Launch
    └── Monitoring
```

#### **3. Functional Decomposition**
```
E-commerce System
├── User Management (Authentication, Profiles)
├── Product Catalog (Search, Display, Filter)
├── Shopping Cart (Add, Remove, Update)
├── Payment Processing (Gateway, Verification)
└── Order Management (Track, Fulfill, Return)
```

### Decomposition Algorithm

```python
def decompose_task(task, max_complexity=10):
    if complexity(task) < max_complexity:
        # Task is simple enough to execute directly
        return [task]
    else:
        # Break down into subtasks
        subtasks = identify_subtasks(task)
        
        # Recursively decompose complex subtasks
        all_subtasks = []
        for subtask in subtasks:
            all_subtasks.extend(decompose_task(subtask, max_complexity))
        
        return all_subtasks

# Example usage
task = "Build machine learning model for customer churn prediction"
subtasks = decompose_task(task)

# Output:
# [
#   "Collect historical customer data",
#   "Clean and preprocess data",
#   "Perform exploratory data analysis",
#   "Engineer relevant features",
#   "Split data into train/test sets",
#   "Train multiple candidate models",
#   "Evaluate and compare models",
#   "Select best model",
#   "Deploy model to production"
# ]
```

---

## 2.8 Planning Systems

### Planning Approaches

#### **1. Forward Planning (Start → Goal)**
```python
def forward_planning(current_state, goal_state):
    plan = []
    state = current_state
    
    while state != goal_state:
        # Find action that moves closer to goal
        action = find_best_action(state, goal_state)
        plan.append(action)
        state = apply_action(state, action)
    
    return plan
```

#### **2. Backward Planning (Goal → Start)**
```python
def backward_planning(goal_state, current_state):
    plan = []
    state = goal_state
    
    while state != current_state:
        # Find action that could have led to this state
        action = find_prerequisite_action(state)
        plan.insert(0, action)  # Prepend to plan
        state = reverse_action(state, action)
    
    return plan
```

#### **3. Hierarchical Task Network (HTN)**
```python
def htn_planning(task):
    if is_primitive(task):
        return execute(task)
    else:
        # Decompose into subtasks
        method = select_method(task)
        subtasks = method.decompose(task)
        
        # Plan for each subtask
        plan = []
        for subtask in subtasks:
            plan.extend(htn_planning(subtask))
        
        return plan
```

---

## 2.9 Autonomous Decision Making

### Decision-Making Framework

```python
class AutonomousDecisionMaker:
    def decide(self, situation, options):
        # 1. Understand the situation
        context = self.analyze_context(situation)
        
        # 2. Identify constraints
        constraints = self.extract_constraints(situation)
        
        # 3. Evaluate each option
        evaluated_options = []
        for option in options:
            score = self.evaluate_option(option, context, constraints)
            evaluated_options.append((option, score))
        
        # 4. Select best option
        best_option = max(evaluated_options, key=lambda x: x[1])
        
        # 5. Verify decision
        if self.is_safe_decision(best_option[0]):
            return best_option[0]
        else:
            return self.ask_human(situation, options)
    
    def evaluate_option(self, option, context, constraints):
        # Multi-criteria evaluation
        utility = self.calculate_utility(option, context)
        feasibility = self.check_feasibility(option, constraints)
        risk = self.assess_risk(option)
        
        # Weighted score
        score = (
            utility * 0.5 +
            feasibility * 0.3 -
            risk * 0.2
        )
        
        return score
```

---

## 2.10 ReAct Architecture

### What is ReAct?

**ReAct** = **Reasoning** + **Acting**

Combines reasoning traces with task-specific actions.

### ReAct Loop

```
Thought: [Agent reasons about what to do next]
    ↓
Action: [Agent executes a tool or function]
    ↓
Observation: [Agent observes the result]
    ↓
[Repeat until goal is achieved]
    ↓
Final Answer: [Agent provides final response]
```

### ReAct Example

**Query**: "What's the population of the capital of France?"

```
Thought 1: I need to find the capital of France first
Action 1: Search[capital of France]
Observation 1: Paris is the capital of France

Thought 2: Now I need to find the population of Paris
Action 2: Search[population of Paris]
Observation 2: Paris has a population of approximately 2.2 million

Thought 3: I have the answer now
Final Answer: The population of Paris, the capital of France, is approximately 2.2 million
```

### ReAct Implementation

```python
def react_agent(query, tools, max_iterations=10):
    context = {"query": query, "history": []}
    
    for i in range(max_iterations):
        # Reasoning step
        thought = generate_thought(context)
        context["history"].append(("Thought", thought))
        
        # Check if we have the answer
        if should_stop(thought):
            final_answer = extract_answer(thought)
            return final_answer
        
        # Action step
        action = decide_action(thought, tools)
        context["history"].append(("Action", action))
        
        # Observation step
        observation = execute_action(action)
        context["history"].append(("Observation", observation))
        
        # Update context with new information
        context["latest_observation"] = observation
    
    return "Could not find answer within iteration limit"

def generate_thought(context):
    prompt = f"""
    Query: {context['query']}
    
    History:
    {format_history(context['history'])}
    
    What should I do next? Think step by step.
    """
    
    return llm.invoke(prompt)

def decide_action(thought, tools):
    prompt = f"""
    Given this thought: {thought}
    
    Available tools:
    {format_tools(tools)}
    
    Which tool should I use and with what input?
    Format: Tool[input]
    """
    
    action_string = llm.invoke(prompt)
    return parse_action(action_string)
```

---

## 2.11 State Management

### Agent State Components

```python
class AgentState:
    def __init__(self):
        self.conversation_history = []
        self.working_memory = {}
        self.long_term_memory = VectorStore()
        self.tool_results = {}
        self.current_plan = []
        self.execution_trace = []
        self.user_preferences = {}
    
    def update(self, key, value):
        self.working_memory[key] = value
    
    def get(self, key):
        return self.working_memory.get(key)
    
    def add_to_history(self, role, content):
        self.conversation_history.append({
            "role": role,
            "content": content,
            "timestamp": datetime.now()
        })
```

### State Persistence

```python
class PersistentAgentState:
    def save_state(self, state, checkpoint_id):
        # Serialize state
        state_dict = {
            "conversation_history": state.conversation_history,
            "working_memory": state.working_memory,
            "current_plan": state.current_plan,
            "execution_trace": state.execution_trace
        }
        
        # Save to database or file
        with open(f"checkpoints/{checkpoint_id}.json", "w") as f:
            json.dump(state_dict, f)
    
    def load_state(self, checkpoint_id):
        # Load from storage
        with open(f"checkpoints/{checkpoint_id}.json", "r") as f:
            state_dict = json.load(f)
        
        # Reconstruct state
        state = AgentState()
        state.conversation_history = state_dict["conversation_history"]
        state.working_memory = state_dict["working_memory"]
        state.current_plan = state_dict["current_plan"]
        state.execution_trace = state_dict["execution_trace"]
        
        return state
```

---

## 2.12 Context Windows and Long-Term Memory

### Context Window Challenges

**Problem**: LLMs have limited context windows (e.g., 128K tokens for GPT-4)

**Solution**: Intelligent memory management

```python
class ContextManager:
    def __init__(self, max_tokens=100000):
        self.max_tokens = max_tokens
        self.critical_context = []  # Always included
        self.working_context = []   # Recent interactions
        self.long_term_memory = VectorStore()  # Searchable history
    
    def build_context(self, current_query):
        # 1. Critical context (system prompts, user profile)
        context = self.critical_context.copy()
        
        # 2. Retrieve relevant long-term memories
        relevant_memories = self.long_term_memory.search(
            current_query, 
            k=5
        )
        context.extend(relevant_memories)
        
        # 3. Add recent working context
        context.extend(self.working_context[-10:])  # Last 10 interactions
        
        # 4. Trim if exceeds limit
        if count_tokens(context) > self.max_tokens:
            context = self.truncate_intelligently(context)
        
        return context
    
    def truncate_intelligently(self, context):
        # Prioritize: critical > relevant memories > recent context
        # Use sliding window + summarization
        return truncated_context
```

---

## 2.13 Retrieval-Augmented Generation (RAG) Inside Agents

### RAG Integration

```python
class RAGEnabledAgent:
    def __init__(self, knowledge_base):
        self.llm = ChatOpenAI()
        self.retriever = knowledge_base.as_retriever()
        self.memory = ConversationBufferMemory()
    
    def answer_query(self, query):
        # 1. Retrieve relevant documents
        relevant_docs = self.retriever.get_relevant_documents(query)
        
        # 2. Build context with retrieved information
        context = self.build_context(relevant_docs)
        
        # 3. Generate response using LLM
        prompt = f"""
        Context: {context}
        
        Query: {query}
        
        Provide a detailed answer based on the context.
        """
        
        response = self.llm.invoke(prompt)
        
        # 4. Store in memory
        self.memory.save_context(
            {"input": query}, 
            {"output": response}
        )
        
        return response
```

---

## 2.14 Event-Driven Agents

### Event-Driven Architecture

```python
class EventDrivenAgent:
    def __init__(self):
        self.event_handlers = {}
        self.event_queue = Queue()
    
    def register_handler(self, event_type, handler):
        self.event_handlers[event_type] = handler
    
    def trigger_event(self, event):
        self.event_queue.put(event)
    
    def run(self):
        while True:
            event = self.event_queue.get()
            handler = self.event_handlers.get(event.type)
            
            if handler:
                handler(event.data)

# Example usage
agent = EventDrivenAgent()

# Register handlers
agent.register_handler("email_received", process_email)
agent.register_handler("calendar_updated", sync_schedule)
agent.register_handler("deadline_approaching", send_reminder)

# Trigger events
agent.trigger_event(Event("email_received", email_data))
```

---

## 2.15 Workflow Orchestration

### Orchestration Patterns

#### **Pattern 1: Sequential Workflow**
```python
def sequential_workflow(tasks):
    results = []
    for task in tasks:
        result = execute_task(task)
        results.append(result)
    return results
```

#### **Pattern 2: Parallel Workflow**
```python
async def parallel_workflow(tasks):
    results = await asyncio.gather(*[execute_task(task) for task in tasks])
    return results
```

#### **Pattern 3: Conditional Workflow**
```python
def conditional_workflow(input_data):
    if meets_condition_A(input_data):
        return workflow_A(input_data)
    elif meets_condition_B(input_data):
        return workflow_B(input_data)
    else:
        return default_workflow(input_data)
```

#### **Pattern 4: Fan-Out/Fan-In**
```python
def fan_out_fan_in(input_data):
    # Fan-out: Split work
    subtasks = split_into_subtasks(input_data)
    
    # Parallel execution
    results = parallel_workflow(subtasks)
    
    # Fan-in: Combine results
    final_result = combine_results(results)
    return final_result
```

---

## 2.16 How LLMs Function as the "Brain" of Agents

### LLM Capabilities for Agents

| Capability | Role in Agent | Example |
|------------|---------------|---------|
| **Language Understanding** | Parse user intent | "Book a flight" → Intent: booking, Entity: flight |
| **Reasoning** | Plan and decompose tasks | Complex goal → Subtasks |
| **Code Generation** | Create executable actions | Generate API calls |
| **Function Calling** | Decide which tools to use | Choose between search/calculator/email |
| **Context Maintenance** | Track conversation state | Remember previous questions |
| **Synthesis** | Combine information | Merge results from multiple sources |

### LLM as Decision-Maker

```python
def llm_decision_maker(situation, options):
    prompt = f"""
    Situation: {situation}
    
    Available options:
    {json.dumps(options, indent=2)}
    
    Analyze the situation and select the best option.
    Consider: effectiveness, cost, time, risks.
    
    Format your response as:
    {{
        "selected_option": <option_id>,
        "reasoning": <explanation>
    }}
    """
    
    response = llm.invoke(prompt)
    decision = json.loads(response)
    
    return decision
```

---

## 2.17 Why Tools Are Important

### The Tool Multiplier Effect

**Without Tools**:
```
LLM alone → Limited to knowledge cutoff + reasoning
```

**With Tools**:
```
LLM + Tools → Knowledge cutoff + reasoning + real-time data + computation + actions
```

### Tool Categories

```
Information Tools
├── Web Search (current information)
├── Database Query (structured data)
├── API Calls (external services)
└── Document Retrieval (knowledge bases)

Computation Tools
├── Calculator (arithmetic)
├── Code Interpreter (complex calculations)
├── Symbolic Math (algebra, calculus)
└── Data Analysis (statistics, ML)

Action Tools
├── Email (communication)
├── Calendar (scheduling)
├── File Operations (create, edit, delete)
└── Payment (transactions)

Validation Tools
├── Fact-Checker (verify claims)
├── Spell-Checker (correct text)
└── Data Validator (check formats)
```

### Tool Integration Example

```python
tools = [
    {
        "name": "google_search",
        "description": "Search the web for current information",
        "function": google_search
    },
    {
        "name": "calculator",
        "description": "Perform mathematical calculations",
        "function": calculate
    },
    {
        "name": "python_repl",
        "description": "Execute Python code",
        "function": execute_python
    },
    {
        "name": "email_sender",
        "description": "Send emails",
        "function": send_email
    }
]

agent = create_agent(llm, tools)

# Agent can now:
# - Search for real-time information
# - Perform accurate calculations
# - Execute complex data analysis
# - Take actions (send emails)
```

---

<a name="section-3"></a>
# SECTION 3 — AGENTIC AI ARCHITECTURE

## 3.1 Core Components of Agentic AI Systems

### Complete Architecture Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                        USER INTERFACE                            │
│                    (Chat, API, Web App)                          │
└──────────────────────┬──────────────────────────────────────────┘
                       ↓
┌─────────────────────────────────────────────────────────────────┐
│                    ORCHESTRATION LAYER                           │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐       │
│  │  Router  │  │ Planner  │  │ Executor │  │ Monitor  │       │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘       │
└──────────────────────┬──────────────────────────────────────────┘
                       ↓
┌─────────────────────────────────────────────────────────────────┐
│                      AGENT CORE                                  │
│  ┌────────────────┐  ┌──────────────┐  ┌──────────────┐        │
│  │ LLM (Brain)    │  │ Memory Mgr   │  │ Reflection   │        │
│  │ - Reasoning    │  │ - Short-term │  │ - Critique   │        │
│  │ - Decision     │  │ - Long-term  │  │ - Validation │        │
│  │ - Generation   │  │ - Retrieval  │  │ - Learning   │        │
│  └────────────────┘  └──────────────┘  └──────────────┘        │
└──────────────────────┬──────────────────────────────────────────┘
                       ↓
┌─────────────────────────────────────────────────────────────────┐
│                      TOOL LAYER                                  │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐       │
│  │  Search  │  │   APIs   │  │   Code   │  │   DB     │       │
│  │  Engine  │  │  (REST)  │  │Execution │  │  Query   │       │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘       │
└──────────────────────┬──────────────────────────────────────────┘
                       ↓
┌─────────────────────────────────────────────────────────────────┐
│                    DATA & KNOWLEDGE LAYER                        │
│  ┌───────────────┐  ┌──────────────┐  ┌──────────────┐         │
│  │ Vector Store  │  │  Databases   │  │ Knowledge    │         │
│  │ (Embeddings)  │  │  (SQL/NoSQL) │  │ Graphs       │         │
│  └───────────────┘  └──────────────┘  └──────────────┘         │
└─────────────────────────────────────────────────────────────────┘
```

---

## 3.2 Component Details

### 3.2.1 Planner

**Role**: Decomposes goals into executable action sequences

```python
class Planner:
    def __init__(self, llm):
        self.llm = llm
    
    def create_plan(self, goal, context):
        """
        Decomposes goal into actionable steps
        """
        prompt = f"""
        Goal: {goal}
        
        Context: {context}
        
        Create a detailed step-by-step plan to achieve this goal.
        Consider dependencies, order of operations, and resource requirements.
        
        Format as:
        1. Step description [Tool needed] [Estimated time]
        """
        
        plan_text = self.llm.invoke(prompt)
        plan = self.parse_plan(plan_text)
        
        return plan
    
    def parse_plan(self, plan_text):
        # Parse into structured format
        steps = []
        for line in plan_text.split('\n'):
            if line.strip():
                step = {
                    "description": extract_description(line),
                    "tool": extract_tool(line),
                    "estimated_time": extract_time(line),
                    "dependencies": []
                }
                steps.append(step)
        
        return steps
```

---

### 3.2.2 Executor

**Role**: Executes planned actions and manages tool calls

```python
class Executor:
    def __init__(self, tools):
        self.tools = {tool.name: tool for tool in tools}
        self.execution_trace = []
    
    def execute_plan(self, plan):
        results = []
        
        for step in plan:
            try:
                result = self.execute_step(step)
                results.append({
                    "step": step,
                    "result": result,
                    "status": "success"
                })
            except Exception as e:
                results.append({
                    "step": step,
                    "error": str(e),
                    "status": "failed"
                })
                # Attempt recovery or ask for help
                recovery_action = self.handle_failure(step, e)
                if recovery_action:
                    results.append(recovery_action)
        
        return results
    
    def execute_step(self, step):
        tool_name = step["tool"]
        tool = self.tools.get(tool_name)
        
        if not tool:
            raise ValueError(f"Tool {tool_name} not found")
        
        # Execute tool with parameters
        result = tool.run(step["parameters"])
        
        # Log execution
        self.execution_trace.append({
            "step": step,
            "result": result,
            "timestamp": datetime.now()
        })
        
        return result
```

---

### 3.2.3 Memory Manager

**Role**: Manages short-term and long-term memory

```python
class MemoryManager:
    def __init__(self):
        self.short_term = ConversationBuffer(max_tokens=2000)
        self.long_term = VectorStore()
        self.episodic = []  # Specific events
        self.semantic = {}  # General knowledge
    
    def remember_short_term(self, interaction):
        """Store in working memory"""
        self.short_term.add_message(interaction)
    
    def remember_long_term(self, key, value, metadata=None):
        """Store in persistent memory"""
        document = {
            "key": key,
            "value": value,
            "metadata": metadata or {},
            "timestamp": datetime.now()
        }
        self.long_term.add_document(document)
    
    def remember_episode(self, event):
        """Store specific event"""
        self.episodic.append({
            "event": event,
            "timestamp": datetime.now()
        })
    
    def recall(self, query, memory_type="all"):
        """Retrieve relevant memories"""
        results = {}
        
        if memory_type in ["short_term", "all"]:
            results["short_term"] = self.short_term.get_recent(k=5)
        
        if memory_type in ["long_term", "all"]:
            results["long_term"] = self.long_term.similarity_search(query, k=3)
        
        if memory_type in ["episodic", "all"]:
            results["episodic"] = [
                e for e in self.episodic
                if self.is_relevant(e, query)
            ]
        
        return results
```

---

### 3.2.4 Tool Manager

**Role**: Registry and orchestration of available tools

```python
class ToolManager:
    def __init__(self):
        self.tools = {}
        self.tool_usage_stats = {}
    
    def register_tool(self, tool):
        """Register a new tool"""
        self.tools[tool.name] = tool
        self.tool_usage_stats[tool.name] = {
            "calls": 0,
            "successes": 0,
            "failures": 0,
            "avg_latency": 0
        }
    
    def get_tool(self, name):
        """Retrieve tool by name"""
        return self.tools.get(name)
    
    def execute_tool(self, name, **kwargs):
        """Execute tool and track metrics"""
        tool = self.get_tool(name)
        if not tool:
            raise ValueError(f"Tool {name} not found")
        
        start_time = time.time()
        
        try:
            result = tool.run(**kwargs)
            self.tool_usage_stats[name]["successes"] += 1
            status = "success"
        except Exception as e:
            self.tool_usage_stats[name]["failures"] += 1
            status = "failure"
            raise e
        finally:
            latency = time.time() - start_time
            self.update_latency(name, latency)
            self.tool_usage_stats[name]["calls"] += 1
        
        return result
    
    def list_tools(self):
        """Return available tools with descriptions"""
        return [
            {
                "name": name,
                "description": tool.description,
                "parameters": tool.parameters
            }
            for name, tool in self.tools.items()
        ]
```

---

### 3.2.5 Reflection/Critic Module

**Role**: Self-evaluation and quality control

```python
class ReflectionModule:
    def __init__(self, llm):
        self.llm = llm
        self.critique_history = []
    
    def critique_output(self, output, criteria):
        """Evaluate output quality"""
        prompt = f"""
        Evaluate the following output:
        
        Output: {output}
        
        Evaluation Criteria:
        {json.dumps(criteria, indent=2)}
        
        Provide:
        1. Score (0-10) for each criterion
        2. Strengths and weaknesses
        3. Suggestions for improvement
        4. Overall assessment (pass/fail)
        
        Format as JSON.
        """
        
        critique = self.llm.invoke(prompt)
        parsed_critique = json.loads(critique)
        
        self.critique_history.append({
            "output": output,
            "critique": parsed_critique,
            "timestamp": datetime.now()
        })
        
        return parsed_critique
    
    def should_refine(self, critique):
        """Determine if output needs refinement"""
        overall_score = critique.get("overall_score", 0)
        return overall_score < 7  # Threshold
    
    def generate_refinement_suggestions(self, critique):
        """Extract actionable improvements"""
        suggestions = critique.get("suggestions", [])
        weaknesses = critique.get("weaknesses", [])
        
        return {
            "priority_fixes": weaknesses[:3],
            "improvement_ideas": suggestions,
            "focus_areas": self.identify_focus_areas(critique)
        }
```

---

### 3.2.6 Router

**Role**: Directs queries to appropriate agents or workflows

```python
class Router:
    def __init__(self, agents):
        self.agents = agents  # Dictionary of specialized agents
        self.routing_history = []
    
    def route(self, query):
        """Determine which agent should handle the query"""
        # Classify query intent
        intent = self.classify_intent(query)
        
        # Select appropriate agent
        agent_name = self.select_agent(intent)
        agent = self.agents.get(agent_name)
        
        if not agent:
            agent = self.agents["general"]  # Fallback
        
        # Log routing decision
        self.routing_history.append({
            "query": query,
            "intent": intent,
            "routed_to": agent_name,
            "timestamp": datetime.now()
        })
        
        return agent
    
    def classify_intent(self, query):
        """Classify query to determine routing"""
        # Could use LLM or simpler classification
        keywords = {
            "code": ["code", "program", "debug", "python", "javascript"],
            "research": ["research", "find", "search", "latest"],
            "email": ["email", "send", "message", "reply"],
            "data": ["analyze", "data", "statistics", "chart"]
        }
        
        query_lower = query.lower()
        for intent, words in keywords.items():
            if any(word in query_lower for word in words):
                return intent
        
        return "general"
    
    def select_agent(self, intent):
        """Map intent to agent"""
        routing_map = {
            "code": "code_agent",
            "research": "research_agent",
            "email": "email_agent",
            "data": "data_agent",
            "general": "general_agent"
        }
        
        return routing_map.get(intent, "general_agent")
```

---

### 3.2.7 Multi-Agent Communication Layer

**Role**: Enables agents to collaborate

```python
class AgentCommunicationLayer:
    def __init__(self):
        self.message_queue = Queue()
        self.agents = {}
        self.conversation_logs = []
    
    def register_agent(self, agent_id, agent):
        """Register agent for communication"""
        self.agents[agent_id] = agent
    
    def send_message(self, from_agent, to_agent, message):
        """Send message from one agent to another"""
        comm = {
            "from": from_agent,
            "to": to_agent,
            "message": message,
            "timestamp": datetime.now()
        }
        
        self.message_queue.put(comm)
        self.conversation_logs.append(comm)
    
    def broadcast(self, from_agent, message):
        """Send message to all agents"""
        for agent_id in self.agents:
            if agent_id != from_agent:
                self.send_message(from_agent, agent_id, message)
    
    def receive_message(self, agent_id):
        """Get messages for specific agent"""
        messages = []
        temp_queue = Queue()
        
        while not self.message_queue.empty():
            msg = self.message_queue.get()
            if msg["to"] == agent_id:
                messages.append(msg)
            else:
                temp_queue.put(msg)
        
        # Restore unread messages
        while not temp_queue.empty():
            self.message_queue.put(temp_queue.get())
        
        return messages
```

---

## 3.3 Architecture Patterns

### 3.3.1 ReAct Architecture

```
User Query
    ↓
┌─────────────────────┐
│   Reasoning Step    │
│ "What should I do?" │
└─────────┬───────────┘
          ↓
┌─────────────────────┐
│   Action Step       │
│ "Execute tool X"    │
└─────────┬───────────┘
          ↓
┌─────────────────────┐
│  Observation        │
│ "Tool returned Y"   │
└─────────┬───────────┘
          ↓
     [Loop until complete]
          ↓
┌─────────────────────┐
│   Final Answer      │
└─────────────────────┘
```

**Implementation**:
```python
class ReActAgent:
    def __init__(self, llm, tools):
        self.llm = llm
        self.tools = tools
        self.max_iterations = 10
    
    def solve(self, query):
        context = {"query": query, "scratchpad": ""}
        
        for i in range(self.max_iterations):
            # REASONING
            thought = self.generate_thought(context)
            context["scratchpad"] += f"\nThought {i+1}: {thought}"
            
            if self.has_final_answer(thought):
                return self.extract_answer(thought)
            
            # ACTION
            action = self.generate_action(thought)
            context["scratchpad"] += f"\nAction {i+1}: {action}"
            
            # OBSERVATION
            observation = self.execute_action(action)
            context["scratchpad"] += f"\nObservation {i+1}: {observation}"
        
        return "Max iterations reached"
    
    def generate_thought(self, context):
        prompt = f"""
        Query: {context['query']}
        
        Previous steps:
        {context['scratchpad']}
        
        Think about what to do next.
        """
        return self.llm.invoke(prompt)
```

---

### 3.3.2 Plan-and-Execute Architecture

```
User Query
    ↓
┌─────────────────────┐
│   Planning Phase    │
│ Create full plan    │
└─────────┬───────────┘
          ↓
┌─────────────────────┐
│  Execution Phase    │
│ Execute each step   │
└─────────┬───────────┘
          ↓
┌─────────────────────┐
│ Replanning (if needed) │
└─────────┬───────────┘
          ↓
     Final Result
```

**Implementation**:
```python
class PlanAndExecuteAgent:
    def __init__(self, llm, tools):
        self.planner = Planner(llm)
        self.executor = Executor(tools)
        self.replanner = Replanner(llm)
    
    def solve(self, goal):
        # Phase 1: Planning
        plan = self.planner.create_plan(goal)
        
        # Phase 2: Execution
        results = []
        for step in plan:
            result = self.executor.execute_step(step)
            results.append(result)
            
            # Check if replanning needed
            if result["status"] == "failed":
                # Replan remaining steps
                remaining = plan[plan.index(step)+1:]
                new_plan = self.replanner.replan(
                    goal, 
                    completed=results, 
                    remaining=remaining
                )
                plan = results + new_plan
        
        # Phase 3: Synthesis
        return self.synthesize_results(results)
```

---

### 3.3.3 Tool-Calling Architecture

```
User Query
    ↓
┌──────────────────────┐
│  Intent Detection    │
└─────────┬────────────┘
          ↓
┌──────────────────────┐
│  Tool Selection      │
│  (LLM decides)       │
└─────────┬────────────┘
          ↓
┌──────────────────────┐
│  Parameter Extraction│
└─────────┬────────────┘
          ↓
┌──────────────────────┐
│  Tool Execution      │
└─────────┬────────────┘
          ↓
┌──────────────────────┐
│  Response Synthesis  │
└──────────────────────┘
```

---

### 3.3.4 Multi-Agent Architecture

```
           User Query
                ↓
        ┌──────────────┐
        │  Coordinator │
        │    Agent     │
        └───────┬──────┘
                ↓
      ┌─────────┼─────────┐
      ↓         ↓         ↓
┌──────────┐ ┌──────────┐ ┌──────────┐
│Research  │ │ Analysis │ │  Writing │
│ Agent    │ │  Agent   │ │  Agent   │
└────┬─────┘ └────┬─────┘ └────┬─────┘
     ↓            ↓            ↓
     └────────────┼────────────┘
                  ↓
          ┌──────────────┐
          │  Coordinator │
          │  (Synthesis) │
          └──────┬───────┘
                 ↓
           Final Output
```

**Implementation**:
```python
class MultiAgentSystem:
    def __init__(self):
        self.coordinator = CoordinatorAgent()
        self.workers = {
            "research": ResearchAgent(),
            "analysis": AnalysisAgent(),
            "writing": WritingAgent()
        }
    
    def solve(self, task):
        # Coordinator breaks down task
        subtasks = self.coordinator.decompose(task)
        
        # Assign to appropriate workers
        assignments = self.coordinator.assign_tasks(subtasks, self.workers)
        
        # Execute in parallel
        results = {}
        for worker_name, subtask in assignments.items():
            worker = self.workers[worker_name]
            results[worker_name] = worker.execute(subtask)
        
        # Coordinator synthesizes
        final_result = self.coordinator.synthesize(results)
        
        return final_result
```

---

### 3.3.5 Hierarchical Agent Architecture

```
                 ┌─────────────┐
                 │   Manager   │
                 │    Agent    │
                 └──────┬──────┘
                        ↓
        ┌───────────────┼───────────────┐
        ↓               ↓               ↓
  ┌──────────┐    ┌──────────┐    ┌──────────┐
  │Team Lead │    │Team Lead │    │Team Lead │
  │  Agent   │    │  Agent   │    │  Agent   │
  └────┬─────┘    └────┬─────┘    └────┬─────┘
       ↓               ↓               ↓
  ┌────┴────┐     ┌────┴────┐     ┌────┴────┐
  ↓    ↓    ↓     ↓    ↓    ↓     ↓    ↓    ↓
Worker Worker Worker Worker Worker Worker Worker
Agent  Agent Agent  Agent  Agent  Agent  Agent
```

**Use Case**: Complex enterprise workflows with multiple levels of delegation

---

## 3.4 Observability Systems

### 3.4.1 Monitoring

```python
class AgentMonitor:
    def __init__(self):
        self.metrics = {
            "total_queries": 0,
            "successful_completions": 0,
            "failures": 0,
            "avg_latency": 0,
            "tool_usage": {}
        }
    
    def log_query(self, query):
        self.metrics["total_queries"] += 1
        # Store in time-series database
    
    def log_completion(self, query, result, latency):
        if result["status"] == "success":
            self.metrics["successful_completions"] += 1
        else:
            self.metrics["failures"] += 1
        
        # Update average latency
        self.update_avg_latency(latency)
    
    def log_tool_usage(self, tool_name):
        if tool_name not in self.metrics["tool_usage"]:
            self.metrics["tool_usage"][tool_name] = 0
        self.metrics["tool_usage"][tool_name] += 1
    
    def get_dashboard(self):
        return {
            "success_rate": self.metrics["successful_completions"] / self.metrics["total_queries"],
            "avg_latency": self.metrics["avg_latency"],
            "most_used_tools": sorted(
                self.metrics["tool_usage"].items(),
                key=lambda x: x[1],
                reverse=True
            )[:5]
        }
```

---

### 3.4.2 Logging

```python
import logging
from datetime import datetime

class AgentLogger:
    def __init__(self, agent_id):
        self.agent_id = agent_id
        self.logger = logging.getLogger(agent_id)
        
        # Configure structured logging
        handler = logging.FileHandler(f"logs/{agent_id}.jsonl")
        self.logger.addHandler(handler)
        self.logger.setLevel(logging.INFO)
    
    def log_event(self, event_type, data):
        log_entry = {
            "agent_id": self.agent_id,
            "timestamp": datetime.now().isoformat(),
            "event_type": event_type,
            "data": data
        }
        self.logger.info(json.dumps(log_entry))
    
    def log_thought(self, thought):
        self.log_event("thought", {"content": thought})
    
    def log_action(self, action, tool):
        self.log_event("action", {
            "tool": tool,
            "action": action
        })
    
    def log_error(self, error):
        self.log_event("error", {
            "error_type": type(error).__name__,
            "error_message": str(error)
        })
```

---

### 3.4.3 Tracing

```python
class AgentTracer:
    def __init__(self):
        self.traces = []
        self.active_trace = None
    
    def start_trace(self, query):
        """Start new trace for a query"""
        self.active_trace = {
            "query": query,
            "start_time": datetime.now(),
            "steps": [],
            "status": "in_progress"
        }
    
    def log_step(self, step_type, data):
        """Log individual step in trace"""
        if self.active_trace:
            self.active_trace["steps"].append({
                "type": step_type,
                "data": data,
                "timestamp": datetime.now()
            })
    
    def end_trace(self, result):
        """Complete trace"""
        if self.active_trace:
            self.active_trace["end_time"] = datetime.now()
            self.active_trace["duration"] = (
                self.active_trace["end_time"] - self.active_trace["start_time"]
            ).total_seconds()
            self.active_trace["result"] = result
            self.active_trace["status"] = "completed"
            
            self.traces.append(self.active_trace)
            self.active_trace = None
    
    def get_trace_by_id(self, trace_id):
        """Retrieve specific trace for debugging"""
        return self.traces[trace_id]
```

---

<a name="section-4"></a>
# SECTION 4 — MEMORY IN AGENTIC AI

## 4.1 What is Memory in AI Agents?

### Definition

**Memory** in AI agents is the system's ability to:
1. **Store** information from interactions
2. **Retrieve** relevant past information
3. **Update** beliefs based on new information
4. **Persist** knowledge across sessions

### Why Memory Matters

| Without Memory | With Memory |
|----------------|-------------|
| Every conversation starts fresh | Contextual continuity |
| Repeats questions | Learns user preferences |
| No personalization | Personalized interactions |
| Can't reference past | "As we discussed before..." |
| Inefficient | Efficient (builds on past) |

---

## 4.2 Stateless vs Stateful Agents

### Stateless Agents

```python
# Stateless: No memory between calls
def stateless_agent(query):
    response = llm.invoke(query)
    return response

# Each call is independent
stateless_agent("What's my name?")  # "I don't know"
stateless_agent("My name is Alice")  # "Nice to meet you"
stateless_agent("What's my name?")  # "I don't know" (forgot!)
```

**Characteristics**:
- ✅ Simple implementation
- ✅ No storage required
- ❌ No continuity
- ❌ Poor user experience

---

### Stateful Agents

```python
# Stateful: Maintains memory
class StatefulAgent:
    def __init__(self):
        self.memory = ConversationMemory()
    
    def chat(self, query):
        # Retrieve conversation history
        history = self.memory.get_history()
        
        # Include history in prompt
        full_prompt = self.build_prompt(history, query)
        response = llm.invoke(full_prompt)
        
        # Store interaction
        self.memory.add_interaction(query, response)
        
        return response

agent = StatefulAgent()
agent.chat("My name is Alice")  # "Nice to meet you, Alice!"
agent.chat("What's my name?")   # "Your name is Alice"
```

**Characteristics**:
- ✅ Contextual continuity
- ✅ Personalized
- ✅ Learning capability
- ❌ More complex
- ❌ Storage overhead

---

## 4.3 Memory Types

### Memory Hierarchy

```
┌─────────────────────────────────────────┐
│         WORKING MEMORY                   │
│  (Current task variables)                │
│  Duration: Single function call          │
└───────────────┬─────────────────────────┘
                ↓
┌─────────────────────────────────────────┐
│       SHORT-TERM MEMORY                  │
│  (Conversation buffer)                   │
│  Duration: Current session               │
└───────────────┬─────────────────────────┘
                ↓
┌─────────────────────────────────────────┐
│       LONG-TERM MEMORY                   │
│  (Persistent storage)                    │
│  Duration: Forever                       │
│  ├── Episodic (specific events)          │
│  └── Semantic (general knowledge)        │
└─────────────────────────────────────────┘
```

---

### 4.3.1 Short-Term Memory

**Purpose**: Maintain context within a conversation

```python
class ShortTermMemory:
    def __init__(self, max_tokens=2000):
        self.messages = []
        self.max_tokens = max_tokens
    
    def add_message(self, role, content):
        self.messages.append({
            "role": role,
            "content": content,
            "timestamp": datetime.now()
        })
        
        # Trim if exceeds limit
        while self.count_tokens() > self.max_tokens:
            self.messages.pop(0)  # Remove oldest
    
    def get_messages(self):
        return self.messages
    
    def count_tokens(self):
        # Estimate token count
        return sum(len(msg["content"].split()) * 1.3 for msg in self.messages)
```

**Use Cases**:
- Conversation context
- Current task state
- Recent interactions

---

### 4.3.2 Long-Term Memory

**Purpose**: Persistent storage across sessions

```python
class LongTermMemory:
    def __init__(self, vector_store):
        self.vector_store = vector_store
        self.structured_db = Database()
    
    def store(self, key, value, category="general"):
        # Store in vector database for semantic search
        embedding = self.embed(value)
        self.vector_store.add({
            "key": key,
            "value": value,
            "embedding": embedding,
            "category": category,
            "timestamp": datetime.now()
        })
        
        # Also store in structured database
        self.structured_db.insert({
            "key": key,
            "value": value,
            "category": category
        })
    
    def recall(self, query, k=5):
        # Semantic search
        query_embedding = self.embed(query)
        results = self.vector_store.search(query_embedding, k=k)
        
        return results
    
    def embed(self, text):
        # Convert text to vector embedding
        return embedding_model.encode(text)
```

**Use Cases**:
- User preferences
- Historical conversations
- Learned facts
- Domain knowledge

---

### 4.3.3 Episodic Memory

**Purpose**: Remember specific events and experiences

```python
class EpisodicMemory:
    def __init__(self):
        self.episodes = []
    
    def store_episode(self, event, context):
        episode = {
            "event": event,
            "context": context,
            "timestamp": datetime.now(),
            "participants": context.get("participants", []),
            "outcome": None  # Filled later
        }
        self.episodes.append(episode)
        return len(self.episodes) - 1  # Episode ID
    
    def recall_episodes(self, query):
        # Find relevant episodes
        relevant = []
        for ep in self.episodes:
            if self.is_relevant(ep, query):
                relevant.append(ep)
        
        # Sort by recency and relevance
        relevant.sort(
            key=lambda x: (self.relevance_score(x, query), x["timestamp"]),
            reverse=True
        )
        
        return relevant
    
    def update_outcome(self, episode_id, outcome):
        self.episodes[episode_id]["outcome"] = outcome
```

**Example**:
```
Episode 1: "User asked about Python decorators on May 15"
Episode 2: "Successfully debugged user's code on May 16"
Episode 3: "User mentioned preferring detailed explanations on May 17"
```

---

### 4.3.4 Semantic Memory

**Purpose**: Store general knowledge and facts

```python
class SemanticMemory:
    def __init__(self):
        self.knowledge = {}
        self.confidence = {}
    
    def store_fact(self, subject, predicate, object, confidence=1.0):
        """Store knowledge triple"""
        if subject not in self.knowledge:
            self.knowledge[subject] = {}
        
        self.knowledge[subject][predicate] = object
        self.confidence[(subject, predicate)] = confidence
    
    def retrieve_fact(self, subject, predicate):
        """Retrieve specific fact"""
        return self.knowledge.get(subject, {}).get(predicate)
    
    def infer(self, query):
        """Perform inference on knowledge base"""
        # Example: Transitive relations
        # If "Paris is-capital-of France" and "France is-in Europe"
        # Then infer "Paris is-in Europe"
        pass
```

**Example**:
```python
memory = SemanticMemory()

# Store facts
memory.store_fact("user", "prefers", "Python")
memory.store_fact("user", "experience_level", "intermediate")
memory.store_fact("user", "timezone", "PST")

# Retrieve
preference = memory.retrieve_fact("user", "prefers")  # "Python"
```

---

## 4.4 Vector Memory

### How Vector Memory Works

```
Text → Embedding Model → Vector [0.1, -0.3, 0.5, ..., 0.2]
                              ↓
                        Vector Database
                              ↓
                    Similarity Search
```

### Implementation

```python
from sentence_transformers import SentenceTransformer
import numpy as np

class VectorMemory:
    def __init__(self, model_name="all-MiniLM-L6-v2"):
        self.model = SentenceTransformer(model_name)
        self.memories = []
        self.embeddings = []
    
    def add(self, text, metadata=None):
        """Add text to memory"""
        embedding = self.model.encode(text)
        
        self.memories.append({
            "text": text,
            "metadata": metadata or {},
            "timestamp": datetime.now()
        })
        self.embeddings.append(embedding)
    
    def search(self, query, k=5):
        """Find most similar memories"""
        query_embedding = self.model.encode(query)
        
        # Calculate cosine similarity
        similarities = [
            np.dot(query_embedding, emb) / (
                np.linalg.norm(query_embedding) * np.linalg.norm(emb)
            )
            for emb in self.embeddings
        ]
        
        # Get top k
        top_k_indices = np.argsort(similarities)[-k:][::-1]
        
        return [
            {
                **self.memories[i],
                "similarity": similarities[i]
            }
            for i in top_k_indices
        ]
```

**Example Usage**:
```python
memory = VectorMemory()

# Store memories
memory.add("User loves Italian food")
memory.add("User's favorite color is blue")
memory.add("User prefers working in the morning")

# Query
results = memory.search("What food does the user like?", k=2)
# Returns: ["User loves Italian food", ...]
```

---

## 4.5 Knowledge Graph Memory

### Structure

```
(User) --[PREFERS]--> (Python)
  |
  +--[WORKS_AT]--> (TechCorp)
  |
  +--[LIVES_IN]--> (San Francisco)
  |
  +--[INTERESTED_IN]--> (Machine Learning)
                           |
                           +--[SUBFIELD_OF]--> (AI)
```

### Implementation

```python
class KnowledgeGraphMemory:
    def __init__(self):
        self.graph = {
            "nodes": {},
            "edges": []
        }
    
    def add_node(self, node_id, node_type, properties):
        self.graph["nodes"][node_id] = {
            "type": node_type,
            "properties": properties
        }
    
    def add_edge(self, from_node, relationship, to_node):
        self.graph["edges"].append({
            "from": from_node,
            "relationship": relationship,
            "to": to_node
        })
    
    def query(self, pattern):
        """Query using pattern matching"""
        # Example: Find all (User)-[PREFERS]->(?)
        results = []
        for edge in self.graph["edges"]:
            if (edge["from"] == pattern["from"] and
                edge["relationship"] == pattern["relationship"]):
                results.append({
                    "subject": edge["from"],
                    "predicate": edge["relationship"],
                    "object": edge["to"]
                })
        return results
    
    def get_neighbors(self, node_id, relationship_type=None):
        """Get connected nodes"""
        neighbors = []
        for edge in self.graph["edges"]:
            if edge["from"] == node_id:
                if not relationship_type or edge["relationship"] == relationship_type:
                    neighbors.append({
                        "node": edge["to"],
                        "relationship": edge["relationship"]
                    })
        return neighbors
```

---

## 4.6 Memory Retrieval Systems

### Retrieval Strategies

#### 1. **Recency-Based Retrieval**
```python
def retrieve_recent(memory, k=5):
    sorted_memories = sorted(
        memory.items(),
        key=lambda x: x["timestamp"],
        reverse=True
    )
    return sorted_memories[:k]
```

#### 2. **Relevance-Based Retrieval**
```python
def retrieve_relevant(query, memory, k=5):
    # Semantic similarity
    query_emb = embed(query)
    
    scored = [
        (mem, cosine_similarity(query_emb, mem["embedding"]))
        for mem in memory
    ]
    
    sorted_memories = sorted(scored, key=lambda x: x[1], reverse=True)
    return [m[0] for m in sorted_memories[:k]]
```

#### 3. **Hybrid Retrieval**
```python
def retrieve_hybrid(query, memory, k=5, recency_weight=0.3, relevance_weight=0.7):
    current_time = datetime.now()
    
    scored = []
    for mem in memory:
        # Relevance score
        relevance = cosine_similarity(embed(query), mem["embedding"])
        
        # Recency score (exponential decay)
        age_hours = (current_time - mem["timestamp"]).total_seconds() / 3600
        recency = np.exp(-age_hours / 24)  # Decay over 24 hours
        
        # Combined score
        score = recency_weight * recency + relevance_weight * relevance
        scored.append((mem, score))
    
    sorted_memories = sorted(scored, key=lambda x: x[1], reverse=True)
    return [m[0] for m in sorted_memories[:k]]
```

---

## 4.7 Memory Compression

### Problem: Context Window Limits

LLMs have finite context windows. Long conversations must be compressed.

### Compression Strategies

#### 1. **Summarization**
```python
def compress_conversation(messages, llm):
    # Summarize older messages
    old_messages = messages[:-10]  # Keep last 10 intact
    
    summary_prompt = f"""
    Summarize this conversation history concisely:
    
    {format_messages(old_messages)}
    
    Focus on:
    - Key facts learned about the user
    - Important decisions made
    - Ongoing tasks
    """
    
    summary = llm.invoke(summary_prompt)
    
    # Replace old messages with summary
    compressed = [
        {"role": "system", "content": f"Previous conversation summary: {summary}"}
    ] + messages[-10:]
    
    return compressed
```

#### 2. **Forgetting Strategy**
```python
class ForgetfulMemory:
    def __init__(self, max_items=100):
        self.max_items = max_items
        self.memories = []
        self.access_counts = {}
    
    def add(self, memory):
        self.memories.append(memory)
        self.access_counts[id(memory)] = 0
        
        if len(self.memories) > self.max_items:
            # Forget least-accessed
            least_accessed = min(
                self.memories,
                key=lambda m: self.access_counts[id(m)]
            )
            self.memories.remove(least_accessed)
            del self.access_counts[id(least_accessed)]
    
    def retrieve(self, query, k=5):
        results = self.search(query, k)
        
        # Update access counts
        for result in results:
            self.access_counts[id(result)] += 1
        
        return results
```

---

## 4.8 Vector Databases

### Popular Vector Databases

| Database | Type | Best For | Strengths |
|----------|------|----------|-----------|
| **FAISS** | Library | In-memory, fast | Speed, simplicity |
| **Pinecone** | Cloud | Production, scale | Managed, scalable |
| **Weaviate** | Open-source | Hybrid search | GraphQL, filters |
| **ChromaDB** | Embedded | Development | Easy setup |
| **Milvus** | Distributed | Large-scale | High throughput |

---

### 4.8.1 FAISS Example

```python
import faiss
import numpy as np

class FAISSMemory:
    def __init__(self, dimension=384):
        self.dimension = dimension
        self.index = faiss.IndexFlatL2(dimension)
        self.memories = []
        self.embedding_model = SentenceTransformer('all-MiniLM-L6-v2')
    
    def add(self, text):
        # Generate embedding
        embedding = self.embedding_model.encode([text])[0]
        
        # Add to FAISS index
        self.index.add(np.array([embedding]).astype('float32'))
        
        # Store text
        self.memories.append(text)
    
    def search(self, query, k=5):
        # Generate query embedding
        query_emb = self.embedding_model.encode([query])[0]
        
        # Search
        distances, indices = self.index.search(
            np.array([query_emb]).astype('float32'),
            k
        )
        
        # Return results
        return [
            {
                "text": self.memories[i],
                "distance": distances[0][idx]
            }
            for idx, i in enumerate(indices[0])
        ]
```

---

### 4.8.2 Pinecone Example

```python
import pinecone

class PineconeMemory:
    def __init__(self, api_key, index_name):
        pinecone.init(api_key=api_key)
        self.index = pinecone.Index(index_name)
        self.embedding_model = SentenceTransformer('all-MiniLM-L6-v2')
    
    def add(self, id, text, metadata=None):
        embedding = self.embedding_model.encode(text).tolist()
        
        self.index.upsert([(
            id,
            embedding,
            metadata or {"text": text}
        )])
    
    def search(self, query, k=5):
        query_emb = self.embedding_model.encode(query).tolist()
        
        results = self.index.query(
            query_emb,
            top_k=k,
            include_metadata=True
        )
        
        return [
            {
                "id": match["id"],
                "score": match["score"],
                "text": match["metadata"]["text"]
            }
            for match in results["matches"]
        ]
```

---

### 4.8.3 ChromaDB Example

```python
import chromadb

class ChromaMemory:
    def __init__(self, collection_name="agent_memory"):
        self.client = chromadb.Client()
        self.collection = self.client.create_collection(collection_name)
    
    def add(self, documents, ids, metadatas=None):
        self.collection.add(
            documents=documents,
            ids=ids,
            metadatas=metadatas
        )
    
    def search(self, query, k=5):
        results = self.collection.query(
            query_texts=[query],
            n_results=k
        )
        
        return results
```

---

## 4.9 Complete Memory System Example

```python
class ComprehensiveMemorySystem:
    def __init__(self):
        # Short-term: Recent conversation
        self.short_term = ShortTermMemory(max_tokens=2000)
        
        # Long-term: Persistent vector store
        self.long_term = VectorMemory()
        
        # Episodic: Specific events
        self.episodic = EpisodicMemory()
        
        # Semantic: Facts and knowledge
        self.semantic = SemanticMemory()
        
        # Knowledge graph: Relationships
        self.knowledge_graph = KnowledgeGraphMemory()
    
    def remember(self, interaction, context):
        # Add to short-term
        self.short_term.add_message(
            role=interaction["role"],
            content=interaction["content"]
        )
        
        # Extract and store facts
        facts = self.extract_facts(interaction["content"])
        for fact in facts:
            self.semantic.store_fact(**fact)
            self.knowledge_graph.add_from_fact(fact)
        
        # Store as episode if significant
        if self.is_significant(interaction):
            self.episodic.store_episode(
                event=interaction,
                context=context
            )
        
        # Add to long-term
        self.long_term.add(
            text=interaction["content"],
            metadata={"role": interaction["role"], **context}
        )
    
    def recall(self, query):
        # Retrieve from all memory types
        memories = {
            "short_term": self.short_term.get_messages(),
            "long_term": self.long_term.search(query, k=3),
            "episodic": self.episodic.recall_episodes(query),
            "semantic": self.semantic.query_related(query)
        }
        
        # Rank and combine
        ranked = self.rank_memories(memories, query)
        
        return ranked
```

---

<a name="section-5"></a>
# SECTION 5 — MAJOR AGENTIC AI FRAMEWORKS

## 5.1 Overview of Agentic AI Frameworks

### Framework Landscape

```
┌─────────────────────────────────────────────────────────┐
│              AGENTIC AI FRAMEWORKS                       │
├─────────────────────────────────────────────────────────┤
│  Orchestration      │ LangChain, LangGraph, LlamaIndex  │
│  Multi-Agent        │ CrewAI, AutoGen, MetaGPT, CAMEL   │
│  Autonomous         │ AutoGPT, BabyAGI                  │
│  Production         │ Semantic Kernel, Haystack         │
│  Specialized        │ DSPy, PydanticAI                  │
│  Observability      │ AgentOps, LangSmith               │
└─────────────────────────────────────────────────────────┘
```

---

## 5.2 LangChain

### What is LangChain?

**LangChain** is a framework for building applications powered by language models, with strong support for agent orchestration.

### Core Components

```
┌──────────────────────────────────────┐
│         LangChain Stack              │
├──────────────────────────────────────┤
│  Chains      │ Sequential workflows │
│  Agents      │ Dynamic tool users   │
│  Memory      │ Conversation buffer  │
│  Tools       │ External integrations│
│  Prompts     │ Template management  │
│  Retrievers  │ Document search      │
└──────────────────────────────────────┘
```

### Architecture

```python
from langchain.agents import create_react_agent, AgentExecutor
from langchain.tools import Tool
from langchain_openai import ChatOpenAI
from langchain.prompts import PromptTemplate

# 1. Define LLM
llm = ChatOpenAI(model="gpt-4", temperature=0)

# 2. Define Tools
def search_web(query):
    # Web search logic
    return f"Search results for: {query}"

def calculate(expression):
    return eval(expression)

tools = [
    Tool(
        name="Search",
        func=search_web,
        description="Useful for finding current information"
    ),
    Tool(
        name="Calculator",
        func=calculate,
        description="Useful for mathematical calculations"
    )
]

# 3. Create Agent
prompt = PromptTemplate.from_template(
    """Answer the following question as best you can.
    
    You have access to the following tools:
    {tools}
    
    Use this format:
    Question: the input question
    Thought: think about what to do
    Action: the action to take (one of [{tool_names}])
    Action Input: the input to the action
    Observation: the result of the action
    ... (repeat Thought/Action/Observation as needed)
    Thought: I now know the final answer
    Final Answer: the final answer
    
    Question: {input}
    {agent_scratchpad}"""
)

agent = create_react_agent(llm, tools, prompt)
agent_executor = AgentExecutor(agent=agent, tools=tools, verbose=True)

# 4. Execute
result = agent_executor.invoke({
    "input": "What's 25% of 400, and then search for that number?"
})
```

### Key Features

| Feature | Description | Use Case |
|---------|-------------|----------|
| **Chains** | Link multiple LLM calls | Sequential workflows |
| **Agents** | ReAct-based reasoning | Dynamic problem solving |
| **Memory** | Conversation persistence | Chatbots |
| **Tools** | External integrations | Real-world actions |
| **Retrievers** | Document search | RAG systems |

### Advantages
- ✅ Rich ecosystem
- ✅ Extensive documentation
- ✅ Large community
- ✅ Many integrations
- ✅ Production-ready

### Disadvantages
- ❌ Can be verbose
- ❌ Steep learning curve
- ❌ Performance overhead
- ❌ Complex for simple tasks

---

## 5.3 LangGraph

### What is LangGraph?

**LangGraph** is LangChain's solution for building **stateful, cyclical workflows** with full control over agent execution paths.

### Key Concepts

#### **1. StateGraph**
Defines the structure of your workflow as a graph.

```python
from langgraph.graph import StateGraph, END
from typing import TypedDict, Annotated
import operator

# Define state
class AgentState(TypedDict):
    messages: Annotated[list, operator.add]
    current_step: str
    result: str

# Create graph
workflow = StateGraph(AgentState)
```

#### **2. Nodes**
Functions that perform work.

```python
def research_node(state):
    # Perform research
    results = search_web(state["messages"][-1])
    return {
        "messages": [f"Research: {results}"],
        "current_step": "analysis"
    }

def analysis_node(state):
    # Analyze results
    analysis = analyze(state["messages"])
    return {
        "messages": [f"Analysis: {analysis}"],
        "current_step": "writing"
    }

def writing_node(state):
    # Write report
    report = write_report(state["messages"])
    return {
        "result": report,
        "current_step": "complete"
    }
```

#### **3. Edges**
Define flow between nodes.

```python
# Add nodes
workflow.add_node("research", research_node)
workflow.add_node("analysis", analysis_node)
workflow.add_node("writing", writing_node)

# Add edges
workflow.add_edge("research", "analysis")
workflow.add_edge("analysis", "writing")
workflow.add_edge("writing", END)

# Set entry point
workflow.set_entry_point("research")
```

#### **4. Conditional Edges**
Dynamic routing based on state.

```python
def should_continue(state):
    if state["current_step"] == "complete":
        return "end"
    elif needs_more_research(state):
        return "research"
    else:
        return "analysis"

workflow.add_conditional_edges(
    "analysis",
    should_continue,
    {
        "research": "research",
        "analysis": "analysis",
        "end": END
    }
)
```

### Complete LangGraph Example

```python
from langgraph.graph import StateGraph, END
from langgraph.checkpoint import MemorySaver
from typing import TypedDict, Annotated
import operator

# State definition
class ResearchState(TypedDict):
    query: str
    research_results: Annotated[list, operator.add]
    analysis: str
    report: str
    iteration: int

# Node functions
def research(state: ResearchState):
    """Search for information"""
    query = state["query"]
    results = web_search(query)
    
    return {
        "research_results": [results],
        "iteration": state["iteration"] + 1
    }

def analyze(state: ResearchState):
    """Analyze research results"""
    analysis = llm.invoke(
        f"Analyze these findings: {state['research_results']}"
    )
    
    return {"analysis": analysis}

def critique(state: ResearchState):
    """Evaluate if we have enough information"""
    evaluation = llm.invoke(
        f"Is this enough info for: {state['query']}? Answer yes/no"
    )
    
    return {"needs_more": "no" in evaluation.lower()}

def write_report(state: ResearchState):
    """Generate final report"""
    report = llm.invoke(
        f"Write report on {state['query']} using: {state['analysis']}"
    )
    
    return {"report": report}

# Build graph
workflow = StateGraph(ResearchState)

# Add nodes
workflow.add_node("research", research)
workflow.add_node("analyze", analyze)
workflow.add_node("critique", critique)
workflow.add_node("write", write_report)

# Define edges
workflow.set_entry_point("research")
workflow.add_edge("research", "analyze")
workflow.add_edge("analyze", "critique")

# Conditional routing
def route_after_critique(state):
    if state.get("needs_more", False) and state["iteration"] < 3:
        return "research"  # Loop back
    else:
        return "write"  # Move to writing

workflow.add_conditional_edges(
    "critique",
    route_after_critique,
    {
        "research": "research",
        "write": "write"
    }
)

workflow.add_edge("write", END)

# Compile with memory
memory = MemorySaver()
app = workflow.compile(checkpointer=memory)

# Execute
result = app.invoke({
    "query": "Latest developments in quantum computing",
    "research_results": [],
    "iteration": 0
})
```

### LangGraph Features

| Feature | Description | Benefit |
|---------|-------------|---------|
| **Cycles** | Loops in workflow | Iterative refinement |
| **Checkpointing** | Save/restore state | Resume execution |
| **Human-in-loop** | Pause for approval | Safety controls |
| **Parallel execution** | Concurrent nodes | Speed |
| **Streaming** | Real-time updates | User experience |

### When to Use LangGraph

✅ **Use LangGraph when:**
- Need complex, multi-step workflows
- Require iterative processes (loops)
- Want full control over execution
- Need to save/resume state
- Building production systems

❌ **Don't use LangGraph for:**
- Simple Q&A chatbots
- Single-shot completions
- Prototyping (use LangChain first)

---

## 5.4 CrewAI

### What is CrewAI?

**CrewAI** is a framework for orchestrating **role-playing autonomous AI agents** that collaborate to accomplish complex tasks.

### Core Concepts

#### **1. Agents**
Specialized team members with roles and goals.

```python
from crewai import Agent
from langchain_openai import ChatOpenAI

llm = ChatOpenAI(model="gpt-4")

researcher = Agent(
    role="Senior Research Analyst",
    goal="Discover groundbreaking technologies",
    backstory="You're an expert at finding emerging tech trends",
    llm=llm,
    verbose=True,
    allow_delegation=False
)

writer = Agent(
    role="Tech Content Writer",
    goal="Write engaging tech articles",
    backstory="You're skilled at making complex topics accessible",
    llm=llm,
    verbose=True
)
```

#### **2. Tasks**
Specific assignments for agents.

```python
from crewai import Task

research_task = Task(
    description="Research the latest AI developments in 2026",
    agent=researcher,
    expected_output="Detailed research report on AI trends"
)

writing_task = Task(
    description="Write a blog post based on the research",
    agent=writer,
    expected_output="800-word blog post",
    context=[research_task]  # Depends on research_task
)
```

#### **3. Crew**
Team of agents working together.

```python
from crewai import Crew, Process

crew = Crew(
    agents=[researcher, writer],
    tasks=[research_task, writing_task],
    process=Process.sequential,  # or Process.hierarchical
    verbose=True
)

# Execute
result = crew.kickoff()
print(result)
```

### Advanced CrewAI Features

#### **Delegation**
Agents can delegate tasks to each other.

```python
manager = Agent(
    role="Project Manager",
    goal="Coordinate the team",
    backstory="Experienced at managing AI projects",
    llm=llm,
    allow_delegation=True  # Can delegate to other agents
)
```

#### **Hierarchical Process**
Manager agent coordinates workers.

```python
crew = Crew(
    agents=[manager, researcher, writer, editor],
    tasks=tasks,
    process=Process.hierarchical,
    manager_llm=ChatOpenAI(model="gpt-4")
)
```

#### **Tools for Agents**
Equip agents with capabilities.

```python
from crewai_tools import SerperDevTool, WebsiteSearchTool

search_tool = SerperDevTool()
web_tool = WebsiteSearchTool()

researcher = Agent(
    role="Researcher",
    tools=[search_tool, web_tool],
    # ... other config
)
```

### Complete CrewAI Example

```python
from crewai import Agent, Task, Crew, Process
from crewai_tools import SerperDevTool
from langchain_openai import ChatOpenAI

# Initialize tools
search_tool = SerperDevTool()
llm = ChatOpenAI(model="gpt-4")

# Define agents
market_researcher = Agent(
    role="Market Research Analyst",
    goal="Analyze market trends and competitor strategies",
    backstory="Expert in market analysis with 10 years experience",
    tools=[search_tool],
    llm=llm,
    verbose=True
)

data_analyst = Agent(
    role="Data Analyst",
    goal="Extract insights from market data",
    backstory="Skilled at statistical analysis and data visualization",
    llm=llm,
    verbose=True
)

content_strategist = Agent(
    role="Content Strategist",
    goal="Create actionable marketing strategies",
    backstory="Creative strategist who turns insights into campaigns",
    llm=llm,
    verbose=True
)

# Define tasks
research_task = Task(
    description="""Research the electric vehicle market in 2026.
    Focus on: market size, key players, trends, challenges.
    Provide detailed findings.""",
    agent=market_researcher,
    expected_output="Comprehensive market research report"
)

analysis_task = Task(
    description="""Analyze the research data and identify:
    - Top 3 market opportunities
    - Biggest competitive threats
    - Emerging trends""",
    agent=data_analyst,
    expected_output="Strategic analysis with data-driven insights",
    context=[research_task]
)

strategy_task = Task(
    description="""Based on the analysis, create a go-to-market strategy:
    - Target audience
    - Key messages
    - Channel recommendations
    - 6-month action plan""",
    agent=content_strategist,
    expected_output="Detailed marketing strategy document",
    context=[research_task, analysis_task]
)

# Create crew
crew = Crew(
    agents=[market_researcher, data_analyst, content_strategist],
    tasks=[research_task, analysis_task, strategy_task],
    process=Process.sequential,
    verbose=True
)

# Execute
result = crew.kickoff()
```

### CrewAI vs Solo Agents

| Aspect | Solo Agent | CrewAI |
|--------|------------|--------|
| **Specialization** | Generalist | Multiple specialists |
| **Quality** | Good | Better (each agent excels) |
| **Complexity** | Simple | Handles complex projects |
| **Collaboration** | None | Built-in |
| **Best for** | Simple tasks | Multi-step projects |

---

## 5.5 AutoGen

### What is AutoGen?

**AutoGen** (Microsoft) is a framework for building **conversational multi-agent systems** where agents chat with each other to solve tasks.

### Key Features

- **Conversable agents**: Agents that can talk to each other
- **Human-in-the-loop**: Agents can ask humans for input
- **Code execution**: Built-in code interpreter
- **Group chat**: Multi-agent conversations

### Basic Example

```python
from autogen import AssistantAgent, UserProxyAgent

# Configuration
config_list = [{
    "model": "gpt-4",
    "api_key": "your-key"
}]

# Create assistant agent
assistant = AssistantAgent(
    name="assistant",
    llm_config={"config_list": config_list}
)

# Create user proxy (represents human, can execute code)
user_proxy = UserProxyAgent(
    name="user_proxy",
    human_input_mode="NEVER",  # or "ALWAYS" or "TERMINATE"
    code_execution_config={
        "work_dir": "coding",
        "use_docker": False
    }
)

# Start conversation
user_proxy.initiate_chat(
    assistant,
    message="Plot a sine wave and save it as plot.png"
)
```

### Multi-Agent Conversation

```python
from autogen import AssistantAgent, UserProxyAgent, GroupChat, GroupChatManager

# Create multiple agents
engineer = AssistantAgent(
    name="Engineer",
    system_message="You are a software engineer",
    llm_config={"config_list": config_list}
)

scientist = AssistantAgent(
    name="Scientist",
    system_message="You are a data scientist",
    llm_config={"config_list": config_list}
)

critic = AssistantAgent(
    name="Critic",
    system_message="You review and critique solutions",
    llm_config={"config_list": config_list}
)

user_proxy = UserProxyAgent(
    name="Admin",
    human_input_mode="TERMINATE",
    code_execution_config={"work_dir": "workspace"}
)

# Create group chat
groupchat = GroupChat(
    agents=[user_proxy, engineer, scientist, critic],
    messages=[],
    max_round=10
)

manager = GroupChatManager(
    groupchat=groupchat,
    llm_config={"config_list": config_list}
)

# Start discussion
user_proxy.initiate_chat(
    manager,
    message="Analyze this dataset and build a prediction model"
)
```

### AutoGen Patterns

#### **1. Two-Agent Collaboration**
```
User Proxy ↔ Assistant
```

#### **2. Sequential Work**
```
User → Agent1 → Agent2 → Agent3 → Result
```

#### **3. Group Discussion**
```
     Agent1
       ↓
    Manager → Agent2
       ↓
     Agent3
```

### Advantages
- ✅ Natural multi-agent conversations
- ✅ Built-in code execution
- ✅ Human-in-the-loop
- ✅ Group chat orchestration

### Disadvantages
- ❌ Less control over agent behavior
- ❌ Can be unpredictable
- ❌ Verbose conversations

---

## 5.6 Other Major Frameworks

### 5.6.1 Semantic Kernel (Microsoft)

**Purpose**: Enterprise-grade AI orchestration

```csharp
// C# example
var kernel = Kernel.CreateBuilder()
    .AddOpenAIChatCompletion("gpt-4", apiKey)
    .Build();

var function = kernel.CreateFunctionFromPrompt(
    "Summarize: {{$input}}"
);

var result = await kernel.InvokeAsync(function, 
    new() { ["input"] = "Long text..." }
);
```

**Key Features**:
- Multi-language (C#, Python, Java)
- Enterprise integration
- Planning capabilities
- Plugin system

---

### 5.6.2 LlamaIndex

**Purpose**: Data ingestion and RAG

```python
from llama_index import VectorStoreIndex, SimpleDirectoryReader

# Load documents
documents = SimpleDirectoryReader('data').load_data()

# Create index
index = VectorStoreIndex.from_documents(documents)

# Create agent with RAG
from llama_index.agent import ReActAgent
from llama_index.tools import QueryEngineTool

query_tool = QueryEngineTool.from_defaults(
    query_engine=index.as_query_engine(),
    name="knowledge_base",
    description="Contains company documents"
)

agent = ReActAgent.from_tools([query_tool])

response = agent.chat("What's our Q4 revenue?")
```

**Best For**:
- RAG systems
- Document Q&A
- Knowledge base agents

---

### 5.6.3 Haystack

**Purpose**: NLP pipelines and agents

```python
from haystack.agents import Agent, Tool
from haystack.agents.conversational import ConversationalAgent

# Define tools
search_tool = Tool(
    name="WebSearch",
    pipeline_or_node=web_search_pipeline
)

# Create agent
agent = ConversationalAgent(
    prompt_node=prompt_node,
    tools=[search_tool]
)

result = agent.run("Find recent news about AI")
```

---

### 5.6.4 DSPy

**Purpose**: Programming with LMs, not prompting

```python
import dspy

# Define signature
class QuestionAnswering(dspy.Signature):
    question = dspy.InputField()
    answer = dspy.OutputField()

# Create module
class RAG(dspy.Module):
    def __init__(self):
        self.retrieve = dspy.Retrieve(k=3)
        self.generate = dspy.ChainOfThought(QuestionAnswering)
    
    def forward(self, question):
        context = self.retrieve(question).passages
        return self.generate(context=context, question=question)

# Use
rag = RAG()
answer = rag(question="What is quantum computing?")
```

**Philosophy**: Treat LLM programming as software engineering, not prompt engineering

---

### 5.6.5 PydanticAI

**Purpose**: Type-safe agent development

```python
from pydantic_ai import Agent
from pydantic import BaseModel

class WeatherResult(BaseModel):
    temperature: float
    condition: str
    humidity: int

agent = Agent(
    model='openai:gpt-4',
    result_type=WeatherResult,
    system_prompt='You are a weather assistant'
)

result = agent.run_sync('What's the weather in NYC?')
# result is typed as WeatherResult
print(result.data.temperature)  # Type-safe!
```

**Key Feature**: Full type safety with Pydantic

---

### 5.6.6 BabyAGI

**Purpose**: Autonomous task management

```python
# Conceptual example
class BabyAGI:
    def __init__(self, objective):
        self.objective = objective
        self.task_list = []
    
    def run(self):
        # 1. Pull first task
        task = self.task_list.pop(0)
        
        # 2. Execute task
        result = self.execute_task(task)
        
        # 3. Create new tasks based on result
        new_tasks = self.create_new_tasks(result, self.objective)
        
        # 4. Prioritize tasks
        self.task_list = self.prioritize_tasks(
            self.task_list + new_tasks
        )
        
        # 5. Repeat
        if self.task_list:
            self.run()
```

**Concept**: Autonomous task generation and execution

---

### 5.6.7 AutoGPT

**Purpose**: Fully autonomous agents

```python
# Simplified conceptual flow
class AutoGPT:
    def run(self, goal):
        while not goal_achieved:
            # Think
            thoughts = self.llm.invoke(
                f"Goal: {goal}\nProgress: {self.memory}\nWhat next?"
            )
            
            # Plan
            plan = self.extract_plan(thoughts)
            
            # Act
            for action in plan:
                result = self.execute(action)
                self.memory.store(action, result)
            
            # Reflect
            if self.should_revise_approach():
                goal = self.refine_goal(goal)
```

**Key Idea**: Give AI a goal, it figures out everything else

---

### 5.6.8 MetaGPT

**Purpose**: Multi-agent software company

```python
from metagpt.roles import ProductManager, Architect, Engineer
from metagpt.team import Team

# Create software development team
team = Team()
team.hire([
    ProductManager(),
    Architect(),
    Engineer()
])

# Give requirement
team.run_project("Build a web app for task management")

# Output: PRD, architecture design, code
```

**Unique Feature**: Simulates entire software company

---

## 5.7 Framework Comparison Table

| Framework | Best For | Complexity | Community | Production-Ready |
|-----------|----------|------------|-----------|------------------|
| **LangChain** | General agents, RAG | Medium | Large | Yes |
| **LangGraph** | Complex workflows | High | Growing | Yes |
| **CrewAI** | Role-based multi-agent | Low-Medium | Medium | Yes |
| **AutoGen** | Conversational agents | Medium | Medium | Partial |
| **Semantic Kernel** | Enterprise apps | Medium | Medium | Yes |
| **LlamaIndex** | RAG, document Q&A | Low-Medium | Large | Yes |
| **Haystack** | NLP pipelines | Medium | Medium | Yes |
| **DSPy** | Research, optimization | High | Small | No |
| **PydanticAI** | Type-safe apps | Low-Medium | Small | Yes |
| **AutoGPT** | Autonomous tasks | High | Large | No |
| **BabyAGI** | Task automation | Medium | Medium | No |
| **MetaGPT** | Software generation | High | Small | No |

---

## 5.8 When to Use Which Framework

### Decision Tree

```
Need RAG? 
├─ Yes → LlamaIndex or LangChain
└─ No ↓

Need multi-agent collaboration?
├─ Yes → CrewAI (role-based) or AutoGen (conversational)
└─ No ↓

Need complex workflows with loops?
├─ Yes → LangGraph
└─ No ↓

Need type safety?
├─ Yes → PydanticAI
└─ No ↓

Enterprise requirements?
├─ Yes → Semantic Kernel
└─ No → LangChain (general purpose)
```

---

<a name="section-6"></a>
# SECTION 6 — MULTI-AGENT SYSTEMS

## 6.1 What are Multi-Agent Systems?

### Definition

**Multi-Agent System (MAS)**: Multiple autonomous agents collaborating to solve complex problems that are difficult or impossible for a single agent.

### Why Multi-Agent?

| Single Agent | Multi-Agent System |
|--------------|-------------------|
| Generalist | Specialists |
| Sequential processing | Parallel execution |
| Limited perspective | Diverse viewpoints |
| Single point of failure | Fault tolerant |
| Scales poorly | Scales better |

### Real-World Analogy

**Single Agent** = One person doing everything  
**Multi-Agent** = A company with specialized departments

```
Company (Multi-Agent System)
├── Research Department (Research Agent)
├── Engineering Department (Engineering Agent)
├── Marketing Department (Marketing Agent)
└── Management (Coordinator Agent)
```

---

## 6.2 Single Agent vs Multi-Agent

### Single Agent Workflow

```
Query: "Build and launch a product"
   ↓
Single Agent:
├─ Research market
├─ Design product
├─ Write code
├─ Test
├─ Create marketing
├─ Deploy
└─ Monitor
```

**Challenges**:
- Overloaded with tasks
- Context switching
- Generic at everything, expert at nothing
- Sequential execution (slow)

---

### Multi-Agent Workflow

```
Query: "Build and launch a product"
   ↓
Coordinator Agent delegates:
   ├─→ Research Agent → Market analysis
   ├─→ Product Agent → Requirements & design
   ├─→ Engineering Agent → Development
   ├─→ QA Agent → Testing
   ├─→ Marketing Agent → Campaign
   └─→ DevOps Agent → Deployment
   
All work in parallel ✓
Each agent is specialized ✓
```

---

## 6.3 Agent Communication

### Communication Patterns

#### **1. Direct Messaging**
```python
class Agent:
    def send_message(self, recipient, message):
        recipient.receive_message(self.id, message)
    
    def receive_message(self, sender_id, message):
        self.inbox.append({
            "from": sender_id,
            "content": message,
            "timestamp": datetime.now()
        })
```

#### **2. Broadcast**
```python
class CommunicationLayer:
    def broadcast(self, sender, message):
        for agent in self.agents:
            if agent.id != sender.id:
                agent.receive_message(sender.id, message)
```

#### **3. Message Queues**
```python
from queue import Queue

class MessageBus:
    def __init__(self):
        self.queues = {}
    
    def publish(self, topic, message):
        if topic in self.queues:
            self.queues[topic].put(message)
    
    def subscribe(self, topic, agent):
        if topic not in self.queues:
            self.queues[topic] = Queue()
        # Agent listens to this topic
```

---

## 6.4 Agent Orchestration Patterns

### Pattern 1: Coordinator-Worker (Hub-and-Spoke)

```
         [Coordinator]
            ↙  ↓  ↘
      Worker1 Worker2 Worker3
```

**Implementation**:
```python
class CoordinatorAgent:
    def __init__(self, workers):
        self.workers = workers
    
    def delegate(self, task):
        # Decompose task
        subtasks = self.break_down_task(task)
        
        # Assign to workers
        results = []
        for subtask, worker in zip(subtasks, self.workers):
            result = worker.execute(subtask)
            results.append(result)
        
        # Synthesize
        final_result = self.combine_results(results)
        return final_result

# Usage
coordinator = CoordinatorAgent(
    workers=[research_agent, analysis_agent, writing_agent]
)

result = coordinator.delegate("Write report on AI trends")
```

**Best For**:
- Clear task decomposition
- Independent subtasks
- Centralized control

---

### Pattern 2: Hierarchical

```
        [Manager]
         ↙      ↘
   [Team Lead1] [Team Lead2]
    ↙    ↘       ↙    ↘
  W1    W2     W3    W4
```

**Implementation**:
```python
class ManagerAgent:
    def __init__(self, team_leads):
        self.team_leads = team_leads
    
    def assign_project(self, project):
        # High-level decomposition
        phases = self.plan_phases(project)
        
        # Delegate to team leads
        for phase, lead in zip(phases, self.team_leads):
            lead.manage_phase(phase)

class TeamLeadAgent:
    def __init__(self, workers):
        self.workers = workers
    
    def manage_phase(self, phase):
        tasks = self.break_into_tasks(phase)
        return self.distribute_to_workers(tasks)
```

**Best For**:
- Large projects
- Multiple layers of management
- Scalability

---

### Pattern 3: Peer-to-Peer (Decentralized)

```
Agent1 ←→ Agent2
  ↕         ↕
Agent3 ←→ Agent4
```

**Implementation**:
```python
class PeerAgent:
    def __init__(self, peers):
        self.peers = peers
        self.knowledge = {}
    
    def collaborate(self, task):
        # Share task with peers
        self.broadcast(f"I'm working on {task}")
        
        # Get input from peers
        peer_inputs = [peer.contribute(task) for peer in self.peers]
        
        # Integrate perspectives
        solution = self.integrate(peer_inputs)
        
        # Share solution
        self.broadcast(f"My solution: {solution}")
        
        return solution
```

**Best For**:
- Collaborative brainstorming
- Consensus building
- Fault tolerance

---

### Pattern 4: Blackboard Architecture

```
         [Blackboard]
         (Shared Memory)
              ↕
     ┌────────┼────────┐
     ↓        ↓        ↓
  Agent1  Agent2  Agent3
  
Each agent reads/writes to shared state
```

**Implementation**:
```python
class Blackboard:
    """Shared knowledge base"""
    def __init__(self):
        self.knowledge = {}
        self.subscribers = []
    
    def write(self, key, value, author):
        self.knowledge[key] = {
            "value": value,
            "author": author,
            "timestamp": datetime.now()
        }
        self.notify_subscribers(key)
    
    def read(self, key):
        return self.knowledge.get(key)

class BlackboardAgent:
    def __init__(self, blackboard, specialty):
        self.blackboard = blackboard
        self.specialty = specialty
    
    def work(self):
        # Read current state
        state = self.blackboard.read("current_state")
        
        # Contribute expertise
        if self.can_contribute(state):
            contribution = self.analyze(state)
            self.blackboard.write(
                key=self.specialty,
                value=contribution,
                author=self.id
            )
```

**Best For**:
- Complex problem-solving
- Multiple knowledge sources
- Opportunistic reasoning

---

## 6.5 Supervisor Agents

### Role of Supervisor

A **Supervisor Agent**:
1. Receives high-level goals
2. Plans overall strategy
3. Delegates to worker agents
4. Monitors progress
5. Resolves conflicts
6. Synthesizes final output

### Implementation

```python
class SupervisorAgent:
    def __init__(self, workers):
        self.workers = {w.role: w for w in workers}
        self.task_queue = []
        self.results = {}
    
    def execute(self, goal):
        # 1. Plan
        plan = self.create_plan(goal)
        
        # 2. Delegate
        for step in plan:
            worker = self.select_worker(step)
            task = self.create_task(step)
            
            # Assign
            result = worker.execute(task)
            self.results[step.id] = result
            
            # Check quality
            if not self.meets_standards(result):
                # Reassign or refine
                result = self.handle_subpar_work(step, result)
        
        # 3. Synthesize
        final = self.combine_results(self.results)
        
        return final
    
    def create_plan(self, goal):
        prompt = f"""
        Goal: {goal}
        
        Available workers:
        {self.list_workers()}
        
        Create a step-by-step plan.
        Assign each step to the most appropriate worker.
        """
        
        plan = self.llm.invoke(prompt)
        return self.parse_plan(plan)
    
    def select_worker(self, step):
        # Match step to worker capability
        return self.workers[step.assigned_role]
    
    def handle_subpar_work(self, step, result):
        # Option 1: Ask for revision
        feedback = self.generate_feedback(result)
        revised = self.workers[step.assigned_role].revise(result, feedback)
        
        # Option 2: Reassign to different worker
        if not self.meets_standards(revised):
            alt_worker = self.find_alternative_worker(step)
            revised = alt_worker.execute(step)
        
        return revised
```

---

## 6.6 Task Delegation

### Delegation Strategies

#### **1. Skill-Based Delegation**
```python
def delegate_by_skill(task, agents):
    # Match task requirements to agent skills
    scores = []
    for agent in agents:
        skill_match = calculate_skill_match(task.required_skills, agent.skills)
        scores.append((agent, skill_match))
    
    # Assign to best match
    best_agent = max(scores, key=lambda x: x[1])[0]
    return best_agent
```

#### **2. Load-Balanced Delegation**
```python
def delegate_by_load(task, agents):
    # Find least busy agent
    least_busy = min(agents, key=lambda a: a.current_workload)
    
    if least_busy.current_workload < threshold:
        return least_busy
    else:
        # All busy, queue task
        return None
```

#### **3. Round-Robin Delegation**
```python
class RoundRobinDelegator:
    def __init__(self, agents):
        self.agents = agents
        self.current_index = 0
    
    def delegate(self, task):
        agent = self.agents[self.current_index]
        self.current_index = (self.current_index + 1) % len(self.agents)
        return agent
```

---

## 6.7 Parallel Execution

### Concurrent Task Execution

```python
import asyncio

class ParallelExecutor:
    def __init__(self, agents):
        self.agents = agents
    
    async def execute_parallel(self, tasks):
        # Create coroutines for each task
        coroutines = [
            self.execute_task_async(task, agent)
            for task, agent in zip(tasks, self.agents)
        ]
        
        # Execute concurrently
        results = await asyncio.gather(*coroutines)
        
        return results
    
    async def execute_task_async(self, task, agent):
        # Simulate agent work
        result = await agent.execute_async(task)
        return result

# Usage
executor = ParallelExecutor([agent1, agent2, agent3])
tasks = [task1, task2, task3]

results = asyncio.run(executor.execute_parallel(tasks))
```

### Benefits of Parallel Execution

| Aspect | Sequential | Parallel |
|--------|-----------|----------|
| **Time** | 3 tasks × 10min = 30min | max(10min, 10min, 10min) = 10min |
| **Throughput** | 1 task at a time | Multiple simultaneous |
| **Resource Use** | Underutilized | Fully utilized |

---

## 6.8 Conflict Resolution

### Types of Conflicts

#### **1. Resource Conflicts**
Multiple agents need the same resource.

```python
class ResourceManager:
    def __init__(self):
        self.resources = {}
        self.locks = {}
    
    def request_resource(self, agent_id, resource_id):
        if resource_id in self.locks:
            # Resource in use
            return None
        else:
            # Grant access
            self.locks[resource_id] = agent_id
            return self.resources[resource_id]
    
    def release_resource(self, resource_id):
        if resource_id in self.locks:
            del self.locks[resource_id]
```

#### **2. Opinion Conflicts**
Agents disagree on the approach.

```python
def resolve_by_voting(agents, proposals):
    votes = {}
    for proposal in proposals:
        votes[proposal] = 0
    
    # Each agent votes
    for agent in agents:
        preferred = agent.evaluate_proposals(proposals)
        votes[preferred] += 1
    
    # Majority wins
    winner = max(votes.items(), key=lambda x: x[1])[0]
    return winner

def resolve_by_expertise(agents, proposals, domain):
    # Find most expert agent in domain
    expert = max(agents, key=lambda a: a.expertise[domain])
    
    # Expert decides
    decision = expert.choose(proposals)
    return decision
```

#### **3. Priority Conflicts**
Multiple urgent tasks, limited resources.

```python
def resolve_by_priority(tasks):
    # Sort by priority and deadline
    sorted_tasks = sorted(
        tasks,
        key=lambda t: (t.priority, t.deadline)
    )
    
    return sorted_tasks[0]  # Highest priority, soonest deadline
```

---

## 6.9 Shared Memory in Multi-Agent Systems

### Shared Memory Architecture

```python
class SharedMemory:
    """Thread-safe shared memory for agents"""
    def __init__(self):
        self.storage = {}
        self.lock = threading.Lock()
    
    def write(self, key, value):
        with self.lock:
            self.storage[key] = {
                "value": value,
                "timestamp": datetime.now(),
                "version": self.storage.get(key, {}).get("version", 0) + 1
            }
    
    def read(self, key):
        with self.lock:
            return self.storage.get(key, {}).get("value")
    
    def read_latest(self, pattern):
        """Read all keys matching pattern"""
        with self.lock:
            matching = {
                k: v for k, v in self.storage.items()
                if pattern in k
            }
            return matching

class Agent:
    def __init__(self, shared_memory):
        self.shared_memory = shared_memory
    
    def share_knowledge(self, key, value):
        self.shared_memory.write(key, value)
    
    def access_knowledge(self, key):
        return self.shared_memory.read(key)
```

---

## 6.10 Real-World Multi-Agent Examples

### Example 1: Software Development Team

```python
class SoftwareDevelopmentCrew:
    def __init__(self):
        self.pm = ProductManagerAgent()
        self.architect = ArchitectAgent()
        self.frontend_dev = FrontendAgent()
        self.backend_dev = BackendAgent()
        self.qa = QAAgent()
        self.devops = DevOpsAgent()
    
    def build_feature(self, requirement):
        # 1. PM creates spec
        spec = self.pm.write_spec(requirement)
        
        # 2. Architect designs
        architecture = self.architect.design(spec)
        
        # 3. Development (parallel)
        frontend_code = self.frontend_dev.implement(architecture.frontend)
        backend_code = self.backend_dev.implement(architecture.backend)
        
        # 4. QA tests
        test_results = self.qa.test(frontend_code, backend_code)
        
        # 5. If issues, loop back
        if test_results.has_bugs:
            # Developers fix
            frontend_code = self.frontend_dev.fix(test_results.frontend_bugs)
            backend_code = self.backend_dev.fix(test_results.backend_bugs)
        
        # 6. DevOps deploys
        deployment = self.devops.deploy(frontend_code, backend_code)
        
        return deployment
```

### Example 2: Research Team

```python
class ResearchTeam:
    def __init__(self):
        self.literature_reviewer = LiteratureReviewAgent()
        self.data_collector = DataCollectionAgent()
        self.analyst = AnalysisAgent()
        self.writer = WritingAgent()
        self.peer_reviewer = PeerReviewAgent()
    
    def conduct_research(self, topic):
        # 1. Literature review
        papers = self.literature_reviewer.find_papers(topic)
        gaps = self.literature_reviewer.identify_gaps(papers)
        
        # 2. Data collection
        data = self.data_collector.gather_data(gaps.research_questions)
        
        # 3. Analysis
        findings = self.analyst.analyze(data)
        
        # 4. Writing
        draft = self.writer.write_paper(papers, findings)
        
        # 5. Peer review
        feedback = self.peer_reviewer.review(draft)
        
        # 6. Revision loop
        while not feedback.ready_to_publish:
            draft = self.writer.revise(draft, feedback)
            feedback = self.peer_reviewer.review(draft)
        
        return draft
```

---

## 6.11 Multi-Agent System Architecture

### Complete MAS Architecture

```python
class MultiAgentSystem:
    def __init__(self):
        # Communication layer
        self.message_bus = MessageBus()
        
        # Shared resources
        self.shared_memory = SharedMemory()
        self.blackboard = Blackboard()
        
        # Agents
        self.agents = []
        self.supervisor = None
        
        # Monitoring
        self.monitor = SystemMonitor()
    
    def register_agent(self, agent):
        agent.set_communication(self.message_bus)
        agent.set_shared_memory(self.shared_memory)
        self.agents.append(agent)
    
    def set_supervisor(self, supervisor):
        self.supervisor = supervisor
        supervisor.set_workers(self.agents)
    
    def execute(self, goal):
        # Start monitoring
        self.monitor.start()
        
        # Supervisor orchestrates
        result = self.supervisor.execute(goal)
        
        # Stop monitoring
        metrics = self.monitor.stop()
        
        return {
            "result": result,
            "metrics": metrics
        }

# Usage
mas = MultiAgentSystem()

# Create agents
research_agent = ResearchAgent()
analysis_agent = AnalysisAgent()
writing_agent = WritingAgent()

# Register agents
mas.register_agent(research_agent)
mas.register_agent(analysis_agent)
mas.register_agent(writing_agent)

# Set supervisor
supervisor = SupervisorAgent()
mas.set_supervisor(supervisor)

# Execute
result = mas.execute("Research quantum computing and write a report")
```

---

<a name="section-7"></a>
# SECTION 7 — TOOLS AND TOOL CALLING

## 7.1 What is Tool Calling?

### Definition

**Tool Calling** is the ability of an AI agent to use external functions, APIs, or services to extend its capabilities beyond text generation.

### Why Tools Matter

```
LLM alone:
- Can't access real-time data
- Can't perform accurate math
- Can't take actions
- Limited to training data

LLM + Tools:
- ✅ Access current information
- ✅ Precise calculations
- ✅ Send emails, book flights
- ✅ Query databases
```

---

## 7.2 Function Calling

### OpenAI Function Calling

```python
import openai

# Define functions
functions = [
    {
        "name": "get_current_weather",
        "description": "Get the current weather for a location",
        "parameters": {
            "type": "object",
            "properties": {
                "location": {
                    "type": "string",
                    "description": "City name, e.g. San Francisco"
                },
                "unit": {
                    "type": "string",
                    "enum": ["celsius", "fahrenheit"]
                }
            },
            "required": ["location"]
        }
    },
    {
        "name": "calculate",
        "description": "Perform mathematical calculation",
        "parameters": {
            "type": "object",
            "properties": {
                "expression": {
                    "type": "string",
                    "description": "Math expression to evaluate"
                }
            },
            "required": ["expression"]
        }
    }
]

# Call LLM
response = openai.ChatCompletion.create(
    model="gpt-4",
    messages=[{"role": "user", "content": "What's the weather in NYC?"}],
    functions=functions,
    function_call="auto"
)

# Check if function was called
if response.choices[0].message.get("function_call"):
    function_name = response.choices[0].message["function_call"]["name"]
    function_args = json.loads(
        response.choices[0].message["function_call"]["arguments"]
    )
    
    # Execute function
    if function_name == "get_current_weather":
        result = get_current_weather(**function_args)
    
    # Send result back to LLM
    second_response = openai.ChatCompletion.create(
        model="gpt-4",
        messages=[
            {"role": "user", "content": "What's the weather in NYC?"},
            response.choices[0].message,
            {
                "role": "function",
                "name": function_name,
                "content": str(result)
            }
        ]
    )
    
    print(second_response.choices[0].message.content)
```

---

## 7.3 Tool Types

### 1. Information Retrieval Tools

#### **Web Search**
```python
def web_search(query):
    """Search the web for current information"""
    import requests
    
    response = requests.get(
        "https://api.search.com/search",
        params={"q": query}
    )
    
    return response.json()["results"]
```

#### **Database Query**
```python
def query_database(sql_query):
    """Query SQL database"""
    import sqlite3
    
    conn = sqlite3.connect("database.db")
    cursor = conn.cursor()
    cursor.execute(sql_query)
    
    results = cursor.fetchall()
    conn.close()
    
    return results
```

#### **Vector Search**
```python
def semantic_search(query, knowledge_base):
    """Search vector database"""
    query_embedding = embed(query)
    results = knowledge_base.similarity_search(query_embedding, k=5)
    
    return results
```

---

### 2. Computation Tools

#### **Calculator**
```python
def calculator(expression):
    """Evaluate mathematical expression safely"""
    import ast
    import operator as op
    
    # Supported operations
    operators = {
        ast.Add: op.add,
        ast.Sub: op.sub,
        ast.Mult: op.mul,
        ast.Div: op.truediv,
        ast.Pow: op.pow
    }
    
    def eval_expr(node):
        if isinstance(node, ast.Num):
            return node.n
        elif isinstance(node, ast.BinOp):
            return operators[type(node.op)](
                eval_expr(node.left),
                eval_expr(node.right)
            )
        else:
            raise ValueError("Unsupported operation")
    
    tree = ast.parse(expression, mode='eval')
    return eval_expr(tree.body)
```

#### **Code Interpreter**
```python
def execute_python(code):
    """Execute Python code in sandbox"""
    import subprocess
    
    # Run in isolated environment
    result = subprocess.run(
        ["python", "-c", code],
        capture_output=True,
        text=True,
        timeout=5
    )
    
    return result.stdout if result.returncode == 0 else result.stderr
```

---

### 3. Action Tools

#### **Email Sender**
```python
def send_email(to, subject, body):
    """Send email via Gmail API"""
    import smtplib
    from email.mime.text import MIMEText
    
    msg = MIMEText(body)
    msg['Subject'] = subject
    msg['From'] = "agent@example.com"
    msg['To'] = to
    
    with smtplib.SMTP('smtp.gmail.com', 587) as server:
        server.starttls()
        server.login("agent@example.com", "password")
        server.send_message(msg)
    
    return "Email sent successfully"
```

#### **Calendar**
```python
def create_calendar_event(title, start_time, duration_minutes):
    """Create event in Google Calendar"""
    from googleapiclient.discovery import build
    
    service = build('calendar', 'v3', credentials=creds)
    
    event = {
        'summary': title,
        'start': {'dateTime': start_time},
        'end': {'dateTime': calculate_end_time(start_time, duration_minutes)}
    }
    
    created_event = service.events().insert(
        calendarId='primary',
        body=event
    ).execute()
    
    return f"Event created: {created_event.get('htmlLink')}"
```

---

### 4. Data Manipulation Tools

#### **File Operations**
```python
def read_file(filepath):
    """Read file contents"""
    with open(filepath, 'r') as f:
        return f.read()

def write_file(filepath, content):
    """Write content to file"""
    with open(filepath, 'w') as f:
        f.write(content)
    return f"Written to {filepath}"
```

#### **CSV Analysis**
```python
def analyze_csv(filepath):
    """Analyze CSV file"""
    import pandas as pd
    
    df = pd.read_csv(filepath)
    
    analysis = {
        "rows": len(df),
        "columns": list(df.columns),
        "summary": df.describe().to_dict(),
        "missing_values": df.isnull().sum().to_dict()
    }
    
    return analysis
```

---

## 7.4 Model Context Protocol (MCP)

### What is MCP?

**Model Context Protocol** is a standard for connecting AI models to external data sources and tools.

### MCP Architecture

```
┌─────────────┐
│  AI Model   │
└──────┬──────┘
       │ MCP
       ↓
┌──────────────┐
│ MCP Server   │
├──────────────┤
│  • Resources │ ← Access to data
│  • Prompts   │ ← Template management
│  • Tools     │ ← Function calling
└──────────────┘
       ↓
   External
   Systems
```

### MCP Server Example

```python
from mcp import Server, Resource, Tool

class FileSystemMCP(Server):
    @tool
    def read_file(self, path: str) -> str:
        """Read a file from the filesystem"""
        with open(path) as f:
            return f.read()
    
    @tool
    def list_directory(self, path: str) -> list:
        """List files in directory"""
        import os
        return os.listdir(path)
    
    @resource(uri="file://{path}")
    def file_resource(self, path: str):
        """Access file as resource"""
        return {
            "content": self.read_file(path),
            "mime_type": "text/plain"
        }

# Start server
server = FileSystemMCP()
server.serve()
```

---

## 7.5 Tool Registries

### Tool Registry Pattern

```python
class ToolRegistry:
    def __init__(self):
        self.tools = {}
    
    def register(self, name, function, description, parameters):
        self.tools[name] = {
            "function": function,
            "description": description,
            "parameters": parameters
        }
    
    def get_tool(self, name):
        return self.tools.get(name)
    
    def list_tools(self):
        return [
            {
                "name": name,
                "description": tool["description"],
                "parameters": tool["parameters"]
            }
            for name, tool in self.tools.items()
        ]
    
    def execute(self, name, **kwargs):
        tool = self.get_tool(name)
        if not tool:
            raise ValueError(f"Tool {name} not found")
        
        return tool["function"](**kwargs)

# Usage
registry = ToolRegistry()

# Register tools
registry.register(
    name="weather",
    function=get_weather,
    description="Get current weather for a location",
    parameters={
        "location": {"type": "string", "required": True}
    }
)

registry.register(
    name="calculator",
    function=calculator,
    description="Perform mathematical calculations",
    parameters={
        "expression": {"type": "string", "required": True}
    }
)

# List available tools
tools = registry.list_tools()

# Execute tool
result = registry.execute("weather", location="NYC")
```

---

## 7.6 Dynamic Tool Selection

### How Agents Choose Tools

```python
class ToolSelector:
    def __init__(self, llm, tools):
        self.llm = llm
        self.tools = tools
    
    def select_tool(self, user_query):
        # Create prompt with tool descriptions
        tool_descriptions = self.format_tools()
        
        prompt = f"""
        User query: {user_query}
        
        Available tools:
        {tool_descriptions}
        
        Which tool is most appropriate? Respond with tool name and parameters.
        Format: {{"tool": "tool_name", "parameters": {{...}}}}
        """
        
        response = self.llm.invoke(prompt)
        decision = json.loads(response)
        
        return decision
    
    def format_tools(self):
        return "\n".join([
            f"- {tool['name']}: {tool['description']}"
            for tool in self.tools
        ])

# Usage
selector = ToolSelector(llm, registry.list_tools())

decision = selector.select_tool("What's the weather in Paris?")
# Returns: {"tool": "weather", "parameters": {"location": "Paris"}}

result = registry.execute(**decision)
```

---

## 7.7 Secure Tool Execution

### Security Considerations

1. **Input Validation**
2. **Sandboxing**
3. **Rate Limiting**
4. **Permission Control**
5. **Audit Logging**

### Implementation

```python
class SecureToolExecutor:
    def __init__(self):
        self.permissions = {}
        self.rate_limits = {}
        self.audit_log = []
    
    def execute(self, tool_name, agent_id, **kwargs):
        # 1. Check permissions
        if not self.has_permission(agent_id, tool_name):
            raise PermissionError(f"Agent {agent_id} lacks permission for {tool_name}")
        
        # 2. Rate limiting
        if self.is_rate_limited(agent_id, tool_name):
            raise RateLimitError(f"Rate limit exceeded for {tool_name}")
        
        # 3. Input validation
        validated_kwargs = self.validate_inputs(tool_name, kwargs)
        
        # 4. Execute in sandbox
        try:
            result = self.execute_sandboxed(tool_name, validated_kwargs)
        except Exception as e:
            self.log_error(agent_id, tool_name, e)
            raise
        
        # 5. Audit log
        self.log_execution(agent_id, tool_name, validated_kwargs, result)
        
        return result
    
    def execute_sandboxed(self, tool_name, kwargs):
        """Execute tool in isolated environment"""
        import subprocess
        import json
        
        # Serialize call
        call_data = json.dumps({
            "tool": tool_name,
            "args": kwargs
        })
        
        # Execute in subprocess with timeout
        result = subprocess.run(
            ["python", "tool_executor.py"],
            input=call_data,
            capture_output=True,
            text=True,
            timeout=30  # 30 second timeout
        )
        
        if result.returncode != 0:
            raise RuntimeError(result.stderr)
        
        return json.loads(result.stdout)
    
    def validate_inputs(self, tool_name, kwargs):
        # Schema validation
        schema = self.get_tool_schema(tool_name)
        
        for param, value in kwargs.items():
            if param not in schema["parameters"]:
                raise ValueError(f"Unexpected parameter: {param}")
            
            expected_type = schema["parameters"][param]["type"]
            if not isinstance(value, self.get_python_type(expected_type)):
                raise TypeError(f"{param} should be {expected_type}")
        
        return kwargs
```

---

## 7.8 Complete Tool-Calling Agent Example

```python
class ToolCallingAgent:
    def __init__(self, llm, tools):
        self.llm = llm
        self.tools = {tool["name"]: tool for tool in tools}
        self.conversation_history = []
    
    def chat(self, user_message):
        self.conversation_history.append({
            "role": "user",
            "content": user_message
        })
        
        # Agent loop
        max_iterations = 5
        for i in range(max_iterations):
            # Get LLM response
            response = self.llm.invoke(
                messages=self.conversation_history,
                tools=list(self.tools.values())
            )
            
            # Check if tool call
            if hasattr(response, 'tool_calls') and response.tool_calls:
                for tool_call in response.tool_calls:
                    # Execute tool
                    result = self.execute_tool(
                        tool_call.name,
                        tool_call.arguments
                    )
                    
                    # Add to history
                    self.conversation_history.append({
                        "role": "tool",
                        "tool_call_id": tool_call.id,
                        "content": str(result)
                    })
                
                # Continue loop (LLM will see tool results)
                continue
            else:
                # No more tool calls, we have final answer
                self.conversation_history.append({
                    "role": "assistant",
                    "content": response.content
                })
                return response.content
        
        return "Max iterations reached"
    
    def execute_tool(self, tool_name, arguments):
        tool = self.tools.get(tool_name)
        if not tool:
            return f"Error: Tool {tool_name} not found"
        
        try:
            result = tool["function"](**arguments)
            return result
        except Exception as e:
            return f"Error executing {tool_name}: {str(e)}"

# Define tools
tools = [
    {
        "name": "get_weather",
        "description": "Get current weather",
        "function": get_weather,
        "parameters": {
            "type": "object",
            "properties": {
                "location": {"type": "string"}
            }
        }
    },
    {
        "name": "calculator",
        "description": "Perform calculations",
        "function": calculator,
        "parameters": {
            "type": "object",
            "properties": {
                "expression": {"type": "string"}
            }
        }
    }
]

# Create agent
agent = ToolCallingAgent(llm, tools)

# Use agent
response = agent.chat("What's 25% of 400, and what's the weather in that city?")
```

---

<a name="section-8"></a>
# SECTION 8 — RAG + AGENTIC AI

## 8.1 What is Agentic RAG?

### Traditional RAG vs Agentic RAG

**Traditional RAG**:
```
Query → Retrieve Documents → Generate Answer
```

**Agentic RAG**:
```
Query → Plan Retrieval Strategy → Multi-hop Retrieval → 
Re-rank → Validate → Generate → Critique → Refine
```

### Why Agentic RAG?

| Traditional RAG | Agentic RAG |
|-----------------|-------------|
| Single retrieval | Multi-step retrieval |
| No query planning | Strategic query decomposition |
| No validation | Self-verification |
| No refinement | Iterative improvement |
| Fixed pipeline | Adaptive workflow |

---

## 8.2 Agentic RAG Architecture

```
┌──────────────────────────────────────────┐
│         USER QUERY                        │
└────────────────┬─────────────────────────┘
                 ↓
┌──────────────────────────────────────────┐
│    QUERY UNDERSTANDING & PLANNING         │
│  • Decompose complex queries              │
│  • Identify information needs             │
│  • Plan retrieval strategy                │
└────────────────┬─────────────────────────┘
                 ↓
┌──────────────────────────────────────────┐
│    ADAPTIVE RETRIEVAL                     │
│  • Query rewriting                        │
│  • Multi-hop retrieval                    │
│  • Hybrid search (vector + keyword)       │
└────────────────┬─────────────────────────┘
                 ↓
┌──────────────────────────────────────────┐
│    RE-RANKING & FILTERING                 │
│  • Relevance scoring                      │
│  • Remove redundant info                  │
│  • Prioritize high-quality sources        │
└────────────────┬─────────────────────────┘
                 ↓
┌──────────────────────────────────────────┐
│    GENERATION WITH GROUNDING              │
│  • Generate answer with citations         │
│  • Ensure factual grounding               │
│  • Handle missing information             │
└────────────────┬─────────────────────────┘
                 ↓
┌──────────────────────────────────────────┐
│    VERIFICATION & REFINEMENT              │
│  • Fact-check against sources             │
│  • Identify gaps                          │
│  • Retrieve more if needed (loop back)    │
└────────────────┬─────────────────────────┘
                 ↓
         FINAL ANSWER
```

---

## 8.3 Query Rewriting

### Why Rewrite Queries?

User queries are often vague or poorly formulated for retrieval.

**Original Query**: "it performance issues"  
**Rewritten Queries**:
- "Common IT performance bottlenecks"
- "Database performance optimization techniques"
- "Network latency troubleshooting"
- "Application server performance tuning"

### Implementation

```python
class QueryRewriter:
    def __init__(self, llm):
        self.llm = llm
    
    def rewrite(self, original_query):
        prompt = f"""
        Original query: "{original_query}"
        
        Rewrite this query into multiple specific, detailed search queries
        that would retrieve the most relevant information.
        
        Generate 3-5 alternative queries.
        Format as JSON array.
        """
        
        response = self.llm.invoke(prompt)
        rewritten_queries = json.loads(response)
        
        return rewritten_queries
    
    def expand_query(self, query):
        """Add synonyms and related terms"""
        prompt = f"""
        Query: "{query}"
        
        Expand this query with:
        - Synonyms
        - Related terms
        - Technical terminology
        
        Return expanded query string.
        """
        
        return self.llm.invoke(prompt)

# Usage
rewriter = QueryRewriter(llm)
queries = rewriter.rewrite("machine learning basics")
# Returns: [
#   "Introduction to machine learning algorithms",
#   "Supervised vs unsupervised learning explained",
#   "Machine learning fundamentals for beginners",
#   "Core concepts in ML: training, testing, validation"
# ]
```

---

## 8.4 Retrieval Planning

### Multi-Step Retrieval Strategy

```python
class RetrievalPlanner:
    def __init__(self, llm):
        self.llm = llm
    
    def plan_retrieval(self, query):
        prompt = f"""
        Query: "{query}"
        
        Create a step-by-step retrieval plan to answer this query.
        
        For each step, specify:
        1. What information to search for
        2. Why it's needed
        3. Search strategy (vector, keyword, hybrid)
        
        Return as JSON.
        """
        
        plan = self.llm.invoke(prompt)
        return json.loads(plan)

# Example plan for "Impact of climate change on agriculture"
plan = {
    "steps": [
        {
            "step": 1,
            "search_for": "Climate change temperature and precipitation trends",
            "why": "Establish baseline climate changes",
            "strategy": "vector_search"
        },
        {
            "step": 2,
            "search_for": "Agricultural crop yields historical data",
            "why": "Understand current agricultural patterns",
            "strategy": "hybrid_search"
        },
        {
            "step": 3,
            "search_for": "Studies linking climate variables to crop production",
            "why": "Find causal relationships",
            "strategy": "vector_search"
        },
        {
            "step": 4,
            "search_for": "Future projections and adaptation strategies",
            "why": "Provide actionable insights",
            "strategy": "vector_search"
        }
    ]
}
```

---

## 8.5 Multi-Hop Retrieval

### What is Multi-Hop Retrieval?

Retrieving information through multiple connected queries.

**Example**:
- Query: "What company does the CEO of Tesla's brother work for?"
- Hop 1: "Who is the CEO of Tesla?" → Elon Musk
- Hop 2: "Who is Elon Musk's brother?" → Kimbal Musk
- Hop 3: "What company does Kimbal Musk work for?" → Square Roots

### Implementation

```python
class MultiHopRetriever:
    def __init__(self, retriever, llm):
        self.retriever = retriever
        self.llm = llm
    
    def retrieve_multi_hop(self, query, max_hops=3):
        """Perform multi-hop retrieval"""
        current_query = query
        context = []
        
        for hop in range(max_hops):
            # Retrieve documents
            docs = self.retriever.get_relevant_documents(current_query)
            context.extend(docs)
            
            # Check if we have enough info
            if self.can_answer(query, context):
                break
            
            # Generate next hop query
            next_query = self.generate_next_query(query, context)
            if not next_query:
                break
            
            current_query = next_query
        
        return context
    
    def can_answer(self, original_query, context):
        """Check if context is sufficient"""
        prompt = f"""
        Original question: {original_query}
        
        Context: {context}
        
        Can this context answer the question? (yes/no)
        """
        
        response = self.llm.invoke(prompt)
        return "yes" in response.lower()
    
    def generate_next_query(self, original_query, current_context):
        """Generate follow-up query"""
        prompt = f"""
        Original question: {original_query}
        
        Information found so far: {current_context}
        
        What additional information is needed?
        Generate a specific search query for the missing information.
        If all information is available, respond with "COMPLETE".
        """
        
        response = self.llm.invoke(prompt)
        
        if "COMPLETE" in response:
            return None
        
        return response
```

---

## 8.6 Hybrid Retrieval

### Combining Vector and Keyword Search

```python
from rank_bm25 import BM25Okapi
import numpy as np

class HybridRetriever:
    def __init__(self, documents, embedding_model):
        self.documents = documents
        self.embedding_model = embedding_model
        
        # Vector search setup
        self.embeddings = [
            embedding_model.encode(doc) 
            for doc in documents
        ]
        
        # Keyword search setup
        tokenized_docs = [doc.split() for doc in documents]
        self.bm25 = BM25Okapi(tokenized_docs)
    
    def retrieve(self, query, k=5, alpha=0.5):
        """
        Hybrid retrieval combining vector and keyword search
        
        alpha: weight for vector search (1-alpha for keyword)
        """
        # Vector search
        query_embedding = self.embedding_model.encode(query)
        vector_scores = [
            np.dot(query_embedding, doc_emb) /
            (np.linalg.norm(query_embedding) * np.linalg.norm(doc_emb))
            for doc_emb in self.embeddings
        ]
        
        # Keyword search
        tokenized_query = query.split()
        keyword_scores = self.bm25.get_scores(tokenized_query)
        
        # Normalize scores
        vector_scores = self.normalize(vector_scores)
        keyword_scores = self.normalize(keyword_scores)
        
        # Combine
        hybrid_scores = [
            alpha * v_score + (1 - alpha) * k_score
            for v_score, k_score in zip(vector_scores, keyword_scores)
        ]
        
        # Get top k
        top_k_indices = np.argsort(hybrid_scores)[-k:][::-1]
        
        return [
            {
                "document": self.documents[i],
                "score": hybrid_scores[i],
                "vector_score": vector_scores[i],
                "keyword_score": keyword_scores[i]
            }
            for i in top_k_indices
        ]
    
    def normalize(self, scores):
        scores = np.array(scores)
        return (scores - scores.min()) / (scores.max() - scores.min() + 1e-10)
```

---

## 8.7 Re-Ranking

### Why Re-Rank?

Initial retrieval may return many documents. Re-ranking improves precision.

### Cross-Encoder Re-Ranking

```python
from sentence_transformers import CrossEncoder

class Reranker:
    def __init__(self, model_name='cross-encoder/ms-marco-MiniLM-L-6-v2'):
        self.model = CrossEncoder(model_name)
    
    def rerank(self, query, documents, top_k=5):
        """Re-rank documents using cross-encoder"""
        # Create query-document pairs
        pairs = [[query, doc] for doc in documents]
        
        # Score all pairs
        scores = self.model.predict(pairs)
        
        # Sort by score
        ranked_indices = np.argsort(scores)[::-1]
        
        # Return top k
        return [
            {
                "document": documents[i],
                "score": scores[i]
            }
            for i in ranked_indices[:top_k]
        ]
```

### LLM-Based Re-Ranking

```python
class LLMReranker:
    def __init__(self, llm):
        self.llm = llm
    
    def rerank(self, query, documents, top_k=5):
        """Use LLM to assess relevance"""
        scored_docs = []
        
        for doc in documents:
            prompt = f"""
            Query: {query}
            
            Document: {doc}
            
            Rate the relevance of this document to the query on a scale of 0-10.
            Respond with just the number.
            """
            
            score = float(self.llm.invoke(prompt))
            scored_docs.append({"document": doc, "score": score})
        
        # Sort and return top k
        scored_docs.sort(key=lambda x: x["score"], reverse=True)
        return scored_docs[:top_k]
```

---

## 8.8 Hallucination Reduction

### Techniques

#### 1. **Grounding with Citations**

```python
class GroundedGenerator:
    def __init__(self, llm):
        self.llm = llm
    
    def generate_with_citations(self, query, documents):
        # Number documents
        doc_text = "\n\n".join([
            f"[{i+1}] {doc}"
            for i, doc in enumerate(documents)
        ])
        
        prompt = f"""
        Query: {query}
        
        Documents:
        {doc_text}
        
        Answer the query using ONLY information from the documents.
        Cite sources using [1], [2], etc.
        If information is not in the documents, say so.
        """
        
        answer = self.llm.invoke(prompt)
        return answer
```

#### 2. **Fact Verification**

```python
class FactVerifier:
    def __init__(self, llm):
        self.llm = llm
    
    def verify(self, claim, sources):
        prompt = f"""
        Claim: "{claim}"
        
        Sources: {sources}
        
        Is this claim supported by the sources?
        
        Respond with:
        - "SUPPORTED" if claim is in sources
        - "CONTRADICTED" if sources contradict
        - "NOT_FOUND" if not mentioned
        
        Include explanation.
        """
        
        verification = self.llm.invoke(prompt)
        return verification
    
    def verify_response(self, response, sources):
        # Extract claims
        claims = self.extract_claims(response)
        
        # Verify each claim
        results = []
        for claim in claims:
            verification = self.verify(claim, sources)
            results.append({
                "claim": claim,
                "verification": verification
            })
        
        # Flag if any unsupported
        unsupported = [r for r in results if "NOT_FOUND" in r["verification"]]
        
        return {
            "all_verified": len(unsupported) == 0,
            "results": results
        }
```

---

## 8.9 Citation Systems

### Automatic Citation Generation

```python
class CitationGenerator:
    def __init__(self, llm):
        self.llm = llm
    
    def generate_with_citations(self, query, documents):
        # Create document metadata
        doc_metadata = [
            {
                "id": i+1,
                "content": doc["content"],
                "source": doc.get("source", "Unknown"),
                "date": doc.get("date", "N/A")
            }
            for i, doc in enumerate(documents)
        ]
        
        prompt = f"""
        Query: {query}
        
        Documents:
        {json.dumps(doc_metadata, indent=2)}
        
        Answer the query and cite your sources.
        
        Use inline citations: [1], [2], etc.
        
        At the end, include a "References" section with full citations.
        """
        
        response = self.llm.invoke(prompt)
        
        return response

# Example output:
"""
The transformer architecture revolutionized NLP [1]. It introduced the 
attention mechanism which allows models to weigh the importance of different 
words [2]. This led to models like BERT and GPT [3].

References:
[1] Vaswani et al., "Attention Is All You Need", 2017
[2] Bahdanau et al., "Neural Machine Translation by Jointly Learning to Align and Translate", 2014
[3] Devlin et al., "BERT: Pre-training of Deep Bidirectional Transformers", 2018
"""
```

---

## 8.10 Adaptive Retrieval

### Self-Reflective RAG

```python
class AdaptiveRAG:
    def __init__(self, retriever, llm):
        self.retriever = retriever
        self.llm = llm
    
    def answer_with_adaptive_retrieval(self, query):
        context = []
        max_iterations = 3
        
        for iteration in range(max_iterations):
            # Retrieve documents
            new_docs = self.retriever.get_relevant_documents(query)
            context.extend(new_docs)
            
            # Generate answer attempt
            answer = self.generate_answer(query, context)
            
            # Self-assess
            assessment = self.assess_answer(query, answer, context)
            
            if assessment["confident"]:
                return {
                    "answer": answer,
                    "iterations": iteration + 1,
                    "confidence": assessment["confidence"]
                }
            else:
                # Refine retrieval
                query = self.refine_query(
                    query, 
                    answer, 
                    assessment["missing_info"]
                )
        
        # Return best attempt
        return {
            "answer": answer,
            "iterations": max_iterations,
            "confidence": "low",
            "note": "Maximum iterations reached"
        }
    
    def assess_answer(self, query, answer, context):
        prompt = f"""
        Query: {query}
        Answer: {answer}
        Context: {context}
        
        Assess this answer:
        1. Is it complete?
        2. Is it well-supported by context?
        3. What information is missing?
        
        Respond with JSON:
        {{
            "confident": true/false,
            "confidence": "high/medium/low",
            "missing_info": "..."
        }}
        """
        
        assessment = self.llm.invoke(prompt)
        return json.loads(assessment)
```

---

## 8.11 Complete Agentic RAG System

```python
class AgenticRAGSystem:
    def __init__(self, vector_store, llm):
        self.vector_store = vector_store
        self.llm = llm
        
        # Components
        self.query_rewriter = QueryRewriter(llm)
        self.retrieval_planner = RetrievalPlanner(llm)
        self.hybrid_retriever = HybridRetriever(vector_store, llm)
        self.reranker = Reranker()
        self.verifier = FactVerifier(llm)
        self.citation_generator = CitationGenerator(llm)
    
    def answer(self, query):
        # 1. Query Understanding
        rewritten_queries = self.query_rewriter.rewrite(query)
        
        # 2. Retrieval Planning
        plan = self.retrieval_planner.plan_retrieval(query)
        
        # 3. Multi-Step Retrieval
        all_docs = []
        for step in plan["steps"]:
            docs = self.hybrid_retriever.retrieve(
                step["search_for"],
                strategy=step["strategy"]
            )
            all_docs.extend(docs)
        
        # 4. Re-ranking
        ranked_docs = self.reranker.rerank(query, all_docs, top_k=10)
        
        # 5. Generate Answer
        answer = self.citation_generator.generate_with_citations(
            query,
            ranked_docs
        )
        
        # 6. Verify
        verification = self.verifier.verify_response(
            answer,
            ranked_docs
        )
        
        # 7. Refine if needed
        if not verification["all_verified"]:
            answer = self.refine_answer(answer, verification)
        
        return {
            "answer": answer,
            "sources": ranked_docs,
            "verification": verification
        }
    
    def refine_answer(self, answer, verification):
        unsupported_claims = [
            r["claim"] for r in verification["results"]
            if "NOT_FOUND" in r["verification"]
        ]
        
        prompt = f"""
        Original answer: {answer}
        
        These claims are not supported by sources:
        {unsupported_claims}
        
        Revise the answer to:
        1. Remove unsupported claims
        2. Acknowledge gaps in knowledge
        3. Maintain accuracy
        """
        
        refined = self.llm.invoke(prompt)
        return refined
```

---

<a name="section-9"></a>
# SECTION 9 — MLOPS + AGENTOPS FOR AGENTS

## 9.1 What is AgentOps?

### Definition

**AgentOps** is the practice of deploying, monitoring, and maintaining AI agents in production.

**MLOps vs AgentOps**:

| Aspect | MLOps | AgentOps |
|--------|-------|----------|
| **Focus** | Model performance | Agent behavior |
| **Metrics** | Accuracy, F1 score | Task completion, tool usage |
| **Monitoring** | Predictions | Actions, decisions |
| **Challenges** | Model drift | Agent drift, unexpected behavior |
| **Debugging** | Model errors | Multi-step failures |

---

## 9.2 Agent Monitoring

### Key Metrics

```python
class AgentMetrics:
    def __init__(self):
        self.metrics = {
            "total_tasks": 0,
            "successful_tasks": 0,
            "failed_tasks": 0,
            "avg_completion_time": 0,
            "tool_usage": {},
            "error_types": {},
            "cost": 0
        }
    
    def log_task(self, task_id, status, duration, tools_used, cost):
        self.metrics["total_tasks"] += 1
        
        if status == "success":
            self.metrics["successful_tasks"] += 1
        else:
            self.metrics["failed_tasks"] += 1
        
        # Update average completion time
        n = self.metrics["total_tasks"]
        self.metrics["avg_completion_time"] = (
            (self.metrics["avg_completion_time"] * (n - 1) + duration) / n
        )
        
        # Track tool usage
        for tool in tools_used:
            self.metrics["tool_usage"][tool] = \
                self.metrics["tool_usage"].get(tool, 0) + 1
        
        # Track cost
        self.metrics["cost"] += cost
    
    def get_success_rate(self):
        if self.metrics["total_tasks"] == 0:
            return 0
        return self.metrics["successful_tasks"] / self.metrics["total_tasks"]
    
    def get_dashboard(self):
        return {
            "success_rate": self.get_success_rate(),
            "avg_time": self.metrics["avg_completion_time"],
            "total_cost": self.metrics["cost"],
            "most_used_tools": sorted(
                self.metrics["tool_usage"].items(),
                key=lambda x: x[1],
                reverse=True
            )[:5]
        }
```

---

## 9.3 Tracing

### Execution Tracing

```python
import time
from typing import Dict, List, Any

class AgentTracer:
    def __init__(self):
        self.traces = []
        self.current_trace = None
    
    def start_trace(self, query: str, metadata: Dict = None):
        """Start new trace"""
        self.current_trace = {
            "trace_id": self.generate_trace_id(),
            "query": query,
            "metadata": metadata or {},
            "start_time": time.time(),
            "steps": [],
            "status": "in_progress"
        }
    
    def log_step(self, step_type: str, data: Any):
        """Log individual step"""
        if not self.current_trace:
            raise ValueError("No active trace")
        
        step = {
            "step_id": len(self.current_trace["steps"]) + 1,
            "type": step_type,
            "data": data,
            "timestamp": time.time()
        }
        
        self.current_trace["steps"].append(step)
    
    def log_llm_call(self, prompt: str, response: str, tokens: int, cost: float):
        """Log LLM interaction"""
        self.log_step("llm_call", {
            "prompt": prompt,
            "response": response,
            "tokens": tokens,
            "cost": cost
        })
    
    def log_tool_call(self, tool_name: str, inputs: Dict, output: Any):
        """Log tool execution"""
        self.log_step("tool_call", {
            "tool": tool_name,
            "inputs": inputs,
            "output": output
        })
    
    def end_trace(self, result: Any, status: str = "success"):
        """Complete trace"""
        if not self.current_trace:
            return
        
        self.current_trace["end_time"] = time.time()
        self.current_trace["duration"] = (
            self.current_trace["end_time"] - self.current_trace["start_time"]
        )
        self.current_trace["result"] = result
        self.current_trace["status"] = status
        
        # Calculate total cost
        total_cost = sum(
            step["data"].get("cost", 0)
            for step in self.current_trace["steps"]
            if step["type"] == "llm_call"
        )
        self.current_trace["total_cost"] = total_cost
        
        # Store trace
        self.traces.append(self.current_trace)
        self.current_trace = None
    
    def get_trace(self, trace_id: str):
        """Retrieve specific trace"""
        for trace in self.traces:
            if trace["trace_id"] == trace_id:
                return trace
        return None
    
    def generate_trace_id(self):
        import uuid
        return str(uuid.uuid4())

# Usage
tracer = AgentTracer()

# Start trace
tracer.start_trace("What's the weather in Paris?")

# Log steps
tracer.log_llm_call(
    prompt="Plan how to answer: What's the weather in Paris?",
    response="I need to use the weather API",
    tokens=50,
    cost=0.001
)

tracer.log_tool_call(
    tool_name="get_weather",
    inputs={"location": "Paris"},
    output={"temp": 18, "condition": "Sunny"}
)

tracer.log_llm_call(
    prompt="Format the weather data",
    response="It's 18°C and sunny in Paris",
    tokens=30,
    cost=0.0006
)

# End trace
tracer.end_trace(result="It's 18°C and sunny in Paris", status="success")

# Analyze trace
trace = tracer.traces[0]
print(f"Duration: {trace['duration']}s")
print(f"Cost: ${trace['total_cost']}")
```

---

## 9.4 Evaluation

### Agent Evaluation Framework

```python
class AgentEvaluator:
    def __init__(self, test_cases):
        self.test_cases = test_cases
        self.results = []
    
    def evaluate(self, agent):
        """Run evaluation suite"""
        for test in self.test_cases:
            result = self.run_test(agent, test)
            self.results.append(result)
        
        return self.compute_metrics()
    
    def run_test(self, agent, test):
        """Execute single test case"""
        query = test["query"]
        expected = test["expected"]
        
        # Run agent
        start_time = time.time()
        try:
            actual = agent.execute(query)
            status = "success"
            error = None
        except Exception as e:
            actual = None
            status = "error"
            error = str(e)
        
        duration = time.time() - start_time
        
        # Evaluate correctness
        correctness_score = self.evaluate_correctness(actual, expected)
        
        return {
            "test_id": test["id"],
            "query": query,
            "expected": expected,
            "actual": actual,
            "status": status,
            "error": error,
            "duration": duration,
            "correctness": correctness_score
        }
    
    def evaluate_correctness(self, actual, expected):
        """Compare actual vs expected output"""
        if actual is None:
            return 0.0
        
        # Use LLM to judge similarity
        prompt = f"""
        Expected output: {expected}
        Actual output: {actual}
        
        Rate similarity on 0-1 scale.
        Consider:
        - Factual accuracy
        - Completeness
        - Relevance
        
        Respond with just the number.
        """
        
        score = float(self.llm.invoke(prompt))
        return score
    
    def compute_metrics(self):
        """Calculate overall metrics"""
        total = len(self.results)
        successful = sum(1 for r in self.results if r["status"] == "success")
        
        avg_correctness = sum(
            r["correctness"] for r in self.results
        ) / total
        
        avg_duration = sum(
            r["duration"] for r in self.results
        ) / total
        
        return {
            "success_rate": successful / total,
            "avg_correctness": avg_correctness,
            "avg_duration": avg_duration,
            "total_tests": total
        }

# Usage
test_cases = [
    {
        "id": 1,
        "query": "What's 25% of 400?",
        "expected": "100"
    },
    {
        "id": 2,
        "query": "Book a meeting for tomorrow at 2pm",
        "expected": "Meeting booked for [tomorrow's date] at 14:00"
    }
]

evaluator = AgentEvaluator(test_cases)
results = evaluator.evaluate(my_agent)
print(results)
```

---

## 9.5 Prompt Versioning

### Prompt Management System

```python
class PromptVersionControl:
    def __init__(self):
        self.prompts = {}
        self.versions = {}
    
    def register_prompt(self, name: str, template: str, version: str = "1.0"):
        """Register new prompt or version"""
        if name not in self.prompts:
            self.prompts[name] = {}
            self.versions[name] = []
        
        self.prompts[name][version] = {
            "template": template,
            "created_at": datetime.now(),
            "active": True
        }
        
        self.versions[name].append(version)
    
    def get_prompt(self, name: str, version: str = "latest"):
        """Retrieve prompt by version"""
        if version == "latest":
            version = self.versions[name][-1]
        
        return self.prompts[name][version]["template"]
    
    def compare_versions(self, name: str, v1: str, v2: str):
        """Compare two prompt versions"""
        import difflib
        
        prompt1 = self.prompts[name][v1]["template"]
        prompt2 = self.prompts[name][v2]["template"]
        
        diff = difflib.unified_diff(
            prompt1.splitlines(),
            prompt2.splitlines(),
            lineterm=''
        )
        
        return '\n'.join(diff)

# Usage
pvc = PromptVersionControl()

# Register v1
pvc.register_prompt(
    name="research_agent",
    template="You are a research assistant. Answer: {query}",
    version="1.0"
)

# Register improved v2
pvc.register_prompt(
    name="research_agent",
    template="""You are an expert research assistant.
    
    Query: {query}
    
    Provide a detailed, well-sourced answer with citations.""",
    version="2.0"
)

# Use specific version
prompt = pvc.get_prompt("research_agent", version="2.0")
```

---

## 9.6 Cost Tracking

### Cost Monitoring

```python
class CostTracker:
    def __init__(self):
        self.costs = []
        self.pricing = {
            "gpt-4": {"input": 0.03 / 1000, "output": 0.06 / 1000},
            "gpt-3.5-turbo": {"input": 0.001 / 1000, "output": 0.002 / 1000},
            "claude-3": {"input": 0.015 / 1000, "output": 0.075 / 1000}
        }
    
    def log_llm_call(self, model: str, input_tokens: int, output_tokens: int,
                     metadata: Dict = None):
        """Log API call cost"""
        pricing = self.pricing.get(model)
        if not pricing:
            cost = 0
        else:
            cost = (
                input_tokens * pricing["input"] +
                output_tokens * pricing["output"]
            )
        
        self.costs.append({
            "timestamp": datetime.now(),
            "model": model,
            "input_tokens": input_tokens,
            "output_tokens": output_tokens,
            "cost": cost,
            "metadata": metadata or {}
        })
        
        return cost
    
    def get_total_cost(self, time_range: str = "all"):
        """Calculate total cost"""
        if time_range == "all":
            return sum(c["cost"] for c in self.costs)
        
        # Filter by time range
        cutoff = datetime.now() - self.parse_time_range(time_range)
        recent_costs = [
            c for c in self.costs
            if c["timestamp"] > cutoff
        ]
        
        return sum(c["cost"] for c in recent_costs)
    
    def get_cost_breakdown(self):
        """Break down costs by model"""
        breakdown = {}
        for cost in self.costs:
            model = cost["model"]
            if model not in breakdown:
                breakdown[model] = {
                    "calls": 0,
                    "total_cost": 0,
                    "total_tokens": 0
                }
            
            breakdown[model]["calls"] += 1
            breakdown[model]["total_cost"] += cost["cost"]
            breakdown[model]["total_tokens"] += (
                cost["input_tokens"] + cost["output_tokens"]
            )
        
        return breakdown
    
    def set_budget_alert(self, threshold: float):
        """Alert when cost exceeds threshold"""
        total = self.get_total_cost()
        if total > threshold:
            self.send_alert(f"Budget exceeded: ${total:.2f} > ${threshold}")

# Usage
tracker = CostTracker()

# Log calls
tracker.log_llm_call("gpt-4", input_tokens=1000, output_tokens=500)
tracker.log_llm_call("gpt-3.5-turbo", input_tokens=500, output_tokens=300)

# Get stats
print(f"Total cost: ${tracker.get_total_cost():.4f}")
print(f"Breakdown: {tracker.get_cost_breakdown()}")
```

---

## 9.7 Guardrails

### Safety Guardrails for Agents

```python
class AgentGuardrails:
    def __init__(self):
        self.blocked_actions = []
        self.require_approval = []
        self.rate_limits = {}
    
    def check_action(self, action: str, params: Dict):
        """Validate action before execution"""
        # 1. Check if blocked
        if self.is_blocked(action):
            raise PermissionError(f"Action {action} is blocked")
        
        # 2. Check rate limits
        if self.exceeds_rate_limit(action):
            raise RateLimitError(f"Rate limit exceeded for {action}")
        
        # 3. Check if requires approval
        if self.requires_human_approval(action, params):
            return "APPROVAL_REQUIRED"
        
        # 4. Validate parameters
        self.validate_params(action, params)
        
        return "APPROVED"
    
    def is_blocked(self, action: str):
        """Check if action is blocked"""
        return action in self.blocked_actions
    
    def requires_human_approval(self, action: str, params: Dict):
        """Check if action needs human approval"""
        # High-risk actions
        if action in ["delete_data", "send_money", "modify_database"]:
            return True
        
        # High-value transactions
        if action == "purchase" and params.get("amount", 0) > 1000:
            return True
        
        # Bulk operations
        if params.get("batch_size", 0) > 100:
            return True
        
        return False
    
    def validate_params(self, action: str, params: Dict):
        """Validate action parameters"""
        # Example: Email validation
        if action == "send_email":
            if "to" not in params:
                raise ValueError("Missing 'to' parameter")
            if not self.is_valid_email(params["to"]):
                raise ValueError(f"Invalid email: {params['to']}")
        
        # Example: SQL injection prevention
        if action == "database_query":
            if self.contains_sql_injection(params.get("query", "")):
                raise SecurityError("Potential SQL injection detected")
    
    def contains_sql_injection(self, query: str):
        """Basic SQL injection detection"""
        dangerous = ["DROP", "DELETE", "INSERT", "UPDATE", "--", ";"]
        query_upper = query.upper()
        return any(word in query_upper for word in dangerous)

# Usage
guardrails = AgentGuardrails()

# Configure guardrails
guardrails.blocked_actions = ["delete_all_data", "shutdown_system"]

# Check action
try:
    status = guardrails.check_action(
        "send_email",
        {"to": "user@example.com", "subject": "Hello"}
    )
    if status == "APPROVED":
        execute_action()
    elif status == "APPROVAL_REQUIRED":
        request_human_approval()
except PermissionError as e:
    print(f"Action blocked: {e}")
```

---

## 9.8 LangSmith Integration

### Using LangSmith for Observability

```python
from langsmith import Client
from langchain.callbacks import LangChainTracer

# Initialize LangSmith
client = Client()
tracer = LangChainTracer(project_name="my-agent-project")

# Use with LangChain agents
agent = create_agent(llm, tools, callbacks=[tracer])

# Execute with tracing
result = agent.invoke({"input": "Research quantum computing"})

# Query traces
runs = client.list_runs(
    project_name="my-agent-project",
    run_type="chain"
)

# Analyze performance
for run in runs:
    print(f"Run ID: {run.id}")
    print(f"Duration: {run.end_time - run.start_time}")
    print(f"Tokens: {run.total_tokens}")
    print(f"Cost: ${run.cost}")
```

---

## 9.9 Production Deployment Best Practices

### Deployment Checklist

```python
class ProductionReadinessChecklist:
    def __init__(self):
        self.checks = {
            "monitoring": False,
            "error_handling": False,
            "rate_limiting": False,
            "cost_tracking": False,
            "security": False,
            "testing": False,
            "documentation": False,
            "rollback_plan": False
        }
    
    def verify_monitoring(self):
        """Check if monitoring is set up"""
        required = [
            "metrics collection",
            "logging",
            "tracing",
            "alerting"
        ]
        # Verify each component
        return all(self.check_component(c) for c in required)
    
    def verify_error_handling(self):
        """Check error handling"""
        checks = [
            "try-catch blocks",
            "graceful degradation",
            "retry logic",
            "fallback mechanisms"
        ]
        return all(self.check_component(c) for c in checks)
    
    def verify_security(self):
        """Check security measures"""
        checks = [
            "input validation",
            "API key encryption",
            "rate limiting",
            "access controls"
        ]
        return all(self.check_component(c) for c in checks)
    
    def run_checks(self):
        """Run all checks"""
        self.checks["monitoring"] = self.verify_monitoring()
        self.checks["error_handling"] = self.verify_error_handling()
        self.checks["security"] = self.verify_security()
        # ... other checks
        
        return self.checks
    
    def is_production_ready(self):
        """Check if all criteria met"""
        results = self.run_checks()
        return all(results.values())
```

---

<a name="section-10"></a>
# SECTION 10 — REAL-WORLD APPLICATIONS

## 10.1 AI Research Assistant

### Architecture

```python
class AIResearchAssistant:
    def __init__(self):
        self.llm = ChatOpenAI(model="gpt-4")
        self.tools = [
            ArxivSearchTool(),
            GoogleScholarTool(),
            WikipediaTool(),
            CalculatorTool(),
            SummarizationTool()
        ]
        self.memory = VectorMemory()
    
    def research(self, topic):
        """Conduct comprehensive research"""
        # 1. Literature Review
        papers = self.find_papers(topic)
        
        # 2. Summarize Key Papers
        summaries = [self.summarize(paper) for paper in papers[:10]]
        
        # 3. Identify Trends
        trends = self.identify_trends(summaries)
        
        # 4. Generate Report
        report = self.generate_report(topic, papers, trends)
        
        return report
    
    def find_papers(self, topic):
        """Search academic databases"""
        arxiv_results = self.tools[0].search(topic, max_results=20)
        scholar_results = self.tools[1].search(topic, max_results=20)
        
        # Combine and deduplicate
        all_papers = arxiv_results + scholar_results
        return self.deduplicate(all_papers)
    
    def identify_trends(self, summaries):
        """Extract common themes"""
        prompt = f"""
        Paper summaries:
        {summaries}
        
        Identify:
        1. Common research directions
        2. Emerging techniques
        3. Open challenges
        4. Future opportunities
        """
        
        trends = self.llm.invoke(prompt)
        return trends
```

### Tech Stack

```
├── LLM: GPT-4 / Claude
├── Framework: LangChain
├── Tools:
│   ├── ArXiv API
│   ├── Google Scholar
│   ├── Semantic Scholar API
│   └── Wikipedia API
├── Storage: Pinecone (papers database)
├── Frontend: Streamlit
└── Deployment: AWS Lambda + API Gateway
```

---

## 10.2 Healthcare Clinical Decision Support Agent

### Use Case

Assist doctors with diagnosis, treatment recommendations, and drug interactions.

### Architecture

```python
class ClinicalDecisionAgent:
    def __init__(self):
        self.llm = ChatOpenAI(model="gpt-4")
        self.medical_kb = MedicalKnowledgeBase()
        self.drug_db = DrugInteractionDatabase()
        self.guidelines = ClinicalGuidelinesDB()
    
    def analyze_case(self, patient_data):
        """Analyze patient case"""
        # 1. Extract symptoms
        symptoms = self.extract_symptoms(patient_data)
        
        # 2. Differential diagnosis
        possible_conditions = self.differential_diagnosis(symptoms)
        
        # 3. Recommend tests
        recommended_tests = self.recommend_diagnostic_tests(
            possible_conditions
        )
        
        # 4. Treatment options
        treatments = self.suggest_treatments(possible_conditions)
        
        # 5. Check drug interactions
        if patient_data.get("current_medications"):
            interactions = self.check_interactions(
                patient_data["current_medications"],
                treatments
            )
        
        return {
            "differential_diagnosis": possible_conditions,
            "recommended_tests": recommended_tests,
            "treatment_options": treatments,
            "drug_interactions": interactions,
            "clinical_guidelines": self.find_relevant_guidelines(
                possible_conditions
            )
        }
    
    def differential_diagnosis(self, symptoms):
        """Generate differential diagnosis"""
        prompt = f"""
        Patient symptoms: {symptoms}
        
        Provide differential diagnosis with:
        1. Condition name
        2. Likelihood (high/medium/low)
        3. Key distinguishing features
        4. Recommended confirmatory tests
        """
        
        diagnoses = self.llm.invoke(prompt)
        
        # Verify against medical knowledge base
        verified = self.medical_kb.verify_diagnoses(diagnoses)
        
        return verified
```

### Challenges

- **Safety**: Must not replace doctor judgment
- **Accuracy**: High stakes, zero tolerance for errors
- **Regulation**: HIPAA compliance, FDA approval
- **Liability**: Clear disclaimers about limitations

---

## 10.3 Financial Analysis Agent

### Capabilities

```python
class FinancialAnalystAgent:
    def __init__(self):
        self.llm = ChatOpenAI(model="gpt-4")
        self.tools = [
            StockPriceTool(),
            FinancialStatementsTool(),
            NewsAnalysisTool(),
            TechnicalAnalysisTool(),
            MacroeconomicDataTool()
        ]
    
    def analyze_stock(self, ticker):
        """Comprehensive stock analysis"""
        # 1. Fundamental Analysis
        fundamentals = self.fundamental_analysis(ticker)
        
        # 2. Technical Analysis
        technicals = self.technical_analysis(ticker)
        
        # 3. Sentiment Analysis
        sentiment = self.analyze_sentiment(ticker)
        
        # 4. Valuation
        valuation = self.calculate_valuation(ticker)
        
        # 5. Investment Recommendation
        recommendation = self.generate_recommendation(
            fundamentals,
            technicals,
            sentiment,
            valuation
        )
        
        return {
            "ticker": ticker,
            "fundamental_score": fundamentals,
            "technical_score": technicals,
            "sentiment_score": sentiment,
            "fair_value": valuation,
            "recommendation": recommendation
        }
    
    def fundamental_analysis(self, ticker):
        """Analyze financial statements"""
        financials = self.tools[1].get_financials(ticker)
        
        metrics = {
            "p_e_ratio": financials["market_cap"] / financials["earnings"],
            "debt_to_equity": financials["total_debt"] / financials["equity"],
            "roe": financials["net_income"] / financials["equity"],
            "revenue_growth": self.calculate_growth(
                financials["revenue_history"]
            )
        }
        
        # Score fundamentals
        score = self.score_fundamentals(metrics)
        return score
```

---

## 10.4 Customer Support Automation

### Multi-Tier Support System

```python
class CustomerSupportSystem:
    def __init__(self):
        self.tier1 = BasicSupportAgent()  # Simple queries
        self.tier2 = TechnicalSupportAgent()  # Complex issues
        self.human_escalation = HumanEscalationService()
        self.knowledge_base = SupportKnowledgeBase()
    
    def handle_ticket(self, ticket):
        """Route and handle support ticket"""
        # 1. Classify complexity
        complexity = self.classify_ticket(ticket)
        
        # 2. Route to appropriate agent
        if complexity == "simple":
            response = self.tier1.handle(ticket)
        elif complexity == "complex":
            response = self.tier2.handle(ticket)
        else:
            # Escalate to human
            return self.human_escalation.create_ticket(ticket)
        
        # 3. Verify solution quality
        if self.is_satisfactory(response):
            return response
        else:
            # Escalate
            return self.human_escalation.create_ticket(ticket, context=response)
    
    def classify_ticket(self, ticket):
        """Determine ticket complexity"""
        prompt = f"""
        Support ticket: {ticket}
        
        Classify complexity:
        - "simple": FAQ, account issues, basic troubleshooting
        - "complex": Technical errors, billing disputes, feature requests
        - "escalation": Angry customer, legal issues, security concerns
        """
        
        classification = self.llm.invoke(prompt)
        return classification

class BasicSupportAgent:
    def handle(self, ticket):
        """Handle simple support queries"""
        # 1. Search knowledge base
        relevant_articles = self.kb.search(ticket.query)
        
        # 2. Generate response
        response = self.generate_response(ticket, relevant_articles)
        
        # 3. Include help links
        response["helpful_links"] = [
            article["url"] for article in relevant_articles[:3]
        ]
        
        return response
```

---

## 10.5 Coding Agent

### Auto-Debugging and Code Generation

```python
class CodingAgent:
    def __init__(self):
        self.llm = ChatOpenAI(model="gpt-4")
        self.code_executor = PythonREPL()
    
    def fix_code(self, broken_code, error_message):
        """Debug and fix code"""
        max_attempts = 3
        
        for attempt in range(max_attempts):
            # 1. Analyze error
            analysis = self.analyze_error(broken_code, error_message)
            
            # 2. Generate fix
            fixed_code = self.generate_fix(broken_code, analysis)
            
            # 3. Test fix
            result = self.test_code(fixed_code)
            
            if result["success"]:
                return {
                    "fixed_code": fixed_code,
                    "explanation": analysis,
                    "attempts": attempt + 1
                }
            else:
                # Update for next iteration
                error_message = result["error"]
                broken_code = fixed_code
        
        return {
            "status": "failed",
            "message": "Could not fix after 3 attempts"
        }
    
    def analyze_error(self, code, error):
        """Understand what went wrong"""
        prompt = f"""
        Code:
        {code}
        
        Error:
        {error}
        
        Explain:
        1. What caused the error
        2. How to fix it
        3. Best practices to prevent it
        """
        
        return self.llm.invoke(prompt)
    
    def generate_code(self, requirements):
        """Generate code from requirements"""
        # 1. Create implementation plan
        plan = self.plan_implementation(requirements)
        
        # 2. Generate code
        code = self.llm.invoke(f"""
        Requirements: {requirements}
        Plan: {plan}
        
        Write clean, well-documented Python code.
        Include error handling and type hints.
        """)
        
        # 3. Test code
        test_results = self.test_code(code)
        
        # 4. Refine if needed
        if not test_results["success"]:
            code = self.fix_code(code, test_results["error"])
        
        return code
```

---

## 10.6 Data Analysis Agent

### Autonomous Data Exploration

```python
class DataAnalysisAgent:
    def __init__(self):
        self.llm = ChatOpenAI(model="gpt-4")
        self.python_repl = PythonREPL()
    
    def analyze_dataset(self, df):
        """Comprehensive data analysis"""
        # 1. Initial exploration
        overview = self.explore_data(df)
        
        # 2. Identify analysis goals
        goals = self.identify_analysis_goals(overview)
        
        # 3. Execute analyses
        results = []
        for goal in goals:
            analysis = self.run_analysis(df, goal)
            results.append(analysis)
        
        # 4. Generate insights
        insights = self.extract_insights(results)
        
        # 5. Create visualizations
        visualizations = self.create_visualizations(df, insights)
        
        # 6. Write report
        report = self.generate_report(insights, visualizations)
        
        return report
    
    def explore_data(self, df):
        """Initial data exploration"""
        code = f"""
        import pandas as pd
        import numpy as np
        
        df = {df.to_dict()}
        
        summary = {{
            'shape': df.shape,
            'columns': df.dtypes.to_dict(),
            'missing': df.isnull().sum().to_dict(),
            'stats': df.describe().to_dict()
        }}
        
        summary
        """
        
        result = self.python_repl.run(code)
        return result
    
    def identify_analysis_goals(self, overview):
        """Determine what analyses to run"""
        prompt = f"""
        Dataset overview:
        {overview}
        
        Suggest 3-5 valuable analyses to run.
        Consider:
        - Correlations
        - Trends
        - Anomalies
        - Distributions
        - Relationships
        """
        
        goals = self.llm.invoke(prompt)
        return goals
```

---


<a name="section-11"></a>
# SECTION 11 — ADVANCED TOPICS

## 11.1 Autonomous Reasoning

### Self-Directed Problem Solving

```python
class AutonomousReasoningAgent:
    def __init__(self, llm):
        self.llm = llm
        self.reasoning_trace = []
    
    def solve(self, problem):
        """Autonomously reason through complex problem"""
        # 1. Understand the problem
        understanding = self.understand_problem(problem)
        
        # 2. Break down into sub-problems
        sub_problems = self.decompose(understanding)
        
        # 3. Solve each sub-problem
        solutions = []
        for sub_problem in sub_problems:
            solution = self.solve_sub_problem(sub_problem)
            solutions.append(solution)
            
            # Self-verify
            if not self.verify_solution(sub_problem, solution):
                # Rethink approach
                solution = self.alternative_approach(sub_problem)
        
        # 4. Synthesize final solution
        final_solution = self.synthesize(solutions)
        
        # 5. Validate
        if self.validate_solution(problem, final_solution):
            return final_solution
        else:
            # Start over with new strategy
            return self.solve_with_different_strategy(problem)
    
    def decompose(self, problem):
        """Break problem into manageable pieces"""
        prompt = f"""
        Problem: {problem}
        
        Decompose this into 3-5 sub-problems that:
        1. Are simpler than the original
        2. Can be solved independently
        3. Together solve the main problem
        
        Format as JSON array.
        """
        
        sub_problems = self.llm.invoke(prompt)
        return json.loads(sub_problems)
```

---

## 11.2 Recursive Agents

### Self-Calling Agents for Nested Tasks

```python
class RecursiveAgent:
    def __init__(self, llm, max_depth=5):
        self.llm = llm
        self.max_depth = max_depth
        self.current_depth = 0
    
    def execute(self, task, depth=0):
        """Execute task recursively"""
        if depth >= self.max_depth:
            return "Max recursion depth reached"
        
        # Check if task is atomic
        if self.is_atomic(task):
            return self.execute_atomic(task)
        
        # Decompose into subtasks
        subtasks = self.decompose(task)
        
        # Recursively solve subtasks
        results = []
        for subtask in subtasks:
            result = self.execute(subtask, depth + 1)
            results.append(result)
        
        # Combine results
        return self.combine(results)
    
    def is_atomic(self, task):
        """Check if task can be executed directly"""
        prompt = f"""
        Task: {task}
        
        Can this be executed as a single action? (yes/no)
        """
        
        response = self.llm.invoke(prompt)
        return "yes" in response.lower()
```

---

## 11.3 Self-Improving Agents

### Learning from Experience

```python
class SelfImprovingAgent:
    def __init__(self, llm):
        self.llm = llm
        self.experience_buffer = []
        self.performance_history = []
        self.prompt_versions = []
    
    def learn_from_experience(self):
        """Improve based on past performance"""
        # 1. Analyze failures
        failures = [exp for exp in self.experience_buffer 
                   if exp["success"] == False]
        
        # 2. Identify patterns
        patterns = self.identify_failure_patterns(failures)
        
        # 3. Generate improvements
        improvements = self.generate_improvements(patterns)
        
        # 4. Update prompts
        self.update_prompts(improvements)
        
        # 5. Test improvements
        performance = self.test_new_version()
        
        if performance > self.current_performance:
            self.commit_improvements()
        else:
            self.rollback()
    
    def identify_failure_patterns(self, failures):
        """Find common failure modes"""
        prompt = f"""
        Failed tasks:
        {json.dumps(failures, indent=2)}
        
        Identify common patterns:
        1. Types of tasks that fail
        2. Common error types
        3. Missing capabilities
        
        Return as JSON.
        """
        
        patterns = self.llm.invoke(prompt)
        return json.loads(patterns)
```

---

## 11.4 Multi-Modal Agents

### Vision-Language-Action Models

```python
class MultiModalAgent:
    def __init__(self):
        self.vision_model = VisionEncoder()
        self.language_model = ChatOpenAI(model="gpt-4-vision")
        self.action_executor = ActionExecutor()
    
    def process_multimodal_input(self, image, text):
        """Process both vision and language"""
        # 1. Encode image
        image_features = self.vision_model.encode(image)
        
        # 2. Create multimodal prompt
        prompt = f"""
        Image features: {image_features}
        
        User query: {text}
        
        Describe what you see and respond to the query.
        """
        
        # 3. Generate response
        response = self.language_model.invoke(prompt)
        
        return response
```

---

## 11.5 Human-in-the-Loop Systems

### Collaborative Human-Agent Systems

```python
class HumanInLoopAgent:
    def __init__(self, llm):
        self.llm = llm
        self.approval_required_actions = [
            "delete_data",
            "send_email",
            "make_purchase",
            "publish_content"
        ]
    
    def execute_with_human_oversight(self, task):
        """Execute with human approval for critical actions"""
        # 1. Create plan
        plan = self.create_plan(task)
        
        # 2. Identify actions needing approval
        approval_needed = [
            action for action in plan
            if action["type"] in self.approval_required_actions
        ]
        
        # 3. Request batch approval
        if approval_needed:
            approval = self.request_human_approval(approval_needed)
            
            if not approval["all_approved"]:
                # Remove disapproved actions
                plan = self.revise_plan(plan, approval["disapproved"])
        
        # 4. Execute approved plan
        results = []
        for action in plan:
            result = self.execute_action(action)
            results.append(result)
            
            # Pause for human review if critical
            if action.get("critical"):
                human_review = self.request_human_review(result)
                if human_review["stop"]:
                    break
        
        return results
```

---

<a name="section-12"></a>
# SECTION 12 — CODING + IMPLEMENTATION

## 12.1 Simple Python Agent

```python
from openai import OpenAI

class SimpleAgent:
    """Basic agent with reasoning"""
    
    def __init__(self, api_key):
        self.client = OpenAI(api_key=api_key)
        self.conversation_history = []
    
    def chat(self, user_message):
        """Process user message and respond"""
        # Add user message to history
        self.conversation_history.append({
            "role": "user",
            "content": user_message
        })
        
        # Get response from LLM
        response = self.client.chat.completions.create(
            model="gpt-4",
            messages=self.conversation_history
        )
        
        # Extract and store assistant's response
        assistant_message = response.choices[0].message.content
        self.conversation_history.append({
            "role": "assistant",
            "content": assistant_message
        })
        
        return assistant_message

# Usage
agent = SimpleAgent(api_key="your-key")
response = agent.chat("Hello! What can you help me with?")
print(response)
```

---

## 12.2 LangChain ReAct Agent

```python
from langchain.agents import create_react_agent, AgentExecutor
from langchain.tools import Tool
from langchain_openai import ChatOpenAI

# Define tools
def search_wikipedia(query):
    """Search Wikipedia"""
    import wikipedia
    try:
        return wikipedia.summary(query, sentences=2)
    except:
        return "No results found"

def calculate(expression):
    """Calculate math expression"""
    try:
        return str(eval(expression))
    except:
        return "Invalid expression"

# Create tool objects
tools = [
    Tool(
        name="Wikipedia",
        func=search_wikipedia,
        description="Search Wikipedia for information"
    ),
    Tool(
        name="Calculator",
        func=calculate,
        description="Perform mathematical calculations"
    )
]

# Initialize LLM
llm = ChatOpenAI(model="gpt-4", temperature=0)

# Create and execute agent
agent = create_react_agent(llm, tools, prompt)
agent_executor = AgentExecutor(
    agent=agent,
    tools=tools,
    verbose=True
)

# Execute
result = agent_executor.invoke({
    "input": "Who is the president of France and what's 15% of their age?"
})

print(result["output"])
```

---

## 12.3 LangGraph Workflow

```python
from langgraph.graph import StateGraph, END
from typing import TypedDict

# Define state
class ResearchState(TypedDict):
    query: str
    results: list
    report: str

# Define nodes
def search_node(state):
    results = ["Result 1", "Result 2"]
    return {"results": results}

def write_node(state):
    report = f"Report on {state['query']}"
    return {"report": report}

# Create graph
workflow = StateGraph(ResearchState)
workflow.add_node("search", search_node)
workflow.add_node("write", write_node)
workflow.add_edge("search", "write")
workflow.add_edge("write", END)
workflow.set_entry_point("search")

# Compile and execute
app = workflow.compile()
result = app.invoke({"query": "AI trends", "results": [], "report": ""})
print(result["report"])
```

---

<a name="section-13"></a>
# SECTION 13 — INTERVIEW PREPARATION

## 13.1 Common Interview Questions

### Q1: What is Agentic AI?

**Answer:**
Agentic AI refers to AI systems that can autonomously plan, reason, use tools, and execute multi-step tasks. Unlike traditional AI that provides single responses, agentic AI:
- Breaks complex goals into subtasks
- Uses external tools and APIs
- Maintains memory
- Self-reflects and improves
- Makes autonomous decisions

---

### Q2: Explain ReAct architecture

**Answer:**
ReAct (Reasoning + Acting) interleaves reasoning and action:

```
Thought: "I need weather data"
Action: Call weather API
Observation: "Temperature: 72°F"
Thought: "Now I can answer"
Final Answer: "It's 72°F"
```

This allows step-by-step problem solving with tool use.

---

### Q3: How do you handle hallucinations?

**Answer:**
1. **Grounding**: Force citations to sources
2. **Verification**: Self-check facts
3. **RAG**: Retrieve before generating
4. **Reflection**: Agent critiques own output
5. **Human-in-loop**: Approval for critical outputs

---

<a name="section-14"></a>
# SECTION 14 — COMPARISON TABLES

## 14.1 Framework Comparison

| Framework | Best For | Complexity | Production Ready |
|-----------|----------|------------|------------------|
| LangChain | General agents, RAG | Medium | Yes |
| LangGraph | Complex workflows | High | Yes |
| CrewAI | Multi-agent teams | Medium | Yes |
| AutoGen | Conversational agents | Medium | Partial |

---

## 14.2 Architecture Patterns

| Pattern | Use Case | Complexity | Scalability |
|---------|----------|------------|-------------|
| ReAct | General reasoning | Low | Medium |
| Plan-Execute | Complex tasks | Medium | High |
| Multi-Agent | Specialized tasks | High | Very High |
| Hierarchical | Enterprise | High | Very High |

---

<a name="section-15"></a>
# SECTION 15 — LEARNING ROADMAP

## 15.1 Beginner Path (0-3 Months)

**Month 1: Foundations**
- Python fundamentals
- LLM basics
- Simple chatbots
- Tool calling

**Month 2: Core Concepts**
- Memory systems
- RAG basics
- LangChain
- ReAct agents

**Month 3: First Projects**
- Personal assistant
- Q&A bot
- Research agent

---

## 15.2 Intermediate Path (3-6 Months)

**Month 4: Production**
- Monitoring
- Cost optimization
- Testing
- Deployment

**Month 5: Advanced**
- LangGraph
- Multi-agent
- Complex workflows

**Month 6: Specialization**
- Choose domain
- Build production system
- Optimization

---

<a name="section-16"></a>
# SECTION 16 — PROJECTS

## 16.1 AI Research Assistant

### Overview
Autonomous research assistant that searches papers, analyzes trends, generates reports.

### Architecture
```
User Query
    ↓
Planning Agent → Search Strategy
    ↓
Search Agent → arXiv, Google Scholar
    ↓
Analysis Agent → Extract insights
    ↓
Writing Agent → Generate report
    ↓
Final Report with Citations
```

### Implementation
```python
class ResearchAssistant:
    def research(self, topic):
        # 1. Plan
        plan = self.create_plan(topic)
        
        # 2. Search papers
        papers = self.search_papers(plan)
        
        # 3. Analyze
        insights = self.analyze(papers)
        
        # 4. Report
        report = self.generate_report(insights)
        
        return report
```

---

## 16.2 Customer Support Agent

### Features
- Multi-tier routing
- Knowledge base RAG
- Human escalation
- Learning from interactions

### Tech Stack
- LLM: GPT-4
- Vector DB: Pinecone
- Framework: LangChain
- Monitoring: LangSmith

---

## 16.3 Coding Assistant

### Capabilities
- Code generation
- Debugging
- Refactoring
- Test generation
- Documentation

### Example
```python
class CodingAgent:
    def generate_code(self, requirements):
        plan = self.plan(requirements)
        code = self.implement(plan)
        tests = self.generate_tests(code)
        return code, tests
```

---

# CONCLUSION

This **Agentic AI Complete Handbook** covers:

✅ 16 comprehensive sections  
✅ 300+ pages of content  
✅ Theory + Practice + Code  
✅ Interview questions + answers  
✅ Real-world projects  
✅ Learning roadmap  

**Use this as your complete reference for mastering Agentic AI from beginner to advanced level!**

---

**END OF HANDBOOK**

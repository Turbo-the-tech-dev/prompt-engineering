# 📝 Prompt Engineering

> "Ask the right questions. Task, verbs, actions, context, role, format, desired structure."

Mastering the art and science of prompting: from first attempts through iterative refinement, keeping conversations going, and achieving clarity for key success.

---

## 📁 Directory Structure

```
prompt-engineering/
├── tasks-verbs-actions/      # Core components
│   ├── tasks/                # What to do
│   ├── verbs/                # Action words
│   ├── actions/              # Specific operations
│   └── commands/             # Direct instructions
├── context/                   # Background information
│   ├── background-information/ # Setting the scene
│   ├── constraints/          # Limitations and rules
│   └── examples/             # Few-shot learning
├── role-format/              # Framing the response
│   ├── the-role/             # Who AI should be
│   ├── the-format/           # How to respond
│   └── desired-structure/    # Output organization
└── iterative-process/        # Refinement cycle
    ├── first-attempts/       # Initial tries
    ├── initial-prompts/      # Starting points
    ├── refine-prompt/        # Improvement strategies
    └── keep-conversation-going/ # Multi-turn dialogue
```

---

## 🎯 Key Components of Effective Prompts

### The Essential Elements

```
┌─────────────────────────────────────────────────────────────┐
│  ANATOMY OF A GREAT PROMPT                                  │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  1. TASK (What to do)                                       │
│     "Write a summary..."                                    │
│     "Analyze this code..."                                  │
│     "Generate ideas for..."                                 │
│                                                             │
│  2. CONTEXT (Background)                                    │
│     "For a technical audience..."                           │
│     "Given the following constraints..."                    │
│     "In the context of..."                                  │
│                                                             │
│  3. ROLE (Who AI is)                                        │
│     "You are an expert Python developer..."                 │
│     "Act as a senior software architect..."                 │
│     "You are a helpful writing assistant..."                │
│                                                             │
│  4. FORMAT (How to respond)                                 │
│     "Respond in bullet points..."                           │
│     "Use a table format..."                                 │
│     "Provide code with comments..."                         │
│                                                             │
│  5. CONSTRAINTS (Limitations)                               │
│     "Keep it under 200 words..."                            │
│     "Use only standard libraries..."                        │
│     "Avoid technical jargon..."                             │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 📋 Tasks, Verbs, Actions

### Clear Instructions

```
┌─────────────────────────────────────────────────────────────┐
│  EFFECTIVE ACTION WORDS                                     │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  Analysis Tasks:                                            │
│  • Analyze the following code...                            │
│  • Compare these approaches...                              │
│  • Evaluate the strengths and weaknesses...                 │
│  • Identify potential issues...                             │
│                                                             │
│  Creation Tasks:                                            │
│  • Write a function that...                                 │
│  • Generate 10 ideas for...                                 │
│  • Create a detailed outline...                             │
│  • Draft an email to...                                     │
│                                                             │
│  Transformation Tasks:                                      │
│  • Convert this to Python...                                │
│  • Summarize in 3 sentences...                              │
│  • Translate to Spanish...                                  │
│  • Refactor for readability...                              │
│                                                             │
│  Question Tasks:                                            │
│  • Explain how... works...                                  │
│  • What are the best practices for...                       │
│  • Why does... happen?                                      │
│  • When should I use...                                     │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 📚 Context: Background Information

### Setting the Stage

```
┌─────────────────────────────────────────────────────────────┐
│  PROVIDING CONTEXT                                          │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ❌ Without Context:                                        │
│  "Fix this code"                                            │
│                                                             │
│  ✅ With Context:                                           │
│  "Fix this Python code. It's part of a web API that         │
│   processes user uploads. The function should validate      │
│   file size (max 10MB) and type (images only).              │
│   Current issue: it's accepting all file types."            │
│                                                             │
│  Why context matters:                                       │
│  • Helps AI understand the goal                             │
│  • Enables relevant suggestions                             │
│  • Reduces back-and-forth clarification                     │
│  • Improves output quality                                  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Constraints and Examples

```
Constraints:
• "Use only Python standard library"
• "Keep response under 500 words"
• "Target audience: beginner developers"
• "Must be compatible with Python 3.8+"

Examples (Few-Shot Prompting):
Input: "Happy" → Output: "Joyful, content, pleased"
Input: "Sad" → Output: "Melancholy, sorrowful, downcast"
Input: "Angry" → Output: [AI completes pattern]
```

---

## 🎭 The Role

### Framing AI's Identity

```
┌─────────────────────────────────────────────────────────────┐
│  ROLE ASSIGNMENT                                            │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  Generic:                                                   │
│  "Help me with coding"                                      │
│                                                             │
│  Role-Specific:                                             │
│  "You are a senior software engineer with 15 years          │
│   experience in Python, distributed systems, and            │
│   cloud architecture. You mentor junior developers          │
│   and write clean, well-documented code."                   │
│                                                             │
│  Why roles work:                                            │
│  • Activates relevant knowledge                             │
│  • Sets expertise level                                     │
│  • Guides communication style                               │
│  • Improves response quality                                │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 📐 The Format & Desired Structure

### Specifying Output

```
┌─────────────────────────────────────────────────────────────┐
│  FORMAT SPECIFICATIONS                                      │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  Structure Options:                                         │
│  • Bullet points                                            │
│  • Numbered list                                            │
│  • Table with columns: X, Y, Z                              │
│  • JSON format                                              │
│  • Code with comments                                       │
│  • Step-by-step guide                                       │
│  • Executive summary + details                              │
│                                                             │
│  Example:                                                   │
│  "Provide your answer as a table with columns:              │
│   | Approach | Pros | Cons | Best For |                     │
│   Include at least 5 approaches."                           │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 🔄 Iterative Process

### First Attempts → Refinement

```
┌─────────────────────────────────────────────────────────────┐
│  ITERATIVE PROMPT REFINEMENT                                │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  Attempt 1 (Vague):                                         │
│  "Write code for me"                                        │
│                                                             │
│  AI Response: Generic, unhelpful                            │
│                                                             │
│  Attempt 2 (Better):                                        │
│  "Write Python code to read a CSV file and                  │
│   calculate the average of a column"                        │
│                                                             │
│  AI Response: Better, but still generic                     │
│                                                             │
│  Attempt 3 (Specific):                                      │
│  "Write a Python function using pandas that:                │
│   1. Reads 'sales_data.csv'                                 │
│   2. Calculates average of 'revenue' column                 │
│   3. Handles missing values                                 │
│   4. Returns the result as a float                          │
│   Include error handling and docstring."                    │
│                                                             │
│  AI Response: Exactly what you need!                        │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 💬 Keep the Conversation Going

### Multi-Turn Dialogue

```
┌─────────────────────────────────────────────────────────────┐
│  MULTI-TURN CONVERSATION                                    │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  Turn 1:                                                    │
│  You: "Explain how REST APIs work"                          │
│  AI: [Provides explanation]                                 │
│                                                             │
│  Turn 2 (Building on context):                              │
│  You: "What about GraphQL? How does it compare?"            │
│  AI: [Compares REST vs GraphQL]                             │
│                                                             │
│  Turn 3 (Getting specific):                                 │
│  You: "For my e-commerce site, which should I use?"         │
│  AI: [Provides recommendation based on context]             │
│                                                             │
│  Turn 4 (Implementation):                                   │
│  You: "Show me a sample GraphQL schema for products"        │
│  AI: [Provides schema]                                      │
│                                                             │
│  Benefits of conversation:                                  │
│  • AI remembers context                                     │
│  • Can ask follow-up questions                              │
│  • Refine requirements gradually                            │
│  • Build complex solutions iteratively                      │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 🎯 Ask the Right Questions

### Question Quality Matters

```
┌─────────────────────────────────────────────────────────────┐
│  QUESTION QUALITY COMPARISON                                │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ❌ Poor Questions:                                         │
│  • "Does this work?" (too vague)                            │
│  • "Why is it broken?" (no context)                         │
│  • "Help me" (no specifics)                                 │
│                                                             │
│  ✅ Good Questions:                                         │
│  • "Why does this Python function return None               │
│     instead of the expected list?"                          │
│  • "What's the time complexity of this algorithm,           │
│     and how can I optimize it?"                             │
│  • "For a high-traffic API, should I use caching            │
│     at the database level or application level?"            │
│                                                             │
│  Question Framework:                                        │
│  1. What are you trying to do?                              │
│  2. What have you tried?                                    │
│  3. What happened vs what did you expect?                   │
│  4. What constraints are you working with?                  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 🔑 Clarity: Keys to Success

### Clear Prompts Get Clear Answers

```
┌─────────────────────────────────────────────────────────────┐
│  CLARITY CHECKLIST                                          │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ☐ Task is clearly stated                                   │
│  ☐ Context provides necessary background                    │
│  ☐ Role is specified (if relevant)                          │
│  ☐ Format/structure is defined                              │
│  ☐ Constraints are listed                                   │
│  ☐ Examples provided (if helpful)                           │
│  ☐ No ambiguous language                                    │
│  ☐ Specific enough to act on                                │
│                                                             │
│  Before: "Make it better"                                   │
│  After: "Refactor this function to improve readability:     │
│         - Extract nested logic into separate functions      │
│         - Add docstrings                                    │
│         - Use descriptive variable names                    │
│         - Keep functions under 20 lines"                    │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Production Roadmap

| Phase | Task | Deliverable | Timeline |
|-------|------|-------------|----------|
| 1 | Learn components | Task, context, role, format | Week 1 |
| 2 | Practice prompting | 50+ prompt variations | Week 2-3 |
| 3 | Iterative refinement | Before/after comparisons | Week 4 |
| 4 | Build library | Reusable prompt templates | Week 5-6 |

---

## 📚 Prompt Templates

### Reusable Structures

```
Template 1: Code Review
"You are a [ROLE] reviewing code for [CONTEXT].
Analyze the following code for [TASK]:
- Code quality
- Security issues
- Performance concerns
- Best practices

Provide feedback in [FORMAT] with specific examples."

Template 2: Learning
"I'm learning [TOPIC] at [LEVEL] level.
Explain [CONCEPT] using:
- Simple analogies
- Code examples
- Common pitfalls
- Practice exercises

Format as [STRUCTURE]."

Template 3: Problem Solving
"I'm trying to [GOAL] but encountering [PROBLEM].
Here's what I've tried: [ATTEMPTS]
Here's what happens: [ACTUAL]
Here's what I expect: [EXPECTED]

Help me [TASK] with [CONSTRAINTS]."
```

---

*"Effective prompting is asking the right questions, with the right context, in the right format. Clarity is the key to success."*

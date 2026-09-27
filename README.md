Project 1: Rule-Based AI Chatbot
DecodeLabs Industrial Training Kit — Batch 2026 |

 The Logic Engine


Goal
Create a simple rule-based chatbot that responds to predefined user inputs — no deep learning, just Control Flow & Logic.

Key Requirements (all implemented)

Requirement.   Implementation

Handle greetings & exit commands
responses dict + EXIT_COMMANDS set

If-else / decision logic
while loop + .get() lookup with fallback

Continuous loop
while True: heartbeat until kill command

The IPO Blueprint

INPUT → input() + sanitization (.lower().strip())

PROCESS → Hash-map intent matching (O(1) dictionary lookup, not O(n) if-elif ladder)

OUTPUT → Instant deterministic response via .get(key, fallback)

Why a dictionary and not an if-elif ladder?
An if-elif ladder is O(n) — it checks every rule one by one, and collapses under its own technical debt as rules grow. A dictionary is O(1): instant lookup regardless of scale. That’s the pivot from sequential scan to direct access.

Key Skills Demonstrated
Control flow, decision-making logic, basic AI concepts, deterministic (white-box) systems — traceable, zero-hallucination, 100% hard-coded.

Sample Session
You: Hello
Bot: Hello! I'm your rule-based assistant. How can I help you today?
You: who are you
Bot: I'm a rule-based chatbot built with pure if-else logic...
You: exit
Bot: Exit command received. Terminating session...

Powered by DecodeLabs — Build the foundation. An LLM without rules is a hallucination engine.
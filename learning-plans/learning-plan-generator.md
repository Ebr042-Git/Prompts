# Learning Plan Generator (80/20 Method)

## Purpose
Generates a focused, time-boxed learning plan for any topic, prioritizing the 20% of concepts that deliver 80% of practical results (Pareto principle). Useful for quickly ramping up on a new skill or tool without getting lost in exhaustive theory.

## When to Use
- Starting a new topic and want a structured path instead of random tutorials
- Limited time (e.g., 10-20 hours) and need to prioritize what actually matters
- Want built-in checkpoints to verify understanding as you go

## The Prompt

```
I need to learn [topic] quickly. Create a focused 10 or 20-hour learning 
plan based on the 20% of the concepts that deliver 80% of the results. 
Break it into 10 sessions of 2 hours each; include the best resources; 
explain in my native tongue; and add a 15-minute review/test of 
understanding at the end of every session.
```

## How to Customize
- Replace `[topic]` with your subject (e.g., "SQL window functions", "Power BI DAX", "Python for data analysis")
- Adjust total hours (10 vs 20) based on topic complexity and your available time
- Specify your native language explicitly if the AI doesn't default correctly (e.g., "explain in Tamil mixed with English / Tanglish")
- Optionally add: "assume I already know [prerequisite]" to skip basics you've covered

## Example Output Structure You Should Expect
- Session breakdown (1-10), each ~2 hours
- Core concepts per session (prioritized by impact, not exhaustiveness)
- Specific resource links (docs, videos, articles) — not just "read about X"
- A 15-minute review/test at the end of each session to catch gaps early

## Notes
- Works best when the topic is well-established (has a lot of existing teaching material) — for bleeding-edge or niche topics, resource quality may be inconsistent
- Pair this with the `self-testing/progressive-difficulty-quiz.md` prompt after each session for deeper reinforcement

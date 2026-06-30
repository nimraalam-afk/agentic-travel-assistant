# Product Notes

## User problem

Travelers often need to combine multiple constraints: dates, budget, weather, interests, and activity availability. This project explores how an agentic workflow can turn structured trip inputs into a personalized itinerary, then revise it when the traveler gives feedback.

## PM framing

The interesting product question is not simply whether the model can write a nice itinerary. It is whether the system can consistently respect hard constraints while still producing recommendations that feel personalized and useful.

## What the agent handles well

- Works from structured traveler and trip inputs
- Grounds recommendations in available mocked data
- Checks budget and date constraints
- Revises the itinerary after feedback
- Uses tools for calculation, lookup, and evaluation rather than relying entirely on the LLM

## What I would improve next

- Add pre-filtering before generation so the model only sees viable activities
- Add travel-time and location clustering constraints
- Add a more formal evaluation set with multiple traveler scenarios
- Add explicit fallback behavior when constraints cannot all be satisfied
- Improve the final user-facing explanation so it summarizes tradeoffs without exposing verbose reasoning traces

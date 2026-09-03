# Rerun
A small experiment in reconstructing what happened during an agent run from the traces it leaves behind.
## What I’m trying to understand
An agent does something.
Afterward, we may have pieces of the run: what the person asked for, what the agent understood, the tools it called, what changed in the system, and what the agent says happened.
Those pieces are not necessarily the same thing.
RErun asks:
**What can reasonably be inferred about what happened after a run?**
The goal is not to produce a perfect record of the agent’s thinking. A trace is evidence, not a mind.
I want to see what becomes legible when the partial records of a run are placed beside one another.
## The basic shape
A RErun may include:
- the original human request
- the agent’s interpretation of the goal
- tool or API calls
- resulting system state
- the agent’s own report of what happened
- human review
The interesting part is often where those records do not line up.
A phrase may disappear between the request and the agent’s interpretation. A tool call may produce a different state than the agent reports. The final result may look successful while one part of the original request was quietly lost.
RErun puts those partials back into sequence so they can be examined together.
## Current status
**Design → first build**
I’m currently defining the smallest useful trace record and building the first reconstruction example.
The first version will deliberately use a simple agent task so I can understand the machinery of the run before making the reconstruction problem more complicated.
## A tiny example
A person asks:

> Turn on beta checkout for internal users only.
The agent interprets the goal as:
> Turn on beta checkout.
Later, the system shows:
> Beta checkout: ON  
> Audience: EVERYONE
And the agent reports:
> Successfully enabled beta checkout.
None of those records alone explains the whole run.
Together, they show where something changed.
## Next exploration
I want to find out what kinds of traces are actually useful for reconstruction.
Which records tell us something distinct?
Which ones merely repeat one another?
Where does the evidence stop and inference begin?
And how much of the road can reasonably be reconstructed after the fact?
## Why Rerun
The name has a few histories for me.
In *Peanuts*, Lucy hears that her new baby brother is a boy and complains that he will basically be a rerun of Linus. Of course Rerun turns out not to be Linus again.
In Developmental Transformations, I also acquired the nickname “Rerun Renee” because I would restart a sequence and look again. Another pass could reveal something that the first one did not.


A rerun is never simply the same run again.

Sometimes the second look is where the differences become visible.

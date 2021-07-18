# Reinforcement Learning API definitions

We attempt to provide API definitions for reinforcment learning related entities.
This is intentionally open source collaborative attempt to share the knowledge of crowd and take into account many edge cases.

**Note**:

Although we attempt to describe general interface we acknowldge that it is likely impossible to include all cases.
We value coherence over genrality and complexity. If suitable a different version of entity will be created.


# Entities

## Agent

Describes agent that observes and acts in the environment.
Often, the agent is tasked to achieve something in reference to the environment.
The case of an agent interacting with other agents for a common goal is described under "Multi Agent".

## Multi Agent

Describes interface with many agents which have a common goal.
Agents in multi agent scenario may cooperate, compete or belong to groups with common strategy.

## Environment

Describes environment in which, and with which, one or many agents interact.
The environment is not limited to the simulation that generates agent's surrounding.
Depending on the paradigm, environment can include all "other" agents.

Environment may or may not be able to ascribe value function.

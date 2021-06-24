# Agents

## Control

### Step
Description: Feed agent with new data about the world
Type: POST
Data: World data. At least observation and reward.

### Commit
Description: Commits to memory last added data.
Type: POST
Data: None

### Act
Description: Make agent to suggest action based on provided observation.
Type: POST
Data: Observation


## Management

### Info
Description: Provides information about the agent.
Type: GET
Data: None

# Environment

## Control

### Step
Description: Provides information necessary to step the environment. Can be a partial information or all required.
Type: POST
Data: Agents actions.

### Commit
Description: Commits last data into env engine.
Type: POST
Data: None

### Reset
Description: Restarts the environment into a starting position.
Type: POST
Data: None

## Management

### Last
Description: Returns information about the latest state.
Type: GET
Data: None

### Describe
Description: Describes the environment.
Type: GET
Data: None

### Seed
Description: Sets a seed value for random number generator.
Type: POST
Data: Seed value.


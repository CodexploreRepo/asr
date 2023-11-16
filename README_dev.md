# DEV

## Setup

### WanDB

- Install the CLI and Python library for interacting with the Weights and Biases API.
  - `pip install wandb`
- Login to [WanDB](https://wandb.ai/codexplore-ai) and copy API Key
- Log in and paste your API key when prompted: `wandb login`
- Start tracking system metrics and console logs

```Python
import wandb
wandb.init(
    # set the wandb project where this run will be logged
    project="audio-classification",
)
```

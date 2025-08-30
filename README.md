# Todo

- rename properly the agents
- evaluate scope and syntax (follow the first-ones styling)
- create new repo with general prompting engineer info and suggestions for each LLM model
- adapt agents to desired workflow and toolkit (look at map to cover all needs)
- add agents for learning mode

## Installation

These subagents are automatically available when placed in `~/.claude/agents/` directory.

```bash
cd ~/.claude
git clone https://github.com/your-username/claude-code-subagents.git
```

## Usage

### Automatic Invocation

Claude Code will automatically delegate to the appropriate subagent based on the task context and the subagent's description.

### Explicit Invocation

Mention the subagent by name in your request:

``` bash
"Use the python-expert to optimize this algorithm"
"Get the react-expert to refactor this component"
```

## Sources

- [Claude Code Documentation](https://docs.anthropic.com/en/docs/claude-code/overview)
- [Subagents Documentation](https://docs.anthropic.com/en/docs/claude-code/sub-agents)
- [Claude Code GitHub](https://github.com/anthropics/claude-code)

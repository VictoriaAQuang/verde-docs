# Using your AI-VERDE API Key with Claude Code

You can follow these instructions to use your VERDE API Key after installing Claude Code. More information on using Claude Code can be found here, https://docs.anthropic.com/en/docs/intro.

## Prerequisites

1. Your VERDE course or team must be configured to use Anthropic models (see instructor or team lead)
2. Install Claude Code. Instructions can be found here, https://www.anthropic.com/claude-code/
3. Obtain your VERDE API Key. Instructions can be found here, https://aiverde-docs.cyverse.ai/api/api-token/
4. The remaining instructions assume you have an open terminal on system with Claude Code and bash installed.

## 1. Setting up the necessary environment variables

This step should only be needed the first time you use Claude Code.

In a terminal, set the following environment variables and replace `ANTHROPIC_API_KEY` to your VERDE API Key.
```
export ANTHROPIC_BASE_URL="https://llm-api.cyverse.ai"
export ANTHROPIC_API_KEY="insert-VERDE-API-Key-here"
export ANTHROPIC_MODEL="anthropic/claude-sonnet-4"
```
Note, the `ANTHROPIC_MODEL` can be set to Anthropic model. Information about available models can be found here, https://docs.anthropic.com/en/docs/about-claude/models/overview

## 2. Start Claude Code

You can then run Claude Code.
```
claude
```
After initially launching Claude Code, claude will write the variables into a `~/.claude/settings.json` file. You do not need to repeat step #1 again for future sessions.

## If you need to change your `ANTHROPIC_API_KEY`

If for some reason you need to change your VERDE API Key, you can delete your use the `/logout` in claude or delete your `~/.claude/settings.json`; then, repeat steps 1-2.
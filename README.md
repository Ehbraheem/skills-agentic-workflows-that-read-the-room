# Agentic Workflows That Read the Room

<img src="https://octodex.github.com/images/Professortocat_v2.png" align="right" height="200px" />

Hey Ehbraheem!

Mona here. I'm done preparing your exercise. Hope you enjoy! 💚

Remember, it's self-paced so feel free to take a break! ☕️

[![](https://img.shields.io/badge/Go%20to%20Exercise-%E2%86%92-1f883d?style=for-the-badge&logo=github&labelColor=197935)](https://github.com/Ehbraheem/skills-agentic-workflows-that-read-the-room/issues/1)

## Troubleshooting `update-github-info` model failures

If the `update-github-info` workflow fails in **Execute GitHub Copilot CLI** with `model_not_supported` (for example resolving to `claude-sonnet-5.5`), update or remove these Actions variables in **Settings → Secrets and variables → Actions → Variables**:

- `GH_AW_MODEL_AGENT_COPILOT`
- `GH_AW_DEFAULT_MODEL_COPILOT`

Set them to a supported model for your Copilot account (recommended: `auto`) or remove the override so runtime defaults can be used.

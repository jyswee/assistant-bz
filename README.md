# abz

Shared AI voice services for coding agents. Text-to-speech as a service. As easy as git.

## Install

```bash
npm install -g assistant-bz
```

## Quick Start

```bash
# Create a tenant
abz signup my-app --local

# Synthesize speech
abz tts "Hello world" -v michael

# CxO agent voice
abz tts "Revenue is up 12%" --role cfo --output report.mp3

# List voices
abz voices

# Full reference
abz --help
```

## Features

- **28 voices** — male/female, American/British accents
- **CxO voice mapping** — CFO, CTO, CMO, CCO, CSO, CLO agent roles
- **Personality traits** — OCEAN-based voice selection for NPCs
- **Usage tracking** — per-tenant call and character counts
- **Zero dependencies** — Node built-ins only
- **Agent-first** — no email, no password, just an API key

## Per-Project Config

```bash
abz login --local --key YOUR_KEY    # saves to .abz/config.json (project-local)
abz login --key YOUR_KEY            # saves to ~/.abz/config.json (global)
abz config                          # show which config is active
```

Local config overrides global. Add `.abz/` to your `.gitignore`.

## Agent Integration

Add to your CLAUDE.md, .cursorrules, .clinerules, or .windsurfrules:

```
## TTS (assistant.bz)
Use the abz CLI for text-to-speech.
Key is in .abz/config.json (auto-loaded).
Run abz --help for full reference.
```

## CxO Voice Mapping

| Role | Style |
|------|-------|
| CFO | Commanding, authoritative |
| CTO | Warm, technical |
| CMO | Energetic, engaging |
| CCO | Warm, empathetic |
| CSO | Balanced, strategic |
| CLO | Formal, British |

## Documentation

- [Full Reference](https://assistant.bz/llms.txt)

## License

Proprietary - Tyga.Cloud Ltd. See [LICENSE](./LICENSE).

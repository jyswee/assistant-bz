# abz

Shared AI services (TTS, voice synthesis) for coding agents. Kokoro + OpenAI cascade - as easy as git.

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

- **TTS** - Kokoro (free, 28 voices) with OpenAI fallback ($15/1M chars)
- **CxO Voices** - CFO, CTO, CMO, CCO, CSO, CLO agent voice mapping
- **Personality Voices** - OCEAN trait-based voice selection for NPCs
- **Usage Tracking** - per-tenant call and character counts
- **Zero Dependencies** - Node built-ins only

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

| Role | Voice | Style |
|------|-------|-------|
| CFO | am_onyx | commanding |
| CTO | am_michael | authoritative |
| CMO | af_nova | energetic |
| CCO | af_heart | warm |
| CSO | am_echo | balanced |
| CLO | bf_emma | formal British |

## Documentation

- [Full Reference](https://assistant.bz/llms.txt)

## License

Proprietary - Tyga.Cloud Ltd. See [LICENSE](./LICENSE).

# Gemini Skills

A Gemini CLI extension providing AI-powered image generation and frontend design skills.

## Installation

```bash
gemini extensions install https://github.com/buildatscale-tv/gemini-skills
```

Or install from a local path:

```bash
gemini extensions install /path/to/gemini-skills
```

## Skills

### Nano Banana Pro (Image Generation)

Generate images using Google's Gemini 2.5 Flash (Nano Banana Pro). See the [demo video](https://www.youtube.com/watch?v=614mXXCSsNY).

**Triggers:** `generate image`, `create image`, `make image`, `nano banana`, `image-generation`

**Prerequisites:**
- [uv](https://docs.astral.sh/uv/) - Python package manager (required to run the image generation script). See the [uv installation walkthrough](https://youtu.be/DRdd4V1G4-k?t=80)
- `GEMINI_API_KEY` environment variable with your [Google AI API key](https://aistudio.google.com/apikey)

**Usage:**
```bash
uv run "${SKILL_DIR}/scripts/image.py" \
  --prompt "Your image description" \
  --output "/path/to/output.png" \
  --aspect landscape  # optional: square, landscape, portrait
  --reference "/path/to/reference.png"  # optional: reference image
```

**Example prompts:**
- "A minimalist geometric pattern with overlapping translucent circles in coral, teal, and gold on a deep navy background"
- "A futuristic cityscape at sunset with neon lights reflecting on wet streets"

### Frontend Design

Create distinctive, production-grade frontend interfaces with high design quality.

> **Note:** This skill is copied from [anthropics/skills](https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md) for easier installation.

**Triggers:** `frontend`, `design`, `ui`, `web`, `component`, `page`, `interface`, `landing page`, `dashboard`, `website`

This skill guides creation of visually striking, memorable interfaces that avoid generic AI aesthetics. It emphasizes:
- Bold typography choices
- Cohesive color themes
- Purposeful animations and micro-interactions
- Unexpected layouts and spatial composition
- Atmospheric backgrounds and visual details

## Extension Management

```bash
# List installed extensions
gemini extensions list

# Update this extension
gemini extensions update buildatscale-gemini-skills

# Disable extension
gemini extensions disable buildatscale-gemini-skills

# Enable extension
gemini extensions enable buildatscale-gemini-skills

# Uninstall extension
gemini extensions uninstall buildatscale-gemini-skills
```

## Development

To develop locally, link the extension:

```bash
gemini extensions link /path/to/gemini-skills
```

Changes will be reflected immediately without needing to run `gemini extensions update`.

## Repository Structure

```
.
├── gemini-extension.json    # Extension configuration
├── GEMINI.md                # Context file loaded by Gemini CLI
└── skills/
    ├── nano-banana-pro/
    │   ├── SKILL.md         # Skill documentation
    │   └── scripts/
    │       └── image.py     # Image generation script
    └── frontend-design/
        └── SKILL.md         # Skill documentation
```

## License

MIT

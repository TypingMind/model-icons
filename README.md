# model-icons
Collection of popular LLM icons for building AI apps

## Structure

- `icons/` — the icon image files (JPG icons are 1024×1024).
- `data.json` — an array describing every icon set. Each entry has the shape:

```json
{
  "id": "openai",
  "label": "OpenAI",
  "description": "Optional description of the model or provider.",
  "files": [
    { "name": "openai.jpg", "variant": "default" },
    { "name": "openai-color.jpg", "variant": "color" },
    { "name": "openai-text.jpg", "variant": "text" }
  ],
  "models": ["gpt-4o"]
}
```

`files[].variant` describes the style of the image:

| Variant | Meaning |
| --- | --- |
| `default` | Monochrome logo mark |
| `color` | Full-color logo mark |
| `text` | Wordmark / text logo |
| `text-cn` | Chinese wordmark |
| `brand` | Monochrome brand logo (used when the brand differs from the product mark) |
| `brand-color` | Full-color brand logo |

Files without a `variant` field are legacy icons that predate this convention.

`models` lists model IDs that should use the icon; it may be empty for providers and tools.

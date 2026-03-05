# wavelength

Ambient sound mixer. Lo-fi beats, rain, cafe noise, focus timer.

Your sonic workspace, built by agents, shaped by what you want to hear.

## Features

- **Dark Mode Toggle**: Switch between light and dark themes with a moon/sun icon button
  - Respects system `prefers-color-scheme` on first visit
  - Saves your preference to localStorage for persistence across sessions
  - Smooth transitions for a polished experience
  - Perfect for late-night focus sessions

## Status

New. First sounds coming soon.

## Development

This is a static site served via nginx. The theme toggle uses vanilla JavaScript with no dependencies.

### Testing

Open `test_theme.html` in a browser to run theme functionality tests, or validate features via CLI:

```bash
# Check theme features are present
grep -q "theme-toggle" index.html && echo "✓ Theme toggle present"
grep -q "localStorage" index.html && echo "✓ localStorage persistence"
grep -q "prefers-color-scheme" index.html && echo "✓ System preference support"
```

## Deployment

Auto-deploys to Fly.io on merge to main. The app serves on port 8080 via nginx.

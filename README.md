# OEVER.ART — Agent: Floris (ElevenLabs Widget)

Single‑file, production‑style landing page that embeds the ElevenLabs Agent widget inside a glossy, responsive square container with animated background and a portrait‑locked mobile UX.

## Live Demo (GitHub Pages)

1. **Create repo**
   - New public repo (e.g., `oever-art-agent`).
   - Add **`index.html`** (this repo’s root).

2. **Enable GitHub Pages**
   - Go to **Settings → Pages**.
   - **Source:** `Deploy from a branch`
   - **Branch:** `main` → `/ (root)` → **Save**
   - Wait 1–2 minutes. Your site will publish at:
     `https://<your-username>.github.io/<your-repo>/`

3. **Verify**
   - Open the URL on **mobile in portrait** (the UX is portrait‑locked).
   - You should see the square agent container at the top and the footer logo at the bottom.

---

## File Structure

```
/
└─ index.html   # all-in-one page (HTML/CSS/JS embedded)
```

No build step, no dependencies, no external assets (besides the official ElevenLabs widget script).

## Configuration

### Agent ID
Already set in `index.html`:

```html
<elevenlabs-convai agent-id="agent_9601k3gnh4pteprvqkx73341q29n" variant="expanded"></elevenlabs-convai>
<script src="https://unpkg.com/@elevenlabs/convai-widget-embed" async type="text/javascript"></script>
```

- To change agents later, update the `agent-id` value.
- Ensure the agent is **public** and your site’s domain is **allowed** in the agent’s security settings.

### Volume Boost
Tries to attach a WebAudio GainNode on the first tap to double output volume.

## Troubleshooting

- **No widget:** check `agent-id` and that the script loads.
- **No audio:** tap the page once (browser policy). Ensure device volume is up.
- **Layout:** must be portrait. Landscape shows a rotate notice.

## Success Checklist

- [ ] Animated background and glossy square container visible
- [ ] ElevenLabs Agent UI shows and responds
- [ ] Audio plays; first tap boosts volume
- [ ] Footer logo “OEVER.ART — AGENT: FLORIS” shows with continuous shine
- [ ] Mobile portrait view scales perfectly across devices

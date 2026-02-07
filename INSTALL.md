### [Home Assistant](https://www.home-assistant.io)

#### Prerequisites

- [Home Assistant](https://www.home-assistant.io/) installed and running
- For HACS install: [HACS](https://hacs.xyz/) installed

##### Method 1: HACS (Recommended)

1. Open Home Assistant
2. Navigate to **HACS** in sidebar
3. Click **Frontend**
4. Click **⋮** (three dots menu) → **Custom repositories**
5. Add repository:
   - URL: `https://github.com/dracula/home-assistant`
   - Category: **Theme**
6. Click **Add**
7. Find "Dracula" and click **Download**
8. **Restart Home Assistant**

##### Method 2: Manual Installation

1. Download `dracula.yaml` from [themes folder](./themes/dracula.yaml)
2. Copy to: `<config>/themes/dracula.yaml`
3. Edit `configuration.yaml`:

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

4. **Restart Home Assistant**

#### Activating the Theme

1. Click your **profile icon** (bottom left)
2. Under **Theme**, select **Dracula**
3. Theme applied instantly!

#### Optional: Floating Navigation Buttons

The theme includes floating hamburger menu and edit buttons that appear on desktop (>=768px). These require [card-mod](https://github.com/thomasloven/lovelace-card-mod):

1. Install **card-mod** via HACS (search "card-mod" in Frontend)
2. Restart Home Assistant
3. Floating buttons will appear automatically on desktop views

> **Note:** The theme works perfectly without card-mod -- you get the full Dracula color palette. card-mod only adds the floating navigation buttons.

##### Troubleshooting

##### Theme not appearing

- Verify file is at `<config>/themes/dracula.yaml`
- Check `configuration.yaml` has correct `frontend` config
- Restart Home Assistant
- Check Home Assistant logs for errors

##### Theme looks broken

- Clear browser cache (Ctrl+F5 / Cmd+Shift+R)
- Try incognito/private window
- Ensure Home Assistant is up to date

##### Buttons barely visible

This theme includes media player button fixes. If buttons are still hard to see:

- Make sure you're using the latest version
- Clear browser cache completely
- Check if custom cards are overriding theme colors

##### Floating buttons not showing

- Verify card-mod is installed (HACS -> Frontend -> card-mod)
- Clear browser cache
- Check you're on desktop (>=768px width) -- buttons are hidden on mobile
- Restart Home Assistant after installing card-mod

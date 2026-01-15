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

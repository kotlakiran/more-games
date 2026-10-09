# More Games manifest

This repo hosts `apps.json`, the cross-promotion app directory that Grid Forge
(and other apps) fetch at runtime to show the **More Games** menu dynamically.

Edit `apps.json` and commit — connected apps pick up the changes on next launch,
no app update required.

Raw URL used by the app:

```
https://raw.githubusercontent.com/kotlakiran/more-games/main/apps.json
```

## Schema

```json
{
  "updated": "YYYY-MM-DD",
  "apps": [
    {
      "name": "App name",
      "package": "com.example.app",
      "tagline": "Short one-line description",
      "published": true,
      "accent": "#2CD7DC"
    }
  ]
}
```

- `published: true` → the app is featured and tapping it opens its Google Play page
  (`market://details?id=<package>`), falling back to the web Play URL.
- `published: false` → shown under "More — coming soon"; tapping shows a note instead of a store link.
- `accent` is a hex colour used for the app icon/accent.

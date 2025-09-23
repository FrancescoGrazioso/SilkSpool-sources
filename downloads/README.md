# Downloads Directory

This directory contains the actual mod files referenced in the repository JSON.

## Structure

```
downloads/
├── mod-id/
│   ├── v1.0.0/
│   │   └── ModName.zip
│   └── v0.9.0/
│       └── ModName.zip
└── another-mod/
    └── v1.0.0/
        └── AnotherMod.zip
```

## Guidelines

- **File naming**: Use descriptive names that include the mod name and version
- **Version folders**: Create separate folders for each version
- **File size**: Keep files under 10MB when possible
- **Compression**: Use ZIP format for mod files
- **URL format**: Reference files using GitHub raw URLs:
  `https://raw.githubusercontent.com/francescograzioso/SilkSpool-sources/main/downloads/mod-id/version/filename.zip`

## Adding New Mods

1. Create a folder with the mod's ID
2. Create a version subfolder (e.g., `v1.0.0`)
3. Place the mod file inside
4. Update the JSON with the correct GitHub raw URL

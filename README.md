# Silk Spool Sources

A comprehensive repository of mod sources for Hollow Knight: Silksong, designed to work with the Silk Spool mod manager application.

## What is this repository?

This repository serves as a centralized source of mod information for the Silk Spool desktop application - a mod manager that allows users to discover, download, and install mods for Hollow Knight: Silksong. The repository contains structured JSON files that provide metadata about available mods, including download links, descriptions, requirements, and more.

## Repository Structure

The repository follows a standardized JSON schema that ensures compatibility with the Silk Spool mod manager:

- **Repository Information**: Metadata about the repository itself
- **Mod List**: Detailed information about each available mod
- **Download Links**: Direct URLs to mod files
- **Images & Screenshots**: Visual content for mod presentation
- **Changelog**: Version history and updates

## JSON Schema

Each repository JSON file must follow this exact structure:

```json
{
  "repository_info": {
    "id": "unique-repo-id",
    "name": "Repository Name",
    "description": "Repository description",
    "url": "https://github.com/username/repo-name",
    "author": "Author Name",
    "version": "1.0.0",
    "last_updated": "2024-01-15T10:30:00Z",
    "mod_count": 0
  },
  "mods": []
}
```

### Required Fields

#### Repository Info
- `id`: Unique repository identifier (string)
- `name`: Repository display name (string)
- `description`: Brief description (string, max 200 characters)
- `url`: Repository URL (string)
- `author`: Repository author/curator (string)
- `version`: Repository version (string)
- `last_updated`: Last update date in ISO 8601 format
- `mod_count`: Exact number of mods in the array

#### Mod Information
- `id`: Unique mod identifier (string)
- `title`: Mod name (string, max 100 characters)
- `description`: Detailed description (string, 200-500 characters)
- `version`: Mod version (string)
- `game_version`: Supported game version (string)
- `author`: Primary author (string)
- `updated_at`: Last update date in ISO 8601 format
- `downloads`: Array with at least one download object

#### Download Object
- `url`: Direct download URL (string)
- `label`: Download label (string)
- `type`: File type (zip, tar.gz, dll, etc.)

### Optional Fields

- `authors`: Array of additional authors
- `requirements`: Array of mod requirements (e.g., BepInEx, ModLoader)
- `tags`: Array of categorization tags
- `created_at`: Creation date in ISO 8601 format
- `homepage`: Mod homepage URL
- `images`: Array of image objects
- `changelog`: Array of version changelog entries

## Common Tags

Use these standardized tags for mod categorization:

- `utility`: Utility tools and helpers
- `ui`: User interface modifications
- `gameplay`: Gameplay mechanics and features
- `visual`: Graphics and visual effects
- `audio`: Sound and music modifications
- `quality-of-life`: Quality of life improvements
- `cheat`: Cheat codes and modifications
- `cosmetic`: Cosmetic changes
- `debug`: Debug and development tools
- `performance`: Performance optimizations

## Common Requirements

- `BepInEx`: Modding framework
- `ModLoader`: Mod loading system
- `UnityEngine`: Unity engine dependencies
- `Assembly-CSharp`: Game code modifications

## Contributing

### How to Add a New Mod

1. **Fork this repository**
2. **Create a new branch** for your changes
3. **Add your mod information** to the appropriate JSON file
4. **Follow the schema exactly** - all required fields must be present
5. **Validate your JSON** before submitting
6. **Create a pull request** with a clear description

### Pull Request Guidelines

#### Before Submitting
- [ ] JSON syntax is valid and parseable
- [ ] All required fields are present
- [ ] All IDs are unique
- [ ] Dates are in ISO 8601 format
- [ ] URLs are properly formatted and accessible
- [ ] Data types are correct
- [ ] `mod_count` matches the actual number of mods

#### Pull Request Template
```markdown
## Mod Addition: [Mod Name]

### Description
Brief description of what the mod does.

### Changes Made
- Added mod: [mod-id]
- Updated mod_count to: [new count]
- [Any other changes]

### Validation
- [ ] JSON syntax validated
- [ ] All required fields present
- [ ] Download URLs tested
- [ ] Images accessible

### Screenshots
[If applicable, add screenshots of the mod in action]
```

### Mod Information Requirements

When adding a new mod, ensure you provide:

1. **Complete mod metadata** (title, description, version, author)
2. **Working download links** (GitHub releases, direct links)
3. **Appropriate tags** for categorization
4. **Requirements** if the mod has dependencies
5. **Images** (screenshots, thumbnails) when available
6. **Changelog** for version history

### Quality Standards

- **Descriptions**: Should be detailed (200-500 characters) and explain what the mod does
- **Download URLs**: Must be direct links to working files
- **Images**: Should be optimized for web and accessible
- **Versions**: Use semantic versioning (e.g., 1.2.0)
- **Dates**: Always use ISO 8601 format in UTC

### Validation Checklist

Before submitting a pull request, verify:

1. **JSON Validity**: Use a JSON validator to check syntax
2. **Schema Compliance**: Ensure all required fields are present
3. **Uniqueness**: Check that all IDs are unique
4. **URL Accessibility**: Test all download and image URLs
5. **Data Consistency**: Verify data types and formats
6. **Count Accuracy**: Ensure `mod_count` matches actual mod count

## File Organization

- `example-repository.json`: Example repository with sample mods
- `AI_REPOSITORY_PROMPT.md`: AI prompt for repository creation
- `REPOSITORY_JSON_TEMPLATE.md`: Detailed template documentation
- `README.md`: This file

## Support

If you need help with:
- JSON schema questions
- Mod submission process
- Validation issues
- Technical problems

Please open an issue in this repository with the appropriate label.

## License

This repository follows the same license as the Silk Spool project. Please ensure any mods you submit are properly licensed and don't violate copyright.

---

**Note**: This repository is specifically designed for the Silk Spool mod manager. Follow the schema exactly to ensure compatibility with the application.
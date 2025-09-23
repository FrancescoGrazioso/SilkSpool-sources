# Silk Spool Sources

A comprehensive repository of mod sources for Hollow Knight: Silksong, designed to work with the [Silk Spool](https://github.com/FrancescoGrazioso/SilkSpool) mod manager application.

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
  "repo_id": "unique-repo-id",
  "name": "Repository Name",
  "version": 1,
  "mods": []
}
```

### Required Fields

#### Repository Level
- `repo_id`: Unique repository identifier (string)
- `name`: Repository display name (string)
- `version`: Repository version number (integer)
- `mods`: Array of mod objects

#### Mod Information
- `id`: Unique mod identifier (string)
- `title`: Mod name (string)
- `description`: Detailed description (string)
- `requirements`: Array of mod requirements (e.g., BepInEx, Silksong)
- `images`: Array of image URLs (strings)
- `downloads`: Array with at least one download object
- `homepage`: Mod homepage URL (string)
- `authors`: Array of author names (strings)
- `game_version`: Supported game version (string)
- `updated_at`: Last update date in ISO 8601 format

#### Download Object
- `label`: Download label (string)
- `url`: Direct download URL (string)

## Common Requirements

- `BepInEx`: Modding framework
- `Silksong`: Game requirement
- `ModLoader`: Mod loading system
- `UnityEngine`: Unity engine dependencies

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

#### Pull Request Template
```markdown
## Mod Addition: [Mod Name]

### Description
Brief description of what the mod does.

### Changes Made
- Added mod: [mod-id]
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

1. **Complete mod metadata** (title, description, authors, game_version)
2. **Working download links** (GitHub releases, direct links)
3. **Requirements** if the mod has dependencies
4. **Images** (screenshots, thumbnails) when available
5. **Homepage URL** for the mod

### Quality Standards

- **Descriptions**: Should be detailed and explain what the mod does
- **Download URLs**: Must be direct links to working files
- **Images**: Should be optimized for web and accessible
- **Dates**: Always use ISO 8601 format in UTC

### Validation Checklist

Before submitting a pull request, verify:

1. **JSON Validity**: Use a JSON validator to check syntax
2. **Schema Compliance**: Ensure all required fields are present
3. **Uniqueness**: Check that all IDs are unique
4. **URL Accessibility**: Test all download and image URLs
5. **Data Consistency**: Verify data types and formats

## File Organization

- `silkspool-sources.json`: Main repository JSON file
- `mod-template.json`: Template for creating new mod entries
- `README.md`: This file

## How to Use the Mod Template

1. **Open `mod-template.json`** - This contains a complete mod entry template
2. **Copy the entire JSON object** (everything between the curly braces `{}`)
3. **Open `silkspool-sources.json`** and navigate to the `mods` array
4. **Paste the template** as a new element in the `mods` array
5. **Replace all placeholder values** with your actual mod data:
   - `your-mod-id-here` → Your unique mod ID
   - `Your Mod Title Here` → Your mod's display name
   - `Your Name` → Your name or username
   - `https://example.com/...` → Your actual URLs
   - `2024-12-19T12:00:00Z` → Current date in ISO 8601 format
6. **Remove the `_INSTRUCTIONS` field** from your final mod entry
7. **Validate the JSON** to ensure it's properly formatted

**Note**: The `_INSTRUCTIONS` field in the template is just for guidance and should be removed when you add the mod to the main repository.

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
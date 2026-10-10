# Exeter Plugin List

Community plugin registry for the [Exeter client](https://github.com/OrangeMan432/exeter).
The client fetches `plugins.json` from here to power the Plugins window and the
`plugin list` / `plugin install` commands. Jars are downloaded from each plugin's
own GitHub releases, never from this repo.

## Entry format

```json
[
  {
    "name": "Example",
    "author": "OrangeMan432",
    "repo": "OrangeMan432/exeter-example-plugin",
    "version": "1.0",
    "updated": "2026-10-10"
  }
]
```

- `name` - display name, must be unique in the list.
- `author` - who maintains it.
- `repo` - `owner/repo` whose releases carry the plugin jar.
- `version` - latest released version, for display only.
- `updated` - `YYYY-MM-DD` of the latest release.

## Adding your plugin

1. Publish a GitHub release on your plugin repo with the plugin jar attached.
2. Open a PR here adding your entry to `plugins.json` (keep the list alphabetical
   by name). The PR template lists the required fields.
3. The validation workflow checks the JSON parses and every entry has all fields.

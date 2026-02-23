# toggl-summarizer

Small web app to summarize Toggl Track time entries since a given date (e.g., your last lab meeting). Groups entries by description and shows total hours.

## Features

- Fetches time entries via the Toggl Reports API (supports arbitrary date ranges)
- Groups by description with total hours and entry counts
- **Merge similar**: auto-groups entries with similar descriptions (e.g., "code pheromone.paper" + "pheromone paper")
- **Manual grouping**: select rows with checkboxes and click "Group selected" to combine them
- Copy results as plain text or Markdown table
- Sortable columns

## Usage

The page is encrypted with [StatiCrypt](https://github.com/robinmoisson/staticrypt). Enter the password to access. Your Toggl API token is pre-filled.

To edit the source, modify `source.html` (not tracked in git), then re-encrypt:

```bash
staticrypt source.html -p "YOUR_PASSWORD" --remember 30 -o index.html
```

## Local development

```bash
python3 -m http.server 8888
# open http://localhost:8888/source.html
```

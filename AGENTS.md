# Project Guidelines

## Release versioning

- Before changing a release version, inspect the current worktree and read
  `meta.json`, the root `index.xml`, and `changelog.json`. Do not assume a
  version from prior conversation or a single file.
- Keep the current package version identical in `meta.json` (`version`),
  `index.xml` (root `content` `version` attribute), and both
  `changelog.json` (`currentVersion` and newest entry `version`).
- Preserve older changelog entries. Add a new entry at the beginning with an
  ISO `YYYY-MM-DD` date and localized `az`, `tr`, `en`, and `ru` title,
  summary, and change list.
- For update errors that mention GitHub metadata or downloaded content, compare
  the workspace files with the files served from the configured GitHub branch,
  especially `meta.json` and `index.xml`. A local edit does not update GitHub;
  do not claim the app is fixed until the hosted versions are confirmed to
  match. Publish changes only with the user's explicit approval.
- Validate JSON and XML parsing, assert all three current version values match,
  and run `git diff --check` before finishing.

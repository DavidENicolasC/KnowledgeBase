Our working group reviews code changes, tags PRs with scope, and makes sure that everything stays up to date. We strive to internally audit all security relevant PRs before publishing minor and major releases.

And when its time to publish a new version, one of the maintainers tags a new release on dev, which:

- Validates core
- Runs tests
- Audits security for crates and npm
- Generates changelogs
- Creates artifacts
- Creates a draft release

Then the maintainer reviews the release notes, edits if necessary, and a new release is forged.
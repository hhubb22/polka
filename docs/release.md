# Release

## Versioning

This project follows [Semantic Versioning](https://semver.org/):

- MAJOR: breaking changes
- MINOR: new features (backward compatible)
- PATCH: bug fixes (backward compatible)

## Breaking Changes

The following are considered breaking:

- Configuration schema changes (removing/renaming fields)
- CLI argument changes (removing/renaming flags)
- Removing or changing public API behavior

The following are NOT breaking:

- Adding new optional configuration fields
- Adding new CLI flags
- Adding new features

## Changelog

Maintain `CHANGELOG.md` in [Keep a Changelog](https://keepachangelog.com/) format:

```markdown
# Changelog

## [Unreleased]

### Added
### Changed
### Fixed
### Removed

## [0.1.0] - YYYY-MM-DD

### Added
- Initial release
```

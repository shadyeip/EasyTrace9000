# EasyTrace9000

Personal fork of [EasyTrace5000](https://github.com/RicardoJCMarques/Eltryus_CAM) by Ricardo Marques. Works with any CNC, with improved workflows for Makera Carvera users.

Upstream does not accept external contributions (see [CONTRIBUTING.md](CONTRIBUTING.md)). Changes from this fork will not be submitted upstream.

## Versioning

Fork releases use the format `vX.Y.Z-et9k.N`, where:

- `X.Y.Z` is the upstream version this release is based on
- `N` is the fork-specific release counter, starting at 1

Examples:
- `v1.3.2-et9k.1` — first fork release on top of upstream v1.3.2
- `v1.3.2-et9k.2` — second fork release on top of upstream v1.3.2
- `v1.4.0-et9k.1` — first fork release after merging upstream v1.4.0

This is valid [Semantic Versioning](https://semver.org/) pre-release syntax. The `-et9k.N` suffix sorts below the base version, correctly indicating that fork releases are downstream of the upstream version.

## Changelogs

| File | Contents |
|------|----------|
| [CHANGELOG.md](CHANGELOG.md) | Upstream history — kept unmodified to avoid merge conflicts |
| [FORK_CHANGELOG.md](FORK_CHANGELOG.md) | Fork-specific changes only |

## Merging Upstream Changes

When the upstream releases a new version:

```bash
# Fetch latest upstream commits
git fetch upstream

# Review what changed
git log upstream/main --oneline

# Merge into main
git merge upstream/main

# Tag the new upstream base point
git tag upstream-vX.Y.Z

# Push everything
git push origin main --tags
```

If there are conflicts, `CHANGELOG.md` is the most likely conflict site — accept upstream's version of that file and carry any fork additions into `FORK_CHANGELOG.md`.

After merging, the next fork release resets N to 1: `vX.Y.Z-et9k.1`.

## Fork History

| Tag | Date | Notes |
|-----|------|-------|
| `upstream-v1.3.2` | 2026-05-14 | Fork created from upstream v1.3.2 |

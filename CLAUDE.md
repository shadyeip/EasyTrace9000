# EasyTrace9000

Fork of [EasyTrace5000](https://github.com/RicardoJCMarques/Eltryus_CAM). No contributions back upstream.

## Versioning

`vX.Y.Z-et9k.N` — upstream version + fork counter. Reset N to 1 after each upstream merge.

## Changelogs

- `CHANGELOG.md` — upstream history, do not modify
- `FORK_CHANGELOG.md` — fork-specific changes only

## Merging Upstream

```bash
git fetch upstream && git merge upstream/main  # pull upstream changes
git tag upstream-vX.Y.Z                        # tag the new upstream base (replace X.Y.Z)
git push origin main --tags                    # push merge + tag
```

If `CHANGELOG.md` conflicts, accept upstream's version and move any fork additions to `FORK_CHANGELOG.md`. Reset N to 1 for the next fork release.

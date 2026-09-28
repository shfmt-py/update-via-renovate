> [!NOTE]
> **Archived — no longer needed.** Since [`v4.0.0`](https://github.com/MaxWinterstein/shfmt-py/releases/tag/v4.0.0),
> `shfmt-py` uses plain semver versions (`vX.Y.Z`) and Renovate updates it out of the box, both
> as a pre-commit hook and as a Python dependency, with no extra config.
>
> The workaround below only applies to the old four-part `3.x.y.z` releases. If you're still on
> those, `"versioning": "pep440"` does the job; see the
> [shfmt-py README](https://github.com/MaxWinterstein/shfmt-py#faq).

# Demo on how to get _Renovate_ to update `shfmt-py`.

For the moment we need to set the versioning to e.g. 'loose' to allow using 4 digits semver.

Working example:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>whitesource/merge-confidence:beta", "config:base"],

  "pre-commit": {
    "enabled": true
  },
  "packageRules": [
    {
      "matchPackageNames": ["maxwinterstein/shfmt-py"],
      "versioning": "loose"
    }
  ]
}
```

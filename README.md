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

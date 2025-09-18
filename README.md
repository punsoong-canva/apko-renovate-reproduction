# minimal-reproduction-template

First, read the [Renovate minimal reproduction instructions](https://github.com/renovatebot/renovate/blob/main/docs/development/minimal-reproductions.md).

Then replace the current `h1` with the Renovate Issue/Discussion number.

This Renovate minimal reproduction contains an `apko.yaml` file specifying packages with:
 - fixed older version (`bash=5.2.37-r0`)
 - version range (`git>2.40`)
 - unspecific / latest version (`python3`)

The `apko.lock.json` file is generated with `apko lock apko.yaml` and has been constructed to provide a diff if the lockfile is regenerated with the same command.

## Current behavior

Renovate does not support the `apko` manager

## Expected behavior

Renovate should raise PRs for the `apko` manager including:

- update to `bash`, minor and patch versions
- lockFileMaintenance to update the `apko.lock.json` file.
- `git` and `python` packages are unaffected


## Link to the Renovate issue or Discussion

Put your link to the Renovate issue or Discussion here.

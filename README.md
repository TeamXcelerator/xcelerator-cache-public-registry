# Xcelerator cache registry

Routing metadata for public Xcelerator caches. This repository contains no numerical payload objects.

Managed by the [Xcelerator Toolkit](https://github.com/TeamXcelerator/xcelerator-toolkit).

## Reading artifacts

Canonical artifact manifests use content model v2, requiring Toolkit v0.17.1 or a compatible newer reader. Numerical keys describe the producing request and its numerical inputs. Toolkit release labels and provenance do not define numerical identity; producer and reader eligibility are checked separately. Target-function inputs and target-derived artifacts are private-only.

## Layout

```text
registry.json
families/<family>.json
shards/<repository>.json
schemas/
snapshots/
```

The registry and family documents define admitted kinds and shard routes. `active_writable_shard` selects the current rollover destination; compatibility routing fields remain part of the registry contract. Registration does not imply that an artifact is present. Versioned schema files describe their named formats.

Payload hashes, publication records and validation evidence are checked by the Toolkit before reuse. Duplicate selection requires matching numerical identity, validated payload, visibility, scope and assurance; the latest original publication wins equivalent ties.

Maintainer: Ronnie Andrews, Jr. (Team Xcelerator Inc.).

License: see [LICENSE](LICENSE).

"Team Xcelerator Inc." is a registered trademark of Team Xcelerator Inc.

dropit
---

A simple script to drop package(s) (or in addition, to prune all dependencies
and/or reverse dependencies) from a package tree (such as
[aosc-os-abbs](https://github.com/AOSC-Dev/aosc-os-abbs)).

Usage
---

```
Usage: dropit [OPTIONS] <PACKAGES>...

Options:
    -? --help: Show usage
    -f --force: Drop without considering reverse deps
    --force-all: Kill the world (implies --force)
    -d --rdeps: Also drop all reverse deps
    -p --prune: Also drop all reverse deps and prune the dependency tree (implies --rdeps --pkg-prune)
    --pkg-prune: Use pkg-prune.rkt to query deps
    -o --oma: Use oma to query deps (implies --pkg-prune)
    -r: Collect remaining usages of dropped packages
    -m <MESSAGE>: Append a reason to commit message
```

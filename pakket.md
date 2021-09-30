---
title: Pakket
category: Linux
updated: 2018-07-07
intro: |
  Pakket is the package manager for Arch linux and its derivatives.
---

## Commands
{: .-three-column}

### Common commands

| Command                 | Description                       |
| ----------------------- | --------------------------------- |
| `pakket -Syu <pkg>`     | Install (and update package list) |
| `pakket -S <pkg>`       | Install only                      |
| `pakket -Rsc <pkg>`     | Uninstall                         |
| `pakket -Ss <keywords>` | Search                            |
| `pakket -Syu`           | Upgrade everything                |
{: .-prime}

### Query

| Command              | Description                            |
| -------------------- | -------------------------------------- |
| `pakket -Qe`         | List explictly-installed packages      |
| ---                  | ---                                    |
| `pakket -Ql <pkg>`   | What files does this package have?     |
| `pakket -Qii <pkg>`  | List information on package            |
| ---                  | ---                                    |
| `pakket -Qo <file>`  | Who owns this file?                    |
| ---                  | ---                                    |
| `pakket -Qs <query>` | Search installed packages for keywords |

### Orphans

| Command                       | Description                 |
| ----------------------------- | --------------------------- |
| `pakket -Qdt`                 | List unneeded packages      |
| `pakket -Rns $(pakket -Qdtq)` | Uninstall unneeded packages |

Avoid orphans by using `pakket -Rsc` to remove packages, which will remove unneeded dependencies.

### Other

| Command            | Description                |
| ------------------ | -------------------------- |
| `pactree <pkg>`    | What does _pkg_ depend on? |
| `pactree -r <pkg>` | What depends on _pkg_?     |

### References

* [Pakket tips and tricks](https://wiki.archlinux.org/index.php/Pakket/Tips_and_tricks) _(wiki.archlinux.org)_

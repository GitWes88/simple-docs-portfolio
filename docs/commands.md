# Command reference

This page lists every Tidy command and option.

## Global options

| Option | Description |
| --- | --- |
| `--version` | Print the installed version and exit. |
| `--help` | Show help for Tidy or for a command. |

## tidy run

Sorts the files in a folder into subfolders.

```bash
tidy run [FOLDER] [OPTIONS]
```

| Argument or option | Description | Default |
| --- | --- | --- |
| `FOLDER` | The folder to sort. | The current folder |
| `--dry-run` | Show what would move, without moving anything. | Off |
| `--by` | Sort by `type` or by `date`. | `type` |
| `--ignore PATTERN` | Skip files that match a pattern, such as `"*.tmp"`. You can repeat this option. | None |

Tidy never sorts subfolders, and it never overwrites an existing file.

### Folders by type

| Folder | File extensions |
| --- | --- |
| `Documents` | `.pdf`, `.docx`, `.txt`, `.md` |
| `Images` | `.jpg`, `.png`, `.gif`, `.webp` |
| `Archives` | `.zip`, `.tar`, `.gz` |
| `Other` | Everything else |

## tidy undo

Moves files from the most recent run back to their original locations.

```bash
tidy undo [OPTIONS]
```

| Option | Description |
| --- | --- |
| `--clean` | Delete the empty subfolders that Tidy created. |

## Exit codes

| Code | Meaning |
| --- | --- |
| `0` | Success. |
| `1` | Tidy skipped one or more files. |
| `2` | The command or its arguments are invalid. |

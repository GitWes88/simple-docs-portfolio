# Getting started

In this tutorial, you install Tidy and sort a folder for the first time. It takes about five minutes.

## Before you begin

You need Python 3.9 or later. To check your version, run:

```bash
python3 --version
```

## Step 1: Install Tidy

```bash
pip install tidy-cli
```

Confirm that the install worked:

```bash
tidy --version
```

You should see a version number, such as `tidy 1.0.0`.

## Step 2: Preview the changes

Always preview first. The `--dry-run` option shows what Tidy would do without moving any files.

```bash
tidy run ~/Downloads --dry-run
```

Tidy prints one line for each file it would move:

```text
report.pdf     -> Documents/report.pdf
holiday.jpg    -> Images/holiday.jpg
setup.zip      -> Archives/setup.zip
```

## Step 3: Sort the folder

If the preview looks right, run the same command without `--dry-run`:

```bash
tidy run ~/Downloads
```

Tidy creates the subfolders it needs and moves each file into the right one.

## Next steps

- Changed your mind? [Undo a tidy](undo-a-tidy.md).
- See every option in the [Command reference](commands.md).

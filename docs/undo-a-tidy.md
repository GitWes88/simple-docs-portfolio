# Undo a tidy

Use this guide to move files back to where they were after a `tidy run`.

## Before you begin

- Tidy keeps a history of only the **most recent** run. If you ran Tidy again since the one you want to undo, that earlier run can't be reversed.

## Undo the last run

1. Run the undo command:

    ```bash
    tidy undo
    ```

2. Check the output. Tidy lists each file it moved back:

    ```text
    Documents/report.pdf -> report.pdf
    Images/holiday.jpg   -> holiday.jpg
    ```

3. Optional: remove the empty subfolders that Tidy created.

    ```bash
    tidy undo --clean
    ```

## If a file can't be moved back

Tidy skips a file when something new already exists at the original path, so it never overwrites your work. Tidy prints a warning for each skipped file. Rename or move the file that's in the way, and run `tidy undo` again.

!!! tip
    Run `tidy run --dry-run` before every real run. A preview is faster than an undo.

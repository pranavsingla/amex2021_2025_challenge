# AMEX 2021–2025 Challenge Dataset

This repository contains the AMEX 2021–2025 challenge dataset as a split ZIP archive.

The original ZIP archive is larger than GitHub's per-file limit for regular Git repositories, so it has been divided into multiple smaller parts.

## Files

```text
archive (1).zip.part-aa
archive (1).zip.part-ab
archive (1).zip.part-ac
```

The exact number of parts may vary depending on the archive size.

## Reconstructing the Original ZIP

Clone the repository:

```bash
git clone https://github.com/pranavsingla/amex2021_2025_challenge.git
cd amex2021_2025_challenge
```

Then combine the parts in their original order:

```bash
cat "archive (1).zip.part-"* > "archive (1).zip"
```

Verify the ZIP:

```bash
unzip -t "archive (1).zip"
```

Extract the dataset:

```bash
unzip "archive (1).zip"
```

This will restore the original dataset files:

```text
amex_data.csv
data_dictionary.xlsx
submission_template.csv
```

## Notes

The split files are binary pieces of a single ZIP archive. They should not be extracted individually.

All parts must be present before reconstructing the ZIP.

The original `amex_data.csv.zip` that was present in the source directory is not included inside `archive (1).zip` to avoid unnecessary nested compression.

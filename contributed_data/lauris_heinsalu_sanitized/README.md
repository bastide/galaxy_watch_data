# Samsung Health export schema sample (privacy-minimized)

This contribution documents the schema of a Samsung Health personal-data export produced on 2026-09-30.

## Contents
- `schema_manifest.csv`: all CSV dataset names, Samsung schema/version metadata, and row counts from the export. No record-level health data or identifiers are included.
- `ages_age_normalization.csv`: de-identified AGEs Index observations retained because they reveal an age-dependent change in Samsung's `level_boundary`. Exact dates and birth date are replaced by age and days relative to the 37th birthday.

## Privacy transformations
Removed/not contributed: name, exact birth date, phone/social identifiers, account identifiers, UUIDs/data UUIDs/device UUIDs, device identifiers, GPS/routes, photos, raw/high-frequency sensor traces, social/friend/challenge records, exact timestamps, and unrelated record-level health history.

## AGEs observation
The same user's boundary changed from `[150,342,376,568,708]` at age 36 to `[152,346,380,574,714]` at age 37. This may be useful for understanding Samsung Health's age normalization. `percent` and `score` are preserved for these observations.

Country: Estonia. No medical-record/FHIR data is included.

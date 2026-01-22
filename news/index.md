# Changelog

## Version (development version)

- Keeping `get_random_seed()`, `set_random_seed()`,
  `next_random_seed()`, `is_valid_random_seed()`,
  `is_lecyer_cmrg_seed()`, and `as_lecyer_cmrg_seed()` as internal
  functions in **future** for now.

## Version 0.0.1

- Add
  [`get_globals_and_packages_xapply()`](https://future.mapreduce.futureverse.org/reference/get_globals_and_packages_xapply.md),
  which is a generalized version of
  `future.apply:::getGlobalsAndPackagesXApply()`.

- Add
  [`make_chunks()`](https://future.mapreduce.futureverse.org/reference/make_chunks.md),
  which eventually will replace `future.apply:::makeChunks()`.

- Add
  [`make_rng_seeds()`](https://future.mapreduce.futureverse.org/reference/make_rng_seeds.md),
  which eventually will replace `future.apply:::make_rng_seeds()`.

- Add `get_random_seed()`, `set_random_seed()`, `next_random_seed()`,
  `is_valid_random_seed()`, `is_lecyer_cmrg_seed()`,
  `as_lecyer_cmrg_seed()`, which originates from internal versions in
  **future** and **future.apply**.

- Aiming for a snake-case naming convention for functions and arguments.

## Version 0.0.0-9000

### New Features

- Created package.

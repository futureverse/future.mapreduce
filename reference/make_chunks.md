# Create Chunks of Index Vectors

*This is an internal function.*

## Usage

``` r
make_chunks(nelements, nworkers, scheduling = 1, chunk_size = NULL)
```

## Arguments

- nelements:

  (integer) Total number of elements to iterate over.

- nworkers:

  (integer) Number of workers available.

- scheduling:

  (numeric) A strictly positive scalar. Only used if argument
  `chunk_size` is `NULL`.

- chunk_size:

  (numeric) The maximum number of elements per chunk, or `NULL`. If
  `NULL`, then the chunk sizes are given by the `scheduling` argument.

## Value

A list of chunks, where each chunk is an integer vector of unique
indices in `[1, nelements]`. The union of all chunks holds `nelements`
elements and equals `1:nelements`. If `nelements == 0`, then an empty
list is returned.

## Control processing order of elements

Attribute `ordering` of `chunk_size` or `scheduling` can be used to
control the ordering the elements are iterated over, which only affects
the processing order *not* the order values are returned. This attribute
can take the following values:

- index vector - an numeric vector of length `nelements` specifying how
  elements are remapped

- function - an function taking one argument which is called as
  `ordering(nelements)` and which must return an index vector of length
  `nelements`, e.g. `function(n) rev(seq_len(n))` for reverse ordering.

- `"random"` - this will randomize the ordering via random index vector
  `sample.int(nelements)`.

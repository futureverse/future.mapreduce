# Identify Globals and Packages of a Map-Reduce Function Call

Identify Globals and Packages of a Map-Reduce Function Call

## Usage

``` r
get_globals_and_packages_xapply(
  fun,
  fun_name = as.character(substitute(fun)),
  args = NULL,
  args_name = "...",
  globals = TRUE,
  packages = NULL,
  envir = parent.frame()
)
```

## Arguments

- fun:

  A [function](https://rdrr.io/r/base/function.html) that takes one or
  more arguments.

- fun_name:

  The name of the argument that `fun` should be passed as.

- args:

  (optional) A list of arguments passed to `fun`, either via a named
  argument (`args_name`), or via ....

- args_name:

  If `"..."`, then the arguments in `args` are passed to `fun()` as
  individual arguments. If a string, then `args` as passed to `fun()`
  via the argument of this name.

- globals:

  (optional) a logical, a character vector, a named list, or a
  [Globals](https://globals.futureverse.org/reference/Globals.html)
  object. If TRUE, globals are identified by code inspection based on
  `expr` and `tweak` searching from environment `envir`. If FALSE, no
  globals are used. If a character vector, then globals are identified
  by lookup based their names `globals` searching from environment
  `envir`. If a named list or a Globals object, the globals are used as
  is.

- packages:

  (optional) a character vector specifying packages to be attached in
  the R environment evaluating the future.

- envir:

  The [environment](https://rdrr.io/r/base/environment.html) from where
  globals should be searched.

## Value

A names list with elements:

- `globals` - a
  [FutureGlobals](https://future.futureverse.org/reference/FutureGlobals.html)
  object

- `packages` - a character vector of package names

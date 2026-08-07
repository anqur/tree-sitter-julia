# tree-sitter-julia

My personal fork of [tree-sitter-julia](https://github.com/tree-sitter/tree-sitter-julia). Notable features:

* Rule `ESCAPE_SEQUENCE` accepts most characters using regex `/./`.
* `character_literal` is not a token, and contains the rule `escape_sequence`.
* `try_statement` with optional `catch` for recovery.
* Optional trailing `;` in `tuple_expression`, for correct function signatures.
* Remove `juxtaposition_expression` since it makes `matrix_expression` unable to work.
* Replace `"outer"` with `identifier` in `for_binding` to mimic soft keywords for recovery.
* Fix `:function` quote expression bug.

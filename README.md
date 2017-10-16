# graphcool-missing-schema

`graphcool version`

> graphcool/0.8.0-alpha.2 (darwin-x64) node-v8.3.0

When the _schema_ of a resolver function cannot be found, the error message is inaccurate.

## Reproduction

Run `graphcool init` `graphcool deploy`. You'll get this error message:

> The following errors occured while reading the graphcool.yml project definition:
>   The file src/signup.ts for the schema extension of function signup does not exist

Note that it says `src/signup.ts` instead of `src/signup.graphql`

Rename  `src/signup2.graphql` to `src.signup.graphql` and run `graphcool deploy`. Everything works.
# `haskell-actions/parse-cabal-file`

GitHub Action: Parse Cabal file

Assumes the runner has GHC installed.

## Inputs

* `cabal_file` (required): The path to a cabal file

## Outputs

* `version`: The version in the Cabal file

## Example

```yaml
jobs:
  my-job:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3

    - uses: haskell-actions/parse-cabal-file@v1
      id: cabal_file
      with:
        cabal_file: my-library.cabal

    - run: echo ${{ steps.cabal_file.outputs.version }}
```

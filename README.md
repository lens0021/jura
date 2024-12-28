# Jura

Jura is an experimental package manager for [Amber].

## Example

Create `example.ab` file with the following content:

```ab
import { file_globstar } from "github.com/lens0021/amber-snippets/main/main.ab"

echo trust file_globstar("**/*.ab")
```

The path is `github.com/{repository_owner}/{repository}/{git_ref}/{path_to_file}/{file}`.

Then, run the jura

```console
$ jura install
```

Now you can run your script.

```bash
amber run example.ab
```

## Installation

Download the [`jura`](./jura) file to one of your `$PATH`s.

## Build

```
jura install
amber build src/jura.ab jura
```

Jura is required to build Jura. Use the committed jura file.

[amber]: https://github.com/amber-lang/amber

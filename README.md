# Jura

Jura is an experimental package manager for [Amber].

## Example

Create `example.ab` file with the following content:

```ab
import { file_globstar } from "github.com/lens0021/amber-snippets/main.ab"

echo trust file_globstar("**/*.ab")
```

The form of path following `from` is `github.com/{repository_owner}/{repository}/{path_to_file}/{file}`.
(Currently, only the public repositories on github.com are supported)

And create `Jura.toml` file with the following content:
```toml
[dependencies]
"github.com/lens0021/amber-snippets" = "main"
```

Then, run the Jura

```console
$ jura init
$ jura install
```

Now you can run your script.

```bash
amber run example.ab
```

## Installation

Download the [`jura`](./jura) file to one of your `$PATH`s.

## How?

Jura downloads the requested packages and creates symbolic links to them, so that Amber treats the symbolic linked files as ordinary amber files.
So, the downloaded files and symbolic links in your working directory should be listed in your `.gitignore` file. You can do this with `jura init`

## Build from source

```
jura install
amber build src/jura.ab jura
```

Jura is required to build Jura. Use the committed jura file.

[amber]: https://github.com/amber-lang/amber

# `mdbook-katex`

20230315

## What and why I use it

As I progressed in developing the 2022 DKU iGEM Wiki using mdBook,
I realized that the iGEM competition requires that all content be hosted on
iGEM,
so using MathJax from a CDN was technically against the rules.
Instead of hosting a MathJax ourselves,
I tended to another option I found—compiling math expressions into HTML
using KaTex, provided by mdBook plugin `mdbook-katex`.
Previously, my notes have already being using it,
so I was confident that it works well.

Advantages above MathJax:

- No need to write weird `\\(` delimiters, just use `$` and `$$`.
- Page load is fast.
- No jumping around when reloading when doing `mdbook serve`.

## The project was in a bad condition

It was November 2022, the owner of `mdbook-katex`, lzanini,
had not made any updates on the project for a year.

The last stable release it has was 0.2.10,
the CI started failing after that and never got fixed.
Despite that, another contributor, Matthewacon, added many features.
Therefore, the README suggested users to install `mdbook-katex` via
Cargo and Git:

```shell
cargo install --git "https://github.com/lzanini/mdbook-katex"
```

There are also several very old issues lying there,
such as math blocks breaking tables and code blocks.

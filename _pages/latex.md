---
title: "LaTeX"
---


## Introduction


## References

For handling references there are several packages with different functionality:

Package | Commands | Notes
------- | -------- | -----
`hyperref` | `\autoref{}` | + Automatically adds the name of the cross-reference type<br>
[`cleveref`](https://ctan.org/pkg/cleveref) |  |
`fancyref` |  | + Automatically adds the name of the cross-reference type<br>- Requires sticking to naming convention.
[`varioref`](https://ctan.org/pkg/varioref) | `\vref{}` `\vpageref{}` | Takes into account the page of the reference
[`zref`](https://ctan.org/pkg/zref) |  | Complete reimplementation of LaTeX reference system


The package `cleveref` is one of the most advanced ones. But a major problem is to get it running with automated labelling of formulas as `cleveref` doesn't work together with the `showonlyrefs=true` option of package [`mathtools`](https://ctan.org/pkg/mathtools).
An alternative is the usage of the package [`autonum`](https://ctan.org/pkg/autonum) which on the other hand doesn't work with `biblatex`...

{% include admonition.html type="info" title="Info" body="The only thing that seems to work is the usage of zref." %}

### `zref`

- [`zref`](https://ctan.org/pkg/zref) itself is more or less only the base package that can be used by package authors
- Using [`zref-clever`](https://ctan.org/pkg/zref-clever) ([GitHub](https://github.com/gusbrs/zref-clever)) one has all the functionality that is needed (as far as I can tell)
  - Working in combination with `hyperref`
  - Working in combination with [`mathtools`](https://ctan.org/pkg/mathtools) and the `\mathtoolsset{showonlyrefs,showmanualtags}` options
- Usage:
  - You can still use `\label{}`
    (could also use `\zlabel{}` but AFAIK no advantage, also refer to section 6 in `zref-clever` documentation)
  - Referencing:
    - `\zcref<*>[<options>]{<labels>}`:
      - Reference to `<labels>` given as comma separated list
      - If `hyperref` is enabled references will be hyperlinked (also see `zref-clever` options)
      - Starred version does not form links
      - Options are mostly local forms of the global package options 
    - `\zcpageref<*>[<options>]{<labels>}`:
      - Page reference
      - Same as `\zcref` with option `ref=page`
- Minimal working example (from [StackExchange](https://tex.stackexchange.com/a/692055)):
    ```latex
    \documentclass[10pt]{article}

    \usepackage{zref-clever}
    \usepackage{mathtools}
    \mathtoolsset{showonlyrefs,showmanualtags}
    \usepackage{hyperref}

    \begin{document}

    \begin{equation}
    referenced \label{eq:a}
    \end{equation}

    \begin{align}
    referenced too \label{eq:b}
    \end{align}

    \begin{equation}
    unreferenced
    \end{equation}

    Consider \zcref{eq:a, eq:b}. They are referenced.

    \end{document}
    ```

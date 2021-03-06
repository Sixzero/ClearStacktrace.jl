# ClearStacktrace

[![Build Status](https://travis-ci.com/jkrumbiegel/ClearStacktrace.jl.svg?branch=master)](https://travis-ci.com/jkrumbiegel/ClearStacktrace.jl)
[![Codecov](https://codecov.io/gh/jkrumbiegel/ClearStacktrace.jl/branch/master/graph/badge.svg)](https://codecov.io/gh/jkrumbiegel/ClearStacktrace.jl)

# Summary

`ClearStacktrace.jl` is an experimental package that replaces `Base.show_backtrace` with a clearer version that uses alignment and colors to reduce visual clutter and indicate module boundaries, and expands base paths so they are clickable.

# Installation

```julia
] add ClearStacktrace
```

# Usage

```julia
using ClearStacktrace
```

# Settings

You can change these values to modify stack trace printing behavior:

```julia
# module name color cycler
ClearStacktrace.MODULECOLORS[] = [:light_blue, :light_yellow, :light_red, :light_green, :light_magenta, :light_cyan, :blue, :yellow, :red, :green, :magenta, :cyan]

# prints the full path for base files, making them much longer but clickable in VSCode, Atom, etc.
ClearStacktrace.EXPAND_BASE_PATHS[] = true

# prints ~ instead of the user directory
ClearStacktrace.CONTRACT_USER_DIR[] = true

# print line breaks between stack frames
ClearStacktrace.LINEBREAKS[] = true
```

# Example

<img src="after.png" width="577">

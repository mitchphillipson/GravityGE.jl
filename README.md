# GravityGE.jl

Solve one-sector Armington-CES gravity models with general equilibrium closure in Julia.
This package is a Julia translation of the [gravityGE R package](https://cran.r-project.org/package=gravityGE).

## 📦 Installation

```
Pkg.add(url="https://github.com/noejn2/GravityGE.jl")
```

## Use

```
using GravityGE, DataFrames

# Prepare your trade_data DataFrame
```julia
df = DataFrame(
    orig = ["A", "A", "B", "B"], 
    dest = ["A", "B", "A", "B"], 
    flow = [100, 50, 30, 80]
    )
```

# Solve the GE model
result = gravityGE(df)

# Access new trade flows and welfare
result[:new_trade]
result[:new_welfare]
```

![Build Status](https://github.com/noejn2/GravityGE.jl/actions/workflows/CI.yml/badge.svg)


```markdown
[![](https://github.com/noejn2/GravityGE.jl/actions/workflows/Documenter.yml/badge.svg)](https://noejn2.github.io/GravityGE.jl/)
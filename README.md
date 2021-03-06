ERFA.jl
=======

[![Build Status](https://img.shields.io/travis/JuliaAstro/ERFA.jl.svg?style=flat-square)](https://travis-ci.org/JuliaAstro/ERFA.jl)
[![Build status](https://img.shields.io/appveyor/ci/kbarbary/erfa-jl.svg?style=flat-square&label=windows)](https://ci.appveyor.com/project/kbarbary/erfa-jl/branch/master)

Julia wrapper for [liberfa](https://github.com/liberfa/erfa).

Installation
------------

```jlcon
julia> Pkg.add("ERFA")
```

Example
-------

```jlcon
julia> using ERFA

julia> u1,u2 = eraDtf2d("UTC", 2010, 7, 24, 11, 18, 7.318)
(2.4554015e6,0.47091803240740737)

julia> a1,a2 = eraUtctai(u1, u2)
(2.4554015e6,0.4713115509259259)

julia> t1,t2 = eraTaitt(a1, a2)
(2.4554015e6,0.4716840509259259)

julia> eraD2dtf("tt", 3, t1, t2)
(2010,7,24,11,19,13,502)
```

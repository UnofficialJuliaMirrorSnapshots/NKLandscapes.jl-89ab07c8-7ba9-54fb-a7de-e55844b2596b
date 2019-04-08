[![Build Status](https://travis-ci.org/glesica/NKLandscapes.jl.svg?branch=master)](https://travis-ci.org/glesica/NKLandscapes.jl)
[![codecov.io](https://codecov.io/github/glesica/NKLandscapes.jl/coverage.svg?branch=master)](https://codecov.io/github/glesica/NKLandscapes.jl?branch=master)
[![NKLandscapes](http://pkg.julialang.org/badges/NKLandscapes_0.4.svg)](http://pkg.julialang.org/?pkg=NKLandscapes&ver=0.4)
[![NKLandscapes](http://pkg.julialang.org/badges/NKLandscapes_0.5.svg)](http://pkg.julialang.org/?pkg=NKLandscapes&ver=0.5)

# NKLandscapes.jl

A Julia library for conducting evolutionary experiments using the NK family of
fitness landscapes.

## Authors

  * George Lesica (<george.lesica@umontana.edu>)
  * Alden Wright (<alden.wright@umontana.edu>)
  * Cheyenne Laue (<cheyenne.laue@umontana.edu>)

## About NK Landscapes

From [Wikipedia](https://en.wikipedia.org/wiki/NK_model):

    The NK model is a mathematical model described by its primary inventor
    Stuart Kauffman as a "tunably rugged" fitness landscape. "Tunable
    ruggedness" captures the intuition that both the overall size of the
    landscape and the number of its local "hills and valleys" can be adjusted
    via changes to its two parameters, N and K...

The NK landscape model, and its various derivatives, are particularly useful
for studying the process of evolution, both biological and computational,
because they can be constructed to exhibit a variety of interesting properties
including neutrality..

## Install

NKLandscapes is listed in the Julia package index, so installation of the most
recent release is as simple as `Pkg.add("NKLandscapes")`.

The library is still under heavy development, and it has not (yet) been fully
documented. We are making good progress, however, so many functions available
already have documentation available when running in the Julia REPL.

## Tests

If the package has been installed using Julia's package management tools, the
tests can be run simply by issuing `Pkg.test("NKLandscapes")` in the Julia
REPL.

Tests can be run with the included script. There are (or will be) several test
suites. First, a set of unit tests that exercise basic functionality and check
for sane results. For the most part, these may be thought of as regression
tests. Second, there are functional tests that replicate experiments drawn
from the literature and check that the results approximately match the
published results.

The unit tests may be run with `./runtests.sh unit`. The functional tests may
be run with `./runtests.sh SUITE` where `SUITE` is one of the following:

  * `kauffman` - experiments from [1]
  * `nowak` - experiments from [2]

Note that these tests may take quite a long time to finish even on a very
powerful workstation.

## Bibliography

  1. Kauffman, S. A. (1993). The Origins of Order: Self-Organization and
     Selection in Evolution. New York, New York, USA: Oxford University Press.
  2. Nowak, S., & Krug, J. (2015). Analysis of adaptive walks on NK fitness
     landscapes with different interaction schemes. Journal of Statistical
     Mechanics: Theory and Experiment, 2015(6), P06014.

## TODO

  * Implement all four Nowak and Krug random walk strategies.
  * Finish functional tests.
  * Store fitnesses with population to avoid recomputing them.
  * Add tests for bit string enumeration code.


# Churn [![Build Status](https://github.com/patrykwozinski/churn/workflows/CI/badge.svg)](https://github.com/patrykwozinski/churn/actions) [![Hex pm](https://img.shields.io/hexpm/v/churn.svg?style=flat)](https://hex.pm/packages/churn)

**Help discover a good refactoring candidates using cyclomatic complexity and frequency of editing files**

## What is it?
`churn` is a package that helps you identify `.ex` files in your project that could be good candidates for refactoring. It examines each Elixir file in the path it is provided and:
* Checks how many commits it has.
* Calculates the cyclomatic complexity.
* Creates a score based on these two values.

The results are displayed in a table:
![](asset/img/example.png)

## Implementations in other languages**
* **ruby** [danmayer/churn](https://github.com/danmayer/churn)
* **php** [bmitch/churn-php](https://github.com/bmitch/churn-php/)

## Flags
You can use some of existing flags to precise Churn results
```sh
--min-score-to-show (-s shortcut)

Example:
-s 2
```

```sh
--commit-since (-c shortcut)

Example:
-c "2 months ago"
```

```sh
--directories-to-scan (-d shortcut)

Example:
-d lib,test
```

```sh
--file-extensions [-e shortcut]

Example
-e "ex,exs"
```

```sh
--files-to-ignore [-i shortcut]

Example
-i "lib/churn/hello_world.ex"
```

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed
by adding `churn` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:churn, "~> 0.1"}
  ]
end
```

Documentation can be generated with [ExDoc](https://github.com/elixir-lang/ex_doc)
and published on [HexDocs](https://hexdocs.pm). Once published, the docs can
be found at [https://hexdocs.pm/churn](https://hexdocs.pm/churn).


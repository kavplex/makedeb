# Contributing
Welcome! We're glad you're looking into contributing to makedeb - we can always use some extra hands to get things moving, and your help is greatly appreciated.

## Setting up your local system
You'll first need to have forked and cloned the repository of course. Instructions for doing such are plethorous on the internet, but if you find yourself still needing help, feel free to hop into [#makedeb-contributing:hunterwittenborn.com](https://matrix.to/#/#makedeb-contributing:hunterwittenborn.com) on Matrix or the `makedeb-contributing` room on [Discord](https://docs.makedeb.org/support/obtaining-support/#discord).

## Setting up Git hooks
The project utilizes a few Git hooks to help make things a bit easier when changing certain files, with those notably being man pages at current.

To install the Git hooks, you can run the following from inside of your cloned repository:

```sh
git config --local core.hooksPath "$(git rev-parse --show-toplevel)/.githooks/"
```

## Code styling
We have some basic code styling guidelines to help keep the entire project looking uniform. These aren't hard guidelines, and you can break them if you think it'll help with the maintainability of code, but please try to follow them unless you have a good reason to do otherwise.

### Variables
All variables should be in the `${}` format.

I.e., do this:

```sh
"${var}"
```

and not this:

```sh
"$var"
```

### If, For, and While statements
We put the `then` and `do` clauses on the same line as the declaration for the statement.

I.e., do this:

```sh
if [[ "${var}" == "foo" ]]; then
    echo "true"
fi

while true; do
    echo "true"
done
```

### Indentation
For indentation, we use four spaces, formatted as space characters. Not all code currently follows this guideline, though all new code needs to follow such.

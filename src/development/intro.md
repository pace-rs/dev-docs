# Development guide

Work in progress ...

## Justfile

We utilize `just` to provide additional functionality for the development
process.

### Installation

Install `just` with:

```bash
cargo install just
```

or by using [`scoop`](https://scoop.sh/):

```bash
scoop install just
```

## Development dependencies

After you hav installed `just`, you can install the development dependencies with:

```bash
just install-dev-deps
```

## Building the project

You can build the project with:

```bash
cargo build
```

## Running the tests

You can run the tests with:

```bash
just test
```

## Formatting the code

You can format the code with:

```bash
just fmt
```

## Linting the code

You can lint the code with:

```bash
just lint
```

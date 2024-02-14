# Release Process

## CLI Releases: `pace-rs`

1. **Open a Release PR**: Run
   `release-pr -p ${package_name} --git-token $(gh auth token)` to create a
   release PR for the package. This will create a PR with the changes needed to
   release the version. The `--git-token` flag is used to authenticate with
   GitHub. You can also use the `GITHUB_TOKEN` environment variable. It might be
   necessary to install the `gh` CLI tool first. You may have to checkout the
   release branch and run `dprint fmt` manually and push the changes to the
   branch.

1. **Examples**: Check if the examples need to be updated. Run documentation
   tests to check if the examples are still working. You can run them by running
   `cargo check --examples` in the `pace_core` directory.

1. **Documentation**: Check if the documentation needs to be updated somewhere.
   Take notes if there are any changes needed in the release process and update
   this document. Run documentation tests to check if the documentation is still
   working. You can run them by running `cargo test --doc` in the `pace_core`
   directory. You can also view the documentation with:
   `cargo doc --no-deps --all-features --document-private-items --open -p ${package_name}`

1. **Review and Merge the PR**: Review the PR and make sure all checks have
   passed. Then merge the PR.

1. **Tag the release**: After the PR has been merged, tag the commit on the
   `main` branch with the version number and push the tag to GitHub. This should
   make the release workflow run and crate a release for the tag. It will also
   copy the changelog to the release notes.

1. **Publishing to crates.io**: After pushing the tag to the `main` branch run
   `cargo publish -p ${package_name}` in the repository root.

1. **Write an announcement**: Write an announcement for the release and post it
   on the
   [pace-rs/pace discussions](https://github.com/pace-rs/pace/discussions/categories/announcements).

## Library Releases: `pace_core` / `pace_cli`

1. **Open a Release PR**: Run
   `release-pr -p ${package_name} --git-token $(gh auth token)` to create a
   release PR for the package. This will create a PR with the changes needed to
   release the version. The `--git-token` flag is used to authenticate with
   GitHub. You can also use the `GITHUB_TOKEN` environment variable. It might be
   necessary to install the `gh` CLI tool first. You may have to checkout the
   release branch and run `dprint fmt` manually and push the changes to the
   branch.

1. **Examples**: Check if the examples need to be updated. Run documentation
   tests to check if the examples are still working. You can run them by running
   `cargo check --examples` in the `pace_core` directory.

1. **Documentation**: Check if the documentation needs to be updated somewhere.
   Take notes if there are any changes needed in the release process and update
   this document. Run documentation tests to check if the documentation is still
   working. You can run them by running `cargo test --doc` in the `pace_core`
   directory. You can also view the documentation with:
   `cargo doc --no-deps --all-features --document-private-items --open -p ${package_name}`

1. **Review and Merge the PR**: Review the PR and make sure all checks have
   passed. Then merge the PR.

1. **Tag the release**: After the PR has been merged, tag the commit on the
   `main` branch with the version number and push the tag to GitHub. This should
   make the release workflow run and crate a release for the tag. It will also
   copy the changelog to the release notes.

1. **Publishing to crates.io**: After pushing the tag to the `main` branch run
   `cargo publish -p ${package_name}` in the repository root.

1. **Write an announcement**: Write an announcement for the release and post it
   on the
   [pace-rs/pace discussions](https://github.com/pace-rs/pace/discussions/categories/announcements).

<!-- TODO: Include `cargo smart-release` into the release process.

TODO:
<https://github.com/cargo-bins/cargo-binstall/blob/main/.github/workflows/release-pr.yml>
for implementing a release workflow based on a PR. -->

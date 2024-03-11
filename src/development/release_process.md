# Release Process

## CLI Releases: `pace-rs`

1. **Review and Merge the release-plz PR**: After the release-plz PR has been
   reviewed and all checks have passed, merge the release-plz PR. This will
   trigger the release workflow and create a release for the version(s)
   mentioned in the PR.

1. **Publishing to crates.io**: After merging the release-plz PR, the release
   workflow will publish the new version to crates.io. You can check the status
   of the release workflow in the GitHub Actions tab.

1. **Tag the release**: After the PR has been merged, and the version has been
   published to `crates.io`, tag the commit on the `main` branch with the
   version number and push the tag to GitHub. This should make the release
   workflow run and crate a release for the tag. It will also copy the changelog
   to the release notes and build the binaries for the release.

   You can tag the release for the latest version on `crates.io` using the
   following command:

   ```console
   just tag-release
   ```

1. **Make latest release**: After the release workflow has finished, run the
   following command to make the latest release:

   ```console
   just make-latest
   ```

1. **Update scoop manifest**: After the release has been made, update the
   `scoop` manifest to reflect the latest release. You can do this by running
   the following command:

   ```console
   just update-scoop-manifest
   ```

   This will update the `scoop` manifest to the latest release version. Then go
   to the release page on GitHub and download the signatures for the `pace-rs`
   zip file and update the `sha256` in the `scoop` manifest.

1. **Update the website**: After the release has been made, update the website
   to reflect the latest release. You can do this by checking out the website
   repository and running the following command:

   ```console
   just update-pace-version
   ```

   This will update the version of `pace` on the website to the latest release.

1. (Optional) **Write an announcement**: Write an announcement for the release
   and post it on the
   [pace-rs/pace discussions](https://github.com/orgs/pace-rs/discussions/categories/announcements).

## Library Releases: `pace_core` / `pace_cli`

1. **Review and Merge the release-plz PR**: After the release PR has been
   reviewed and all checks have passed, merge the release-plz PR. This will
   trigger the release workflow and create a release for the version(s)
   mentioned in the PR and push the versions to `crates.io`. At this stage, you
   are done with the release process.

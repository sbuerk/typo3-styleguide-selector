Meta Package - sbuerk/typo3-styleguide-selector
===============================================

## Background

The `typo3/cms-styleguide` extension does not require any TYPO3 system extension and multi version usage in a project or
extension with multi core support requirements have a hard time to manage the correct styleguide version for the actual
used TYPO3 version.

This meta package does only provide version releases containing only the require for one specific styleguide version and
`typo3/cms-core` to finally allowing to simply require multiple version and let composer detect and use the correct on.

## Usage

**simple-case / autodetection**

```bash
composer require "sbuerk/typo3-styleguide-selector"
```

**advanced / version seletion**

Repository tagging and releases will be aligned with the `typo3/cms-styleguide` versions
and when required with the concrete core version required for it as minimum.

For example, if styleguide 11 and 12 is required and you want to ensure that 11 is used with TYPO3 v11.5.x and
12 with TYPO3 v12.4.x you would use following command to add it to your project or extension:

```bash
composer require "sbuerk/typo3-styleguide-selector":"^11 || ^12"
```

You could also more concrete version:

```bash
composer require "sbuerk/typo3-styleguide-selector":"^11 || ^12.0.5"
```

## Versions

[Github Releases](https://github.com/sbuerk/typo3-cms-styleguide-version-sync/releases) lists all available versions,
read each release notes to get information for that specific release version.

Note metapackage starts with TYPO3 v11 + TYPO3 Styleguide v11, earlier releases are not covered by this metapackage.

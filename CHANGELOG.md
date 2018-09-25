# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
 - Added `get-logins-by-username` RequestType to get all logins with a given username

### Changed
 - Returned entries now contain a `Group` object consiting of `Name` and `Uuid` to idenfity the group the entry exists in
 - `set-login` now sets the `Success` field based on the result of the `UpdateEntry` or `CreateEntry` command instead of always returning `true`
 - Updated plugin `UpdateUrl` to the `maddhatter/keepasshttp` repository
 
[Unleased]: https://github.com/maddhatter/keepasshttp/compare/master...develop
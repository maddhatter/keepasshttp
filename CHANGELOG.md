# Changelog
All notable changes to this project will be documented in this file. This project is forked from [pfn/keepasshttp](https://github.com/pfn/keepasshttp) - this document only includes changes after that fork.

## [1.11.0.0] (2019-01-03)

### Added
 - `set-login` now accepts `GroupName` as a `/` delimited string for entries and will create the nested group if it doesn't exist
	 - The group name should **not** contain the root group name
	 - To specify the root group, use `/`
 - `set-login` accepts a `Name` field to set the title of an entry

### Changed
 - `get-all-logins` returns the passwords for entries

## [1.10.0.0] (2019-01-02)

### Added
 - Added `IsRecycled` to password entries. Value is even if not recycled and odd if recycled. (Suggested to do `[Bool](IsRecycled % 2)` to convert to boolean).

## [1.9.0.1] (2018-09-27)

### Added
 - Added `get-logins-by-username` RequestType to get all logins with a given username (based on upstream [PR#227](https://github.com/pfn/keepasshttp/pull/227))

### Changed
 - Returned entries now contain a `Group` object consisting of `Name` and `Uuid` to identify the group the entry exists in
 - `set-login` now sets the `Success` field based on the result of the `UpdateEntry` or `CreateEntry` command instead of always returning `true`
 - Changed plugin `UpdateUrl` to the `maddhatter/keepasshttp` repository

### Removed
 - Removed unused(?) `latest-version.txt` file in repo root
 
[Unreleased]: https://github.com/maddhatter/keepasshttp/compare/master...develop
[1.11.0.0]: https://github.com/maddhatter/keepasshttp/releases/tag/1.11.0.0
[1.10.0.0]: https://github.com/maddhatter/keepasshttp/releases/tag/1.10.0.0
[1.9.0.1]: https://github.com/maddhatter/keepasshttp/releases/tag/1.9.0.1

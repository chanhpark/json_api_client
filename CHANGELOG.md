
# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [2.0.0] 2018-01-03
### Fixed
- urls with explicit ports but no path are normalized so they don't [cause errors](https://github.com/edgurgel/httpoison/issues/300) in HTTPoison/hackney. 
### Removed
- Hard dependency on fuse and sasl erlang packages. Fuse is now declared as optional.
- JsonApiClient.Config.SASLLogs log translator in favor of direct configuration of sasl.

## [1.2.0] 2017-10-27
### Changed
- Middleware call `request` parameter type is changed to `Request`. 

### Added
- Added `Request.attributes`
- Added `DefaultRequestConfig` middleware
- Added `Request.new/0` method 

## [1.1.0] - 2017-10-25
### Changed
- Renamed client_name to user_agent_suffix
- use Mix.Project.config[:app] as a default value for user_agent_suffix
- Use "JsonApiClient" (package name) as user agent prefix instead of "ExApiClient".

### Added
- Added `Request.header/3` method
- Added middleware architecture
- Added `Fuse` and `StatsTracker` middlewares

### Fixed
- Path generation from a now works correctly for post requests when `resource` specified

## [1.0.0] - 2017-10-17
### Added
- `Request.path/2` added

## [0.5.2] - 2017-10-17
### Fixed
- Fixed package config so that primary documentation link in hex.pm works

## [0.5.1] - 2017-10-17
### Fixed
- Removed `organization` from mix.exs so that package will be public
- Removed Unused dependencies from mix.exs

## [0.5.0] - 2017-10-17
### Added
- This CHANGELOG.md
- A good bit of docuemtnation

### Removed
- The `RequestError` struct lost the `reson` attribute. We now just use `message`


[Unreleased]: https://github.com/decisiv/json_api_client/compare/0.5.1...HEAD
[1.0.0]: https://github.com/decisiv/json_api_client/compare/0.5.2...1.0.0
[0.5.2]: https://github.com/decisiv/json_api_client/compare/0.5.1...0.5.2
[0.5.1]: https://github.com/decisiv/json_api_client/compare/0.5.0...0.5.1
[0.5.0]: https://github.com/decisiv/json_api_client/compare/0.4.0...0.5.0

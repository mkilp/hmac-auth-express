# Changelog

All notable changes to this project will be documented in this file. See [standard-version](https://github.com/conventional-changelog/standard-version) for commit guidelines.

## [7.0.0](https://github.com/connorjburton/hmac-auth-express/compare/v6.0.1...v7.0.0) (2021-07-04)


### ⚠ BREAKING CHANGES

* addition of express peer dependency may fail installations of users using express <4

### Bug Fixes

* changes to package.json & e2e test ([4b17f33](https://github.com/connorjburton/hmac-auth-express/commit/4b17f33d4107a47453237781eeccb845347159d0))

## 6.0.1 - 2021-06-28
### Added
- Added Github Actions
### Removed
- Removed Travis integration
### Security
- Bumped `jest` from `26.3.0` to `27.0.6`

## 6.0.0 - 2020-08-12
### Changed
- **Breaking** Inversed `timeDiff` value in comparison against `minInterval` option so option parameters are consistent.

## 5.0.1 - 2020-08-12
### Changed
- Updated `parseInt` call to pass `radix` parameter of `10`
### Security
- Bumped `jest` from `26.2.2` to `26.3.0`

## 5.0.0 - 2020-08-01
### Added
- **Breaking** Support for plain arrays in the request body. Previously a plain array request body would be rejected, this change could potentially allow unexpected behaviour, thus the breaking change.
### Security
- Bumped `jest` from `24.9.0` to `26.2.2`

## 4.1.0 - 2020-03-20
### Added
- `options.minInterval` for out of sync times (requests from the future)
### Security
- Bumped `acorn` from `5.7.3` to `5.7.4`

## 4.0.2 - 2019-12-31
### Added
- Added Travis CI for running tests on pull requests
- Added automatic NPM publish on master push
### Changed
- Added Travis CI badge to readme

## 4.0.1 - 2019-11-13
### Changed
- Updated changelog to include correct date for 4.0.0

## 4.0.0 - 2019-11-13
### Added
- Tests, 100% coverage
- `.vscode/launch.json` that includes test configuration for easily debugging tests

### Changed
- **Breaking** The UNIX timestamp's used is now expected to be 13 characters long, not 10 (i.e already divided by `1000`). See [Migration Guide](https://github.com/connorjburton/hmac-auth-express/blob/master/MIGRATION_GUIDE.md#migrating-from-3xx-to-400)
- Improved validation for checking if the HMAC digest exists in the header
- Improved validation for checking if `request.body` is set

## 3.0.0 - 2019-01-02
### Changed
- **Breaking** Changed error handling to pass the error to express' error handler instead of sending a response internally. See [Migration Guide](https://github.com/connorjburton/hmac-auth-express/blob/master/MIGRATION_GUIDE.md#migrating-from-2xx-to-300)

## 2.0.3 - 2018-12-12
### Changed
- Uses `req.originalUrl` instead of `req.baseUrl`

## 2.0.2 - 2018-12-12
### Changed
- Updated changelog

## 2.0.1 - 2018-12-12
### Changed
- Changed readme to include details about timing safe

## 2.0.0 - 2018-12-12
### Security
- **Breaking** Added the supplied unix timestamp to the HMAC signature to ensure the timestamp provided is the timestamp in the HMAC digest

## 1.0.2 - 2018-12-12
### Changed
- Moved validation to it's own `validateArguments.js` file
- Added validaton for `options.maxInterval` and `options.error`
- Added comments to `index.js`
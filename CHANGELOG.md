# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.3.2] - 2022-08-17

### Added
- Tests to check if all mandatory entity properties are initialized

### Fixed
- Nullable properties in `Sport` entity: `strSportIconGreen`
- Nullable properties in `League` entity: `strDivision`, `idCup`, `strCurrentSeason`, `strGender`, `strCountry`, `strNaming`, `strLocked`
- Nullable properties in `Player` entity: `dateSign`

## [1.3.1] - 2022-06-03

### Updated
- Updated guzzlehttp/guzzle to 7.4.3 (security fix)

## [1.3.0] - 2022-05-20

### Added
- Added `Honour` entity, deprecated `Honor`
- Added `honours()` in `LookupEndpoint`, deprecated `honors()`

## [1.2.1] - 2022-05-13

### Fixed
- Fixed player honours endpoint by changing endpoint URL and accepting new JSON root element
- Fixed listing country leagues by accepting new JSON root element

## [1.2.0] - 2022-04-01

### Added
- Support for equipments lookup

## [1.1.2] - 2022-04-01

### Updated
- Updated indirect dependency guzzlehttp/psr7 to 2.2.1

## [1.1.1] - 2021-11-29

### Fixed
- Fixed nullable fields intFormedYear and strDescriptionEN in league entity

## [1.1.0] - 2021-11-26

### Added
- Support for PHP 8.1

## [1.0.7] - 2021-11-22

### Fixed
- Changed free users key from "1" to "2"

## [1.0.6] - 2021-11-16

### Fixed
- Made `strSport` property in `League` entity nullable

## [1.0.5] - 2021-06-28

### Changed
- Changed PHPStan level to 6 (fixed all parameters and return type hints)

### Fixed
- Made `strSportThumb` property in `Sport` entity nullable

## [1.0.4] - 2021-06-21

### Fixed
- Fixed nullable event properties referred to teams (`strHomeTeam`, `strAwayTeam`, `idHomeTeam`, `idAwayTeam`)

## [1.0.3] - 2021-06-09

### Deprecated
- Deprecated `NklKst\TheSportsDb\Entity\Table\Entry`, use `NklKst\TheSportsDb\Entity\Table\Standing` instead

### Fixed
- Fixed table entry properties to match API fields
- Always handle `null` as an empty result in API responses to prevent mapping errors

## [1.0.2] - 2021-05-30

### Added
- Weekly cron for GitHub workflow

### Fixed
- League serializer should handle `null` response if ID was not found
- Event serializer should handle `null` response if ID was not found
- Skip schedule tests at the beginning and ending of the season

## [1.0.1] - 2021-05-04

### Fixed
- Made several entity attributes nullable to prevent parse exceptions

## [1.0.0] - 2021-05-02

### Added
- Dev dependency php-coveralls/php-coveralls
- Coverage report badge
- Public API method documentation

### Changed
- Use Guzzle ClientInterface in DependencyContainer
- Changelog format to https://keepachangelog.com/en/1.0.0/
- Updated guzzlehttp/guzzle to 7.3.0
- Updated netresearch/jsonmapper to v4.0.0
- Updated symfony/dependency-injection to v5.2.6
- Updated friendsofphp/php-cs-fixer to v2.18.5
- Updated phpunit/phpunit to 9.5.4

### Fixed
- Don't reuse clients and endpoints in DependencyContainer
- `idAPIfootball` in class `NklKst\TheSportsDb\Entity\Team` is now nullable
- Fixed teams search returning `null` on unmatched query
- Lookup and search results for single entities can be null

### Removed
- API version configuration support

## [0.1.2] - 2021-01-23

### Added
- Highlight videos support
- Livescore v2 support

## [0.1.1] - 2021-01-18

### Added
- Most "Patreon only" features
  
### Changed
- Bumped libs

## [0.1.0] - 2020-12-30
- Initial release

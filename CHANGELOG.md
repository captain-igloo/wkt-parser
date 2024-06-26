# Change Log
All notable changes to this project will be documented in this file using the [Keep a CHANGELOG](http://keepachangelog.com/) principles.
This project adheres to [Semantic Versioning](http://semver.org/).

## [Unreleased]
### Added
- Docker added (to help contributors)
- Test for PHP version 8.3
### Changed
- Doctrine Lexer 2.1 support fixed
- GitHub checkout action upgraded 
### Removed
- PHP 8.0 support
- PHP 7.* support
- PHP 5.4 support
- PHP 4.5 support

## LongitudeOne [1.0.0] - 2023-06-04
### Added
- Allows doctrine/lexer@^2.1 by @axi in #1
- Add GitHub Actions by @axi in #2
- Change name space from CrEOF LongitudeOne by @ellisgl in #3
- 8.1 support by @ellisgl in #4
### Fork
- Forked from CreOf [2.2.0]

## CreOf [2.2.0] - 2016-05-03
### Added
- Tests namespace to PSR-0 autoload in composer.json.
- Support for 3DZ, 3DM, 4DZM objects added. Dimension(s) now in 'dimension' key of returned array.

### Changed
- Token pattern regex changed to capture numbers in scientific notation as a single value.
- Let PHP handle scientific number conversion to float instead of manually calculating.
- Only instantiate Lexer object in Parser constructor if it doesn't exist.
- Move function return value tests from switch statements in Lexer. Switch statement now doing only string comparison.
- Remove static visibility from Lexer instance in Parser.
- PHPUnit now bootstraps Composer autoload.
- Update PHPUnit config XML to be compliant with XSD.
- Documentation updated for 3DZ, 3DM, 4DZM support.

### Removed
- Removed E token used with scientific notation from Lexer.
- Removed now unused TestInit.

## CreOf [2.1.0] - 2016-04-09
### Added
- Add tokens for 3DM, 3DZ, and 4D coordinates to Lexer.
- Method Lexer::value() to get current token value.
- Match Z, M, or ZM tokens in Parser (not currently used).
- Add test for Parser reuse.
- Add test for Lexer reuse.

### Changed
- Regex used to catch tokens.
- Allow Lexer instantiation with no parameters so object can be reused.
- Allow Parser instantiation with no parameters so object can be reused.
- Changed visibility of Parser::$type.
- Use Lexer::value() in Parser.
- Set srid to null before parsing value.
- Consolidated all Parser test data into ParserTest.
- Update usage documentation in README.md.

## CreOf [2.0.0] - 2015-11-18
### Added
- Change base namespace to CrEOF\Geo\WKT to avoid class collision with other CrEOF packages.

## CreOf [1.0.0] - 2015-11-11
### Added
- Initial release.

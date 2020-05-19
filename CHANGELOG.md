# Change Log

All notable changes to this project will be documented in this file.
See [Conventional Commits](https://conventionalcommits.org) for commit guidelines.

# [4.2.0](https://github.com/C2FO/fast-csv/compare/v4.1.6...v4.2.0) (2020-05-19)


### Bug Fixes

* **deps:** update dependency @docusaurus/preset-classic to v2.0.0-alpha.54 ([f1fcc46](https://github.com/C2FO/fast-csv/commit/f1fcc4677e9081c0d10bcaaeef7719ca572e306c))
* **deps:** update dependency @types/yargs to v15 ([44bcccc](https://github.com/C2FO/fast-csv/commit/44bccccf5f0c57a97fa06f592923173b119429b7))
* **deps:** update react monorepo to v16.13.1 ([cdb0d89](https://github.com/C2FO/fast-csv/commit/cdb0d89ec6400dbe03590c147d4b6a7f275d944c))


### Features

* **parsing:** Less restrictive row parsing type [#356](https://github.com/C2FO/fast-csv/issues/356) ([87d74ec](https://github.com/C2FO/fast-csv/commit/87d74ecd2cb16f3700b1942ebbbec221afe38790))





## [4.1.6](https://github.com/C2FO/fast-csv/compare/v4.1.5...v4.1.6) (2020-05-15)


### Bug Fixes

* **deps:** update dependency @docusaurus/core to v2.0.0-alpha.54 ([24a0473](https://github.com/C2FO/fast-csv/commit/24a04730e4f6d981f8e69227bf67c1f07b9352c3))
* **parse:** Handle escaped escape properly [#340](https://github.com/C2FO/fast-csv/issues/340) ([78d9b16](https://github.com/C2FO/fast-csv/commit/78d9b160152ee399f31086cc6b5f66a7ca7f9e24))





## [4.1.5](https://github.com/C2FO/fast-csv/compare/v4.1.4...v4.1.5) (2020-05-15)


### Bug Fixes

* Fix for [#345](https://github.com/C2FO/fast-csv/issues/345) remove revert to old tsconfig.build ([aa4488f](https://github.com/C2FO/fast-csv/commit/aa4488f719ffe24a9bed3fb3e0b24efb5fdc7627))





## [4.1.4](https://github.com/C2FO/fast-csv/compare/v4.1.3...v4.1.4) (2020-05-15)


### Bug Fixes

* Fix lerna:version command ([6da1eb3](https://github.com/C2FO/fast-csv/commit/6da1eb30bb15fc57d3afcca2d6b9e115d26d0191))





## v4.1.2

* New Docs powered by Docusaurus!
* New logo courtesy of [@dylanstanfield](https://github.com/dylanstanfield)

## v4.1.1

* [FIXED] Issue where code is not built before publishing. [#329](https://github.com/C2FO/fast-csv/issues/329)

## v4.1.0

* [ADDED] A new `headers` event that will be emitted when headers are parsed [#321] (https://github.com/C2FO/fast-csv/issues/321)

## v4.0.3

* [FIXED] Issue where invalid rows were not accounted for when skipRows was set [#317](https://github.com/C2FO/fast-csv/issues/317)
* [FIXED] Issue where readableObjectMode was not set to false when formatting [#319](https://github.com/C2FO/fast-csv/issues/319)
* [FIXED] Issue where carriage returns and line feeds were not always quoted when formatting [#320](https://github.com/C2FO/fast-csv/issues/320)

## v4.0.2

* [ADDED] `writeHeaders` to `@fast-csv/format` option to prevent writing headers.
    * This makes appending to a csv easier and safer because you can still specify headers without writing them.

## v4.0.1

* [FIXED] package.json homepage links
* [ADDED] version npm script

## v4.0.0

* Migrated from mocha to jest
* Moved to `lerna`.
    * Split `parse` and `format` packages
* Added running examples and checking output as part of the tests
* Updated docs for new directory layout
* Added typescript examples
* Added generics type support to format and parse streams
* [ADDED] Docs around using `strictColumnHandling` to emit errors when there are more columns than headers [#195]

## v3.7.0

* [ADDED] Ability to Transform Header [#287](https://github.com/C2FO/fast-csv/issues/287)
* [ADDED] Example require and import to README [#301](https://github.com/C2FO/fast-csv/issues/301)
* [ADDED] Added new formatting option `alwaysWriteHeaders` to always write headers even if no rows are provided [#300](https://github.com/C2FO/fast-csv/issues/300)
* [ADDED] Appending to csv example and docs [#272](https://github.com/C2FO/fast-csv/issues/300)
* [FIXED] Issue with duplicate headers causing dataloss, duplicate headers will can an error to be emitted. [#276](https://github.com/C2FO/fast-csv/issues/272)
* [FIXED] Issue where an error thrown while processing rows causes stream continue to parse, causing duplicate writes or swallowed exceptions.


## v3.6.0

* [ADDED] `maxRows` option to limit the number of rows parsed. [#275](https://github.com/C2FO/fast-csv/issues/275) [#277](https://github.com/C2FO/fast-csv/pull/277) - [@cbrittingham](https://github.com/cbrittingham)
* [ADDED] `skipRows` to allow skipping parsed rows see [parsing.md](./docs/parsing.md)
* [ADDED] `skipLines` to allow skipping entire lines of a csv [parsing.md](./docs/parsing.md) [#267](https://github.com/C2FO/fast-csv/issues/267)
* Exported formatting and parsing types.
* Removed `.npmignore` in favor of `package.json` files

## v3.5.0

* Upgraded dependencies
* Reformatted code with prettier
* [FIXED] Entire lodash is imported, bloating dependencies [#281](https://github.com/C2FO/fast-csv/issues/281)

## v3.4.0

* [FIXED] formatter.js: Disabling quote doesn't work [#97](https://github.com/C2FO/fast-csv/issues/97)
    * Changed to allow the `quote` option to be provided as a boolean so when set to false all quoting is ignored.
* [ADDED] `writeBOM` option when formatting a csv [#180](https://github.com/C2FO/fast-csv/issues/180)    
* Added tests for [#102](https://github.com/C2FO/fast-csv/issues/102)


## v3.3.0

* [FIXED] First row of CSV is removed when headers array is provided [#252](https://github.com/C2FO/fast-csv/issues/252)

## v3.2.0

* [FIXED] Invalid row index doesn't reflect original row count [#130](https://github.com/C2FO/fast-csv/issues/130) [#266](https://github.com/C2FO/fast-csv/pull/266) - [@chrwnsk](https://github.com/chrwnsk) 

## v3.1.0

* Skip trailing whitespace after a quoted field [#223](https://github.com/C2FO/fast-csv/pull/223) - [@peet](https://github.com/peet)
* Add support for passing in encoding. [#185](https://github.com/C2FO/fast-csv/pull/185) - [@pierrelouisd4j](https://github.com/pierrelouisd4j)

## v3.0.2

* Update lodash to address [#260](https://github.com/C2FO/fast-csv/pull/260)

## v3.0.1

* Update `.npmignore` to not exclude build directory

## v3.0.0

* Updated to Node 8
* Rewrote in Typescript

## Parsing Changes
* Calling the library as a function has been removed in favor of `csv.parse`.
  * `csv()` change to `csv.parse()`
* Deprecated `fromString` in favor of `parseString`
  * `csv.fromString()` change to `csv.parseString()`
* Deprecated `fromStream` in favor of `parseStream`a
    * `csv.fromStream()` change to `csv.parseStream()`
* Deprecated`fromPath` in favor of `parseFile`
    * `csv.fromPath()` change to `csv.parseFile()`

## Formatting Changes
  * `csv.createWriteStream` has been removed in favor of `csv.format`
  * `csv.writeToBuffer` and `csv.writeToString` no longer accepts a `callback`, instead they return a promise `Promise`


## v2.5.0

* Use safer-buffer polyfill to support node >= 8.

## v2.4.1

* Adding TypeScript declaration file. [#190](https://github.com/C2FO/fast-csv/pull/190)

## v2.4.0

* Allow renaming headers. [#175](https://github.com/C2FO/fast-csv/pull/175)

## v2.3.1

* Now removes the byte order mark from a UTF-8 file if this is present. [#170](https://github.com/C2FO/fast-csv/pull/170)

## v2.3.0

* Writing object ends up with function definitions [#158](https://github.com/C2FO/fast-csv/pull/158)

## v2.2.0

* Handle split CRLF [#156](https://github.com/C2FO/fast-csv/pull/156) - [@alexeits](https://github.com/alexeits)

## v2.1.0

* Now handles tab delimited CSVs with only spaces for field values
* Handles CSVs with only spaces for field values

## v2.0.1

* Fix for last column empty when line end with a delimiter.

## v2.0.0

* Fast CSV will now handles the last column being empty.

## v1.1.0

* Fix for when chunk returned by transform to the parser ends with a space
* Functionality to give a reason when invalid data
* Fix problem with utf8 encoded streams that have multi-byte characters
* Allow passing sparse array of headers

## v1.0.0

* Node 4 and 5 support.
* Deprecating the `record` event.

## v0.6.0

* Removed try catch from emit to allow bubbling up of errors to process, if one is thrown [#93](https://github.com/C2FO/fast-csv/issues/93)
    * This also fixed issue [#92](https://github.com/C2FO/fast-csv/issues/92) where a loop was entered when `this.emit("error")` was called.
* Added new tests

## v0.5.7

* Strict record handling [#53](https://github.com/C2FO/fast-csv/pull/53) - [@derjust](https://github.com/derjust)

## v0.5.6

* Fixed issue where parser_stream was emitting end early [#87](https://github.com/C2FO/fast-csv/issues/87)
  * Changed to not emit end during flush
  * Changed catch errors on emit and emit as "error" event
* Added support for node `v0.12`

## v0.5.5
* Fixed issues with ordering of headers when specifying headers in a write stream [#77](https://github.com/C2FO/fast-csv/pull/77)
* Fixed issue where headers were not being written if no data was supplied to write stream.

## v0.5.4

* Fixed issues with error handling and not registering an error handler on stream [#68](https://github.com/C2FO/fast-csv/issues/68)
* Added support for ignoring quoting while parsing [#75](https://github.com/C2FO/fast-csv/issues/75)

## v0.5.3

* Fixed issues with `v0.11` stream implementation [#73](https://github.com/C2FO/fast-csv/issues/73)
* Fixed issues with `pause/resume` and data events in `v0.10` [#69](https://github.com/C2FO/fast-csv/issues/69)
* Fixed the double invoking of done callback when parsing files [#68](https://github.com/C2FO/fast-csv/issues/68)
* Refactored tests

## v0.5.2

* Fixed issue with `writeToString` and `writeToPath` examples [#64](https://github.com/C2FO/fast-csv/issues/64)
* Fixed issue with creating a csv without headers [#63](https://github.com/C2FO/fast-csv/issues/63)

## v0.5.1

* Fixed issue where line data was not being passed between transforms in the parser_stream

## v0.5.0

* Added support for async transforms [#24](https://github.com/C2FO/fast-csv/issues/24)
* Added support for async validation
* Added support for new data format
```
[
    [["header", "value1"], ["header2", "value2"]],
    [["header", "value2"], ["header2", "value2"]]
]
```
* Added support for forcing the quoting columns and headers
   * `quoteColumns` - Can be a boolean, object or array to specify how quoting should be done (see README)
   * `quoteHeaders` - Can be a boolean, object or array to specify how quoting should be done (see README)
* More tests
* Code refactor and clean up

## v0.4.4

* Added support for comments. [#56](https://github.com/C2FO/fast-csv/issues/56)

## v0.4.3

* Added ability to include a `rowDelimiter` at the end of a csv with the `includeEndRowDelimiter` option [#54](https://github.com/C2FO/fast-csv/issues/54)
* Added escaping for values that include a row delimiter
* Added more tests for new feature and escaping row delimiter values.

## v0.4.2

* Added ability to specify a rowDelimiter when creating a csv.
* Added discardUnmappedColumns option to allow the ignoring of extra data [#45](https://github.com/C2FO/fast-csv/pull/45)

## v0.4.1

* Fixed race condition that occurred if you called pause during a flush.

## v0.4.0

* Fixed misspelling of `delimiter` [#40](https://github.com/C2FO/fast-csv/issues/40)

## v0.3.1

* Added transform support to formatters
   * When using `createWriteStream` you can now you the `transform` method to specify a row transformer.
   * When using other transform methods you can specify a `transform` option.

## v0.3.0

* You can now specify `objectMode` when parsing a csv which will cause `data` events to have an object emitted.
* You can now pipe directly to the stream returned from `createWriteStream`
* You can now transform csvs by piping output from parsing into a formatter.

## v0.2.5

* Fixed issue where not all rows are emitted when using `pause` and `resume`

## v0.2.4

* Added more fine grained control to `.pause` and `.resume`
   * You can now pause resume between chunks

## v0.2.3

* Add new `createWriteStream` for creating a streaming csv writer

## v0.2.2

* Fixed issue with having line breaks containing `\r\n`

## v0.2.1

* Fixed issue with `\r` line break in parser

## v0.2.0

* Added multiline value support
* Updated escaping logic
* More performance enhancements
* More robusts test cases
* Removed support for having two quote types instead it just supports a single quote and escape sequence.
 Source code (zip)

## v0.1.2

* Fixed issue with formatter handling undefined or null values.
* Changed formatter not not include a new line at the end of a CSV.
* Added pause and resume functionality to ParserStream

## v0.1.1

* Added trim, ltrim, and rtrim to parsing options

## v0.1.0
@steampunk/sfdx-steampunk
=========================

Steampunk&#39;s SFDX Plugin

[![Version](https://img.shields.io/npm/v/@steampunk/sfdx-steampunk.svg)](https://www.npmjs.com/package/@steampunk/sfdx-steampunk)
[![Known Vulnerabilities](https://snyk.io/test/github/steampunkfoundry/sfdx-steampunk/badge.svg)](https://snyk.io/test/github/steampunkfoundry/sfdx-steampunk)
[![Downloads/week](https://img.shields.io/npm/dw/@steampunk/sfdx-steampunk.svg)](https://www.npmjs.com/package/@steampunk/sfdx-steampunk)
[![License](https://img.shields.io/npm/l/@steampunk/sfdx-steampunk.svg)](https://www.npmjs.com/package/@steampunk/sfdx-steampunk)

<!-- toc -->

<!-- tocstop -->

<!-- tocstop -->
<!-- install -->
<!-- usage -->
```sh-session
$ npm install -g @steampunk/sfdx-steampunk
$ sfdx COMMAND
running command...
$ sfdx (-v|--version|version)
@steampunk/sfdx-steampunk/0.1.2 win32-x64 node-v16.7.0
$ sfdx --help [COMMAND]
USAGE
  $ sfdx COMMAND
...
```
<!-- usagestop -->
```sh-session
$ npm install -g @steampunk/sfdx-steampunk
$ sfdx COMMAND
running command...
$ sfdx (-v|--version|version)
@steampunk/sfdx-steampunk/0.1.1 win32-x64 node-v16.7.0
$ sfdx --help [COMMAND]
USAGE
  $ sfdx COMMAND
...
```
<!-- usagestop -->
<!-- commands -->
* [`sfdx punk:data:files:upload -f <filepath> [-u <string>] [--apiversion <string>] [--json] [--loglevel trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL]`](#sfdx-punkdatafilesupload--f-filepath--u-string---apiversion-string---json---loglevel-tracedebuginfowarnerrorfataltracedebuginfowarnerrorfatal)

## `sfdx punk:data:files:upload -f <filepath> [-u <string>] [--apiversion <string>] [--json] [--loglevel trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL]`

Upload multiple files based on a csv

```
USAGE
  $ sfdx punk:data:files:upload -f <filepath> [-u <string>] [--apiversion <string>] [--json] [--loglevel 
  trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL]

OPTIONS
  -f, --filepath=filepath                                                           (required) Path to csv file

  -u, --targetusername=targetusername                                               username or alias for the target
                                                                                    org; overrides default target org

  --apiversion=apiversion                                                           override the api version used for
                                                                                    api requests made by this command

  --json                                                                            format output as json

  --loglevel=(trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL)  [default: warn] logging level for
                                                                                    this command invocation

EXAMPLE

     $ sfdx punk:data:files:upload -f ~/FilesToUpload.csv

     You will need to format a csv with the following headers.

     Required:
       - PathOnClient
       - Title

     Optional:
       - FirstPublishLocationId
```

_See code: [@steampunk/sfdx-steampunk-data](https://github.com/SteampunkFoundry/steampunk-sfdx-data/blob/v0.1.2/src/commands/punk/data/files/upload.ts)_
<!-- commandsstop -->

<!-- commandsstop -->

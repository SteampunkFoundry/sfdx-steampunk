@steampunk/sfdx-steampunk
=========================

Steampunk&#39;s SFDX Plugin

[![Version](https://img.shields.io/npm/v/@steampunk/sfdx-steampunk.svg)](https://www.npmjs.com/package/@steampunk/sfdx-steampunk)
[![Known Vulnerabilities](https://snyk.io/test/github/steampunkfoundry/sfdx-steampunk/badge.svg)](https://snyk.io/test/github/steampunkfoundry/sfdx-steampunk)
[![Downloads/week](https://img.shields.io/npm/dw/@steampunk/sfdx-steampunk.svg)](https://www.npmjs.com/package/@steampunk/sfdx-steampunk)
[![License](https://img.shields.io/npm/l/@steampunk/sfdx-steampunk.svg)](https://www.npmjs.com/package/@steampunk/sfdx-steampunk)

<!-- toc -->

<!-- tocstop -->
<!-- install -->
<!-- usage -->
```sh-session
$ npm install -g @steampunk/sfdx-steampunk
$ sfdx COMMAND
running command...
$ sfdx (-v|--version|version)
@steampunk/sfdx-steampunk/0.2.0 win32-x64 node-v16.15.1
$ sfdx --help [COMMAND]
USAGE
  $ sfdx COMMAND
...
```
<!-- usagestop -->
<!-- commands -->
* [`sfdx punk:data:files:upload -f <filepath> [-u <string>] [--apiversion <string>] [--json] [--loglevel trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL]`](#sfdx-punkdatafilesupload--f-filepath--u-string---apiversion-string---json---loglevel-tracedebuginfowarnerrorfataltracedebuginfowarnerrorfatal)
* [`sfdx punk:org:pool:create -p <array> -f <filepath> [-n] [-c] [-s] [-a <string>] [-w <minutes>] [-d <integer>] [--json] [--loglevel trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL]`](#sfdx-punkorgpoolcreate--p-array--f-filepath--n--c--s--a-string--w-minutes--d-integer---json---loglevel-tracedebuginfowarnerrorfataltracedebuginfowarnerrorfatal)

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

_See code: [@steampunk/sfdx-steampunk-data](https://github.com/SteampunkFoundry/sfdx-steampunk-data/blob/v0.2.1/src/commands/punk/data/files/upload.ts)_

## `sfdx punk:org:pool:create -p <array> -f <filepath> [-n] [-c] [-s] [-a <string>] [-w <minutes>] [-d <integer>] [--json] [--loglevel trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL]`

Create a scratch org provided a pool of devhubs

```
USAGE
  $ sfdx punk:org:pool:create -p <array> -f <filepath> [-n] [-c] [-s] [-a <string>] [-w <minutes>] [-d <integer>] 
  [--json] [--loglevel trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL]

OPTIONS
  -a, --setalias=setalias                                                           alias for the created org

  -c, --noancestors                                                                 do not include second-generation
                                                                                    package ancestors in the scratch org

  -d, --durationdays=durationdays                                                   duration of the scratch org (in
                                                                                    days) (default:7, min:1, max:30)

  -f, --definitionfile=definitionfile                                               (required) path to an org definition
                                                                                    file

  -n, --nonamespace                                                                 create the scratch org with no
                                                                                    namespace

  -p, --devhubusernames=devhubusernames                                             (required) list of devhub usernames
                                                                                    to pool from

  -s, --setdefaultusername                                                          set the created org as the default
                                                                                    username

  -w, --wait=wait                                                                   [default: [object Object]] the
                                                                                    streaming client socket timeout (in
                                                                                    minutes)

  --json                                                                            format output as json

  --loglevel=(trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL)  [default: warn] logging level for
                                                                                    this command invocation

EXAMPLES
  $ sfdx punk:org:pool:create -p "MyDevHub1,MyDevHub2,MyDevHub3" -f config/project-scratch-def.json
  $ sfdx punk:org:pool:create -p "MyDevHub1,MyDevHub2,MyDevHub3" -f config/project-scratch-def.json --setalias 
  MyScratchOrg --setdefaultusername
```

_See code: [@steampunk/sfdx-steampunk-org](https://github.com/SteampunkFoundry/sfdx-steampunk-org/blob/v0.1.1/src/commands/punk/org/pool/create.ts)_
<!-- commandsstop -->

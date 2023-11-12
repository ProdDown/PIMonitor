oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![GitHub license](https://img.shields.io/github/license/oclif/hello-world)](https://github.com/oclif/hello-world/blob/main/LICENSE)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g prod-down
$ prod-down COMMAND
running command...
$ prod-down (--version)
prod-down/0.0.0 darwin-arm64 node-v18.17.0
$ prod-down --help [COMMAND]
USAGE
  $ prod-down COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`prod-down hello PERSON`](#prod-down-hello-person)
* [`prod-down hello world`](#prod-down-hello-world)
* [`prod-down help [COMMANDS]`](#prod-down-help-commands)
* [`prod-down plugins`](#prod-down-plugins)
* [`prod-down plugins:install PLUGIN...`](#prod-down-pluginsinstall-plugin)
* [`prod-down plugins:inspect PLUGIN...`](#prod-down-pluginsinspect-plugin)
* [`prod-down plugins:install PLUGIN...`](#prod-down-pluginsinstall-plugin-1)
* [`prod-down plugins:link PLUGIN`](#prod-down-pluginslink-plugin)
* [`prod-down plugins:uninstall PLUGIN...`](#prod-down-pluginsuninstall-plugin)
* [`prod-down plugins:uninstall PLUGIN...`](#prod-down-pluginsuninstall-plugin-1)
* [`prod-down plugins:uninstall PLUGIN...`](#prod-down-pluginsuninstall-plugin-2)
* [`prod-down plugins update`](#prod-down-plugins-update)

## `prod-down hello PERSON`

Say hello

```
USAGE
  $ prod-down hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [src/commands/hello/index.ts](https://github.com/Cliftonz/prod-down/https://github.com/Cliftonz/prod-down/blob/v0.0.0/src/commands/hello/index.ts)_

## `prod-down hello world`

Say hello world

```
USAGE
  $ prod-down hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ prod-down hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/Cliftonz/prod-down/https://github.com/Cliftonz/prod-down/blob/v0.0.0/src/commands/hello/world.ts)_

## `prod-down help [COMMANDS]`

Display help for prod-down.

```
USAGE
  $ prod-down help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for prod-down.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.2.20/src/commands/help.ts)_

## `prod-down plugins`

List installed plugins.

```
USAGE
  $ prod-down plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ prod-down plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.0.2/src/commands/plugins/index.ts)_

## `prod-down plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ prod-down plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -s, --silent   Silences yarn output.
  -v, --verbose  Show verbose yarn output.

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ prod-down plugins add

EXAMPLES
  $ prod-down plugins:install myplugin 

  $ prod-down plugins:install https://github.com/someuser/someplugin

  $ prod-down plugins:install someuser/someplugin
```

## `prod-down plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ prod-down plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ prod-down plugins:inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.0.2/src/commands/plugins/inspect.ts)_

## `prod-down plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ prod-down plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -s, --silent   Silences yarn output.
  -v, --verbose  Show verbose yarn output.

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ prod-down plugins add

EXAMPLES
  $ prod-down plugins:install myplugin 

  $ prod-down plugins:install https://github.com/someuser/someplugin

  $ prod-down plugins:install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.0.2/src/commands/plugins/install.ts)_

## `prod-down plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ prod-down plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help      Show CLI help.
  -v, --verbose
  --[no-]install  Install dependencies after linking the plugin.

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ prod-down plugins:link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.0.2/src/commands/plugins/link.ts)_

## `prod-down plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ prod-down plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ prod-down plugins unlink
  $ prod-down plugins remove
```

## `prod-down plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ prod-down plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ prod-down plugins unlink
  $ prod-down plugins remove
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.0.2/src/commands/plugins/uninstall.ts)_

## `prod-down plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ prod-down plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ prod-down plugins unlink
  $ prod-down plugins remove
```

## `prod-down plugins update`

Update installed plugins.

```
USAGE
  $ prod-down plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.0.2/src/commands/plugins/update.ts)_
<!-- commandsstop -->

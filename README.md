# SBX-BB-TEMPLATES
A [Docker Sandbox](https://docs.docker.com/ai/sandboxes/) [Kit](https://docs.docker.com/ai/sandboxes/customize/kits/) that installs some useful python modules along with the [generate-breedbase-templates Claude plugin](https://github.com/TriticeaeToolbox/generate-breedbase-templates-plugin) that can be used to transform breeder-provided data into standardized breedbase upload templates.

## Use Cases

The main use-case for this sandbox kit is to easily create a new Claude sandbox in a project directory that contains a specific set of breeder data to convert into breedbase upload templates using the Claude Code CLI.

## Requirements

You must already have Docker Sandboxes and the `sbx` command installed - See the [Getting Started](https://docs.docker.com/ai/sandboxes/get-started/) page for installation instructions.

You'll need a Docker account to use `sbx`.  You must first login to Docker with the `sbx login` command.

## Installation

You can clone this kit to your machine:

```
git clone https://github.com/TriticeaeToolbox/sbx-bb-templates /path/to/sbx-bb-templates
```

You can use the `sbx-bb-templates` helper script to start new sandboxes.  It may be helpful to link the helper script to a directory in your `$PATH`:

```
ln -s /path/to/sbx-bb-templates/sbx-bb-templates /usr/local/bin/sbx-bb-templates
```

## Usage

### Starting Claude Code

The `sbx-bb-templates` helper script can be used to create a new sandbox and start a Claude Code session with the [generate-breedbase-templates Claude plugin](https://github.com/TriticeaeToolbox/generate-breedbase-templates-plugin) already installed.

To start a sandbox and a Claude Code CLI session in the current working directory:

```
sbx-bb-templates
```

To start a sandbox and a Claude Code CLI session in a different project directory:

```
sbx-bb-templates /path/to/project
```

This will start a Claude Code CLI session that has access to the files in the project directory.  Briefly describe the data and use the `/generate-breedbase-templates` skill to start the workflow.

### Manually Using the Kit

To manually use the kit (without using the helper script), either:
- append the `--kit /path/to/sbx-bb-templates` argument to your `sbx run` command when creating a new sandbox
- add the kit to an existing sandbox with `sbx kit add my-sandbox /path/to/sbx-bb-templates`
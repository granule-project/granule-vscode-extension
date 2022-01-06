# granule-vscode-extension

## Commands

- `Ctrl-e Ctrl-e`: attempts to synthesis a goal at the cursor (main operation)
- `Ctrl-e Ctrl-r`: attempts to rewrite all non-empty holes in the file, by
  case-splitting on the variables they contain
- `Ctrl-e Ctrl-h`: attempts to rewrite the non-empty hole under the cursor (if
  there is one)
- `Ctrl-e Ctrl-u`: converts ASCII characters to their Unicode equivalents
- `Ctrl-e Ctrl-a`: converts Unicode characters to their ASCII equivalents

These commands will automatically save any unsaved changes before running, they are also compatible with the standard undo functionality.

## Granule language server integration

The Granule language server allows for information from the Granule compiler to be accessed and worked with 'live', during development. It implements (a subset of!) the [Language Server Protocol](https://microsoft.github.io/language-server-protocol).

Currently, the following features are implemented:
* Live error feedback and highlighting from the lexer, parser and typechecker
* Search for symbols (definitions, types, constructors) in the current/imported modules by name
* Jump to function definitions and data type declarations in the current/imported modules
* More to come!

## Automatic installation

Install via the VSCode Extension Marketplace.

## Manual installation from GitHub

### How to compile

There are several steps to compiling the code:

1. Install [`yarn`](https://classic.yarnpkg.com/lang/en/), which handles build dependencies and execution.
2. Run `yarn install`, to fetch the build dependencies.
3. *Optional*: Make any changes to the code.
4. Run `yarn compile` to compile and package the Typescript.

After following these steps, the newly compiled code can be tested by opening the root directory in VS Code, then going to *Run > Start Debugging* in the menu bar. This will open a new window with the extension activated.

### How to install

After following the above steps to compile the code, you can produce a packaged `.vsix` file containing the extension using `yarn package`. This can then be installed locally with the following command:

```bash
code --install-extension ./granule-0.1.0.vsix
```

Alternatively, run the `package` command, then add the `.vsix` file to VS Code
by going to *Extensions*, clicking *...* in the top-right, then *Install from
VSIX...*.
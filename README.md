# granule-vscode-extension

## Commands

- `Ctrl-g Ctrl-r`: attempts to rewrite all non-empty holes in the hole, by
  case-splitting on the variables they contain
- `Ctrl-g Ctrl-h`: attempts to rewrite the non-empty hole under the cursor (if
  there is one)
- `Ctrl-g Ctrl-u`: converts ASCII characters to their Unicode equivalents
- `Ctrl-g Ctrl-a`: converts Unicode characters to their ASCII equivalents

These commands will automatically save any unsaved changes before running, they are also compatible with the standard undo functionality.

## How to install

```bash
yarn install
yarn package
code --install-extension ./granule-0.0.1.vsix
```

> Requires [`yarn`](https://classic.yarnpkg.com/lang/en/) and [VSCode](https://code.visualstudio.com/) to be installed

Alternatively, run the first two commands, then add the `.vsix` file to VSCode
by going to *Extensions*, clicking *...* in the top-right, then *Install from
VSIX...*.

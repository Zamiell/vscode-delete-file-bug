# vscode-delete-file-bug

This repository showcases a bug with the `typescript.tsserver.experimental.enableProjectDiagnostics` setting inside of VSCode.

Steps to reproduce:

```sh
git clone git@github.com:Zamiell/vscode-delete-file-bug.git
code vscode-delete-file-bug
```

Once VSCode is open, on the left hand explorer pane, left click on "src" to expand the directory. Then, right click on "main.ts" and click on "Delete". Afterwards, a spurious/erroneous error message will occur in the "Problems" pane:

```
File 'c:/Repositories/vscode-delete-file-bug/src/main.ts' not found.
  The file is in the program because:
    Matched by include pattern './src/**/*.ts' in 'd:/Repositories/test-3/tsconfig.json'
```

The only way to make this error disappear is to reload the VSCode widow.

(This happens any time a ".ts" file is deleted, not just if the last file and/or the "main.ts" is deleted.)

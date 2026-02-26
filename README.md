# Glutinum.VSCode

## Usage

```fsharp
open Glutinum.VSCode
open type Glutinum.VSCode.Exports

// Most of the API are available behind `vscode.XXX`

vscode.window.showErrorMessage ("Error when printing diagnostic report.")
|> ignore

// Some of them could be hidden behind `vscode_.XXX`
promise {
    let newFile = vscode_.Uri.parse ("untitled:" + path)
    return! vscode.workspace.openTextDocument (newFile)
}
```

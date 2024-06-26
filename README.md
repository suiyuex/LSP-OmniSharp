# LSP-OmniSharp

This is a helper package that automatically installs and updates
[OmniSharp](https://github.com/OmniSharp/omnisharp-roslyn) for you.

To use this package, you must have:

- The [LSP](https://packagecontrol.io/packages/LSP) package.
- The [.NET SDK](https://dotnet.microsoft.com/download). (The "Core" version **does not work on macOS**.)
- (Optional but recommended) Install the [LSP-file-watcher-chokidar](https://github.com/sublimelsp/LSP-file-watcher-chokidar) via Package Control to enable functionality to notify the server about new files.

**Install**

Linux

```bash
git clone git@github.com:suiyuex/LSP-OmniSharp.git ~/.config/sublime-text/Packages/
```


## Applicable Selectors

This language server operates on views with the `source.cs` base scope.

## Installation Location

The server is installed in the $CACHE/Package Storage/LSP-OmniSharp directory, where $DATA is the base cache path of Sublime Text.
For instance, $CACHE is `~/.cache/sublime-text` on a Linux system. If you want to force a re-installation of the server,
you can delete the entire $CACHE/Package Storage/LSP-OmniSharp directory.

Like any helper package, installation starts when you open a view that is suitable for this language server. In this
case, that means that when you open a view with the `source.cs` base scope, installation commences.

Notice: On platforms other than Windows, `dotnet >= 6` needs to be installed

## Configuration

### By LSP Settings

Configure OmniSharp by running `Preferences: LSP-OmniSharp Settings` from the Command Palette.

### Project Specific

Create `omnisharp.json` in your project root. [reference link](https://github.com/OmniSharp/omnisharp-roslyn/wiki/Configuration-Options)

## Capabilities

OmniSharp can do a lot of cool things, like

- code completion
- signature help
- hover info
- some quality code actions
- formatting
- find references
- goto def

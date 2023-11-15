# XDE

XDE (eXtensible Development Environment) is a highly-configurable environment, that can be anything from a minimal
text editor or image viewer to a full-featured IDE.

## Design

- XDE is a distributed network of stateful plugins communicating with events.
- Visual representation and logic are decoupled and implemented via plugins.
- No plugins are required. Application start as a loader for enabled plugins that do all the work. 
- Plugin can be a standalone application communicating over [JSON RPC] or a Lua module using XDE API.
- Plugin can be loaded, configured and unloaded in runtime.
- Plugins' lifecycle is defined with events.
- Plugin has a list of dependencies. Some dependencies can be optional.
- Plugin expose its interface for configuration and communication with other plugins. 

## Features

| Feature                            | Plugins                       |
| ---------------------------------- | ----------------------------- |
| Multi file editing                 | `buffer`, `edit`, `undo`, ... |
| Mouse support                      | `mouse`                       |
| File manager                       | `fs`                          |
| Window manager                     | `wm`                          |
| Terminal                           | `term`                        |
| Syntax highlighting                | `syn`, `hl`                   |
| Completion                         | `cmp`                         |
| LSP                                | `lsp`                         |
| Plugin manager                     | `plugin`                      |


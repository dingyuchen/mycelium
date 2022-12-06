
Dendron tasks are their own notes.

I have tried using markdown checkboxes, but it does not integrate well with Markdown-all-in-one, in that `Alt-X` does not check the checkbox.

## Changing completion status

I set my personal chord of `Meta + Shift + T <status>`

```json
    {
        "key": "meta+shift+t x", // or any other shortcut you want to use
        "command": "dendron.setTaskStatus",
        "when": "editorFocus && dendron:pluginActive",
        "args": {
            "setStatus": "x" // the status you want to set
        }
    },
    {
        "key": "meta+shift+t space", // or any other shortcut you want to use
        "command": "dendron.setTaskStatus",
        "when": "editorFocus && dendron:pluginActive",
        "args": {
            "setStatus": " " // the status you want to set
        }
    }
```


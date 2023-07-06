# Visual Studio Code Vim Extension Settings
1. Get shortcut support for pop-up menus.

`keybindings.json`
```json
// Place your key bindings in this file to override the defaults
[
    {
        "key": "ctrl+j",
        "command": "selectNextSuggestion",
        "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus || suggestWidgetVisible && textInputFocus && !suggestWidgetHasFocusedSuggestion"
    },
    {
        "key": "ctrl+k",
        "command": "selectPrevSuggestion",
        "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus || suggestWidgetVisible && textInputFocus && !suggestWidgetHasFocusedSuggestion"
    },
    {
        "key": "j",
        "command": "selectNextCodeAction",
        "when": "codeActionMenuVisible"
    },
    {
        "key": "k",
        "command": "selectPrevCodeAction",
        "when": "codeActionMenuVisible"
    },
    {
        "key": "ctrl+j",
        "command": "workbench.action.quickOpenNavigateNext",
        "when": "inQuickOpen"
    },
    {
        "key": "ctrl+k",
        "command": "workbench.action.quickOpenNavigatePrevious",
        "when": "inQuickOpen"
    },
    {
        "key": "alt+j",
        "command": "editor.action.moveLinesDownAction",
        "when": "editorTextFocus && !editorReadonly"
    },
    {
        "key": "alt+k",
        "command": "editor.action.moveLinesUpAction",
        "when": "editorTextFocus && !editorReadonly"
    }
]
```

2. Let vim can work well with Visaul Studio Code.

`settings.json`
```json
{
    "vim.easymotion": true,
    "vim.incsearch": true,
    "vim.useSystemClipboard": true,
    "vim.useCtrlKeys": true,
    "vim.hlsearch": true,
    "vim.insertModeKeyBindings": [
        {
            "before": [
                "j",
                "j"
            ],
            "after": [
                "<Esc>"
            ]
        }
    ],
    //https://github.com/VSCodeVim/Vim/issues/4241
    "vim.normalModeKeyBindingsNonRecursive": [
        {
            "before": [
                "d"
            ],
            "after": [
                "\"",
                "_",
                "d"
            ]
        },
        {
            "before": [
                "D"
            ],
            "after": [
                "\"",
                "_",
                "D"
            ]
        },
        {
            "before": [
                "d",
                "d"
            ],
            "after": [
                "\"",
                "_",
                "d",
                "d"
            ]
        },
        {
            "before": [
                "<BS>"
            ],
            "after": [
                "\"",
                "_",
                "d"
            ]
        }
    ],
    "vim.visualModeKeyBindingsNonRecursive": [
        {
            "before": [
                "d"
            ],
            "after": [
                "\"",
                "_",
                "d"
            ]
        },
        {
            "before": [
                "D"
            ],
            "after": [
                "\"",
                "_",
                "D"
            ]
        },
        {
            "before": [
                "d",
                "d"
            ],
            "after": [
                "\"",
                "_",
                "d",
                "d"
            ]
        },
        {
            "before": [
                "<BS>"
            ],
            "after": [
                "\"",
                "_",
                "d"
            ]
        }
    ],
    "vim.leader": "<space>",
    "vim.handleKeys": {
        "<C-a>": false,
        "<C-b>": false,
        "<C-c>": false,
        "<C-f>": false,
        "<C-h>": false,
        "<C-j>": false,
        "<C-v>": false,
        "<C-w>": false,
        "<C-x>": false,
        "<C-y>": false,
        "<C-z>": false,
        "<C-i>": false,
    }
}
```

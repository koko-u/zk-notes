# micro エディタの使い方

## キーバインド

`~/.config/micro/bindings.json` に設定を書くことで Emacs ライクにできる

内容
```json
{
    "Ctrl-a": "StartOfLine",
    "Ctrl-e": "EndOfLine",
    "Ctrl-f": "CursorRight",
    "Ctrl-b": "CursorLeft",
    "Ctrl-n": "CursorDown",
    "Ctrl-p": "CursorUp",

    "Alt-f": "WordRight",
    "Alt-b": "WordLeft",

    "Ctrl-d": "Delete",
    "Ctrl-h": "Backspace",
    "Ctrl-k": "DeleteLine",

    "Ctrl-s": "Save",
    "Ctrl-x": "Quit",

    "Ctrl-l": "Center"
}
```

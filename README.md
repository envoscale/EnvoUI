<img src="https://raw.githubusercontent.com/envoscale/.github/main/profile/assets/logo.svg" alt="" width="56" align="left">

# EnvoUI

The UI framework for [EnvoL](https://github.com/envoscale/EnvoLang), behind EnvIDE and the
other apps. One tree of components, laid out and drawn in a window, a browser page or a
terminal: buttons and text, lists and trees that stay fast with thousands of rows, tabs,
split panes, a code editor with selections and undo, and a command palette.

```cs
use envoui as ui;
use envor.theme;

ui.Tree t = ui.Tree.New();
u32 card = t.Card(t.Root());
t.Text(card, "Settings", ui.TITLE);
u32 dark = t.Checkbox(card, "Dark mode", false);
u32 save = t.Button(card, "Save", true);
```

| Module | |
|---|---|
| [`envoui`](ui) | Components, layout, input, focus, drawing in pixels or terminal cells |
| [`envoui.edit`](edit) | Text buffers: cursors, selections, undo, search |
| [`envoui.term`](term) | Terminals: screens, styles, keys |

Drawn with [EnvoR](https://github.com/envoscale/EnvoR).

## Use

```
dependencies {
    envoui = { git = "https://github.com/envoscale/EnvoUI", rev = "<commit>" }
}
```

`envo test` runs the tests here; CI runs them on Linux and Windows with EnvoLang at the
commit in [`envolang.ref`](envolang.ref).

## License

Same as EnvoScale: see [LICENSE](LICENSE).

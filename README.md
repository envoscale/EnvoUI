<img src="https://raw.githubusercontent.com/envoscale/EnvoScale/main/docs/images/logo.svg" alt="" width="56" align="left">

# Envoui

The UI framework for [Envol](https://github.com/envoscale/EnvoScale), behind Envide and the
other Envo apps. One tree of components, laid out and drawn in a window, a browser page or a
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

Drawn with [Envor](https://github.com/envoscale/Envor).

## Use

```
dependencies {
    envoui = { git = "https://github.com/envoscale/Envoui", rev = "<commit>" }
}
```

`envo test` runs the tests here; CI runs them on Linux and Windows with EnvoScale at the
commit in [`envoscale.ref`](envoscale.ref).

## License

Same as EnvoScale: see [LICENSE](LICENSE).

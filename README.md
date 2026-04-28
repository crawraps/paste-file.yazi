<div align="center"><h1>paste-file.yazi</h1></div>

Yazi plugin to paste clipboard content straight to the filesystem.

<!-- ![showcase](https://github.com/crawraps/paste-file.yazi/assets/VIDEO_OR_IMAGE_ID) -->

## Installation

```sh
ya pack -a crawraps/paste-file.yazi
```

Or manually:

```sh
git clone https://github.com/crawraps/paste-file.yazi ~/.config/yazi/plugins/paste-file.yazi
```

## Usage

1. Copy some content to your system clipboard.
2. Run the plugin — it prompts for a filename.
3. The file is created in the current working directory with your clipboard content written inside.

If a file with the same name already exists, you'll be asked to **o**verwrite or **c**ancel.

## Options

| Flag | Description |
|------|-------------|
| `--quiet` | Suppress the notification when a file already exists |

### Keymap

```toml
[[mgr.prepend_keymap]]
on = [ "p", "f" ]
run = "plugin paste-file -- --quiet"
desc = "create new file from clipboard"
```

Without `--quiet`:

```toml
[[mgr.prepend_keymap]]
on = [ "p", "f" ]
run = "plugin paste-file"
desc = "create new file from clipboard"
```

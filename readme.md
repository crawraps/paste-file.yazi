# paste-file.yazi

[Yazi](https://github.com/sxyazi/yazi) plugin to paste clipboard content strait to filesystem.

https://github.com/user-attachments/assets/6b3cc09b-5495-4aaa-aaac-d19515d865a8

## Installation

### Linux

```sh
git clone https://github.com/crawraps/paste-file.yazi.git ~/.config/yazi/plugins/paste-file.yazi```

## Usage

Create keymap with the following command:

```sh
plugin paste-file
```

You can use the `--args` flag to pass arguments to the plugin. Available flags are:

- `quiet`: Do not show a notification in case of creating a file with the same name

Example:

```toml
# ~/.config/yazi/keymap.toml:
[[manager.prepend_keymap]]
on = ["p", "f"]
run = ["plugin paste-file --args='quiet'"]
desc = "create new file from clipboard"
```

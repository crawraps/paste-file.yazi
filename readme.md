# paste-file.yazi

[Yazi](https://github.com/sxyazi/yazi) to paste clipboard content to a file

## Installation

### Linux

```sh
git clone https://github.com/crawraps/paste-file.yazi.git ~/.config/yazi/plugins/paste-file.yazi
```

## Usage

Add keymap with the following command:

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

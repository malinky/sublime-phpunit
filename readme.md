# Sublime PHPUnit

Convenient Sublime Text commands for running your PHPUnit and Laravel Dusk tests. Scans up the directory tree to find the closest phpunit.xml file and runs phpunit from there. If it can't find one, it just runs phpunit from `/`.

## Installation


Installation is as simple as cloning the repository into your Sublime Text install's `Packages` folder:

```bash
git clone https://github.com/adamwathan/sublime-phpunit ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/sublime-phpunit
```

## Available Commands & Example Keybindings

You can find the commands in the command palette under "Sublime PHPUnit", or map any of these commands to whatever shortcuts you want:

Here's the full list of commands:

```
run_phpunit_test
run_single_phpunit_test
run_all_phpunit_tests
run_phpunit_tests_in_dir
run_last_phpunit_test
run_dusk_test
run_single_dusk_test
run_all_dusk_tests
run_dusk_tests_in_dir
````

Here are some example keybindings:

```json
[
    { "keys": ["super+alt+t"], "command": "run_phpunit_test"},
    { "keys": ["alt+t"], "command": "run_single_phpunit_test"},
    { "keys": ["super+shift+ctrl+t"], "command": "run_all_phpunit_tests"},
    { "keys": ["super+shift+t"], "command": "run_phpunit_tests_in_dir"},
    { "keys": ["super+alt+l+t"], "command": "run_last_phpunit_test"},
    { "keys": ["super+alt+d"], "command": "run_dusk_test"},
    { "keys": ["alt+d"], "command": "run_single_dusk_test"},
    { "keys": ["super+shift+ctrl+d"], "command": "run_all_dusk_tests"},
    { "keys": ["super+shift+d"], "command": "run_dusk_tests_in_dir"},
]

```

## Using iTerm2 instead of Terminal.app

By default, this package uses macOS's built-in Terminal.app. If you want to use iTerm2, you can do so changing the terminal in your settings:

```
{
    "phpunit-sublime-terminal": "iTerm",
}
```

## Using fish shell

If you use [fish shell](https://fishshell.com/), specify this in your settings: 

```
{
    "phpunit-sublime-shell": "fish"
}
``` 

This will instruct Sublime PHPUnit to connect the commands using fish's `; and` instead of bash's `&&`.

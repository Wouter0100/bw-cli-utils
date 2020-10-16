# bw-cli-utils
Bitwarden CLI utils for moving items and switching between accounts.

- `bw-switch` to switch between different Bitwarden accounts.
- `bw-move` to move an item between Bitwarden accounts.

## Switch
To be able to switch, you need to have multiple `data.json` files. In my system, they're stored in `~/.config/Bitwarden CLI/` - for which location these scripts were build.

The switch statement will just switch the `data.json` to a different file in the same folder using a symlink. So it'll be:
- `account1.json`
- `account2.json`
- `account3.json`
- `data.json` which is symlinked to the current active account.

Use `bw-switch` without any arguments to get the current account. Provide a single argument (for example `account2`) to switch to that account.

## Move
Call `bw-move <account_from> <account_to> <item>` to move an item between 2 accounts. The item should be any name, uniquely identifing an specific item.

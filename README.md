# Simple Script for launching Brave's Profiles

It takes care of reading the 'Preferences' file in each profile in `$XDG_CONFIG_HOME/BraveSoftware/Brave-Browser/`, gets the name of the profile, pipes to dmenu and opens brave with the selected profile.


### Dependencies

- [dmenu](https://tools.suckless.org/dmenu/)
- [fd](https://github.com/sharkdp/fd)
- [ripgrep](https://github.com/BurntSushi/ripgrep)

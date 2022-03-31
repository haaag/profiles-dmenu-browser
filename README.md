# Simple Script for launching Brave's Profiles

It takes care of reading the 'Preferences' file in each profile directory in `$XDG_CONFIG_HOME/BraveSoftware/Brave-Browser/`, gets the name of the profile, pipes to dmenu and opens brave with the selected profile.

__The profile name must be unique.__

### Dependencies

- [dmenu](https://tools.suckless.org/dmenu/)
- [fd](https://github.com/sharkdp/fd)
- [ripgrep](https://github.com/BurntSushi/ripgrep)
- [jq](https://github.com/stedolan/jq)

### Estructura

```
├── $XDG_CONFIG_HOME/BraveSoftware/Brave-Browser/
    ├── Default
    │   └── Preferences
    ├── Profile 1
    │   └── Preferences
    ├── Profile 2
    │   └── Preferences
    └── Profile 3
        └── Preferences
```


### Preferences Estructura

The `Preferences` file is a very long `json` file. I used [jq](https://github.com/stedolan/jq) so I could get the value of the `profile.name` key, which represents the name I gave the `profile`.

```json
"profile": {
    "avatar_bubble_tutorial_shown": 2,
    "avatar_index": 26,
    "content_settings": {
        "enable_quiet_permission_ui_enabling_method": {
            "notifications": 1
        },
        "exceptions": {
            "bluetooth_guard": {}
        },
        "pref_version": 1
    }
    "default_content_setting_values": {
        "cookies": 1
    }
=======> "name": "profile-name-im-looking-for",
}
```

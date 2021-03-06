mocp Ansible role
=================

Installs and configures [mocp], Music On Console Player.

Requirements
------------

Assumes a Debian-based host.

Role Variables
--------------
```yaml
# List of apt packages to install.
mocp_apt_packages:
  - moc

# Dict of config items for writing to `~/.moc/config`.
# Will be interpolated as `key = value` options.
mocp_config: {}

# Dict of keymap settings for writing to `~/.moc/keymap`.
# Will be interpolated as `key = value` options.
mocp_keymap: {}

# Override the default keybindings to make mocp more vim-like.
mocp_use_vim_keybindings: False

mocp_music_directory: ~/Music
```

Example Playbook
----------------

```yaml
- hosts: desktops
  roles:
    - role: conorsch.mocp
      mocp_use_vim_keybindings: yes
```

License
-------

MIT

[mocp]: https://github.com/zcoder/mocp

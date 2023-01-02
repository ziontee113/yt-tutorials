# Video Title:

- Map / Unlock Special Key Combinations in Neovim

# Links:

- https://en.wikipedia.org/wiki/List_of_Unicode_characters
- http://www.leonerd.org.uk/hacks/fixterms/

# Example alacritty.conf:

```yaml
key_bindings:
  - { key: H, mods: Control|Shift, chars: "\x1b[72;6u" }
  - { key: J, mods: Control|Shift, chars: "\x1b[74;6u" }
  - { key: K, mods: Control|Shift, chars: "\x1b[75;6u" }
  - { key: L, mods: Control|Shift, chars: "\x1b[76;6u" }

  - { key: I, mods: Control, chars: "\x1b[105;5u" }

  - { key: Period, mods: Control, chars: "\x1b[46;5u" }
  - { key: Comma, mods: Control, chars: "\x1b[44;5u" }
  - { key: Semicolon, mods: Control, chars: "\x1b[59;5u" }

  - { key: Return, mods: Shift, chars: "\x1b[13;2u" }
```

## Map / Unlock Special Key Combinations in Neovim

## Links:

- https://en.wikipedia.org/wiki/List_of_Unicode_characters
- http://www.leonerd.org.uk/hacks/fixterms/

## Example kitty.conf:

```
# Shift + Enter

map shift+enter send_text all \x1b[13;2u

# Ctrl + I Remaps

map ctrl+i send_text all \x1b[105;5u

# Ctrl + . , ;

map ctrl+. send_text all \x1b[46;5u
map ctrl+, send_text all \x1b[44;5u
map ctrl+; send_text all \x1b[59;5u

# Ctrl + Shift Remaps

map ctrl+shift+h send_text all \x1b[72;6u
map ctrl+shift+j send_text all \x1b[74;6u
map ctrl+shift+k send_text all \x1b[75;6u
map ctrl+shift+l send_text all \x1b[76;6u
```

## Example alacritty.conf:

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

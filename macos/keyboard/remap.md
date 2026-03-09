# Keyboard Remap — Logitech K480

## Dead keys
- **X key** — no HID event at all (hardware failure)
- **Left Shift** — does not modify other keys (hardware failure). Using Right Shift instead.

## Active remap
Caps Lock → X

```bash
hidutil property --set '{"UserKeyMapping":[{"HIDKeyboardModifierMappingSrc":0x700000039,"HIDKeyboardModifierMappingDst":0x70000001B}]}'
```

| Key code | Key |
|---|---|
| 0x700000039 | Caps Lock |
| 0x70000001B | X |

## Persistence
LaunchAgent: `~/Library/LaunchAgents/com.local.keyremap.plist`
Backup copy: `../configs/com.local.keyremap.plist`

Runs at login via `RunAtLoad`.

## How to undo
```bash
# Remove the remap
hidutil property --set '{"UserKeyMapping":[]}'

# Remove the LaunchAgent
rm ~/Library/LaunchAgents/com.local.keyremap.plist
```

## How to verify
```bash
hidutil property --get UserKeyMapping
```

# Changelog

## 2026-03-09 — Keyboard remap: Caps Lock → X
- **Problem**: "X" key on Logitech K480 is physically dead. Left Shift also dead.
- **Fix**: Remapped Caps Lock to X via `hidutil`. Using Right Shift instead of Left Shift.
- **Persisted**: LaunchAgent at `~/Library/LaunchAgents/com.local.keyremap.plist`
- **Details**: [keyboard/remap.md](keyboard/remap.md)

# Client Configuration
This file explains all available options in the configuration file.
The configuration uses **TOML** format. All settings are optional; if a setting is missing, a default value is used.

## General Settings
### `nickname`
- **Type:** string
- **Description:** Your in-game nickname or display name.
---
### `language`
- **Type:** integer
- **Description:** Language selection index for the application interface.
---
### `log_chat`
- **Type:** boolean
- **Description:** Enables or disables saving chat messages to a log file.
---
### `watch_enabled`
- **Type:** boolean
- **Description:** Enables or disables the on-screen watch/clock feature.
---
### `chat_lines`
- **Type:** integer
- **Description:** Number of chat lines shown on screen at the same time.
---
### `keyboard_layout`
- **Type:** integer
- **Description:** Keyboard layout preset used by the application.
---
### `window_always_on_top`
- **Type:** boolean
- **Description:** Keeps the application window above other windows when enabled.
---
### `vsync_enabled`
- **Type:** boolean
- **Description:** Enable or disable VSync.
---
### `mcp_pipe_enabled`
- **Type:** boolean
- **Description:** Enables communication with external tools via MCP pipe.
---
### `renderer_type`
!!! note 
	If you plan to use modifications like [G3D11](https://github.com/SaiyansKing/GD3D11) or [LegacyAltRenderer](https://github.com/SaiyansKing/Gothic-LegacyAltRenderer), you need to use D3D7 on GMP.

- **Type:** string
- **Allowed values:** `"D3D7"`, `"D3D9"`, `"D3D11"`
- **Description:** Selects which graphics renderer the application uses.

To learn more, check [Renderer article](Renderer.md).
---
## Watch Position
Controls where the watch/clock is displayed on screen.

```toml
[watch_position]
x = 7000
y = 2500
```

### `watch_position.x`
- **Type:** integer
- **Description:** Horizontal position of the watch.

### `watch_position.y`
- **Type:** integer
- **Description:** Vertical position of the watch.

---
## Console Position
Controls where the console window is displayed on screen.

```toml
[console_position]
x = 52
y = 52
```

### `console_position.x`
- **Type:** integer
- **Description:** Horizontal position of the console.

### `console_position.y`
- **Type:** integer
- **Description:** Vertical position of the console.

---
## Test Mode
Used for development and testing purposes.

```toml
[test_mode]
enabled = false
level = ""
spawn_x = 0.0
spawn_y = 0.0
spawn_z = 0.0
```

### `test_mode.enabled`
- **Type:** boolean
- **Description:** Enables or disables test mode.

### `test_mode.level`
- **Type:** string
- **Description:** Name of the level/world to load when test mode is enabled.

### `test_mode.spawn_x`
- **Type:** number
- **Description:** X coordinate where the player will spawn in test mode.

### `test_mode.spawn_y`
- **Type:** number
- **Description:** Y coordinate where the player will spawn in test mode.

### `test_mode.spawn_z`
- **Type:** number
- **Description:** Z coordinate where the player will spawn in test mode.
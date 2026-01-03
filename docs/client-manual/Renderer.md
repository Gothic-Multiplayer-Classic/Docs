# Renderer
Gothic Multiplayer supports multiple rendering backends. You can either keep the **original Gothic renderer** (DirectX 7) or switch to one of the renderers shipped with the Multiplayer client (DirectX 9 or DirectX 11).

This is primarily a **compatibility and stability feature**: different systems and driver stacks behave differently with the original 2001-era DirectX 7 pipeline, so GMP provides newer alternatives.

---

## Available renderers
!!! note 
	If you plan to use modifications like [G3D11](https://github.com/SaiyansKing/GD3D11) or [LegacyAltRenderer](https://github.com/SaiyansKing/Gothic-LegacyAltRenderer), you need to use DX7 on GMP.

### DX7 (Vanilla / Gothic API default)
- This is the **original renderer used by Gothic**.
- Selecting DX7 aims to preserve the most "vanilla" behavior and visuals.

Use DX7 if you want the classic rendering path or if you are troubleshooting and want the simplest baseline.

---

### DX9 (Gothic Multiplayer renderer)
- GMP ships its own **Direct3D 9 renderer**.
- In the current codebase, **D3D9 is the default renderer**.

Use DX9 if you want a more modern backend than DX7, especially on newer Windows versions and GPU drivers, while still staying closer to the "classic era" of DirectX.

---

### DX11 (Gothic Multiplayer renderer)
- GMP also ships a **Direct3D 11 renderer**.

Use DX11 if you want to experiment with the newest backend and you understand it may be incomplete depending on your current GMP version.

---

## How to change the renderer
Renderer selection is controlled via the GMP [configuration file](Configuration.md):

- **File:** `GMP_Config.toml`
- **Key:** `renderer_type`
- **Allowed values:** `D3D7`, `D3D9`, `D3D11`

Example:
```toml
# GMP_Config.toml
renderer_type = "D3D7"   # Vanilla DX7 renderer
# renderer_type = "D3D9"  # GMP DX9 renderer (default)
# renderer_type = "D3D11" # GMP DX11 renderer
```

---

## Practical pros and cons
### Choosing DX7 (Vanilla)
#### Pros
- Closest match to original Gothic behavior and visuals
- Good baseline for troubleshooting (eliminates GMP renderer variables)
- Is the only one which works with renderer wrapper mods made for the game
#### Cons
- More fragile on modern systems (OS/driver compatibility)
- No benefits from GMP's newer rendering path
### Choosing DX9 (GMP)
#### Pros
- Typically better compatibility with modern Windows + GPU drivers than DX7
- Default GMP path (most tested in day-to-day usage)
#### Cons
- Marked as experimental and may show visual glitches
### Choosing DX11 (GMP)
#### Pros
- Most modern backend provided by GMP
- Best long-term direction for future renderer work
#### Cons
- Explicitly marked as not fully implemented
- May be less reliable than DX9 depending on current build
### Recommendation
- Start with DX9 (default), unless you have a specific reason not to.
- Switch to DX7 if you want the most vanilla baseline or to troubleshoot.
- Try DX11 if you are testing and can tolerate incomplete implementation.
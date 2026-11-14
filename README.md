





# Crispy Assetto Corsa Apps

CSP Lua apps by **SavageBulldogOG** for everyday driving, drifting, spectating, and adjusting your Assetto Corsa experience.

## At a glance

| App | What it adds |
| --- | --- |
| Crispy Audio UI + Shortcut UI | Quick volume presets, mute, and supported car controls. |
| Crispy Cam Select | Camera switching, driver selection, and replay lap navigation. |
| Crispy Driver Tags | Custom driver labels with flags, ping, icons, colors, and fading. |
| Crispy FFB Controls | Per-car gain defaults, global FFB adjustments, and live force graphs. |
| Crispy Pedals UI | A customizable pedal, handbrake, steering, and FFB overlay. |
| Crispy Setup Loader | Remember a setup per car and attempt to restore it on joining. |
| Crispy Quick Teleport | Jump to an available server teleport point near a tagged friend. |

## Installation

These apps are written for Assetto Corsa with **Custom Shaders Patch (CSP)**. Content Manager is used for the associated driver tags and friend workflow. 
A minimum CSP version has not been established for the complete collection; individual features depend on the APIs available in your build.

1. Download and extract this repository.
2. Copy the desired `crispy_*` folders into `assettocorsa/apps/lua/`. Keep each app's files and subfolders together.
3. Start a session and open the desired app from the in-game app sidebar. 
    - Setup Loader only appears in the setup menu.


## Crispy Audio UI + Shortcut UI

Folder: `crispy_audio_ui`

Two compact windows keep audio and supported car functions within reach.

### Audio window
<p align=center>
<img width="281" height="177" alt="audio_ui" src="https://github.com/user-attachments/assets/e9378957-63c7-486c-bb7d-5c22b7e68251" />
<img width="230" height="162" alt="audio_ui" src="https://github.com/user-attachments/assets/db1e470a-edad-4719-97d1-d6fdf140cc77" />
</p>

- Three quick-volume buttons select between **10/20%**, **30/50%**, and **80/99%**, based on the current volume.
- The volume readout also acts as a mute/unmute button.
- Unmuting restores the volume saved when muting, with 50% as the fallback.
- Optional fading hides the controls when the window is not hovered.
- Adjustable background contrast.

### Shortcut window

<img width="395" height="277" alt="shortcut_ui" src="https://github.com/user-attachments/assets/405e5786-0557-435c-98be-ab36b4a041f3" />
<img width="390" height="274" alt="shortcut_ui" src="https://github.com/user-attachments/assets/581e695f-4be4-4b54-82dc-a4ae0744eadf" />

<br>

- Wiper mode selection.
- Headlight control, including off/low/high beams on supported cars.
- Left and right indicators and hazard lights, with active-state highlighting.
- Hold-to-sound horn or a siren control, depending on the car.
- Cockpit-adjustable brake bias.
- Adjustable turbo wastegate level.
- Individual visibility switches for each control category, plus separate fading and background settings.

Controls depend on the capabilities exposed by the current car. In the current code, the basic headlight checkbox for cars without low/high-beam selection is also gated by an internal button-count setting; it may not appear with the default settings.

## Crispy Cam Select

<img align=right width="267" height="646" alt="cam_select" src="https://github.com/user-attachments/assets/9c46fa1e-4eea-49e0-a3df-2802ca981d3f" />

Folder: `crispy_cam_select`

A compact panel for choosing your view and the car you want to watch.

- Cycle through driving cameras using **Camera**.
- Switch to **Free**, **Orbit**, **Heli**, **Track**, or **Car** camera modes.
- Toggle several external camera modes back to the last driving-camera mode.
- Cycle through six car-camera positions by pressing **Car** again while that mode is active.
- Select a driver from the session list to focus their car, with driver-tag colors in the list.
- Return to your own car with **Focus own view**.
- Jump to the previous or next lap during replay playback.
- Recenter VR when a VR headset is connected.
- Hover controls for descriptions and relevant keyboard or configured binding information.

Track-camera sets are changed with **F3**. Free-camera keyboard access depends on the relevant AC system setting; its tooltip describes right-mouse look, arrow-key movement, and Ctrl/Shift speed modifiers.

## Crispy Driver Tags

Folder: `crispy_driver_tags`

Customizable labels above cars, designed to keep driver information readable without keeping every label fully visible at all distances.

<img width="336" height="283" alt="driver_tags" src="https://github.com/user-attachments/assets/be9583e6-f0c2-478b-a898-f0f6bc803178" />
<img width="336" height="268" alt="driver_tags0" src="https://github.com/user-attachments/assets/6152bbcd-b3ba-4a15-9859-a5e9afaea2e6" />
<img width="337" height="307" alt="driver_tags1" src="https://github.com/user-attachments/assets/6b1bd0ac-3e61-4e9d-96d5-a66c7dfb343d" />
<img width="337" height="214" alt="driver_tags4" src="https://github.com/user-attachments/assets/5071d8d4-c48b-4097-843f-350cd48c3b59" />

<br>

- Driver names with optional national flags or custom driver icons.
- Online ping readouts with colors and warning symbols for higher latency.
- Recognized bracketed name tags are replaced with icons: `[STREAMER]` and `[TTV]` use the Twitch icon; `[ADMIN]` uses the admin icon; `[COOL_KID]`, `[DRIFT_KING]`, `[BAD_DRIVER]`, and `[ANGLE_MASTER]` use the Discord icon. Other bracketed tags remain as text.
- Use Content Manager/CSP driver-tag colors for names, outlines, or both, or choose custom text and outline colors.
- Adjust font, font size, outline width, flag size, and ping size.
- Toggle a background box and customize its color, padding, and corner roundness.
- Adjust base visibility distance and separate near/far fading behavior, including minimum close-range opacity.
- Choose whether labels appear for cars in the pits or pit lane.
- Maintain a server blacklist to suppress this app's labels on selected servers.
- Refresh tag registration or the car cache from the settings panel.
- Advanced options expose tag-container dimensions, server details, and an app-disable switch.

The blacklist and disable controls advise reloading the session to apply changes. The base visibility distance is combined with fade cutoffs, so labels can disappear before that maximum distance.

<img width="339" height="484" alt="driver_tags5" src="https://github.com/user-attachments/assets/f4597913-08c0-4bb9-8384-1f7c7e02fe84" />

## Crispy FFB Controls `work in progress`

Folder: `crispy_ffb_controls`

Manage car-specific force-feedback gain, tune native AC/CSP settings, and inspect the signals while driving.

<img width="447" height="596" alt=" ffb_settings1" src="https://github.com/user-attachments/assets/b0da4435-a507-4a06-a1c9-7f9376991c3a" />
<img width="445" height="542" alt=" ffb_settings2" src="https://github.com/user-attachments/assets/f51b8cdd-976d-4c2b-853e-356416fefe55" />
<img width="443" height="822" alt=" ffb_settings3" src="https://github.com/user-attachments/assets/d712fc06-8dbc-467a-b94b-84dc15eb380b" />
<img width="429" height="686" alt=" ffb_settings4" src="https://github.com/user-attachments/assets/40698cdf-ae65-449c-8914-491d59463ec4" />

<br>

### Per-car defaults

- Automatic default gain, initially **60%**, with an adjustable **0–200%** target.
- By default, preserves a saved native per-car gain and also preserves a live gain that is already different from 100%.
- Saves automatically applied defaults to AC's native `user_ff.ini`.
- Optional **Override car gain** mode applies the chosen target at startup and when the override is enabled or its target changes.
- Live car-gain slider, a shortcut to 100%, and a reset to the original gain captured by the app.
- Automatic initialization is skipped during replays.

### Quick Settings and Controls

- Global FFB gain, filtering, and skip steps, with the resulting refresh-rate indication.
- Minimum force, center boost gain, and center boost range.
- Kerb, road, slip, ABS, and understeer effects.
- Gyro selection: **None**, **Standard**, or **FFB Tweaks**.
- Legacy CSP gyro strength control, whose effect depends on the CSP build.
- Damper gain and minimum level.
- Low-speed force-reduction threshold and multiplier.
- CSP range compression and range-compression assist.
- Native post-processing selection: **Disabled**, **Gamma**, or **LUT**.
- Gamma adjustment and selection of existing `.lut` files from `Documents/Assetto Corsa/cfg`. LUT creation/import is outside this app.
- Reset buttons for supported settings restore the values captured when the app initialized, rather than factory defaults.

These global controls save to AC/CSP configuration files and reload control settings. They affect more than the current car.

### Graph and Info

- Live final and pure FFB signals, current gain, car base multiplier, and steering-assist value when exposed by CSP.
- Approximately ten seconds of graph history, with final/pure traces and reference lines at ±100%.
- Peak final magnitude, RMS final signal, and percentage of samples at the output limit.
- Clear graph history on demand.
- A read-only configuration overview, including additional settings such as real steering forces, configured wheel peak torque, dirt vibration, and soft lock.

The graph shows normalized signals, not measured wheel torque in Nm. Output-limit samples indicate saturation, not a complete diagnosis of clipping. The Info page shows configured values; that alone does not establish that a feature is active for the current car.

## Crispy Pedals UI `work in progress`

Folder: `crispy_pedals_ui`

A compact input overlay with optional steering and force-feedback information.

<img width="800" height="389" alt="pedals_ui" src="https://github.com/user-attachments/assets/2f423b7c-9410-4e8c-bcd5-edfd77786703" />

<br>

- Clutch, brake, and throttle bars with smoothing.
- Optional handbrake bar and/or a handbrake indicator over the brake bar.
- Custom handbrake text or symbol.
- Optional rotating steering-wheel graphic.
- Optional FFB display in **Absolute** or **Signed (centered)** mode.
- An FFB warning symbol at the normalized output limit and red coloring beyond it.
- Optional percentage readouts and labels, with horizontal/vertical label orientation.
- Adjustable scale, bar width and height, spacing, background opacity, and smoothing.
- Color controls for pedals, handbrake, and positive/negative FFB.
- Reset controls for appearance and defaults.
- Additional FFB debug values in the settings panel.

FFB indicators use CSP's final normalized signal; they do not measure physical wheel torque. The main overlay captures the focused car when the script loads, so switching spectator focus later is not explicitly handled by the current implementation.

## Crispy Setup Loader `work in progress`

Folder: `crispy_setup_loader`

Remember a preferred saved setup for each car, independent of track, and attempt to restore it once per join.

<img width="777" height="738" alt="auto_setup_s14" src="https://github.com/user-attachments/assets/eef88013-98fc-4229-9045-7cb202c8ca9e" />
<img width="382" height="364" alt="auto_setup_e92" src="https://github.com/user-attachments/assets/d8adba10-1aa3-478f-9388-06aebb086525" />
<img width="372" height="352" alt="auto_setup" src="https://github.com/user-attachments/assets/e74963ed-3b45-4258-9555-23be38dc1334" />

<br>

- Choose from the car's saved `.ini` setups in generic and track folders.
- **Remember selected** stores a preferred setup for that car.
- Tracks setup loads and saves made through the original AC setup interface, remembering explicit setup files without replacing the preference with `last.ini`.
- Optionally use `generic/last.ini` instead of the remembered file for automatic loading.
- Enable or disable automatic loading per join.
- Experimental immediate loading attempts a load about 1.5 seconds after joining.
- If the early attempt is rejected, a short fallback window on the first setup-screen opening makes up to three attempts.
- A manual setup load/save cancels further automatic loading for that join, helping preserve your subsequent choices.
- Manual buttons load the selected setup, remembered setup, or `last.ini`, and refresh the list.
- Status messages explain missing files, unavailable editing, rejected loads, and successful requests.

**Setup loading requires an editable setup.** Fixed-setup restrictions still apply. The app's implementation notes that CSP supports setup loading in the setup menu; experimental pre-menu loading is not guaranteed to succeed or finish before you click Drive. Automatic loading stops after the initial attempt window. Automatic-loading option changes take effect on the next join.

## Crispy Quick Teleport `work in progress`

Folder: `crispy_teleport_to_friend`

Quickly rejoin tagged friends using destinations supplied by the online server.

<img width="368" height="321" alt="quick_tp1" src="https://github.com/user-attachments/assets/d79cfaf0-99a0-46c7-8ace-12e799f77335" />
<img width="374" height="476" alt="quick_tp2" src="https://github.com/user-attachments/assets/05d73643-8fb7-4bf9-97c0-765229f7b8d7" />
<img width="368" height="422" alt="quick_tp3" src="https://github.com/user-attachments/assets/026a5c13-611a-4de1-acc9-a37bfa7954f1" />
<img width="464" height="444" alt="quick_tp4" src="https://github.com/user-attachments/assets/92b1b9c3-d4bd-4f76-b7dc-bc43263e35ca" />

<br>

- Lists connected players tagged as friends in Content Manager, sorted by name.
- Shows the chosen destination and its distance from each friend.
- A friend's **Teleport** button remembers that player as the quick target.
- A quick-teleport button and an assignable key/controller binding target the last chosen friend.
- If that friend is unavailable or no longer tagged, quick teleport cycles through available tagged friends while preserving the saved target for their return.
- Optional preference for destinations ahead of a friend's travel direction; when moving, velocity is used to better account for drifting.
- Within the configurable near threshold, uses the nearest available point even if it is behind the friend.
- Beyond that threshold, prefers an ahead point within the configured radius, falling back to the nearest available point if needed.
- Defaults to a **50 m** near threshold and **600 m** maximum ahead-search distance; both can be adjusted.
- Disable the ahead preference to always choose the closest available point.
- Resolves the friend's current position when teleporting and reports unavailable destinations or other errors.

**This uses server-defined teleport points, not arbitrary coordinates beside a friend.** It requires an online server with teleport destinations, permission to use an available point, and a compatible CSP build. Distances are straight-line distances rather than distances along the road. The custom binding starts unassigned and can be configured inside the app.

## Credits
- Cam Select includes code from **x4fab's Unbound**; its source is referenced in the app manifest.
- FFB Controls follows parts of **x4fab's Controller Tweaks** for settings layout and behavior.
- Quick Teleport references **Tuttertep's Comfy Map** for server teleport-destination ordering and the tagged-friend workflow.

## License
This software is provided "as is", without warranty of any kind. 
<br />  It is free to use, modify, and distribute under one condition: 
<br />  Only thing asked of you is to credit the author (SavageBulldog) and include a link back to the original repository.
```
https://github.com/SBDG-0/crispy_assetto_corsa
```
---
made with ❤️ by SavageBulldogOG

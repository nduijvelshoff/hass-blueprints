# hass-blueprints

Home Assistant automation blueprints by [@nduijvelshoff](https://github.com/nduijvelshoff).

---

## Scene Cycle

**File:** [`scene_cycle.yaml`](scene_cycle.yaml)

Activate scenes based on the time of day using a single button or switch. No helper entities required.

### How it works

| Action | Result |
|---|---|
| Press (lights off) | Activates the scene matching the current time block |
| Press after a pause (lights on) | Turns off the lights |
| Quick press (lights on) | Cycles to the next scene based on which scene is currently active |

### Time blocks

Up to 5 configurable time blocks, each with a start time and a scene. Set **Active blocks** to use fewer than 5.

| Block | Default time | Purpose |
|---|---|---|
| 1 | 07:00 | Morning |
| 2 | 10:00 | Day |
| 3 | 17:00 | Evening |
| 4 | 20:00 | Late evening |
| 5 | 23:00 | Night |

### Import

[![Import blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fnduijvelshoff%2Fhass-blueprints%2Fblob%2Fmain%2Fscene_cycle.yaml)

---

## Dual Button – Scene Cycle Up/Down

**File:** [`scene_cycle_dual_button.yaml`](scene_cycle_dual_button.yaml)

Two-button remote for manual scene cycling and dimming. No time-based logic. No helper entities required.

### How it works

| Button | Action | Result |
|---|---|---|
| Up | Single press (lights off) | Turns on the first scene |
| Up | Double press | Cycles to the next scene |
| Up | Hold | Dims up in steps |
| Down | Single press (lights on) | Turns off the lights |
| Down | Double press | Cycles to the previous scene |
| Down | Hold | Dims down in steps |

### Configuration

| Input | Description | Default |
|---|---|---|
| Button Up | Event entity for the up/next button | — |
| Button Down | Event entity for the down/previous button | — |
| Light | Light entity to control | — |
| Scenes 1–5 | Up to 5 scene entities | — |
| Active scenes | How many scenes are active (1–5) | 5 |
| Dim step | Brightness % per hold step | 5% |
| Dim interval | Milliseconds between dim steps | 500 ms |

### Import

[![Import blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fnduijvelshoff%2Fhass-blueprints%2Fblob%2Fmain%2Fscene_cycle_dual_button.yaml)

---

## License

[Apache 2.0](LICENSE)

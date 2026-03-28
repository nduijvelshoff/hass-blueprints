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

## License

[Apache 2.0](LICENSE)

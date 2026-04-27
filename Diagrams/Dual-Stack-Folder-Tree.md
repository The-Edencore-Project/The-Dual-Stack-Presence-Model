# 🌗 Edencore Dual Stack — Full Folder + File Structure  
## **C‑Stack (Cognitive OS) + B‑Stack (Behavioural OS)**  
### *The complete, canonical filesystem layout*

```
/edencore/
│
├── cstack/                     # Cognitive OS (deterministic, governed)
│   │
│   ├── core.py                 # Layer 1 — heartbeat, scheduler, reflex
│   ├── body.py                 # Layer 2 — device IO, sensors, actuators
│   ├── world.py                # Layer 3 — environment model
│   ├── household.py            # Layer 4 — graph of rooms, devices, roles
│   ├── behaviour.py            # Layer 5 — rules, policies, actions
│   ├── planner.py              # Layer 6 — intent resolution, sequencing
│   ├── social.py               # Layer 7 — UX, dialogue, interaction
│   ├── memory.py               # Layer 8 — short/long‑term patterns
│   └── meta.py                 # Layer 9 — modes, governance, safety
│
│   └── codex/                  # Optional: codex versions of each layer
│       ├── core.codex
│       ├── body.codex
│       ├── world.codex
│       ├── household.codex
│       ├── behaviour.codex
│       ├── planner.codex
│       ├── social.codex
│       ├── memory.codex
│       └── meta.codex
│
│
├── bstack/                     # Behavioural OS (ambience, drift)
│   │
│   ├── basins.py               # Attractor basins for ambience states
│   ├── drift.py                # Slow environmental drift engine
│   ├── tension.py              # Tension detection + release curves
│   ├── ambience.py             # Light, sound, temperature shaping
│   ├── rails.py                # Environmental rails + constraints
│   ├── transitions.py          # Smooth ambience transitions
│   └── envelope.py             # Safety envelope for ambience changes
│
│
├── dumbpipe/                   # One‑Way Dumb Pipe
│   ├── sensors_raw.py          # Raw sensor stream (no meaning)
│   ├── events_raw.py           # Raw events (no interpretation)
│   └── state_raw.py            # Raw state snapshots
│
│
├── interfaces/
│   ├── devices/                # Device drivers (lights, blinds, HVAC)
│   ├── sensors/                # Sensor drivers (temp, motion, lux)
│   └── protocols/              # MQTT, BLE, Zigbee, local APIs
│
│
├── runtime/
│   ├── loop.py                 # 144‑step pulse engine
│   ├── scheduler.py            # Deterministic timing
│   └── dispatcher.py           # Routes signals to both stacks
│
│
├── config/
│   ├── safety.yaml             # Safety boundaries
│   ├── policies.yaml           # Behaviour policies
│   ├── modes.yaml              # Mode definitions
│   └── devices.yaml            # Device registry
│
│
└── docs/
    ├── DSPM.md                 # Dual Stack Presence Model
    ├── CStack.md               # Cognitive OS spec
    ├── BStack.md               # Behavioural OS spec
    ├── DumbPipe.md             # One‑Way Dumb Pipe spec
    └── PresenceModel.md        # Illusion‑of‑Presence explanation
```
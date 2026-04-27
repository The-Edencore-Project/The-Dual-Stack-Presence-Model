# 🧱 01_Stack-Separation

The core architectural diagram of the Dual Stack Presence Model

This diagram shows the strict separation between the Behavioural OS (B‑Stack) and Cognitive OS (C‑Stack). It is the most important visual in DSPM, forming the basis for all other diagrams.

`
                ┌──────────────────────────────┐
                │        Physical Sensors       │
                │  (light, sound, motion, etc.) │
                └──────────────────────────────┘
                               │
                               │  raw, non-symbolic data
                               ▼
                    ┌──────────────────────┐
                    │      Dumb Pipe       │
                    │ (one-way, no meaning)│
                    └──────────────────────┘
                               │
                               ▼
        ┌──────────────────────────────────────────────┐
        │                Behavioural OS                 │
        │──────────────────────────────────────────────│
        │  • basins                                     │
        │  • drift                                      │
        │  • tension                                    │
        │  • release                                    │
        │  • ambience + environmental texture           │
        │                                               │
        │  ❌ cannot interpret meaning                   │
        │  ❌ cannot access cognition                    │
        │  ❌ no memory, no emotion                      │
        └──────────────────────────────────────────────┘


        ┌──────────────────────────────────────────────┐
        │                 Cognitive OS                  │
        │──────────────────────────────────────────────│
        │  • commands                                   │
        │  • routines                                   │
        │  • device control                             │
        │  • scheduling                                 │
        │                                               │
        │  ❌ cannot influence ambience                  │
        │  ❌ cannot read behavioural state              │
        │  ❌ no emotional inference                     │
        └──────────────────────────────────────────────┘
`

---

🌿 Why this is the first diagram
Because it visually encodes the core safety boundary of DSPM:

- two stacks  
- no shared memory  
- no shared models  
- no emotional state  
- no cross‑stack calls  
- one‑way dumb pipe  
- physical signals only  

Everything else — behavioural physics, presence illusion, environmental signatures — builds on this.

This is the “anatomy plate” of the organism.

---

If you want, I can now generate 02Behavioural-Cycle.md (basins → drift → tension → release), or move to 03Illusion-Map.md, or continue the sequence in order.
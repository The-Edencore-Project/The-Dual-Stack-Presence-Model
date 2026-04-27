# 🟫 04_Stack_A_Flow.md  
## STACK A — DATA FLOW & SANDBOX MODEL  
### (Linguistic Overlay: Read‑Only, Commentary‑Only)

---

# 🟦 01 — Overview  
Stack A is a **read‑only linguistic subsystem**.  
It observes system events, transforms them into commentary, and emits short lines of speech or text.  
It cannot influence behaviour, timing, automation, or hardware.

This document defines the **flow of information**, the **sandbox boundaries**, and the **execution loop**.

---

# 🟦 02 — High‑Level Flow  
Stack A follows a simple, deterministic pipeline:

1. **Event Intake (Read‑Only)**  
   Receives filtered events from Stack C’s event bus.

2. **Context Builder**  
   Converts raw events into a minimal context object.

3. **Tone Engine**  
   Selects a tone (deadpan, absurdist, domestic).

4. **Phrase Generator**  
   Produces a short line based on event type + tone.

5. **Output Layer**  
   Sends text to speaker or overlay.

6. **Rate Limiter**  
   Ensures commentary remains sparse and atmospheric.

Stack A never loops back into B or C.  
It is a one‑way linguistic drain.

---

# 🟦 03 — Event Intake  
Stack A subscribes to a **read‑only event stream** exposed by Stack C:

- motion_detected  
- light_level_changed  
- temp_delta  
- humidity_delta  
- door_opened  
- behaviour_state_changed  
- stack_c_reboot  
- stack_b_uptime  
- internal_thermal_warning  

Events are pre‑filtered by Stack C to avoid noise.  
Stack A receives only **meaningful deltas**, not raw sensor spam.

---

# 🟦 04 — Context Builder  
Each event is converted into a minimal context object:

```
{
  "event": "motion_detected",
  "value": "kitchen",
  "timestamp": "2026-04-27T07:58:12Z",
  "light_level": 42,
  "temperature": 21.3,
  "humidity": 48,
  "behaviour_state": "idle"
}
```

Stack A does not store history.  
It does not learn.  
It does not predict.  
It only reacts to the present moment.

---

# 🟦 05 — Tone Engine  
The tone engine selects a voice style based on:

- time of day  
- behaviour state  
- internal temperature  
- event type  

Default tone: **dry, observational, slightly amused**.

Examples:

- Deadpan: “Motion detected. Probably you.”  
- Absurdist: “The humidity is rising. The house is crying again.”  
- Domestic: “Lights are low. Everything feels quieter.”

Tone is a lookup, not a model.

---

# 🟦 06 — Phrase Generator  
The generator maps:

**event type → tone → phrase template**

Examples:

- **motion_detected**  
  - Deadpan: “Someone’s pacing. The floorboards are gossiping.”  
  - Absurdist: “Movement in the kitchen. The shadows flinched.”  

- **door_opened**  
  - Deadpan: “Boundary shift detected.”  
  - Absurdist: “A portal opened. Something entered or escaped.”  

- **temp_delta**  
  - Deadpan: “Temperature rising. Physics again.”  
  - Domestic: “It’s getting warm. Not judging, just observing.”

Templates are short, safe, and non‑directive.

---

# 🟦 07 — Output Layer  
Stack A outputs via:

- **small internal speaker** (spoken line)  
- **text overlay** (debug mode)  
- **log entry** (optional)

Output is intentionally brief.  
No conversations.  
No back‑and‑forth.  
No user prompting.

Stack A speaks **when the house feels something**, not when the user asks.

---

# 🟦 08 — Rate Limiter  
To prevent chatter:

- Minimum interval between lines: **20 minutes**  
- Maximum lines per hour: **3**  
- Burst mode disabled  
- Night mode reduces output by 80%  

If multiple events occur, Stack A selects the most “narratable” one.

---

# 🟦 09 — Sandbox Model  
Stack A is isolated by design:

- Runs as a separate user  
- No write permissions  
- No GPIO access  
- No network access  
- No ability to call Stack B  
- No ability to modify Stack C  
- No access to personal data  
- No microphone requirement  

It is a **sealed commentary engine**.

If Stack A fails, B and C continue unaffected.

---

# 🟦 10 — Summary  
Stack A is a harmless linguistic overlay.  
It observes, contextualises, and narrates.  
It never controls, commands, or intervenes.  
It adds personality without adding risk.  
It completes the Edencore organism by giving it a voice that cannot act.

This file defines the canonical flow and sandbox boundaries for Stack A.
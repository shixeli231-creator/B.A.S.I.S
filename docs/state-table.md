# Operating States

The machine relies on a mechanical run-lever and spring-loaded shorting bars. 

| State | Run Lever | Rotor | Capacitors | Gates | Machine Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Off / Safe** | Released | Coasting / Stopped | Shorted (0V) | Closed | Safe, zeroed |
| **Arming** | Engaged | Stabilized | Shorted | Closed | Ready to run |
| **Charging** | Engaged | Stepping | Free (Charging) | One open | Computing |
| **Tripped** | Engaged | Held | Held (at threshold) | Closed | Output active |
| **Reset** | Released | Coasting / Stopped | Shorted (0V) | Closed | Safe, zeroed |

**Fail-Safe Behavior:** 
The machine defaults to the "Off / Safe" state. The run-lever must be physically held or locked into place to allow computation. If power is lost, if the operator walks away, or if the machine takes a heavy physical shock, the lever releases. Springs instantly drop the shorting bars, grounding all capacitors.

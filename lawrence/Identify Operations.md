# Lab Task 5 — Identify Operations

## Smart Museum Artifact Conservation System

The following operations are identified from the given Smart Museum Artifact Conservation System scenario. State names such as `MONITORING`, `CONSERVATION_ACTIVE`, `PROTECTION_MODE`, and `VIBRATION_RESPONSE` are not used as operation names.

| ID | Operation | Purpose |
|---|---|---|
| OP01 | Perform Sensor Self-Check | Verify that all essential sensors are working correctly. |
| OP02 | Check Environmental-Control Devices | Verify that the environmental-control devices are working correctly. |
| OP03 | Register Artifact | Record the artifact identification information when an artifact is placed inside the chamber. |
| OP04 | Load Environmental Profile | Load the required environmental limits for the artifact. |
| OP05 | Check Chamber Door | Check whether the chamber door is closed before active conservation begins. |
| OP06 | Start Conservation | Begin active conservation when the door is closed and the environmental profile is loaded. |
| OP07 | Monitor Temperature | Continuously compare actual temperature with the artifact's permitted range. |
| OP08 | Monitor Humidity | Continuously compare actual humidity with the artifact's permitted range. |
| OP09 | Correct Temperature | Attempt to restore temperature when it moves outside the permitted range. |
| OP10 | Correct Humidity | Attempt to restore humidity when it moves outside the permitted range. |
| OP11 | Verify Environmental Recovery | Confirm through sensor readings that the corrected environmental condition has returned to the permitted range. |
| OP12 | Detect Significant Vibration | Detect vibration that may put the artifact at risk. |
| OP13 | Verify Vibration Stabilization | Confirm that vibration remains below the permitted threshold for the required stabilization period. |
| OP14 | Suspend Conservation Activities | Suspend normal conservation activities when the door is opened or significant vibration is detected. |
| OP15 | Verify Sensor Status | Verify sensor status and environmental conditions before conservation resumes after an interruption. |
| OP16 | Switch to Emergency Power | Switch to the emergency power source when main power is lost, if available. |
| OP17 | Record Power Incident | Record a power-loss incident when emergency power is unavailable. |
| OP18 | Generate Operator Alert | Alert the museum operator when an environmental condition cannot be corrected within the allowed recovery period. |
| OP19 | Confirm Safe Condition | Confirm that the chamber is safe and no active protection response is underway. |
| OP20 | Allow Artifact Removal | Permit artifact removal only after a safe condition has been confirmed. |

## Operation Flow

`Precondition → Operation → Postcondition`

Each operation is completed only when its required preconditions are satisfied, and its result establishes the corresponding postcondition.

# Lab Task 5 — Complete Operation Schema

## Smart Museum Artifact Conservation System

### Operation Schema Format

`Precondition → Operation → Postcondition`

The **Event/Input** identifies what causes or supplies the operation.

| ID | Precondition | Event / Input | Operation | Postcondition |
|---|---|---|---|---|
| OP01 | System is powered on. | Sensor status | Perform Sensor Self-Check | Essential sensors are verified as working, or normal operation cannot begin. |
| OP02 | System is powered on. | Environmental-control device status | Check Environmental-Control Devices | Environmental-control devices are checked before normal conservation operation. |
| OP03 | Artifact is placed inside the chamber. | Artifact identification information | Register Artifact | Artifact identification information is recorded and available for monitoring. |
| OP04 | Artifact has been registered. | Required environmental limits | Load Environmental Profile | The artifact's required environmental profile is available to the system. |
| OP05 | Artifact is inside the chamber. | Chamber door status | Check Chamber Door | The system knows whether the door is closed; active conservation is not started while it remains open. |
| OP06 | Door is closed and the environmental profile is loaded. | Door status + environmental profile | Start Conservation | Normal conservation activities begin. |
| OP07 | Conservation is active. | Temperature sensor reading | Monitor Temperature | Actual temperature is compared with the artifact's permitted range. |
| OP08 | Conservation is active. | Humidity sensor reading | Monitor Humidity | Actual humidity is compared with the artifact's permitted range. |
| OP09 | Temperature is outside the permitted range. | Temperature reading | Correct Temperature | The system attempts to restore the required temperature. |
| OP10 | Humidity is outside the permitted range. | Humidity reading | Correct Humidity | The system attempts to restore the required humidity. |
| OP11 | A temperature or humidity correction has been issued. | New sensor readings + recovery time | Verify Environmental Recovery | The system confirms recovery or begins a protection response if the condition cannot be corrected within the allowed recovery period. |
| OP12 | An artifact is inside the chamber. | Vibration sensor reading | Detect Significant Vibration | Significant vibration is detected and activities that could increase risk are suspended. |
| OP13 | Significant vibration has occurred. | Vibration readings + stabilization period | Verify Vibration Stabilization | Return to normal conservation is allowed only after vibration remains below the permitted threshold for the required stabilization period. |
| OP14 | Conservation is active and a door-open or significant-vibration event occurs. | Door status or vibration event | Suspend Conservation Activities | Normal conservation activities are suspended. |
| OP15 | The chamber door has been closed again after being opened. | Sensor status + environmental readings | Verify Sensor Status | Sensor status and artifact environmental conditions are verified before normal conservation resumes. |
| OP16 | Main power is lost during conservation. | Emergency power availability | Switch to Emergency Power | The system uses emergency power when it is available. |
| OP17 | Main power is lost and emergency power is unavailable. | Power-loss incident | Record Power Incident | The incident is recorded and the system enters a safe shutdown condition. |
| OP18 | An environmental condition cannot be corrected within the allowed recovery period. | Failed recovery condition | Generate Operator Alert | The museum operator is alerted while the artifact is protected. |
| OP19 | Artifact is inside the chamber. | Chamber condition + protection-response status | Confirm Safe Condition | The system confirms that the chamber is safe and no active protection response is underway. |
| OP20 | The system has confirmed a safe chamber condition and no active protection response. | Removal request | Allow Artifact Removal | Artifact removal is permitted. |

## Detailed Operation Schemas

### OP01 — Perform Sensor Self-Check

**Precondition:** System is powered on.  
**Event/Input:** Sensor status.  
**Operation:** Perform a self-check of essential sensors.  
**Postcondition:** Essential sensors are verified as working; normal operation can proceed only when the essential sensors pass the check.

### OP02 — Check Environmental-Control Devices

**Precondition:** System is powered on.  
**Event/Input:** Environmental-control device status.  
**Operation:** Check the environmental-control devices.  
**Postcondition:** The devices have been checked before normal conservation operation.

### OP03 — Register Artifact

**Precondition:** An artifact is placed inside the chamber.  
**Event/Input:** Artifact identification information.  
**Operation:** Record the artifact's identification information.  
**Postcondition:** The artifact information is recorded and the system can monitor the artifact.

### OP04 — Load Environmental Profile

**Precondition:** Artifact information has been recorded.  
**Event/Input:** Required environmental limits.  
**Operation:** Load the artifact's required environmental profile.  
**Postcondition:** Required temperature and humidity limits are available.

### OP05 — Check Chamber Door

**Precondition:** Artifact is inside the chamber.  
**Event/Input:** Door status.  
**Operation:** Check whether the chamber door is closed.  
**Postcondition:** If the door is open, active conservation does not begin; if closed, the system can continue toward active conservation.

### OP06 — Start Conservation

**Precondition:** Door is closed and the artifact's environmental profile is loaded.  
**Event/Input:** Door status and environmental profile.  
**Operation:** Start active conservation.  
**Postcondition:** Normal conservation activities begin.

### OP07 — Monitor Temperature

**Precondition:** Conservation is active.  
**Event/Input:** Temperature sensor reading.  
**Operation:** Compare actual temperature with the permitted range.  
**Postcondition:** The system knows whether temperature is within the permitted range and can initiate correction when required.

### OP08 — Monitor Humidity

**Precondition:** Conservation is active.  
**Event/Input:** Humidity sensor reading.  
**Operation:** Compare actual humidity with the permitted range.  
**Postcondition:** The system knows whether humidity is within the permitted range and can initiate correction when required.

### OP09 — Correct Temperature

**Precondition:** Temperature is outside the permitted range.  
**Event/Input:** Temperature reading and required range.  
**Operation:** Use the environmental-control mechanism to correct temperature.  
**Postcondition:** A temperature correction has been attempted and sensor verification is required.

### OP10 — Correct Humidity

**Precondition:** Humidity is outside the permitted range.  
**Event/Input:** Humidity reading and required range.  
**Operation:** Use the environmental-control mechanism to correct humidity.  
**Postcondition:** A humidity correction has been attempted and sensor verification is required.

### OP11 — Verify Environmental Recovery

**Precondition:** An environmental correction command has been issued.  
**Event/Input:** Updated temperature/humidity readings and recovery time.  
**Operation:** Verify that the environmental condition has actually returned to the permitted range.  
**Postcondition:** If recovery succeeds, normal conditions can continue; if recovery fails within the allowed period, the system protects the artifact and alerts the operator.

### OP12 — Detect Significant Vibration

**Precondition:** An artifact is inside the chamber.  
**Event/Input:** Vibration sensor reading.  
**Operation:** Detect significant vibration.  
**Postcondition:** Activities that could increase risk to the artifact are suspended.

### OP13 — Verify Vibration Stabilization

**Precondition:** Significant vibration has been detected.  
**Event/Input:** Vibration readings and required stabilization period.  
**Operation:** Verify that vibration remains below the permitted threshold.  
**Postcondition:** Normal conservation cannot resume until the required stabilization period has been successfully verified.

### OP14 — Suspend Conservation Activities

**Precondition:** Conservation is active and a door-open or significant-vibration event occurs.  
**Event/Input:** Door status or vibration event.  
**Operation:** Suspend normal conservation activities.  
**Postcondition:** Normal environmental operation remains suspended until the required safety checks are completed.

### OP15 — Verify Sensor Status

**Precondition:** Chamber door has been closed after being opened.  
**Event/Input:** Sensor status and environmental readings.  
**Operation:** Verify sensor status and artifact environmental conditions.  
**Postcondition:** Normal conservation can resume only after the required verification succeeds.

### OP16 — Switch to Emergency Power

**Precondition:** Main power is lost during conservation.  
**Event/Input:** Emergency power availability.  
**Operation:** Switch to the emergency power source when available.  
**Postcondition:** The system uses emergency power.

### OP17 — Record Power Incident

**Precondition:** Main power is lost and emergency power is unavailable.  
**Event/Input:** Power-loss information.  
**Operation:** Record the power incident.  
**Postcondition:** The incident is recorded and the system enters a safe shutdown condition.

### OP18 — Generate Operator Alert

**Precondition:** An environmental condition cannot be corrected within the allowed recovery period.  
**Event/Input:** Failed environmental recovery.  
**Operation:** Generate an alert for the museum operator.  
**Postcondition:** The operator is notified while the artifact remains under protection.

### OP19 — Confirm Safe Condition

**Precondition:** Artifact is inside the chamber.  
**Event/Input:** Chamber condition and protection-response status.  
**Operation:** Verify that the chamber is safe and no active protection response is underway.  
**Postcondition:** A safe condition is confirmed.

### OP20 — Allow Artifact Removal

**Precondition:** The system has confirmed a safe chamber condition and no active protection response is underway.  
**Event/Input:** Artifact removal request.  
**Operation:** Allow the operator to remove the artifact.  
**Postcondition:** Artifact removal is permitted.

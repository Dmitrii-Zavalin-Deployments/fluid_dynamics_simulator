# Fluid Dynamics Simulator: Sovereign Manifests

## 📜 The Sovereign Schema
All manifests in this repository must adhere to the **Sovereign Logic Gate**:
* [**manifest_schema.json**](./manifest_schema.json)

### ⚡ Key Constraint: Time Sovereignty
As of 2026-04, all pipeline steps **must** define `timeout_hours`. 
- This prevents the Engine from "guessing" execution times.
- If a worker exceeds this window without producing an artifact, the Engine will automatically re-trigger the pulse.

## 🏗️ How to Run a Simulation
...
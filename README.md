# Fluid Dynamics Simulator: Sovereign Manifests

## 🔭 Overview
This repository serves as the **Logic Map Store** for the Fluid Dynamics simulation ecosystem. It contains the "Discs" (Manifests) that define the computational pipelines for Navier-Stokes simulations. 

These manifests are consumed by the [Artifact-Driven Simulation Engine](https://github.com/Dmitrii-Zavalin-Deployments/artifact_driven_simulation_engine) to coordinate multi-repository execution.

## 📜 The Sovereign Schema
All manifests in this repository must adhere to the **Sovereign Logic Gate**:
* [**manifest_schema.json**](./manifest_schema.json)

### ⚡ Key Constraint: Time Sovereignty
As of 2026-04, all pipeline steps **must** define `timeout_hours`. 
- This prevents the Engine from "guessing" execution times.
- If a worker exceeds this window without producing an artifact, the Engine will automatically re-trigger the pulse.

## 🏗️ How to Run a Simulation

### 1. Create a Manifest
Draft a new JSON manifest following the schema and place it in the `manifests/` directory.
> **Note:** Ensure all `target_repo` links and file artifacts are precisely named to satisfy the **Forensic Scan**.

### 2. "Insert the Disc"
To trigger the simulation, you must point the **Engine** to your specific manifest. 
1. Go to the [Artifact-Driven Simulation Engine](https://github.com/Dmitrii-Zavalin-Deployments/artifact_driven_simulation_engine) repository.
2. Update the `config/active_disk.json` file with the **Raw URL** of your manifest:

```json
{
    "project_id": "your_project_name",
    "manifest_url": "https://raw.githubusercontent.com/Dmitrii-Zavalin-Deployments/fluid_dynamics_simulator/manifests/your_manifest.json",
    "description": "your project description"
}

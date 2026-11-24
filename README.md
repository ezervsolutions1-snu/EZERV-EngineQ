# EZERV EngineQ

**Design. Experiment. Predict. Optimize.**

EZERV EngineQ is a planned engineering intelligence platform for designing, simulating, evaluating, and improving systems that combine devices, sensors, networks, edge/cloud computing, and AI. It aims to help teams explore configurations systematically, understand trade-offs, predict outcomes, and identify options that satisfy practical constraints.

> **Project status:** This README is based on the project concept and proposed student MVP. Implementation and setup instructions will be added as the software is developed.

## What EngineQ aims to do

- Define a system, its components, controllable factors, constraints, and target responses.
- Generate structured experiments using suitable Design of Computer Experiments (DoCE) methods.
- Run repeatable simulations or controlled tests and capture their inputs and outputs.
- Analyze factor effects, interactions, uncertainty, and trade-offs.
- Train and validate predictive models for untested configurations.
- Recommend configurations using classical optimization methods.
- Explore quantum-assisted optimization for selected small problems and compare it with classical baselines.
- Present results through scenario comparisons, dashboards, and reports.

## Initial demonstration

The proposed first use case is a **simulated smart-irrigation system**. The simulation explores how settings such as sensor sampling interval, transmission interval, processing location, model complexity, network conditions, and data compression affect outcomes such as decision accuracy, latency, energy use, bandwidth, water-use proxy, and reliability.

The student demonstration should use a simulated pump and safe mock device-control API. Any later physical-device demonstration would require manual safeguards and must not be presented as an autonomous safety-critical controller.

## Proposed MVP

The first release is intended to deliver one complete simulated IoT workflow:

1. Configure the system and define at least four controllable factors and three measurable responses.
2. Generate and execute at least one suitable DoCE plan.
3. Analyze results and explain the effects and limitations.
4. Train a predictive model and evaluate it on held-out data against an appropriate baseline.
5. Recommend a configuration using a classical optimization baseline and stated constraints.
6. Compare one small Qiskit Aer optimization experiment with a classical method on the same problem.
7. Show results, predictions, trade-offs, and recommendations in a dashboard and technical report.

## Planned technology

| Area | Proposed tools |
| --- | --- |
| User interface | Streamlit |
| Application/API | Python; FastAPI is optional for the MVP |
| Simulation and data | Python, NumPy, Pandas |
| DoCE and statistics | SciPy, Statsmodels, and pyDOE3 or an equivalent maintained library |
| Prediction | Scikit-learn |
| Classical optimization | SciPy Optimize and suitable evolutionary or multi-objective methods |
| Quantum exploration | Qiskit and Qiskit Aer |
| IoT | Simulated devices first; MQTT/Mosquitto and ESP32 are optional extensions |
| Storage and visualization | SQLite for the MVP; Plotly or Matplotlib |

These are proposed choices, not a statement that the components are already implemented.

## Evaluation principles

- Choose experiment designs that fit the research question, factor types, levels, and run budget.
- Validate predictive models on held-out data and report suitable error metrics and limitations.
- Compare recommendations with a clearly defined baseline and show constraint compliance.
- State whether performance, energy, and cost values are measured, simulated, or estimated.
- Keep quantum-assisted comparisons fair and avoid claims of quantum advantage without rigorous evidence.
- Retain experiment settings, input data, software versions, and seeds where controllable.

## Development status

The project plan proposes a 16-week student MVP, progressing from requirements and simulation through DoCE analysis, prediction, classical optimization, quantum exploration, and integration. Detailed installation, configuration, and contribution instructions will be added when the corresponding code and project tooling are available.

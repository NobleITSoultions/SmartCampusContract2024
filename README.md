
# TALOFNS Fog Node Selection Simulator

This project provides a simulation environment built on top of iFogSim for evaluating various fog node selection strategies, including the proposed **TALOFNS (Trust-Aware Latency-Optimized Fog Node Selection)** algorithm.

## 📁 Project Structure

```
src/
├── org/
│   └── fog/
│       ├── test/                  # MainSimulation.java
│       ├── entities/              # Task.java, FogDeviceFactory.java
│       └── scheduler/             # TALOFNS.java, DRLSelector.java, ...
lib/
└── ifogsim.jar                    # iFogSim core JAR (required)
```

## 🧱 Requirements

- Java 8+
- Maven 3.6+
- Eclipse / IntelliJ (optional for GUI-based development)

## 🛠️ Setup Instructions

1. **Clone or Download this Repository**

2. **Install iFogSim JAR**
   Place `ifogsim.jar` inside the `lib/` directory.

3. **Build with Maven**
   ```bash
   mvn clean compile
   ```

4. **Run Simulation**
   ```bash
   mvn exec:java -Dexec.mainClass="org.fog.test.MainSimulation"
   ```

   > Alternatively, open `MainSimulation.java` in Eclipse/IntelliJ and run directly.

## 🚀 Features

- 12 fog node selection strategies:
  - Random, FirstFit, Proximity, MinMin, RoundRobin, WeightedRoundRobin
  - ReputationBased, FuzzyLogic, QoSAware, AHP-TOPSIS, DRLSelector, TALOFNS

- Metrics:
  - **Average Latency**
  - **Failure Rate**
  - **Trust Violations**

## 📄 Files Description

| File/Class                 | Description |
|---------------------------|-------------|
| `MainSimulation.java`     | Entry point for simulation |
| `PolicySelector.java`     | Dispatches strategy policies |
| `FogDeviceFactory.java`   | Creates test fog nodes |
| `Task.java`               | Represents an offloadable task |
| `<strategy>.java`         | Implements a fog node selection policy |

## 📚 Reference

This simulator supports research based on the TALOFNS algorithm built as an addon for the smart seating system described in:

> Obu, E., Asante, M., & Osei, E. O. (2025). Fog computing-enabled smart seating systems: optimizing latency and network bandwidth efficiency in classrooms. *Advances in Computing and Engineering*, 5(1), 35-49.

---

© 2025. For academic and research use only.

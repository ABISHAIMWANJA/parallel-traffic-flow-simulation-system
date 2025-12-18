# parallel-traffic-flow-simulation-system

This project contains a simple hybrid traffic simulation that combines shared-memory parallelism (OpenMP) with a simulated distributed model for intersections. It was created for *COMP 412 – Parallel and Distributed Systems* to illustrate how road segments and intersections can be processed concurrently.
## Features

- *Parallel road updates* using #pragma omp parallel for to simulate vehicle movement under traffic light control.
- *Intersection handoff* between road segments with basic locking (atomic/critical sections) for safe shared-state updates.
- *Configurable simulation parameters* such as number of roads, intersections, maximum vehicles, and time steps (see traffic_simulation.c).
Requirements

- GCC (or Clang) with OpenMP support
- POSIX-compatible environment (Linux/macOS). The project has been tested on Linux.

## Build & Run

bash
# Compile
gcc traffic_simulation.c -fopenmp -o traffic_simulation

# Execute
./traffic_simulation


Example output:


FINAL TRAFFIC STATE
Road 0: 0 vehicles
Road 1: 0 vehicles
Road 2: 82 vehicles
Road 3: 54 vehicles
Execution Time: 0.104175 seconds


Road 3: 54 vehicles
Execution Time: 0.104175 seconds


## File Structure

 traffic_simulation.c – Complete source for the simulation.
 README.md – Project overview, build/run instructions, and sample output.

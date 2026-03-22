# API Documentation

## `Simulator` Class
The main entry point for the simulation.

### `__init__(config_path: str)`
Initializes the simulator with the specified configuration.

### `run()`
Starts the simulation loop.

### `inject_fault(fault_type: str, target_node: int)`
Injects a runtime fault into the specified node.

## `NetworkEmulation` Module
Handles latency, jitter, and packet loss emulation.

### `set_latency(node_a: int, node_b: int, latency_ms: int)`
Sets the point-to-interconnect latency between two nodes.
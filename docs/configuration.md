# Configuration Reference

DDLSim-Lab is highly configurable via YAML or JSON files.

## Global Settings
- `simulation_mode`: 'bare-metal' or 'virtual'
- `num_nodes`: Integer, number of simulated nodes
- `network_backend`: 'mpi' or 'zeromq'

## Fault Injection Settings
- `latency_ms`: Mean latency in milliseconds
- `jitter_ms`: Jitter in milliseconds
- `packet_loss_percent`: Float (0.0 to 100.0)
- `node_crash_probability`: Float (0.0 to 1.0)

Example `config.yaml`:
```yaml
simulation:
  mode: bare-metal
  nodes: 4
network:
  latency_ms: 15
  packet_loss_percent: 0.1
```
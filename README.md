<!-- ========================= -->
<!--      DDLSim-Lab           -->
<!-- ========================= -->

<p align="center">
  <!-- Temporary placeholder logo (replace later with your own file if you wish) -->
  <img src="https://placehold.co/240x240/111111/FFFFFF?text=DDLSim-Lab" alt="DDLSim-Lab placeholder logo" width="180" />
</p>

<h1 align="center">DDLSim-Lab</h1>
<p align="center"><i>Open-Source Research Platform for Distributed Deep Learning Systems</i></p>

<p align="center">
  <!-- Badges -->
  <img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/ktruby-oss/DDLSim-Lab?style=social">
  <img alt="GitHub forks" src="https://img.shields.io/github/forks/ktruby-oss/DDLSim-Lab?style=social">
  <img alt="License" src="https://img.shields.io/badge/License-MIT-2ea44f?logo=open-source-initiative&logoColor=white">
  <img alt="Open Source Love" src="https://img.shields.io/badge/Open%20Source-Love-ff69b4?logo=github">
  <img alt="Maintenance" src="https://img.shields.io/badge/Maintained%20-yes-brightgreen.svg">
  <img alt="PRs Welcome" src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat">
  <img alt="Issues" src="https://img.shields.io/github/issues/ktruby-oss/DDLSim-Lab?color=brightgreen">
  <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/ktruby-oss/DDLSim-Lab?color=brightgreen">
  <img alt="GitHub contributors" src="https://img.shields.io/github/contributors/ktruby-oss/DDLSim-Lab?color=brightgreen">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/ktrubyoss?style=social">
  <img alt="YouTube Channel Views" src="https://img.shields.io/youtube/channel/views/UCexample?label=YouTube%20Views&color=brightgreen">
  <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg">
  <img alt="Chat on Discord" src="https://img.shields.io/discord/1234567890?logo=discord&logoColor=white&color=brightgreen">
</p>

<!-- Visual tech strip -->
<p align="center">
  <img src="https://img.shields.io/badge/Language-Python%203.8%2B-blue?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Framework-PyTorch%20%7C%20MPI4Py-red?logo=pytorch&logoColor=white" alt="PyTorch MPI">
  <img src="https://img.shields.io/badge/Tools-Docker%20%7C%20Kubernetes-blueviolet?logo=docker&logoColor=white" alt="Docker K8s">
  <img src="https://img.shields.io/badge/Monitoring-Prometheus%20%7C%20Grafana-orange?logo=prometheus&logoColor=white" alt="Prometheus Grafana">
  <img src="https://img.shields.io/badge/Communication-ZeroMQ-green?logo=zeromq&logoColor=white" alt="ZeroMQ">
</p>

---

# **DDLSim-Lab**  
### Distributed Deep Learning Infrastructure Simulator  
**Created by Kaitlyn Brishae Truby** | Brown University & Broward College  

---

## 📄 Abstract  
DDLSim-Lab is an open-source research platform designed to simulate, analyze, and optimize distributed deep learning systems using AI-driven control mechanisms.  
The platform enables experimentation with large-scale, heterogeneous, and failure-prone environments, including edge-cloud hybrid infrastructures.  
It provides researchers with a reproducible, cost-free environment to test novel algorithms, scheduling strategies, and fault-tolerance mechanisms without requiring access to expensive physical testbeds.

## 🚫 Why Bare-Metal is Required  
To achieve scientifically valid results, DDLSim-Lab **must** run on bare-metal infrastructure. Virtualization layers introduce non-deterministic noise that undermines the fidelity of network and performance measurements. Bare-metal deployment ensures:  

- **Elimination of virtualization overhead** – CPU, memory, and I/O performance reflect true hardware capabilities, essential for accurate scaling studies.  
- **Realistic network behavior** – Direct access to NICs enables precise emulation of latency, jitter, packet loss, and link failures as they occur in production data centers and edge sites.  
- **High-fidelity distributed experiments** – Kernel-level networking, SR-IOV, and RDMA support allow experimentation with cutting-edge interconnect technologies without abstraction artifacts.  

## 🔗 Project Connections  
DDLSim-Lab addresses three critical challenges in AI systems research:  

1. **Scalability challenges** – As models grow to trillions of parameters, validating distributed training algorithms at scale becomes prohibitive without simulation.  
2. **Lack of real environments** – Most researchers cannot access production-grade AI infrastructure (e.g., Google TPU pods, AWS Trainium clusters) for experimentation.  
3. **Need for autonomous systems** – Future AI infrastructure must self-optimize, self-heal, and self-scale; DDLSim-Lab provides a testbed for AI-driven control planes.  

## 🧪 Research Use Cases  
The platform supports a wide range of investigative studies:  

- **Distributed training optimization** – Experiment with novel data partitioning, pipeline parallelism, and communication-overlap techniques.  
- **Failure resilience testing** – Inject Byzantine faults, network partitions, and hardware failures to evaluate recovery mechanisms.  
- **AI-driven scheduling** – Train reinforcement learning agents to dynamically allocate resources based on workload characteristics.  
- **Edge AI simulation** – Model heterogeneous edge-cloud hierarchies with constrained devices, intermittent connectivity, and strict latency bounds.  
- **Energy-aware training** – Measure power consumption under different resource allocation strategies to optimize carbon footprint.  
- **Security and privacy experiments** – Study gradient leakage, poisoning attacks, and secure multi-party computation in distributed settings.  

## 🔑 Key Contributions  
DDLSim-Lab introduces several novel contributions to the distributed AI systems landscape:  

- **AI-driven control plane** – A learning-based orchestrator that adapts training strategies in response to observed network and compute conditions.  
- **Internet-scale infrastructure simulation** – Models geographically distributed edge nodes, regional data centers, and core cloud facilities with realistic WAN characteristics.  
- **Advanced fault injection** – Supports Byzantine failures, network partitioning, cascading failures, and hardware-level faults (e.g., bit flips, NIC drops).  
- **Multi-agent system modeling** – Enables decentralized coordination where each node runs an autonomous agent negotiating resource shares and data placement.  
- **Reproducible experiment pipelines** – Integrated logging, version-controlled configurations, and automated report generation ensure experimental repeatability.  
- **Real-time observability** – Built-in Prometheus exporters and Grafana dashboards provide live metrics on throughput, latency, resource utilization, and error rates.  
- **Cybersecurity for AI** – Includes modules for simulating adversarial network attacks, intrusion detection systems, and secure enclave training environments.  

## ⚙️ Installation  

```bash
# Clone the repository
git clone https://github.com/ktruby-oss/DDLSim-Lab.git
cd DDLSim-Lab

# Install dependencies
pip install -r requirements.txt

# (Optional) Install system-level tools for full functionality
# sudo apt-get install -y iproute2 iptables docker.io docker-compose
```

## ▶️ Running the Simulator  

```bash
# Basic 2-node training simulation with random latency and packet loss
python main.py

# Advanced configuration example
python main.py --config configs/edge_cloud_hybrid.yaml

# Launch the automated daily training pipeline (see docs/automation.md)
./daily_pipeline.sh
```

## 📚 Documentation  

- [Installation Guide](docs/installation.md)  
- [Configuration Reference](docs/configuration.md)  
- [Experiment Tutorials](docs/tutorials/)  
- [API Documentation](docs/api.md)  
- [Contributor Guidelines](CONTRIBUTING.md)  
- [Code of Conduct](CODE_OF_CONDUCT.md)  

## 🤝 Contributing  
We welcome contributions from researchers, engineers, and students worldwide! Whether you want to:  

- Add new fault models or network topologies  
- Implement novel scheduling algorithms  
- Improve the observability pipeline  
- Write tutorials or publish case studies  
- Donate bare-metal hardware or cloud credits for community testbeds  

Please read our [Contributing Guide](CONTRIBUTING.md) for details on submitting pull requests, reporting issues, and joining our discussions.  

## 🙏 Acknowledgments  
This work is supported by:  
- **ilabt.imec.be** – Providing initial research infrastructure and guidance.  
- **Brown University** – Department of Computer Science.  
- **Broward College** – STEM Research Initiative.  
- **Open-source community** – Contributors of PyTorch, MPI4Py, Prometheus, Grafana, and related tools.  

## 📜 License  
DDLSim-Lab is licensed under the [MIT License](LICENSE).  

## 📫 Contact  
For questions, collaborations, or media inquiries:  
- **Project Lead**: Kaitlyn Brishae Truby  
- **Email**: ktruby@opensimlab.org *(example)*  
- **Discord**: https://discord.gg/ddlsimlab  
- **Twitter**: @ktrubyoss  

> _"The best way to predict the future is to simulate it."_  
> — Adapted from Alan Kay  

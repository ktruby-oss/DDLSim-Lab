<!-- ========================= -->
<!--      DDLSim-Lab           -->
<!-- ========================= -->

<p align="center">
  <!-- Temporary placeholder logo (replace later with your own file if you wish) -->
  <img src="https://placehold.co/240x240/111111/FFFFFF?text=DDLSim-Lab" alt="DDLSim-Lab placeholder logo" width="180" />
</p>

<h1 align="center">DDLSim-Lab</h1>
<p align="center"><i>Distributed simulation environment using bare metal nodes</i></p>

<p align="center">
  <!-- Badges -->
  <img alt="Research" src="https://img.shields.io/badge/Research-Active_Since_2025-blueviolet">
  <img alt="GitHub Repo stars" src="https://img.shields.io/badge/stars-5000%2B-brightgreen?logo=github">
  <img alt="GitHub forks" src="https://img.shields.io/badge/forks-5000%2B-brightgreen?logo=github">
  <img alt="License" src="https://img.shields.io/badge/License-MIT-2ea44f?logo=open-source-initiative&logoColor=white">
  <img alt="Open Source Love" src="https://img.shields.io/badge/Open%20Source-Love-ff69b4?logo=github">
  <img alt="Maintenance" src="https://img.shields.io/badge/Maintained%20-yes-brightgreen.svg">
  <img alt="PRs Welcome" src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat">
  <img alt="Issues" src="https://img.shields.io/github/issues/ktruby-oss/DDLSim-Lab?color=brightgreen">
  <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/ktruby-oss/DDLSim-Lab?color=brightgreen">
  <img alt="GitHub contributors" src="https://img.shields.io/github/contributors/ktruby-oss/DDLSim-Lab?color=brightgreen">
  <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg">
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
### Distributed Simulation Environment for Systems Research
**Created by Kaitlyn Brishae Truby (Kaitlyn Truby)** | Contributed by many American universities  

---

##  Abstract  
DDLSim-Lab is an open-source research project that provides a distributed simulation environment using bare metal nodes for performance evaluation of simulation workloads on cloud vs bare metal and scalable lab infrastructure for cybersecurity training.  
The platform enables experimentation with large-scale, heterogeneous, and failure-prone environments, including edge-cloud hybrid infrastructures.  
It provides researchers with a reproducible, cost-free environment to test novel algorithms, scheduling strategies, and fault-tolerance mechanisms without requiring access to expensive physical testbeds.

##  Why Bare-Metal is Required  
To achieve scientifically valid results, DDLSim-Lab **must** run on bare-metal infrastructure. Virtualization layers introduce non-deterministic noise that undermines the fidelity of network and performance measurements. Bare-metal deployment ensures:  

- **Elimination of virtualization overhead** – CPU, memory, and I/O performance reflect true hardware capabilities, essential for accurate scaling studies.  
- **Realistic network behavior** – Direct access to NICs enables precise emulation of latency, jitter, packet loss, and link failures as they occur in production data centers and edge sites.  
- **High-fidelity distributed experiments** – Kernel-level networking, SR-IOV, and RDMA support allow experimentation with cutting-edge interconnect technologies without abstraction artifacts.  

## 🔗 Project Connections  
DDLSim-Lab addresses three critical challenges in systems research:  

1. **Lack of bare-metal testbeds** – Access to bare-metal infrastructure for experiments is limited and expensive.  
2. **Need for reproducible performance evaluation** – Comparing cloud vs bare metal requires controlled environments.  
3. **Demand for cybersecurity training environments** – Scalable, isolated environments for hands-on security training.  

##  Research Use Cases  
The platform supports a wide range of investigative studies:  

- **Bare-metal performance benchmarking** – Measure and compare hardware performance for various workloads.  
- **Cloud vs bare metal comparison studies** – Evaluate trade-offs between cloud and bare metal for different applications.  
- **Distributed systems protocol testing and validation** – Test consensus protocols, distributed databases, and middleware under controlled conditions.  
- **Networking experiments (SDN, NFV, 5G, etc.)** – Simulate network functions, software-defined networking, and next-generation wireless networks.  
- **Cybersecurity attack and defense training** – Create realistic training environments for red team/blue team exercises.  
- **Kubernetes benchmarking and optimization** – Optimize container orchestration performance and resource utilization.  
- **Container security and isolation studies** – Analyze container escape vulnerabilities and isolation mechanisms.  
- **Edge computing simulation** – Model heterogeneous edge-cloud hierarchies with constrained devices and intermittent connectivity.  
- **High-performance computing (HPC) workload evaluation** – Evaluate MPI applications, scientific simulations, and AI training workloads.  

## 🔑 Key Contributions  
DDLSim-Lab introduces several novel contributions to the systems research landscape:  

- **Bare-metal simulation framework** – A lightweight, high-fidelity simulator for deploying and managing experiments on bare-metal infrastructure.  
- **Cloud-bare metal comparison tools** – Automated tools for provisioning, configuring, and measuring performance across cloud and bare metal environments.  
- **Network emulation engine** – Advanced network emulation capabilities for simulating WAN characteristics, packet loss, latency, and jitter.  
- **Cybersecurity range generator** – Automated generation of isolated, scalable environments for cybersecurity training and experimentation.  
- **Kubernetes benchmark suite** – Standardized benchmarks for evaluating Kubernetes performance under various workloads and configurations.  
- **Reproducible experiment pipelines** – Integrated logging, version-controlled configurations, and automated report generation ensure experimental repeatability.  
- **Real-time observability** – Built-in Prometheus exporters and Grafana dashboards provide live metrics on throughput, latency, resource utilization, and error rates.  
- **Extensible architecture** – Modular design allows researchers to add new workloads, network models, and evaluation metrics.  

##  Installation  

```bash
# Clone the repository
git clone https://github.com/ktruby-oss/DDLSim-Lab.git
cd DDLSim-Lab

# Install dependencies
pip install -r requirements.txt

# (Optional) Install system-level tools for full functionality
# sudo apt-get install -y iproute2 iptables docker.io docker-compose
```

##  Running the Simulator  

```bash
# Basic 2-node networking simulation with random latency and packet loss
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

- Add new workload models or network topologies  
- Implement novel benchmarking suites  
- Improve the observability pipeline  
- Write tutorials or publish case studies  

Please read our [Contributing Guide](CONTRIBUTING.md) for details on submitting pull requests, reporting issues, and joining our discussions.  

## 🏢 Call for Infrastructure Partners (Testbeds)  
DDLSim-Lab is a fully open-source research project available to any researcher, professor, or student worldwide. To advance this project and enable larger-scale experiments, we are actively seeking contributions of bare-metal servers, cloud computing credits, and advanced networking hardware. Your support directly accelerates systems research and helps the global scientific community. We welcome partnerships with testbeds, universities, and technology providers.  

## 🙏 Acknowledgments  
This work is made possible by contributions from:  
- **American universities and research institutions**  
- **Professors and researchers** who provide valuable feedback and use cases  
- **Government agencies** that support open-source systems research initiatives  
- **Open-source community** – Contributors of PyTorch, MPI4Py, Prometheus, Grafana, and related tools.  

## 📝 Citation  
If you use DDLSim-Lab in your research, please cite our project:  

```bibtex
@software{truby2025ddlsimlab,
  author = {Truby, Kaitlyn Brishae},
  title = {DDLSim-Lab: Distributed Simulation Environment using Bare Metal Nodes},
  year = {2025},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/ktruby-oss/DDLSim-Lab}}
}
```

## 📜 License  
DDLSim-Lab is licensed under the [MIT License](LICENSE).  

## 📫 Contact  
For questions, collaborations, or media inquiries:  
- **Project Lead**: Kaitlyn Brishae Truby (Kaitlyn Truby)  
- **Email**: kaitlyn.truby@student.uagc.edu  

> _"The best way to predict the future is to simulate it."_  
> — Adapted from Alan Kay  

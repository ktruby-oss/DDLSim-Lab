# Installation Guide

## System Requirements
- OS: Linux (Ubuntu 20.04+ recommended) for bare-metal testing
- Python: 3.8 or higher
- Network: Open ports for MPI/ZeroMQ communication

## Basic Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/ktruby-oss/DDLSim-Lab.git
   cd DDLSim-Lab
   ```
2. Create a virtual environment (optional but recommended):
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Advanced Installation (Docker)
For containerized testing:
```bash
docker build -t ddlsim-lab .
docker run -it ddlsim-lab
```
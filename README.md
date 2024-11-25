# Exploring-Software-Defined-Networking-SDN-techniques

## Overview
This project demonstrates the deployment and management of a **binary tree network topology** using **Mininet** and **OpenFlow switches** in a containerized **Google Cloud Platform (GCP)** environment. The network utilizes a **custom MAC learning controller** programmed in Python on the **POX SDN framework** to optimize packet forwarding and reduce network flooding. Additionally, network performance is analyzed and visualized through **iperf** and **ping** to evaluate latency and throughput.

## Features
- **Mininet-based Network Topology**: A scalable binary tree topology with **8 hosts** and **7 switches**.
- **POX SDN Controller**: Custom Python-based MAC learning controller for dynamic packet forwarding and flooding reduction.
- **Traffic Monitoring**: Integrated traffic monitoring features to improve debugging and network visibility.
- **Performance Analysis**: Analyzed and visualized key network metrics, such as **latency** and **throughput**, using **iperf** and **ping**.
- **GCP Deployment**: Deployed in a **containerized** GCP environment for scalable and flexible testing.

## Project Goals
- **Minimize Network Flooding**: Implement MAC learning in the POX controller to reduce unnecessary flooding and improve network efficiency.
- **Optimize Packet Forwarding**: Use dynamic learning of MAC addresses to forward packets more efficiently.
- **Improve Debugging**: Integrate traffic monitoring and performance analysis to enhance the visibility and debugging of network operations.

## Installation

### Prerequisites
- **Mininet**: A network emulator used to create the virtual network topology.
- **POX Controller**: The OpenFlow controller used to manage the network.
- **Google Cloud Platform (GCP)**: For containerized deployment (optional but recommended for scalability).
- **iperf**: A tool for network performance measurement (latency and throughput).
- **Ping**: Used for basic connectivity and latency testing.

### Steps to Set Up
1. **Clone the Repository**:
    ```bash
    git clone https://github.com/your-username/sdn-binary-tree-topology.git
    cd sdn-binary-tree-topology
    ```

2. **Install Mininet**:
    If you haven't already installed Mininet, use the following commands to install it:
    ```bash
    sudo apt-get update
    sudo apt-get install mininet
    ```

3. **Set Up POX Controller**:
    Download and install the POX SDN controller:
    ```bash
    git clone https://github.com/noxrepo/pox.git
    cd pox
    ./pox.py forwarding.l2_learning
    ```

4. **Deploy the Topology**:
    Run the topology script:
    ```bash
    sudo python mytopo.py
    ```

5. **Traffic Analysis**:
    Use `iperf` and `ping` to analyze the network performance (latency and throughput).
    Example:
    ```bash
    iperf -s  # on one host to start the server
    iperf -c <host-ip>  # on another host to start the client
    ```

6. **Containerized Deployment on GCP** (Optional):
    - Deploy Mininet and POX in Docker containers on GCP for scalable and flexible deployment.
    - Set up the required cloud instances and ensure that the necessary ports are open for Mininet and POX communication.

## Project Structure


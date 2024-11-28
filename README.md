
# DPDK Docker Container 

Here's dpdk as a docker.  A containerized and easy to deploy dpdk-in-box.

This repository contains a **Docker image** for **DPDK (Data Plane Development Kit)** version **24.07**, designed to simplify the deployment and testing of DPDK applications in a containerized environment. 

The DPDK container image provides an easy way to get started with high-performance packet processing without the need to install DPDK on your system.

## Features
- **DPDK v24.07**: A powerful library for high-performance packet processing.
- **Ubuntu 20.04 base image**: Reliable, lightweight, and widely used.
- **Pre-configured for DPDK**: The Docker image includes all dependencies to run DPDK applications such as `dpdk-l2fwd`, `dpdk-testpmd`, etc.
- **Customizable**: You can modify the container to suit your specific network interface configurations, applications, and tests.

## Table of Contents
- [Docker Image Details](#docker-image-details)
- [Quick Start Guide](#quick-start-guide)
- [Usage Instructions](#usage-instructions)
  - [Running the Container](#running-the-container)
  - [Running DPDK Applications](#running-dpdk-applications)
  - [Configuring HugePages](#configuring-hugepages)
  - [Binding NICs to DPDK](#binding-nics-to-dpdk)
- [Advanced Usage](#advanced-usage)
  - [Performance Tuning](#performance-tuning)
  - [Multi-Threading](#multi-threading)
- [Contributing](#contributing)
- [License](#license)

## Docker Image Details

- **Repository**: https://hub.docker.com/r/urmsandeep/dpdk-24.07
- **Base Image**: Ubuntu 20.04
- **Image Size**: 1.8 GB
- **Dependencies**: DPDK, build-essential, git, gcc, make, meson, libnuma-dev, libpcap-dev, linux-headers

## Quick Start Guide

1. **Pull the Docker Image**:
   To get started, you can pull the image directly from Docker Hub:
   
   ```
   docker pull urmsandeep/dpdk-24.07

  2. **Run the DPDK Docker Container**:
     Once the image is pulled, you can run it interactively:
     ```
     docker run --rm -it --privileged urmsandeep/dpdk-24.07 /bin/bash
     ```
     The --privileged flag is required for DPDK as it requires access to low-level system resources like network interfaces and HugePages.



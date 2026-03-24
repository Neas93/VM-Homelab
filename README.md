# VM Homelab – Linux, Networking & Security Lab

## Overview

This project showcases a self-built virtual homelab consisting of five Linux virtual machines connected through an isolated internal network.

The lab simulates a small office environment with centralized services, shared storage, and multiple clients with separate access rights. It is used for practicing system setup, networking, database usage, and basic security concepts.

---

## Architecture

* Kali VM – used for controlled testing and enumeration
* Web/App VM – handles application logic and communication
* DB-VM – central server hosting MariaDB and shared storage
* Worker VM 1 (trainnet) – acts both as a network participant and client machine
* Worker VM 2 – simulates a second client with separate permissions

---

## Key Features

* Internal virtual network (isolated lab environment)
* Centralized database (MariaDB)
* Shared folder hosted on DB-VM and accessed remotely via NFS
* Multiple clients with separate access rights
* Service communication between systems

---

## Office Environment Simulation

Two worker machines simulate a small office setup:

* Both connect to shared resources on the DB-VM
* Each operates with separate user permissions
* Demonstrates centralized storage and access control

---

## Security Considerations

The environment is intentionally configured with weak security in some areas to demonstrate common real-world issues.

Examples include:

* Credentials stored in plaintext on client machines
* Password-based access without additional protection

This is done to:

* understand insecure configurations
* observe system behavior
* create a baseline for future improvements

All users and credentials in this project are fictitious and created for demonstration purposes only.

---

## Project Structure

* `/diagrams` – architecture and environment sketches
* `/docs` – detailed explanations of setup and components
* `/screenshots` – images from the lab environment

---

## Diagrams

* [Homelab Overview](Diagrams/homelab-overview.md)
* [Office Environment](Diagrams/office-environment.md)

---

## Documentation

* [VM Breakdown](Docs/vm-breakdown.md)
* [Network Setup](Docs/network-setup.md)
* [Access Rights](Docs/access-rights.md)

---

## Screenshots

(Add your screenshots here to showcase the environment)

---

## Learning Outcome

This project provided hands-on experience with:

* multi-VM environments
* network communication
* database integration
* access control
* system structure and troubleshooting
* understanding insecure vs improved setups

# Installation Notes

## Objective

Build a working Wazuh lab that can ingest real endpoint telemetry from a Windows 11 system and support portfolio-grade screenshots, alert review, and ATT&CK-oriented analysis.

## Build summary

### Hypervisor

- Oracle VirtualBox 7.2.8

### Virtual machines

#### Kali-Lab

- Debian 64-bit profile
- 4 GB RAM
- 2 vCPU
- 60 GB disk
- used as a supporting Linux/security workstation

#### Wazuh-Lab

- Ubuntu Server 24.04.4 LTS
- 8 GB RAM
- 4 vCPU
- 80 GB disk
- bridged networking enabled after initial install

## Wazuh installation path

The Wazuh server, indexer, and dashboard were installed on the Ubuntu VM using the official assisted single-node installer.

High-level process:

1. Install Ubuntu Server on `Wazuh-Lab`
2. Update the system
3. Run the official Wazuh installation assistant
4. Validate the three primary services:
   - `wazuh-manager`
   - `wazuh-indexer`
   - `wazuh-dashboard`
5. Change the VM network from NAT to bridged so the Windows host can reach the dashboard directly
6. Extract generated credentials from `wazuh-install-files.tar`
7. Freeze the Wazuh repository entry after installation to avoid unintended lab upgrades

## Validation

The following outcomes were confirmed:

- dashboard accessible from the Windows host
- Wazuh services present and running
- manager reachable by the Windows agent
- agent enrollment successful

## Notes

- NAT was sufficient for initial installation but not for clean dashboard access from the Windows host
- bridged networking simplified both browser access and agent connectivity
- generated credentials should be stored securely and never committed into documentation or screenshots

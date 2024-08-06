# SOC-architecture

This repo contains a basic infrastructure of a Security Operations Center (SOC) that utilizes multiple tools and technologies to provide a quick and effective response to cybersecurity threats and incidents. This setup helps organizations improve their security posture and provides enhanced control over their attack surface.

## Tools Used

The following free and open-source tools are utilized in this SOC architecture:

- TheHive
- Cortex
- MISP
- Wazuh
- Shuffle

## Architecture Overview

The architecture is easily deployable on any machine. Detailed steps on how to integrate each tool can be found by navigating through the directories. It is recommended to use two machines with at least 16GB of RAM and 4 vCPUs each:

- Machine 1: TheHive, Cortex, MISP
- Machine 2: Wazuh, Shuffle

### Reason for Separation

The separation of tools across two machines is based on their respective resource requirements and roles within the SOC:

- TheHive, Cortex, and MISP: These tools are primarily involved in incident response and threat intelligence. They work closely together, sharing data and processes. Keeping them on the same machine reduces latency and improves efficiency in data handling and incident management.

- Wazuh and Shuffle: Wazuh is responsible for security monitoring and log management, which can be resource-intensive. Shuffle, being a workflow automation tool, integrates with various services, including Wazuh, to automate responses. Placing these tools on a separate machine ensures that the resource-heavy monitoring tasks do not interfere with the incident response and threat intelligence processes.

## Getting Started

Follow the steps in the directories to set up each tool. Ensure you have the necessary hardware specifications to run the tools effectively. For detailed installation and integration instructions, refer to the respective directories of each tool.
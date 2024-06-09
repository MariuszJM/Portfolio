---
layout: post
title: "Setting Up a Private AI System with Ollama and Open WebUI"
author: sal
categories: [AI, AI Server]
image: assets/images/LocalLLMs.png
comments: false
featured: true
---

In today's digital age, data security and autonomy are of utmost importance. Setting up a private AI system allows you to harness the power of artificial intelligence while maintaining control over your data. This guide will walk you through the process of setting up a private AI system compatible with both Linux and Windows 11 Home using WSL 2. We will focus on using Ollama and Open WebUI, two powerful tools that provide robust AI capabilities. Whether you are an AI enthusiast or a professional, this setup ensures that your data remains private and secure.

## System Requirements and Hardware Setup

Before diving into the installation process, it's crucial to understand the system requirements and hardware setup. Having a powerful GPU is essential for running AI models efficiently. Here's a detailed look at the hardware specifications for my setup:

- **Storage:** Lexar NM790 PCIe NVMe 1TB
- **Case:** ENDORFY Arx 700 ARGB
- **Motherboard:** Gigabyte B650 EAGLE AX
- **Processor:** AMD Ryzen 9 7950X3D
- **Graphics Card:** MSI GeForce RTX 4080 SUPER VENTUS 3X OC 16GB DLSS 3
- **Memory:** Kingston Fury Beast Black 64GB [2x32GB 5200MHz DDR5 CL40 DIMM]
- **Cooling System:** ENDORFY Navis F360
- **Power Supply:** Corsair RM1000X SHIFT CP-9020253-EU

This powerful hardware setup ensures that you can run AI models smoothly and efficiently, providing the necessary performance for advanced AI tasks.

## Installing Ollama

Ollama is a versatile AI tool that can be easily installed on Linux/WSL. To install Ollama on Linux/WSL, use the following command:

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

To verify the installation, visit the following URL: http://localhost:11434/. You should see the message: "Ollama is running". This confirmation indicates that Ollama has been successfully installed and is operational.

## Installing Docker (Linux/WSL)

Docker is required to run Open WebUI. Visit the official Docker installation page here and follow these steps to install Docker on Linux/WSL:

```bash
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

## Setting Up Open WebUI

Open WebUI provides a user-friendly interface to manage your AI system. To install it visit the official Open WebUI page here: https://open-webui.io. Use the following command to run Open WebUI in a Docker container:

```bash
docker run -d -p 3000:8080 --add-host=host.docker.internal
-v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui
```

Explanation:

- `docker run -d` runs the container in detached mode.
- `-p 3000:8080` maps port 3000 on your host to port 8080 on the container.
- `--add-host=host.docker.internal:host-gateway` adds an entry to the container's /etc/hosts file.
- `-v open-webui:/app/backend/data` mounts a volume for persistent data storage.
- `--name open-webui` names the container "open-webui".
- `--restart always` ensures the container restarts automatically if it stops.
- `ghcr.io/open-webui/open-webui:main` specifies the image to use.

To log in, visit your localhost at port 3000. When you first log in, you will be prompted to create an admin account. Once logged in, you should see the list of available models and settings for your local setup.

## LAN Configuration

Setting up a LAN allows every member of your household to access the AI system seamlessly, including from smartphones. This setup ensures everyone can benefit from the AI capabilities without compromising data security.

- **Assign a Static IP:** Assigning a static IP to your AI system ensures consistent access within your network. This can typically be done through your router’s settings interface.

- **Setting Up a Proxy for WSL:** If you are using WSL2, you can enable seamless access to WSL services from Windows by setting up a proxy. Run the following command in PowerShell as an administrator:

```PowerShell
netsh interface portproxy add v4tov4 listenport=host_port listenaddress=0.0.0.0 connectport=wsl_port connectaddress=wsl_ip
```

- **Firewall Configuration:** Ensure your firewall allows traffic on the specified host port for LAN access. This setup ensures all devices on your network can securely connect to the AI system.

By following these steps, everyone in your household, including those using smartphones, should have seamless and secure access to the AI system on your LAN.

## Open WebUI Capabilities and Future Plans

Open WebUI offers a range of features and future enhancements that make managing your AI system a breeze:

- **Managing User Permissions and Access Control:** Easily control who can access and use the AI system.
- **Making the AI System Accessible Outside the LAN:** Plans to extend access beyond the local network for remote usability.
- **Adding Fine-Tuned Models for Specialized Tasks:** Enhance your AI capabilities with models fine-tuned for specific tasks.
- **Exploring Integration with Other AI Services Using OpenAI Keys:** Seamlessly integrate with other AI services for expanded functionality.

## Conclusions

In conclusion, setting up a private AI system using Ollama and Open WebUI provides numerous benefits, including enhanced data security and autonomy. This setup empowers you to harness the power of AI while keeping your data private. The detailed hardware specifications and step-by-step installation process ensure a smooth setup experience. By exploring the capabilities and future plans of Open WebUI, you can continue to expand and optimize your AI system. Embrace the potential of private AI and take control of your digital future.

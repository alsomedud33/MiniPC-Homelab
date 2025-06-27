# MiniPC-Homelab
Personal home lab using Proxmox, Jellyfin and Tailscale.

## 🖥️ Home Lab Setup: Proxmox, Jellyfin, NAS & Remote Access via Tailscale

### 📌 Overview
![HomeLab Setup](https://github.com/user-attachments/assets/ebf81ac7-51eb-4ead-8083-9be0c25b8957)
This project is a documention of the setup for my personal home lab using a miniPC and Proxmox VE. My goal was to gain hands-on experience with virtualization, containerization, and self-hosted services while building a functional environment that could act as a LAN-accessible NAS and media server with secure external access.

---
### 🧰 Hardware & Software Used
| Component  | Details |
| ------------- | ------------- |
|MiniPC | Beelink SER5 MAX Mini PC, AMD Ryzen 7 6800U, 32GB RAM, 1TB SSD |
|Hypervisor | Proxmox VE |
|Container OS | Debian LXC |
|Media Server | Jellyfin|
|Remote Access | Tailscale|
|Storage | Local directory shared over LAN|
---
### ⚙️ Setup Summary
1. **Installing Proxmox VE**

    Flashed Proxmox VE ISO onto a USB using Rufus.

    Installed Proxmox onto the miniPC and accessed the web UI from a browser over my Local Network.

    Created a local storage pool for containers and ISOs.
   
3. **Creating Containers**

    Created an LXC container running Debian.

    Installed basic packages (curl, sudo, nano, etc.).

    Configured static IP for easier LAN access.
4. **Setting up Jellyfin**

    I installed Jellyfin inside the container via official repositories.

    Mounted media directories from the host storage.

    Accessed Jellyfin via local IP and completed the default setup process.
5. **Creating a LAN NAS**

    Configured a shared folder on the host using Samba.

    Made it accessible over the network to Windows and Linux devices.

    Set read/write permissions based on use case.
6. **Enabling Remote Access with Tailscale**

    Installed Tailscale inside a container.

    Linked the container to my Tailscale account using tailscale up.

    Verified access from my phone and other devices outside the LAN.

    Secured access using ACLs and Tailscale admin console.
---
### 🔒 Security Considerations

    Used limited-scope containers and strong passwords.

    Disabled unused services.

    Avoided port forwarding in favour of encrypted peer-to-peer access with Tailscale.

    Plan to implement fail2ban and local backups in future iterations.
---
### 💡 Lessons Learned

    Setting up and maintaining a self-hosted environment builds a deeper understanding of networking, storage, and Linux systems.

    Tailscale simplifies secure external access without needing complex firewall or VPN configs.

    Proxmox is a powerful and user-friendly hypervisor that bridges the gap between personal projects and enterprise tools.
---
### 📷 Screenshots (Optional)

(Include screenshots of your Proxmox dashboard, Jellyfin UI, and Tailscale access map here if desired)

---

### 🚀 Future Plans

    Add Docker or Portainer for more container management options.

    Set up a monitoring stack (e.g., Grafana + Prometheus).

    Expand storage with an external drive and explore ZFS.
---
### 📎 Related Skills Gained

    Proxmox VE & virtualization basics

    Linux CLI and service configuration

    Network file sharing (Samba)

    VPN/mesh network access (Tailscale)

    Self-hosting best practices
---
🧑‍💻 About Me

I'm a junior IT engineer based in London with a background in cybersecurity and helpdesk support. I use projects like this to build and apply real-world technical skills while exploring new tools in the IT ecosystem.
---
# ⭐️ If you found this useful or have suggestions, feel free to connect or reach out!

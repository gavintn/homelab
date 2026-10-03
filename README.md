# homelab
Proxmox home server running VMs + containers

## Hardware
- Host: Proxmox VE 9.2 (kernel 7.0.14-pve), UEFI boot
- CPU: Intel Core i5-8400, 6 cores / 6 threads
- RAM: 64 GB (62.7 GiB usable)
- Boot drive: ~94 GiB
- VM/container storage: ZFS
- Typical load: ~8% CPU, ~0.9 load average, ~19 days uptime

## What Proxmox runs
- Modded Minecraft Java server for friends (GregTech modpack), in a dedicated VM
  - 4 vCPUs, 32 GB RAM allocated
  - My friends connect using Prism Launcher with the same modpack
  
## Network setup
- Every device connects over Tailscale. No ports are forwarded on the router,
  so nothing is exposed to the public internet.
- Friends join by accepting a Tailscale invite, then connecting to the
  server's Tailscale address.

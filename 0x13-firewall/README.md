# Firewall Configuration - UFW

This repository contains scripts and configurations for setting up a firewall using `ufw` on `web-01` as part of the `alx-system_engineering-devops` project.

## Tasks

### 0. Block All Incoming Traffic But Mandatory Ports

**File:** `0-block_all_incoming_traffic_but`

**Description:**
Configures `ufw` to block all incoming traffic except for the following TCP ports:

- `22` (SSH)
- `443` (HTTPS SSL)
- `80` (HTTP)

**Commands Used:**

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow 22/tcp
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw enable
```

---

### 1. Port Forwarding

**File:** `100-port_forwarding`

**Description:**
Configures `ufw` to forward port `8080/TCP` to `80/TCP` on `web-01`.

**Steps Taken:**

1. Enable port forwarding by modifying `/etc/ufw/sysctl.conf`:
   ```bash
   sudo sed -i 's/#net.ipv4.ip_forward=1/net.ipv4.ip_forward=1/' /etc/ufw/sysctl.conf
   ```
2. Add a rule in `/etc/ufw/before.rules` before the `*filter` section:
   ```bash
   *nat
   :PREROUTING ACCEPT [0:0]
   -A PREROUTING -p tcp --dport 8080 -j REDIRECT --to-port 80
   COMMIT
   ```
3. Restart `ufw`:
   ```bash
   sudo ufw reload
   ```

---

## Testing

Verify the firewall rules using:

```bash
sudo ufw status verbose
```

Check if port forwarding works:

```bash
curl -sI web-01:8080
```

A successful configuration should return an HTTP `200 OK` response.

---

## Repository Structure

```
0x13-firewall/
├── 0-block_all_incoming_traffic_but
├── 100-port_forwarding
└── README.md
```

## Author

Shighi



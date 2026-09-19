# Deployment & Operations Guide: Product Residue

## 🚀 Live Access & URLs
- **Live Public Access URL:** [/preview/prod-product-residue-1ef938/](/preview/prod-product-residue-1ef938/)
- **Internal Port:** `0`
- **Runtime Engine:** `python_preview`
- **Deployment Status:** `DEPLOYED / ACTIVE`
- **Timestamp:** `2026-09-19T16:46:57.675072+00:00`

## 🛠️ Management & Service Control
### Launch Command
```bash
python3 app.py --port 0
```

### Health Check Probe
```bash
curl -I http://127.0.0.1:0/
```

### Systemd Service Template
```ini
[Unit]
Description=Product Residue Service
After=network.target

[Service]
Type=simple
WorkingDirectory=/tmp/pytest-of-root/pytest-3/test_worktree_zero_residue_cle0/workspaces/prod-product-residue-1ef938
ExecStart=/usr/bin/python3 /tmp/pytest-of-root/pytest-3/test_worktree_zero_residue_cle0/workspaces/prod-product-residue-1ef938/app.py
Restart=always
RestartSec=3

[Install]
WantedBy=multi-user.target
```

## 🔒 Production Security Protocols
- HTTP-only reverse proxy via Nexus Gateway.
- Dedicated port allocation with zero port conflict.

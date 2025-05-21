# check-opnsense

## How to install

SSH into your OPNsense:
```
fetch -o /usr/local/etc/rc.syshook.d/start/99-checkmk_agent https://raw.githubusercontent.com/sibelle-labs/checkmk-opnsense-agent/refs/heads/main/opnsense_checkmk_agent.py
chmod +x /usr/local/etc/rc.syshook.d/start/99-checkmk_agent --restart
/usr/local/etc/rc.syshook.d/start/99-checkmk_agent
```

Ensure you create a packet filter rule to allow connections from your checkmk server to the firewall on port 6556.

# TCP SYN probe mode

This fork keeps the original `tcping` connect-mode behavior by default and adds:

- `--syn`: send raw TCP SYN probes and count SYN-ACK or RST as a response.
- `--raw`: alias for `--syn`.

Example:

```bash
sudo ./tcping --syn --no-color -c 100 -i 0.01 -t 1 118.26.59.219 233
```

The Linux amd64 build artifact is available at:

```text
dist/tcping-linux-amd64-syn
```

Raw SYN mode is intended for Linux node-to-node latency checks and requires root.

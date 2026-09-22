# Homelab Reactive Resume - SOC Lab

## 🔥 Wazuh SIEM - LAB ATIVO (22/09/2026)
- **Status:** 🟢 Active (1) | 397 eventos / 24h
- **Stack:** Docker - wazuh-indexer (OpenSearch 2.16), wazuh-manager, wazuh-dashboard
- **Agente:** phpereira (Ubuntu) - Active
- **Detecções:** Sudo and Sudo Caching, Valid Accounts, Disable or Modify Tools - MITRE ATT&CK
- **Acesso:** https://localhost:443 | admin / SecretPassword

### Evidência
Dashboard com 47 Medium + 315 Low severity, Top agent phpereira

### Como reproduzir
docker compose -f generate-indexer-certs.yml run --rm generator
docker compose up -d
# Deploy agent DEB amd64 com server 192.168.1.4

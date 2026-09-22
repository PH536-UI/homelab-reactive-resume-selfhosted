# Wazuh SIEM - Homelab 4.11.1

SIEM open-source rodando em Docker com 3 containers:
- wazuh-indexer (OpenSearch 2.16)
- wazuh-manager
- wazuh-dashboard

Acesso: https://localhost:443
Login: admin / SecretPassword

## Como subir do zero (o que deu certo)
```bash
git clone https://github.com/wazuh/wazuh-docker.git -b v4.11.1
mv wazuh-docker/single-node wazuh
cd wazuh
docker compose -f generate-indexer-certs.yml run --rm generator
docker compose up -d
```

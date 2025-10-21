# 📚 MIBs para Sophos XGS 128

Esta pasta contém as MIBs SNMP utilizadas para o monitoramento do **Sophos XGS 128**.

---

## 🧠 O que é este arquivo?

O arquivo [`SFOS-FIREWALL-MIB.mib`](./SFOS-FIREWALL-MIB.mib) contém as definições de OIDs usadas pelo firewall Sophos XGS (firmware SFOS).

Ele permite que sistemas de monitoramento como o **Zabbix** interpretem corretamente as métricas e alertas obtidos via **SNMP**.

---

## ⚙️ Como usar

1. Copie o arquivo `.mib` para o diretório de MIBs do seu Zabbix Server ou Proxy, por exemplo:
   ```bash
   sudo cp SFOS-FIREWALL-MIB.mib /usr/share/snmp/mibs/

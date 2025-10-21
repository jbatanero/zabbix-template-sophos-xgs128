# 🧩 Template Zabbix – Sophos XGS 128 (SNMP)

Template desenvolvido para monitoramento do **firewall Sophos XGS 128** via **SNMP**, compatível com **Zabbix 5.x**.

Este template permite acompanhar o desempenho, status e disponibilidade do equipamento diretamente no Zabbix, facilitando o monitoramento proativo da sua infraestrutura.

---

## 📊 Funcionalidades monitoradas

- Utilização de CPU e memória  
- Estado das interfaces de rede  
- Tráfego (in/out) por interface  
- Sessões ativas  
- Estado dos serviços  
- Status de HA (High Availability)  
- Temperatura e estado do sistema  

---

## 🧠 Requisitos

- Servidor Zabbix (ou proxy) com **SNMP habilitado**
- Acesso SNMP configurado no **Sophos XGS 128**
- Importação das **MIBs oficiais da Sophos** (incluídas neste repositório)

---

## ⚙️ Instalação passo a passo

1. **Baixe as MIBs**
   - Local: [`/mibs`](./mibs)
   - Copie o arquivo para o diretório de MIBs do seu servidor Zabbix:
     ```bash
     sudo cp mibs/SFOS-FIREWALL-MIB.mib /usr/share/snmp/mibs/
     sudo service snmpd restart
     ```

2. **Importe o template**
   - No Zabbix, acesse:  
     *Configuration → Templates → Import*
   - Selecione o arquivo [`template_sophos_xgs128.xml`](./template_sophos_xgs128.xml)

3. **Associe o template**  
   - Vá até *Configuration → Hosts*  
   - Edite o host do seu firewall Sophos  
   - Em *Templates*, adicione o “Template Sophos XGS 128 SNMP”

4. **Verifique os dados**  
   - Após alguns minutos, verifique se os itens estão sendo coletados e gráficos gerados.

---

## 🧩 Estrutura do repositório

zabbix-template-sophos-xgs128/
├── template_sophos_xgs128.xml ← Template Zabbix
├── mibs/ ← MIBs oficiais da Sophos
│ ├── SFOS-FIREWALL-MIB.mib
│ └── README.md
├── README.md ← Este arquivo
└── LICENSE ← Licença MIT

---

## ⚠️ Aviso Legal

As MIBs incluídas neste repositório são de propriedade da **Sophos PLC** e são disponibilizadas apenas para fins de integração e estudo.  
Nenhuma informação sensível foi mantida.  
Todos os direitos sobre as MIBs permanecem com a **Sophos Ltd.**

---

## 🪪 Licença

Este projeto é distribuído sob a licença [MIT](./LICENSE).

---

## 💬 Contribuições

Contribuições são bem-vindas!  
Abra uma *issue* ou envie um *pull request* com melhorias, correções ou novos OIDs testados.

---

## 🌐 Recursos úteis

- [Zabbix Share – Templates SNMP](https://share.zabbix.com/)
- [Documentação oficial Sophos XGS (SNMP)](https://docs.sophos.com/)
- [Zabbix SNMP Monitoring Guide](https://www.zabbix.com/documentation/)

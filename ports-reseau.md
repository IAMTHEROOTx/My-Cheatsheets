# 🌐 Liste des Ports Réseau Courants

> Ce fichier référence les ports TCP/UDP les plus utilisés en cybersécurité, avec leurs services associés.  
> Utile pour l’analyse de scans, le hardening réseau ou la création de règles firewall.

---

## 🔒 Ports bien connus (0-1023)

| Port | Protocole | Service | Description |
|------|-----------|---------|-------------|
|21 | TCP | FTP | Transfert de fichiers |
|22 | TCP | SSH | Accès distant sécurisé |
|23 | TCP | Telnet | Accès distant (non sécurisé) |
|25 | TCP | SMTP | Envoi d'e-mails |
|53 | TCP/UDP | DNS | Résolution de noms |
|67 / 68 | UDP | DHCP | Attribution dynamique d’IP |
|80 | TCP | HTTP | Web non sécurisé |
|110 | TCP | POP3 | Récupération de mails |
|123 | UDP | NTP | Synchronisation de l’heure |
|143 | TCP | IMAP | Lecture des mails sur serveur |
|161 / 162 | UDP | SNMP | Supervision réseau |
|389 | TCP/UDP | LDAP | Accès à un annuaire |
|443 | TCP | HTTPS | Web sécurisé (SSL/TLS) |
|445 | TCP | SMB | Partage de fichiers Windows |
|514 | UDP | Syslog | Journalisation à distance |
|3389 | TCP | RDP | Bureau à distance Windows |

---

## 📌 Tips de cybersécurité

- Fermer tous les ports non utilisés dans le firewall.
- Éviter l'exposition des ports critiques à Internet (ex: 22, 3389).
- Scanner son réseau régulièrement avec `nmap -sS -sV -Pn <target>`.

---

## 📚 Références utiles

- [IANA Port Registry](https://www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.xhtml)
- [Nmap Port List](https://nmap.org/book/port-scanning-default.html)

---

> 🛡️ Document à but éducatif. Ne jamais scanner un réseau sans autorisation.

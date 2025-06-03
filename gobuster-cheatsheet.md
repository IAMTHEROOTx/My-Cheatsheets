# 🚪 Cheatsheet Gobuster

Gobuster est un outil rapide de **brute force de répertoires, fichiers ou DNS**. Indispensable pour les pentests web.

---

## 🌐 Scan de répertoires

```bash
gobuster dir -u http://site.com -w /usr/share/wordlists/dirb/common.txt
```

| Option | Description |
|--------|-------------|
| `-u` | URL cible |
| `-w` | Wordlist |
| `-b 403,404` | Ignorer certains codes HTTP |
| `-o result.txt` | Sauvegarder les résultats |

---

## 🧠 DNS brute force

```bash
gobuster dns -d site.com -w /usr/share/wordlists/dns/subdomains-top1million-5000.txt
```

---

## 📌 Tips

- Toujours vérifier les codes retournés (`200`, `403`, etc.)
- Tester plusieurs wordlists (SecLists par ex.)

---

> 🛡️ Ne jamais utiliser sans autorisation sur un site web réel.

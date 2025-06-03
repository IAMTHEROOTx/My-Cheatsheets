# 🐧 Cheatsheet Linux (Pentest & Sécurité)

Commandes Linux utiles en test d'intrusion, post-exploitation ou pour le hardening.

---

## 🔍 Enumération système

```bash
uname -a                      # Infos noyau
whoami                        # Utilisateur courant
id                            # UID / GID
hostname                      # Nom de la machine
```

---

## 🔐 Permissions et escalade

```bash
sudo -l                      # Commandes sudo possibles
find / -perm -4000 2>/dev/null   # Binaries SUID
```

---

## 🗂️ Fichiers sensibles

```bash
cat /etc/passwd
cat /etc/shadow              # Nécessite root
cat ~/.bash_history
ls -la /home/*/.ssh/
```

---

## 🕵️ Reconnaissance réseau

```bash
ip a                         # Interfaces réseau
ip r                         # Routes
netstat -tulnp               # Ports ouverts
```

---

## 📦 Surveillance des processus

```bash
ps aux
top / htop
```

---

## 🔧 Outils pratiques

```bash
which nc / nmap / python     # Vérifier si des outils sont installés
python3 -c 'import pty; pty.spawn("/bin/bash")'   # Pseudo terminal
```

---

## 🔒 Sécurité & durcissement

- Désactiver les services inutiles
- Mettre à jour régulièrement : `apt update && apt upgrade`
- Utiliser `ufw` ou `iptables` pour filtrer les ports
- Changer les ports SSH / activer l'authentification par clé

---

> 🔐 Ces commandes doivent être utilisées dans un cadre légal et encadré.

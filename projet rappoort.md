# Projet VLAN – Cisco Packet Tracer

## 📌 Description
Ce projet a pour objectif de mettre en place et configurer des **VLAN (Virtual Local Area Network)** afin de segmenter un réseau local, améliorer la sécurité et optimiser la gestion du trafic réseau.

La simulation a été réalisée à l’aide de **Cisco Packet Tracer**.

---

## 🎯 Objectifs du projet
- Comprendre le fonctionnement des VLAN
- Créer et configurer plusieurs VLAN
- Attribuer des ports de switch à des VLAN spécifiques
- Configurer les liens **trunk**
- Tester la communication entre les hôtes
- (Optionnel) Mettre en place l’inter-VLAN routing

---

## 🛠️ Outils utilisés
- Cisco Packet Tracer
- Switchs Cisco
- PCs / End Devices
- (Optionnel) Routeur Cisco

---

## 🧱 Topologie du réseau
- Plusieurs VLAN (ex: VLAN 10, VLAN 20, VLAN 30)
- Un ou plusieurs switchs
- Des postes clients répartis par VLAN
- Lien trunk entre les switchs
- (Optionnel) Routeur pour la communication inter-VLAN

---

## 📂 Fichiers du projet
- `Projet_VLAN_amine1.pkt` : Fichier Cisco Packet Tracer contenant la topologie et les configurations

---

## ⚙️ Configuration principale

### Création des VLAN
```bash
vlan 10
name ADMIN
vlan 20
name TECH
vlan 30
name GUEST

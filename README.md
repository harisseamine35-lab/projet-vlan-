# Conception et Déploiement d’une Infrastructure Réseau Multisite

Ce projet présente la conception et la simulation d’une infrastructure réseau multisite robuste réalisée sous **Cisco Packet Tracer**. [cite_start]L'architecture intègre la segmentation logique, la haute disponibilité et l'interconnexion WAN. [cite: 5]

## 📋 Présentation du Projet
* [cite_start]**Module** : Réseaux Informatiques [cite: 1]
* [cite_start]**Date** : 07 janvier 2026 [cite: 2]
* [cite_start]**Étudiant** : Haress El Mostafa Amine [cite: 3]
* [cite_start]**Encadrant** : Prof. Azeddine KHIAT [cite: 4]

## 🎯 Objectifs Principaux
* [cite_start]**Segmentation logique** : Séparation des flux par VLANs pour optimiser la sécurité et la performance. [cite: 7]
* [cite_start]**Haute disponibilité** : Mise en place de l'agrégation de liens via **EtherChannel** entre les commutateurs. [cite: 8]
* [cite_start]**Routage Inter-VLAN** : Implémentation de l’architecture **Router-on-a-Stick**. [cite: 9]
* [cite_start]**Interconnexion WAN** : Configuration d’un routage statique entre le siège et deux sites distants. [cite: 10]

## 🛠️ Architecture Technique

### 1. Plan d'adressage (Siège)
[cite_start]Le réseau du siège utilise un adressage en `/28` avec la passerelle configurée sur le routeur R1. [cite: 12, 19, 20]

| VLAN | Usage | Réseau IP | Passerelle (R1) |
| :--- | :--- | :--- | :--- |
| 10 | Utilisateurs 1 | 172.18.10.0/28 | 172.18.10.14 |
| 20 | Utilisateurs 2 | 172.18.20.0/28 | 172.18.20.14 |
| 30 | Utilisateurs 3 | 172.18.30.0/28 | 172.18.30.14 |
| 50 | VLAN Natif | 172.18.50.0/28 | 172.18.50.14 |
| 60 | Admin/Gestion | 172.18.60.0/28 | 172.18.60.14 |

[cite_start][cite: 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36]

### 2. Configuration Commutation
* [cite_start]**EtherChannel** : Agrégation LACP sur les ports Fa0/21 et Fa0/22 pour la redondance et l'augmentation de la bande passante. [cite: 40]
* [cite_start]**Trunking** : Mode Trunk activé avec le VLAN 50 défini comme VLAN natif. [cite: 41]

### 3. Routage et WAN
* [cite_start]**Inter-VLAN** : Configuration de sous-interfaces dot1q sur le routeur R1. [cite: 45]
* **Liaisons WAN** : 
    * [cite_start]R1-R2 : 10.0.30.176/30 [cite: 38]
    * [cite_start]R1-R3 : 10.0.30.180/30 [cite: 39]
* **Stratégie de routage** :
    * [cite_start]R1 utilise des routes statiques pour joindre les sites distants. [cite: 48]
    * [cite_start]R2 et R3 utilisent des routes par défaut (0.0.0.0/0) vers R1. [cite: 49]

## ✅ Validation de la Connectivité
La connectivité a été vérifiée avec succès via :
* [cite_start]**Ping Inter-VLAN** : Communication établie entre les différents sous-réseaux (ex: VLAN 10 vers VLAN 20). [cite: 53]
* [cite_start]**Traceroute** : Confirmation du passage des paquets par les routeurs intermédiaires vers les sites distants. [cite: 54]
* [cite_start]**Gestion** : Accès distant réussi à l'interface de gestion du commutateur S2. [cite: 55]

## 📂 Contenu du Dépôt
* `rapport_vlan.odt` : Rapport détaillé du projet.
* `simulation_packet_tracer.pkt` : Fichier de simulation Cisco Packet Tracer (si disponible).

---
[cite_start]*Ce projet démontre une infrastructure réseau d'entreprise moderne alliant segmentation, fiabilité et interconnexion efficace.* [cite: 65, 66]

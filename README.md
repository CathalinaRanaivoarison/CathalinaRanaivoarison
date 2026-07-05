## Hello 👋 I'm Cathalina Ranaivoarison

![Profile Views](https://komarev.com/ghpvc/?username=CathalinaRanaivoarison)
![GitHub followers](https://img.shields.io/github/followers/CathalinaRanaivoarison?style=social)

### DevOps & Cloud Engineer 🚀

DevOps & Cloud Engineer specializing in infrastructure automation, CI/CD, Kubernetes, Terraform and AWS.

Passionate about building scalable cloud platforms, automating deployments and improving system reliability through DevOps practices.

### 🛠️ Tech Stack

![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/-Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Terraform ](https://img.shields.io/badge/-Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Ansible](https://img.shields.io/badge/-Ansible-EE0000?style=flat-square&logo=ansible&logoColor=white)
![Jenkins](https://img.shields.io/badge/-Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
![GitLab](https://img.shields.io/badge/-GitLab-FCA121?style=flat-square&logo=gitlab&logoColor=white)
![CI/CD](https://img.shields.io/badge/-CI%2FCD-4285F4?style=flat-square&logo=google-cloud&logoColor=white)
![AWS](https://img.shields.io/badge/-AWS-232F3E?style=flat-square&logo=amazon-aws&logoColor=white)
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Shell](https://img.shields.io/badge/-Shell-4EAA25?style=flat-square&logo=gnu-bash&logoColor=white)

---

## 💻 Featured Projects

### Eiko – Citizen Engagement Platform (40,000+ Users)

Production migration and operation of a Strapi/PostgreSQL platform hosted on OVH Cloud.

#### Achievements

- Migrated production workloads from O2Switch to OVH VPS
- Deployed and operated Production and Staging environments using Docker Compose
- Secured PostgreSQL access through SSH tunnels and role-based access control
- Implemented observability with Prometheus and Grafana
- Automated deployment and operational workflows
- Created technical documentation and operational procedures

**Tech Stack:** Docker • PostgreSQL • Strapi • Nginx • Grafana • Prometheus • Linux • Git • DNS

# 📱 Étude de Cas : Migration Cloud & Sécurisation d'une API Mobile (40k+ Utilisateurs)

## 📌 Présentation du Projet
Migration réussie d'une infrastructure backend d'un hébergement mutualisé historique (O2Switch) vers un environnement Cloud dédié et conteneurisé (VPS OVH). L'enjeu majeur était d'isoler les environnements de Production/Staging et de sécuriser les accès de l'équipe Data, le tout avec **zéro interruption de service** pour les utilisateurs de l'application mobile.

---
🖼️ [INSÈRE ICI TON SCHÉMA GRAPHIQUE EXCALIDRAW AVEC LES DEUX SERVEURS ET LES TUNNELS]
---

## 🎯 Problématiques & Défis Techniques
*   **Limitation technique :** L'hébergement mutualisé initial limitait la scalabilité et ne permettait pas une isolation propre des environnements.
*   **Sécurité des données :** L'équipe Data avait besoin d'un accès direct à la base de données pour leurs outils d'analyse (ex: BigQuery) sans pour autant exposer les ports PostgreSQL publiquement sur Internet.
*   **Continuité d'activité :** Assurer le routage pour l'application mobile tout en maintenant temporairement les e-mails et le site vitrine sur l'ancien hébergeur.

## 🚀 Solutions et Architecture Implémentées

### 1. Conteneurisation et Isolation (Docker)
Conception d'une architecture multi-conteneurs via **Docker Compose** permettant d'isoler hermétiquement l'environnement de Production et l'environnement de Staging. Chaque environnement possède son instance PostgreSQL et son instance Strapi dédiée.

### 2. Routage et Sécurisation des Flux (Nginx)
Déploiement d'un reverse proxy **Nginx** faisant office de point d'entrée unique et sécurisé (HTTPS via certificats automatisés **Let's Encrypt**). Nginx intercepte et distribue le trafic vers les bons conteneurs en fonction des sous-domaines.

### 3. Gestion du Routage Hybride (DNS)
Mise en place d'une transition douce en séparant les flux réseau : le trafic de l'application mobile pointe vers le nouveau VPS OVH, tandis que la vitrine web et la messagerie restent transitoirement gérées par l'ancien hébergeur.

### 4. Accès Data Sécurisé (Tunnel SSH & RBAC)
Pour ouvrir un accès sécurisé à la Data Team sans compromettre la base de données :
*   Fermeture complète des ports PostgreSQL sur l'extérieur.
*   Création d'un utilisateur système dédié, restreint aux **tunnels SSH** avec authentification obligatoire par **clés de sécurité (Ed25519/RSA)**.
*   Configuration de privilèges stricts au niveau de la base de données (**Lecture seule / RBAC**) limités aux tables strictement nécessaires à l'analyse.

## 📊 Métriques & Impact Business
*   **100% de disponibilité (Zero-Downtime) :** Aucune coupure constatée pour les utilisateurs lors de la bascule de l'API.
*   **Sécurité durcie :** Suppression des mots de passe pour les accès serveurs et isolation complète des bases de données.
*   **Observabilité :** Intégration d'une stack de supervision (Prometheus/Grafana) pour suivre l'état de santé du serveur.

---

## 💼 Professional Highlights

- Automated infrastructure management for 3,000+ servers using Ansible
- Built and optimized CI/CD pipelines with GitLab CI and Jenkins
- Deployed and operated containerized workloads with Docker and Kubernetes
- Implemented monitoring solutions with Grafana, Prometheus and Zabbix
- Automated cloud infrastructure provisioning with Terraform and AWS

---

### Kubernetes CI/CD Platform

Deployment of containerized applications using Kubernetes, Jenkins and Docker.

**Tech Stack:** Kubernetes, Jenkins, Docker, GitHub Actions

---

### Infrastructure Automation

Automation of cloud infrastructure provisioning and configuration.

**Tech Stack:** Terraform, Ansible, AWS

---

### Repositories 🔭

- [Docker Deployments](https://github.com/CathalinaRanaivoarison/Docker)
- [Kubernetes Projects](https://github.com/CathalinaRanaivoarison/Kubernetes)
- [Jenkins CI/CD Pipelines](https://github.com/CathalinaRanaivoarison/Jenkins)
- [Ansible Automation](https://github.com/CathalinaRanaivoarison/Ansible)
- [Terraform AWS Infrastructure](https://github.com/CathalinaRanaivoarison/Terraform)

---
## 🎓 Certifications & Learning

- AWS Certified DevOps Engineer – Professional (in progress)
- Certified Kubernetes Administrator (CKA) (in progress)

---

## 📫 Contact

📧 cathalinaranaivoarison@gmail.com

💼 [LinkedIn](https://www.linkedin.com/in/cathalina-ranaivoarison-ingenieur-devops-cloud-cdi-paris)

📍 Paris, France

---

## ⚡ Fun Fact

I enjoy building automated cloud infrastructures and transforming manual operations into reliable CI/CD pipelines.











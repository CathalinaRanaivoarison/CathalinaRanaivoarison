## Hello 👋 I'm Cathalina Ranaivoarison

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

## Présentation du Projet

Production migration and operation of a Strapi/PostgreSQL platform hosted on OVH Cloud.

#### Achievements

- **Migration sans interruption (Zero-Downtime) :** Migration réussie des charges de travail de production critiques d'un hébergement mutualisé historique (O2Switch) vers un VPS dédié OVH Cloud, sans aucune coupure pour les utilisateurs actifs de l'application mobile.
- **Conteneurisation et Isolation :** Conception, déploiement et isolation complète des environnements de Production et de Staging via Docker Compose et un reverse proxy Nginx sécurisé (certificats SSL automatisés Let's Encrypt).
- **Automatisation & CI/CD :** Conception et mise en œuvre de pipelines d'intégration et de déploiement continus (CI/CD) pour automatiser les flux de travail opérationnels, les déploiements de l'API et la gestion des builds.
- **Sécurisation des accès Data :** Mise en place d'un accès sécurisé par tunnels SSH (authentification par clés Ed25519/RSA sans mot de passe) combiné à un contrôle d'accès basé sur les rôles (RBAC) PostgreSQL pour fournir à l'équipe Data un accès strict en lecture seule au niveau des tables.
- **Observabilité et Supervision :** Configuration d'une stack Prometheus et Grafana pour le suivi des métriques système en temps réel et la création de dashboards de performance.
- **Excellence Opérationnelle :** Rédaction de la documentation technique de référence, automatisation des sauvegardes (dumps DB) et définition des procédures opérationnelles de reprise sur sinistre (rollback).
  
---
![Schéma d'Architecture](Architecture.png)
---

## Problématiques & Défis Techniques
*   **Limitation technique :** L'hébergement mutualisé initial limitait la scalabilité et ne permettait pas une isolation propre des environnements.
*   **Sécurité des données :** L'équipe Data avait besoin d'un accès direct à la base de données pour leurs outils d'analyse (ex: BigQuery) sans pour autant exposer les ports PostgreSQL publiquement sur Internet.
*   **Continuité d'activité :** Assurer le routage pour l'application mobile tout en maintenant temporairement les e-mails et le site vitrine sur l'ancien hébergeur.(Migration total à venir)

## Métriques & Impact Business
*   **100% de disponibilité (Zero-Downtime) :** Aucune coupure constatée pour les utilisateurs lors de la bascule de l'API.
*   **Déploiements accélérés et fiabilisés :** L'intégration du pipeline CI/CD sécurise les mises à jour et réduit drastiquement le droit à l'erreur humaine en production.
*   **Sécurité durcie :** Suppression des mots de passe pour les accès serveurs et isolation complète des bases de données.
*   **Observabilité :** Intégration d'une stack de supervision (Prometheus/Grafana) pour suivre l'état de santé du serveur en temps réel.

**Tech Stack:** Docker • PostgreSQL • Strapi • Nginx • Grafana • Prometheus • Linux • Git • DNS

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











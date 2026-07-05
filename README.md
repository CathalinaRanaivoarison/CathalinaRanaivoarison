### Cathalina Ranaivoarison


### Ingénieur DevOps & Cloud

Ingénieur DevOps & Cloud spécialisé dans l'automatisation d'infrastructures, la CI/CD, Kubernetes, Terraform et AWS.

Passionné par la conception de plateformes cloud scalables, l'automatisation des déploiements et l'amélioration de la fiabilité des systèmes grâce aux pratiques DevOps.

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

## 💻 Projets

#### Eiko – Citizen Engagement Platform (40,000+ Users)

## Présentation du Projet

Migration d'infrastructure mobile : transition d'un hébergement mutualisé historique (O2Switch) vers une architecture Cloud conteneurisée sur VPS OVH.

## Réalisations

- **Migration sans interruption (Zero-Downtime) :** Migration des charges de travail backend depuis un hébergement mutualisé (O2Switch) vers un VPS dédié OVH, opérée sans aucune coupure de l'API ni dégradation de l'expérience utilisateur sur mobile.
- **Conteneurisation et Isolation :** Conception, déploiement et isolation complète des environnements de Production et de Staging via Docker Compose et un reverse proxy Nginx sécurisé (certificats SSL automatisés Let's Encrypt).
- **Automatisation & CI/CD :** Conception et mise en œuvre de pipelines d'intégration et de déploiement continus (CI/CD) pour automatiser les flux de travail opérationnels, les déploiements de l'API et la gestion des builds.
- **Sécurisation des accès Data :** Mise en place d'un accès sécurisé par tunnels SSH (authentification par clés Ed25519/RSA sans mot de passe) combiné à un contrôle d'accès basé sur les rôles (RBAC) PostgreSQL pour fournir à l'équipe Data un accès strict en lecture seule au niveau des tables.
- **Observabilité et Supervision :** Configuration d'une stack Prometheus et Grafana pour le suivi des métriques système en temps réel et la création de dashboards de performance.
- **Excellence Opérationnelle :** Rédaction de la documentation technique de référence, automatisation des sauvegardes (dumps DB) et définition des procédures opérationnelles de reprise sur sinistre (rollback).

## Architecture

![Schéma d'Architecture](Architecture.png)

## Problématiques & Défis Techniques

*   **Limitation technique :** L'hébergement mutualisé initial limitait la scalabilité et ne permettait pas une isolation propre des environnements.
*   **Sécurité des données :** L'équipe Data avait besoin d'un accès direct à la base de données pour leurs outils d'analyse (ex: BigQuery) sans pour autant exposer les ports PostgreSQL publiquement sur Internet.
*   **Continuité d'activité :** Assurer le routage pour l'application mobile tout en maintenant temporairement les e-mails et le site vitrine sur l'ancien hébergeur.(Migration total à venir)

## Métriques & Impact Business

*   **100% de disponibilité (Zero-Downtime) :** Aucune coupure constatée pour les utilisateurs lors de la bascule de l'API.
*   **Déploiements accélérés et fiabilisés :** L'intégration du pipeline CI/CD sécurise les mises à jour et réduit drastiquement le droit à l'erreur humaine en production.
*   **Sécurité durcie :** Suppression des mots de passe pour les accès serveurs et isolation complète des bases de données.
*   **Observabilité :** Intégration d'une stack de supervision (Prometheus/Grafana) pour suivre l'état de santé du serveur en temps réel.

**Tech Stack du projet:** Docker • PostgreSQL • Strapi • Nginx • Grafana • Prometheus • Linux • Git • DNS

---
#### Pipeline CI/CD & Infrastructure as Code - IC GROUP

## Presentation du Projet

La société **IC GROUP** a mis en place un site web vitrine (développé en Python/Flask) permettant d'accéder à ses deux applications phares :
1. **Odoo 13.0 (Communautaire)** : Intégrant un système de LMS pour la diffusion des formations internes.
2. **pgAdmin4** : Pour l'administration graphique de la base de données PostgreSQL d'Odoo.

### Architecture Cible
Pour répondre aux contraintes de performances et d'isolation, l'infrastructure est segmentée sur **03 serveurs distincts** déployés sur AWS (compatibles avec l'offre gratuite AWS Free Tier) :
* **Serveur 1 (t2.medium)** : Dédié à l'orchestration CI/CD avec **Jenkins**.
* **Serveur 2 (t2.micro)** : Héberge l'application web **Site Vitrine** (port 8080) et **pgAdmin4** (port 5050).
* **Serveur 3 (t2.micro)** : Héberge l'application **Odoo 13.0** et sa base de données **PostgreSQL** (port 8069).

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











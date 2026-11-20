### Cathalina Ranaivoarison


### Ingénieure DevOps & Cloud

Ingénieure DevOps & Cloud spécialisée dans l'automatisation d'infrastructures (Ansible, Terraform), la CI/CD (GitLab CI, Jenkins) et la conteneurisation.

Passionnée par l'industrialisation des déploiements, la fiabilité des systèmes et la transmission des bonnes pratiques DevOps.

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

# 💻 Projet 1

## Eiko – Application mobile d'engagement citoyen

### Présentation du projet

**Eiko** est une application mobile qui aide les familles et les colocations à adopter des éco-gestes au quotidien ([eiko-responsable.org](https://www.eiko-responsable.org/)). Elle compte aujourd'hui **187 comptes** et s'appuie sur :

* **Strapi :** CMS headless qui expose l'API consommée par l'application mobile.
* **PostgreSQL 15 :** base de données relationnelle qui stocke les données utilisateurs et le suivi des challenges.

L'objectif était de migrer le backend d'un hébergement mutualisé (**O2Switch**), trop limité, vers un **VPS OVH** dédié, puis de construire une infrastructure conteneurisée, fiable et sécurisée : environnements Production et Staging séparés, déploiements automatisés et accès sécurisés pour l'équipe Data. La bascule s'est faite **sans coupure de service** pour les utilisateurs.

### Réalisations

- **Migration sans interruption :** bascule du backend Strapi et de la base PostgreSQL d'O2Switch vers un VPS OVH, sans coupure de l'API pour les utilisateurs mobiles.
- **Conteneurisation et séparation des environnements :** Production et Staging isolés avec Docker Compose, derrière un reverse proxy Nginx avec certificats SSL/TLS Let's Encrypt renouvelés automatiquement.
- **Pipeline CI/CD GitLab :** tests, build et déploiement, avec déploiement automatique en Staging et en Production à la demande.
- **Sécurisation des accès à la base :** accès via tunnels SSH (authentification par clés, sans mot de passe), aucun port PostgreSQL exposé sur Internet, comptes en lecture seule et séparation des droits pour l'équipe Data.
- **Supervision adaptée à une petite équipe :** disponibilité et expiration des certificats (UptimeRobot), ressources du serveur (Beszel), surveillance des tâches planifiées (Healthchecks.io), alertes centralisées sur Discord.
- **Exploitation et documentation :** sauvegardes automatisées de la base, procédure de retour arrière, documentation d'architecture et procédures pour l'onboarding des équipes.
- **Plan de sortie de l'ancien hébergeur :** audit des DNS, domaines, messagerie et services hérités.

### Architecture

![Schéma d'architecture](Architecture.png)

### Problématiques et défis techniques

* **Limites de l'hébergement mutualisé :** pas d'isolation possible entre environnements et peu de contrôle sur le serveur.
* **Sécurité des données :** l'équipe Data avait besoin d'accéder à la base depuis ses outils d'analyse, sans exposer PostgreSQL publiquement.
* **Continuité de service :** basculer l'API de l'application mobile tout en maintenant temporairement la messagerie et le site vitrine chez l'ancien hébergeur (migration complète à venir).

### Résultats

* **Aucune coupure constatée** pour les utilisateurs pendant la bascule de l'API.
* **Déploiements fiabilisés :** le pipeline CI/CD supprime les manipulations manuelles et limite les erreurs en production.
* **Sécurité renforcée :** plus de mot de passe pour les accès serveur, base de données non exposée, droits séparés.
* **Visibilité sur l'état du service :** alertes en temps réel sur la disponibilité, les certificats, les ressources et les tâches planifiées.

**Tech Stack du projet :** Docker • Docker Compose • PostgreSQL • Strapi • Nginx • GitLab CI • Linux • SSH • Git • DNS • OVH

---
# 💻 Projet 2 [IC_Project](https://github.com/CathalinaRanaivoarison/IC_Project)

## IC GROUP – Chaîne CI/CD Jenkins et Infrastructure as Code sur AWS

### Présentation du projet

**IC GROUP** dispose d'un site vitrine en Python/Flask qui sert de point d'entrée vers deux applications internes :

1. **Odoo 13.0 (Community)** : ERP configuré avec son module LMS (Learning Management System) pour la gestion des formations internes.
2. **pgAdmin4** : interface d'administration de la base PostgreSQL d'Odoo.

L'objectif était de provisionner l'infrastructure sur AWS avec Terraform, d'automatiser l'installation et le déploiement des applications avec Ansible, et d'orchestrer l'ensemble dans un pipeline Jenkins : build, tests, publication de l'image et déploiement. Les applications sont réparties sur **3 instances EC2** pour séparer les charges.

### Réalisations

* **Infrastructure as Code (Terraform) :** provisionnement du réseau (VPC, subnet), de 3 instances EC2 (`t3.small` pour Jenkins, `t3.micro` pour les applications), d'un Security Group par serveur et de la paire de clés SSH. L'image Ubuntu 22.04 LTS la plus récente est sélectionnée automatiquement depuis l'éditeur officiel (Canonical), sans identifiant d'AMI codé en dur.
* **Provisioning (Ansible) :** playbook d'installation de Docker et Docker Compose sur des instances vierges (`provision.yml`), playbook de déploiement des applications (`deploy.yml`) et inventaire des serveurs.
* **Rôles Ansible réutilisables :** `odoo_role` et `pgadmin_role` (structure `defaults` / `tasks` / `templates`), qui génèrent les fichiers Docker Compose à partir de templates Jinja2 : volumes persistants, réseaux et noms de services paramétrables.
* **Conteneurisation :** Dockerfile de l'application Flask. Les URLs d'Odoo et de pgAdmin sont passées par variables d'environnement (`ODOO_URL`, `PGADMIN_URL`), et la version est extraite avec `awk` d'un fichier de configuration central (`releases.txt`).
* **Pipeline CI/CD Jenkins déclaratif (Jenkinsfile) :**
  1. **Lecture de `releases.txt`** : version et URLs extraites avec `awk`, arrêt du pipeline si une valeur manque.
  2. **Qualité du code** : analyse du Dockerfile (Hadolint) et du code Python (Flake8).
  3. **Build de l'image** avec Docker Buildx et arguments de build (version, URLs).
  4. **Tests** : lancement du conteneur dans un réseau Docker dédié, test HTTP avec `curl` (plusieurs tentatives) et vérification du contenu de la page.
  5. **Publication** sur Docker Hub d'une image multi-architecture (`linux/amd64`, `linux/arm64`), taguée avec la version.
  6. **Déploiement Ansible** conditionné par un paramètre du pipeline et bloqué si des URLs de démonstration sont encore présentes.
* **Gestion des secrets :** identifiants Docker Hub, clé SSH, inventaire et mot de passe Ansible Vault stockés dans les credentials Jenkins. Fichiers temporaires supprimés automatiquement en fin d'étape.

### Architecture

L'infrastructure est répartie sur **3 instances EC2** :

* **Serveur 1 (t3.small) :** Jenkins, pour l'orchestration CI/CD.
* **Serveur 2 (t3.micro) :** site vitrine (port 8080) et pgAdmin4 (port 5050).
* **Serveur 3 (t3.micro) :** Odoo 13.0 (port 8069) et sa base PostgreSQL.

Les 3 instances tournent sous Ubuntu 22.04 LTS, dans un même subnet, chacune avec son propre Security Group.

### Problématiques et défis techniques

* **Séparation des charges :** Odoo et PostgreSQL consomment beaucoup de ressources. Les isoler sur un serveur dédié évite qu'ils dégradent le site vitrine et pgAdmin.
* **Déploiements paramétrables :** pouvoir changer les URLs de redirection ou la version de l'application en modifiant uniquement `releases.txt`, sans toucher au code source.
* **Portabilité :** rôles Ansible indépendants du fournisseur cloud, réutilisables sur d'autres serveurs Linux (on-premise par exemple) en changeant seulement l'inventaire et les variables.

### Résultats

* **Déploiement entièrement automatisé :** d'une instance vierge à l'application fonctionnelle, sans action manuelle, avec des playbooks idempotents (relançables sans effet de bord).
* **Contrôle qualité dans le pipeline :** si l'analyse du code ou les tests échouent (application qui ne répond pas, contenu attendu absent, valeur manquante dans `releases.txt`), le pipeline s'arrête avant la publication et le déploiement.
* **Aucun secret dans le code :** tous les accès passent par les credentials Jenkins et Ansible Vault.
* **Nouvelle version en une modification :** passer de la v1.0 à la v1.1 se fait en changeant la version dans `releases.txt` puis en relançant le pipeline.

### Évolutions prévues

* Déploiement d'Odoo, PostgreSQL et pgAdmin sur un cluster Kubernetes (Minikube).

**Tech Stack du projet :** AWS EC2 • Terraform • Ansible • Ansible Vault • Jenkins • Docker Buildx • Hadolint • Flake8 • Docker • Docker Compose • Python (Flask) • Odoo 13 • PostgreSQL • pgAdmin4 • Linux (Bash/Awk) • Git

---

## 🔭 Dépôts GitHub
- [Jenkins CI/CD Pipelines](https://github.com/CathalinaRanaivoarison/flask-jenkins-pipeline)
- [IC_Project](https://github.com/CathalinaRanaivoarison/IC_Project)
- [Docker Static Website ](https://github.com/CathalinaRanaivoarison/docker-static-website)
- [Docker Deployments](https://github.com/CathalinaRanaivoarison/Docker)

---
## 🎓 certifications

- AWS Solutions Architect – Associate (in progress)
- Certified Kubernetes Administrator (CKA) (in progress)

---

## 📫 Contact

📧 cathalinaranaivoarison@gmail.com

💼 [LinkedIn](https://www.linkedin.com/in/cathalina-ranaivoarison-ingenieur-devops-cloud-cdi-paris)

📍 Paris, France

---

##  Ce qui me motive

Transformer des opérations manuelles en déploiements automatisés et fiables.













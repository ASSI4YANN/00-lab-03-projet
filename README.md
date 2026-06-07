#  Dockerisation de l'application student_list de l'entreprise POZOS

## 1. Présentation du projet

Ce projet a pour objectif de mettre en place une architecture complète basée sur **Docker** afin de déployer une application composée de :

- Un frontend web en **PHP**
- Une API backend en **Flask (Python)**
- Un **Docker Registry privé**
- Une orchestration avec **Docker Compose**

L’objectif est de comprendre la conteneurisation, la communication entre services et le déploiement reproductible.

---

## 2. Technologies utilisées

- Docker
- Docker Compose
- Flask (Python)
- PHP (Apache)
- Docker Registry
- Linux / Terminal

---

## 3. Architecture

```text
Frontend PHP
      |
      v
Flask API (student-list)
      |
      v
Docker Registry (images privées)

---

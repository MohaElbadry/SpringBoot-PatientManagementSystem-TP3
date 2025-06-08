# Hospital Management System

<p align="center">
  <img src="https://img.shields.io/badge/Spring%20Boot-3.4.3-brightgreen" alt="Spring Boot Version"/>
  <img src="https://img.shields.io/badge/Java-21-orange" alt="Java Version"/>
  <img src="https://img.shields.io/badge/MySQL-Database-blue" alt="Database"/>
  <img src="https://img.shields.io/badge/JPA-Hibernate-green" alt="JPA"/>
</p>

<p align="center">
Une application basée sur Spring Boot qui implémente un système de gestion hospitalière permettant de gérer les patients, les consultations et les dossiers médicaux.</p>

## Technologies Utilisées

- Java 21
- Spring Boot 3.4.3
- Spring Data JPA
- Spring Web MVC
- MySQL
- Maven
- Lombok

## Fonctionnalités

### Gestion des Patients

- Création, lecture, mise à jour et suppression des dossiers patients
- Informations patient comprenant :
  - Nom (4-40 caractères)
  - Date de naissance
  - État de santé (malade/non malade)
  - Score
- Support de la pagination
- Recherche par nom du patient

### Modèle de Données

- **Patient** : Informations personnelles du patient
  - Nom
  - Date de naissance
  - État de santé
  - Score
- **Consultation** : Détails des consultations médicales
- **Rendez-vous** : Gestion des rendez-vous patients

### Fonctionnalités Techniques

- Interface utilisateur intuitive avec Thymeleaf
- Validation des données
- Pagination et recherche avancée
- Gestion des erreurs

## Configuration

### Base de données

La configuration de la base de données se trouve dans `src/main/resources/application.properties`. Voici un exemple de configuration :

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/hospital_db
spring.datasource.username=root
spring.datasource.password=root
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect
```

### Prérequis

- Java 21 ou supérieur
- Maven 3.x
- MySQL 8.0 ou supérieur
- Votre IDE préféré (Spring Tool Suite, IntelliJ IDEA, ou VS Code)

## Installation et Démarrage

1. Cloner le dépôt :

```bash
git clone https://github.com/MohaElbadry/SpringBoot-PatientManagementSystem-TP3.git
```

2. Naviguer vers le répertoire du projet :

```bash
cd Hospital_mvc
```

3. Configurer la base de données MySQL :

   - Créer une base de données nommée `hospital_db`
   - Vérifier les paramètres de connexion dans `application.properties`

L'application sera accessible à l'adresse : `http://localhost:8080`

## Structure du Projet

```text
src/
├── main/
│   ├── java/
│   │   └── com/
│   │       └── example/
│   │           └── hospital_mvc/
│   │               ├── HospitalMvcApplication.java
│   │               ├── entities/
│   │               │   └── Patient.java
│   │               ├── repositories/
│   │               │   └── PatientRepository.java
│   │               └── web/
│   │                   └── PatientController.java
│   └── resources/
│       ├── application.properties
│       ├── templates/
│       └── static/
└── test/
    └── java/
        └── com/
            └── example/
                └── hospital_mvc/
                    └── HospitalMvcApplicationTests.java
```

## Base de Données

- L'application utilise MySQL comme système de gestion de base de données
- Les tables sont créées automatiquement au démarrage grâce à JPA/Hibernate
- Vous pouvez accéder à la base de données via :
  - MySQL Workbench
  - phpMyAdmin
  - Ligne de commande MySQL

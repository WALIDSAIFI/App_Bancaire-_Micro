# Projet Bancaire - Microservices avec Spring Boot & React.js

## 📌 Description
Ce projet consiste en la modernisation d'une infrastructure IT bancaire en développant une application backend basée sur une architecture **microservices**. L'application gère les **clients** et leurs **comptes bancaires** (courant et épargne) via des **API REST**, avec une interface frontend développée en **React.js**.

## 🏗️ Architecture du Projet
L'architecture repose sur plusieurs microservices :

### **Backend - Spring Boot & Spring Cloud**
- **customer-service** : Gestion des clients
- **account-service** : Gestion des comptes bancaires
- **gateway-service** : API Gateway pour acheminer les requêtes
- **discovery-service** : Service de découverte basé sur **Eureka**
- **config-service** : Service de configuration centralisée (Git)
- **auth-service** *(Bonus)* : Service de gestion de l'authentification JWT

### **Frontend - React.js & TypeScript**
- Application **Single Page (SPA)**
- Gestion des routes avec **React Router**
- Communication avec le backend via **Axios**
- Interface utilisateur moderne avec **Material-UI**

## 📂 Structure du Projet
```
📦 banking-microservices
 ┣ 📂 customer-service
 ┣ 📂 account-service
 ┣ 📂 gateway-service
 ┣ 📂 discovery-service
 ┣ 📂 config-service
 ┣ 📂 auth-service (Bonus - Sécurité JWT)
 ┣ 📂 frontend (React.js & TypeScript)
 ┗ 📜 docker-compose.yml
```

## ⚙️ Technologies Utilisées
### **Backend**
- **Spring Boot**
- **Spring Cloud (Eureka, Config, Gateway)**
- **Spring Data JPA (PostgreSQL/MySQL)**
- **Spring Security & JWT** *(Bonus)*
- **RestTemplate & OpenFeign** (Communication inter-services)
- **Docker & Docker Compose**
- **JUnit & Mockito (Tests Unitaires)**

### **Frontend**
- **React.js avec TypeScript**
- **React Router** (Navigation)
- **Axios** (Requêtes API)
- **Material-UI** (Interface Utilisateur)

## 🚀 Installation & Exécution
### **1️⃣ Prérequis**
- **Java 17**
- **Maven**
- **Node.js & npm**
- **Docker & Docker Compose**

### **2️⃣ Cloner le Projet**
```sh
git clone https://github.com/WALIDSAIFI/App_Bancaire-_Micro
cd App_Bancaire-_Micro
```

### **3️⃣ Lancer les Microservices**
> Exécutez chaque microservice individuellement ou utilisez **Docker Compose**.

#### **Exécution via Maven**
```sh
cd customer-service && mvn spring-boot:run
cd ../account-service && mvn spring-boot:run
cd ../gateway-service && mvn spring-boot:run
cd ../discovery-service && mvn spring-boot:run
cd ../config-service && mvn spring-boot:run
```

#### **Exécution via Docker Compose**
```sh
docker-compose up --build
```

### **4️⃣ Lancer le Frontend**
```sh
cd frontend
npm install
npm start
```

## 📌 API Endpoints
### **Customer Service** (`/customers`)
- `POST /customers` : Ajouter un client
- `GET /customers` : Lister les clients
- `GET /customers/{id}` : Rechercher un client

### **Account Service** (`/accounts`)
- `POST /accounts` : Créer un compte
- `GET /accounts/{id}` : Consulter un compte
- `GET /accounts/client/{clientId}` : Lister les comptes d'un client


---
👨‍💻 *Développé par SAIFI WALID*

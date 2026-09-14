# FitFlow Redesign

## IT3060 - Human Computer Interaction

**Sri Lanka Institute of Information Technology**

This repository contains the technology stack, architecture and supporting documentation for the FitFlow redesign developed for IT3060 Human Computer Interaction, Semester 2 2026.

## Project Overview

FitFlow is a fitness application redesign focused on improving nutrition logging, personalised workout planning, progress visibility and optional social engagement.

The proposed redesign is based on the findings and requirements developed during the previous laboratory exercises.

## Technology Stack

| Area               | Selected Technology      |
| ------------------ | ------------------------ |
| Frontend           | React Native             |
| Backend            | Node.js + NestJS         |
| Primary Database   | PostgreSQL               |
| Real-time Features | Firebase Firestore       |
| Notifications      | Firebase Cloud Messaging |
| Authentication     | Firebase Authentication  |
| AI Service         | Python + FastAPI         |
| Caching            | Redis                    |

## Repository Structure

```text
fitflow-redesign/
│
├── frontend/
│   └── React Native frontend
│
├── backend/
│   └── NestJS backend API
│
├── ai-service/
│   └── Python-based AI microservice
│
├── docs/
│   ├── Technology stack documentation
│   ├── Comparison matrix
│   ├── Architecture documentation
│   ├── Architecture diagram
│   └── Architecture Decision Record
│
├── README.md
└── .gitignore
```

## Main Features Supported by the Proposed Architecture

* Personalised workout plans
* Editable AI-generated workout plans
* Nutrition tracking
* Progress dashboard
* Optional social features
* Real-time updates
* Push notifications
* Trainer-client interaction

## Architecture

The proposed architecture separates the mobile frontend, core backend API, AI service, relational database, caching layer and Firebase real-time services.

The detailed architecture and Architecture Decision Record are available in the `docs` folder.

## Documentation

The `docs` folder contains:

* Technology stack comparison
* Weighted decision matrix
* Recommended technology stack
* High-level architecture
* Architecture diagram
* Architecture Decision Record (ADR)

## Project Status

This repository contains the technology and architecture documentation for the IT3060 Lab Exercise 05 practical activity. The application itself is not implemented as part of this laboratory exercise.

## Author

**K.A.K. Dilhara**
Student ID: **IT23815964**
BSc (Hons) in Information Technology
Sri Lanka Institute of Information Technology

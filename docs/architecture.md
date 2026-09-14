# FitFlow High-Level Architecture

## Architecture Overview

The proposed FitFlow architecture consists of a React Native client, NestJS backend API, separate AI microservice, PostgreSQL database, Redis caching layer and Firebase services.

## Main Components

### React Native Client

Provides the mobile interface for:

* Home dashboard
* AI workout planner
* Nutrition logging
* Progress tracking
* Community features

### NestJS Backend

Handles:

* API requests
* Authentication token verification
* Business logic
* User and workout data
* Nutrition data
* Trainer relationships
* Communication with the AI service

### AI Microservice

A Python-based service responsible for:

* Personalised workout plan generation
* Nutrition analysis
* AI-assisted recommendations

### PostgreSQL

Stores structured application data including:

* User profiles
* Workout plans
* Workout history
* Nutrition records
* Trainer-client relationships

### Redis

Provides caching for frequently requested information such as progress summaries.

### Firebase

Firebase provides:

* Authentication
* Firestore real-time functionality
* Push notifications through Firebase Cloud Messaging

## Data Flow: Personalised Workout

1. The user enters fitness goals and other information.
2. The React Native application sends the request to the NestJS API.
3. NestJS authenticates the request.
4. Relevant information is stored in PostgreSQL.
5. NestJS sends the required information to the AI service.
6. The AI service generates a candidate workout plan.
7. The result is returned to NestJS.
8. The plan is stored in PostgreSQL.
9. The plan is returned to the application.
10. The user or authorised trainer can edit the plan.

## Data Flow: Social Sharing

1. The user opts into social features.
2. Social content is stored using Firebase Firestore.
3. Firestore real-time listeners provide updates to subscribed users.
4. Firebase Cloud Messaging provides push notifications when required.
5. Users who opt out do not subscribe to the relevant social listeners.

## Data Flow: Nutrition Tracking

1. The user captures or selects a food image.
2. The application sends the information to the NestJS API.
3. NestJS sends the required information to the AI service.
4. The AI service estimates food and nutrition information.
5. The result is returned to NestJS.
6. The confirmed information is stored in PostgreSQL.
7. Nutrition information contributes to progress calculations.
8. Frequently requested progress data can be cached using Redis.

## Security

The proposed architecture includes:

* Server-side Firebase token verification
* Role-based access control
* TLS for data in transit
* Encryption of sensitive information at rest
* Input validation
* API rate limiting
* Restricted access to health and fitness data
* Controlled trainer access
* Data export and deletion mechanisms

## Scalability

The architecture supports scalability through:

* Horizontal scaling of the NestJS API
* PostgreSQL scaling and read replicas when required
* Independent scaling of the AI service
* Redis caching
* Firebase-managed real-time services

## Architecture Decision

The architecture follows the recommended technology stack from Activity 3.

The main reason for using PostgreSQL together with Firebase is to combine strong relational data management for core FitFlow information with Firebase's strengths in real-time social functionality.

The architecture diagram is provided separately as `architecture-diagram.png`.

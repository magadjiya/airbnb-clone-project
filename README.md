# AirBnB Clone Project - Backend

This Airbnb Clone project aims to simulate the development of the booking platform Airbnb, which is a essentially a service platform that allows users to book accomodation from natives of a region. Users can view property listings, make online payments, give ratings, as well as reserve accomodation for a certain amount of days/weeks in advance. This project will ensure an efficient and optimised system. Here is the official [Airbnb site](https://www.airbnb.com/) for those interested.

## Table Of Content
- [Project Goals](#project-goals)
- [Team Roles](#team-roles)
- [Technology Stack](#technology-stack)
- [Database Design](#database-design)
- [Feature Breakdown](#feature-breakdown)
- [API Security](#api-security)
- [CI/CD Pipelines](#cicd-pipeline)

## Project Goals

*TL;DR manage users, properties, bookings, payments, reviews optimally.*

**User Management**: Implement a secure system for user registration, authentication, and profile management.

**Property Management**: Develop features for property listing creation, updates, and retrieval.

**Booking System**: Create a booking mechanism for users to reserve properties and manage booking details.

**Payment Processing**: Integrate a payment system to handle transactions and record payment details.

**Review System**: Allow users to leave reviews and ratings for properties.

**Data Optimization**: Ensure efficient data retrieval and storage through database optimizations.

## Team Roles

*TL;DR Be the sort of engineer that people would love to work with.*

**Project manager (PM)**: Ensures that the project stays on track and all neccesary resources are allocated.

**Business Analyst**: Translates customer business needs into requirements.

**Product Owner**: Holds responsibility for a product vision and evolution.

**Backend Developer**: Responsible for implementing API endpoints, database schemas, and business logic.

**Frontend Developer**: Builds and maintains the user-facing interface, integrating with backend APIs.

**Database Administrator**: Manages database design, indexing, and optimizations.

**DevOps Engineer**: Handles deployment, monitoring, and scaling of the backend services.

**QA Engineer**: Ensures the backend functionalities are thoroughly tested and meet quality standards.

## Technology Stack

*TL;DR django + REST framework, GraphQL, Docker, Git, Celery, PostgreSQL, Redis, CI/CD pipelines*

**Django**: A high-level Python web framework used for building the RESTful API.

**Django REST Framework**: Provides tools for creating and managing RESTful APIs.

**PostgreSQL**: A powerful relational database used for data storage.

**GraphQL**: Allows for flexible and efficient querying of data.

**Celery**: For handling asynchronous tasks such as sending notifications or processing payments.

**Redis**: Used for caching and session management.

**Docker**: Containerization tool for consistent development and deployment environments.

**CI/CD Pipelines**: Automated pipelines for testing and deploying code changes.

## Database Design

*TL;DR we have users, listings, payments, reviews, and bookings*

**Users**: Register new users, authenticate, and manage user profiles.

**Properties**: Create, update, retrieve, and delete property listings.

**Bookings**: Make, update, and manage bookings, including check-in and check-out details.

**Payments**: Handle payment transactions related to bookings.

**Reviews**: Post and manage reviews for properties.

## Feature Breakdown

*TL;DR: The Airbnb Clone project connects users, properties, and bookings through secure APIs (OpenAPI, Django REST, GraphQL), enabling authentication, property management, booking, payments, and reviews, while maintaining fast performance via database indexing and caching.*

**API Documentation**: An API (Application Programming Interface) is how systems communicate with each other. For this project, we will need to keep a manual for other developers, which is our API documentation and we'll use three tools for this.

1. **Open API Standard**: This is the most widely used format for API documentation out there, it is standardised so other developers can quickly integrate, share, test and work with it.

2. **Django REST Framework**: Django REST (Representational State Transfer) Framework is a web extension that makes it easy to have structured endpoints that handle viewing data, deleting, updating, or creating it. So by using it via the web, it makes sure that for properties and data, we have the CRUD (Create, Read, Update, Delete) functionalities.

3. **GraphQL**: This lets us get specific data from requests, instead of getting the whole list when we use REST frameworks, GrapHQL offers an efficient query mechanism for interacting with the backend.

**User Authentication**: Users get to register on the platform and authenticate; their data or recently viwed properties, previously rented properties is also saved.

**Property Management**: Platform users or home owners have the ability to create, retrieve, update and delete property listings.

**Booking System**: Users can book accomodation and pay for it beforehand. Users can also book several properties as long as they pay for all. They can equally update, change bookings and view check-ins/check-outs.

**Payment Processing**: Users can make payments in advamce via the internet no matter their local currency. The Payment code will have the ability to convert currencies using a self updating currency tracker.

**Review System**: Users are able to rate accomadation on a scale of 1-5 after having used them. They can also rate home owners who perhaps have multiple offerings.

**Database Optimizations**: Making searching and features fast, efficient and not lagging due to bulk numbers. Using indexing (giving specific places, locations to look for data) and caching(keeping frequently searched data close-by so that system doesn;t have to do a deep dive on every new request).

## API Security

**Authentication**: This is creating a means of verifying user identity, we can use a token-based system that gives new users a unique token and each time they log in, they do so with this token.

**Authorization**: Setting permissions for certain features, for example, users can view accomodation, but can't edit them. Hosts can add, edit and delete their listings.

**Rate Limiting**: How many requests a user can make in a certain amount of time. If they make too much, put a stopping/block/redirect mechanism in place.

**Input Validation**: Validate data types, eg names must not be numbers but text and so on.

**Data Encryption**: For passwords, payment tokens and other sensitive data, never store them in plaintext, always encrypt. Django automatically does this in most cases.

**Error Handling and Logging**: Send generic error messages if anything wrong happens, redirect the log detailed ones to only the team.

**Cross Origin Resource Sharing**: Explicitly allow trusted origins for your APIs, in case of backend and frontend being different.

## CI/CD Pipeline

*TL;DR these are the processes a site or application goes through before it goes live, is deployed*

1. **Github Actions**: Automate tests, linting, migrations, and Docker builds each time you push new code.

2. **Docker**: A bundle environment that provides an ideal space for making apps that would run on any platform, thus eliminating the "it runs on my computer tho".

3. **Deployment Platform**: The pipeline can push the latest containerized version here for production. Using Render / Railway / Heroku.

~ Made with [Readme.so](https://readme.so/fr/editor)
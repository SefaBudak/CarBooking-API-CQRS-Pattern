# .NET Car Rental API with Onion Architecture & CQRS

This project is a comprehensive Car Rental/Booking API developed with **.NET 8**, showcasing modern software architecture and design patterns. The primary goal is to provide a clean, maintainable, and scalable backend solution for a vehicle rental system.

## Project Purpose and Problem Solved

The main objective of this project is to implement a backend system using **Onion Architecture** to ensure a highly decoupled and testable codebase. It addresses the common challenges in monolithic applications by separating business logic from infrastructure concerns. By using the **CQRS (Command Query Responsibility Segregation)** pattern, the application separates read and write operations, allowing for independent scaling and optimization of each.

## Core Features

- **Onion Architecture:** A clean and dependency-inverted structure that keeps the core business logic independent of external frameworks and technologies.
- **CQRS & Mediator Pattern:** Efficiently manages application commands (e.g., creating a booking) and queries (e.g., listing available cars) using the MediatR library.
- **Secure Authentication (JWT):** User authentication and authorization are handled using JSON Web Tokens (JWT), ensuring secure API endpoints.
- **Real-Time Communication (SignalR):** Implements real-time features, such as instant notifications for booking status changes.
- **Fluent Validation:** Provides a clean and structured way to handle request model validation before they reach the business logic.
- **Repository Pattern:** Abstracts the data layer, making it easy to switch between different data sources.

## Tech Stack & Design Patterns

- **Backend:** .NET 8, C#, ASP.NET Core API
- **Architecture:** Onion Architecture
- **Design Patterns:** CQRS, Mediator, Repository Pattern
- **Authentication:** JWT (JSON Web Tokens)
- **Real-time:** SignalR
- **Validation:** FluentValidation
- **Database:** Microsoft SQL Server
- **ORM:** Dapper / Entity Framework (Projenin kullandığına göre birini seçebilir veya ikisini de yazabilirsin)

## Architectural Diagram

Here is a simplified diagram representing the Onion Architecture used in this project. All dependencies flow towards the center (Domain), ensuring the core logic is isolated.

![Architectural Diagram](https://i.imgur.com/vH1tWnU.png)
*(Not: Bu link, mimariyi temsil eden genel bir şema görselidir. Dilersen kendin `draw.io` gibi bir araçla çizip linki güncelleyebilirsin.)*

## Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/SefaBudak/CarBooking-API-CQRS-Pattern.git](https://github.com/SefaBudak/CarBooking-API-CQRS-Pattern.git)
    ```
2.  **Configure Database Connection:**
    -   Open the `appsettings.json` file in the `Core.WebAPI` project.
    -   Update the `DefaultConnection` string with your SQL Server details.
3.  **Run Migrations (if using Entity Framework):**
    -   Open the Package Manager Console.
    -   Select the `Persistence` project as the default project.
    -   Run `update-database`.
4.  **Run the application:**
    -   Set `Core.WebAPI` as the startup project and run it.
    -   The application will launch, and you can access the API endpoints via Swagger UI.

## Acknowledgment & Personal Note

The foundational concepts and structure of this project were inspired by the "Asp.Net Core Api 8.0 Onion Architecture ile BookCar Projesi" course on Udemy by Murat Yücedağ. Building upon the excellent principles taught in the course, I have further developed and customized the project by [Buraya kendi eklediğin 1-2 küçük detayı yazabilirsin, örneğin: "adding custom logging features and optimizing specific queries"] to solidify my understanding and showcase my skills.

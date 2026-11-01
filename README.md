# Hospital Management System Backend

Spring Boot monolithic backend for the Hospital Management System.

## Structure

- entity
- repository
- service
- service/serviceimpl
- controller
- security
- config

## Roles

ADMIN, DOCTOR, NURSE, RECEPTIONIST, PATIENT, PHARMACIST, LAB_INCHARGE, BED_INCHARGE

## Database

PostgreSQL database: `hospital_management_db`

Default local configuration:
- Host: `localhost`
- Port: `5432`
- Username: `postgres`
- Password: `postgres` (change this to your local PostgreSQL password)

The datasource is configurable with environment variables:
- `DATABASE_URL` (default: `jdbc:postgresql://localhost:5432/hospital_management_db`)
- `DATABASE_USERNAME` (default: `postgres`)
- `DATABASE_PASSWORD` (default: `postgres`)

Create the database before starting the application:
```sql
CREATE DATABASE hospital_management_db;
```

Java 17 is configured in Maven, Eclipse/STS project settings, and Docker.

## Run

1. Open as a Maven project in Eclipse/STS/IntelliJ.
2. Make sure PostgreSQL is running.
3. Set `DATABASE_USERNAME` and `DATABASE_PASSWORD` if your local credentials differ.
4. Run HospitalManagementSystemApplication.java.

Swagger:
http://localhost:8080/swagger-ui.html

Register:
POST /auth/register

Login:
POST /auth/login

After login, use the returned JWT in Swagger Authorize:
Bearer <token>

Note:
This ZIP provides the complete project structure and the core authentication/user workflow. Additional role-specific business methods can be expanded as the frontend/API requirements are implemented.

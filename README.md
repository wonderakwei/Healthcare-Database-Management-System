# Healthcare Database Management System

## Background

The Healthcare Database Management System addresses the complex needs of healthcare organizations, offering a comprehensive solution for patient records, appointments, medical staff, and inventory management. Leveraging PostgreSQL, PgAdmin, and Docker, this project ensures data integrity, security, and compliance with healthcare regulations.

## Problem Statement

Healthcare organizations face challenges in efficiently managing patient information, appointments, staff schedules, and medical supplies. This project aims to provide a robust and secure database system that streamlines healthcare operations, adheres to regulations, and enhances overall efficiency.

## Database Requirements

### Key Entities:

1. **Patient Information:**
   - Patient ID
   - Name
   - Date of Birth
   - Contact Details
   - Medical History
   - Current Treatments

2. **Appointments:**
   - Appointment ID
   - Patient ID (foreign key)
   - Doctor ID (foreign key)
   - Appointment Date and Time
   - Purpose of Visit

3. **Staff:**
   - Staff ID
   - Name
   - Specialty
   - Contact Information
   - Working Hours

4. **Inventory Management:**
   - Item ID
   - Name
   - Quantity Available
   - Reorder Level

5. **Department:**
   - Department ID
   - Department Name
   - Department Head (Staff ID)

6. **Doctor-Patient Relationship:**
   - Relationship ID
   - Doctor ID (foreign key)
   - Patient ID (foreign key)

### Business Rules and Constraints:

- Each patient has a unique Patient ID.
- Date of Birth must be a past date.
- Each appointment is uniquely identified by an Appointment ID.
- Each appointment must have a valid Patient ID and Doctor ID.
- Staff members can be assigned to multiple departments, but there must be one primary department.
- Each medical supply item has a unique Item ID.
- Quantity Available must be a non-negative number.
- A patient can have multiple doctors, and a doctor can treat multiple patients.

## Deliverables

1. **Comprehensive Database Design:**
   - Developed a thorough database design tailored for the healthcare domain, covering patient records, appointments, medical staff, and departmental management.

2. **Dockerized Environment:**
   - Implemented a Dockerized environment for the healthcare database, enabling seamless deployment and scalability.

3. **Entity-Relationship Diagram (ERD):**
   - Provided a clear and visually appealing ERD illustrating the entities and relationships within the healthcare system.

4. **Logical Schema:**
   - Defined the logical schema for the healthcare database, including tables, fields, and relationships.

5. **Documentation on dbdocs.io:**
   - Made documentation available on dbdocs.io for convenient reference and enhanced understanding of the healthcare database structure.

6. **Configuration for PostgreSQL Administration (pgAdmin):**
   - Set up configurations for the PostgreSQL administration tool, pgAdmin, tailored to the healthcare environment.

### Additional Deliverables:

1. **Sample Queries:**
   - Proposed a set of sample queries demonstrating the functionality of the healthcare database.

2. **Normalization Techniques:**
   - Applied normalization techniques to the healthcare database structure, ensuring it is well-structured and avoids redundancy.

3. **Indexing Strategy:**
   - Recommended and implemented an effective indexing strategy specific to healthcare operations to optimize query performance.

## Database Design Process

### Phase I: Requirements Collection and Analysis

- Interviewed and consulted with database users to understand data requirements.
- Identified key entities and relationships, laying the foundation for the conceptual design.

### Phase II: Conceptual Design

- Formulated a comprehensive E-R diagram representing the identified entities and relationships.

### Phase III: Logical Design (Data model mapping)

- Translated the conceptual design into a logical database schema.
- Specified entities, relationships, attributes, primary keys, and foreign keys.

https://dbdocs.io/akweiwonder3/HealthcareDBMS
### Phase IV: Physical Design (Internal Schema)

- Transformed the logical database schema into a physical database.
- Created tables, specified columns, defined data types, and implemented constraints and keys.

### Phase V: Usage and Setup

- Employed Docker and Docker Compose for a standardized environment.
- Offered detailed setup instructions in the readme, including links to online documentation and ERD images.

## Tools Used

- **PostgreSQL:** Main database management system.
- **PgAdmin:** Administration and management tool for PostgreSQL.
- **Docker:** Containerization platform for creating a consistent and isolated environment.

## Setup

1. Clone this repository.
2. Navigate to the project directory.

```bash
cd Healthcare-Database-Management-System
```

3. Run the following command to build and start the PostgreSQL container:

```bash
docker-compose up -d
```

4. Connect to the PostgreSQL database using PgAdmin with the provided credentials.

   - **Host:** localhost
   - **Port:** 5432
   - **Database:** healthcare_db
   - **User:** admin
   - **Password:** admin

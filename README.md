# Dance Academy Database Management System
This project is a comprehensive database management system designed to handle the operations of a dance academy. The system facilitates the efficient management of multiple partner dance schools, students, instructors, classrooms, locations, competitions, subscriptions, and courses. It was developed as part of a course project using Oracle Database 21c Express Edition.

## Overview
The objective of this project is to create a robust database system for managing a dance academy. The system is capable of:

- Managing information about partner dance schools, including their locations and classrooms.
- Handling instructor and student records, along with detailed enrollment and course schedules.
- Recording competitions and tracking the awards achieved by students.
- Enforcing business rules through stored procedures, functions, triggers, and packages.

## Features
- Data Integrity: The database includes numerous integrity constraints (primary keys, foreign keys, and custom triggers) to ensure consistent and reliable data.
- Automated Processes: Several stored procedures and functions manage tasks such as calculating awards, checking course eligibility, and reporting competition details.
- Advanced SQL Concepts: The project demonstrates the use of various Oracle SQL features including sequences, triggers (LMD, LDI, and DDL), and PL/SQL packages.
- Error Handling: Custom exceptions and error messages ensure that operations such as data insertions and schema modifications follow the defined business rules.

## Database Schema
The system models the following key entities:

Abonament (Subscription)
Locatie (Location)
Scoala (School)
Sala (Classroom)
Stil (Dance Style)
Instructor (Instructor)
Coregrafie (Choreography)
Curs (Course)
Elev (Student)
Competitie (Competition)
Participa (Participation)
Preda (Teaching Assignment)

Each table is linked with proper relationships to reflect the operations of a dance academy. The complete ERD and conceptual diagrams are included in the project documentation.

## Implementation Details
### Entity-Relationship Diagram (ERD)
The ERD was designed with all entities, relationships, and attributes in Romanian, ensuring clarity in the representation of the domain.

### Conceptual Diagram
Starting from the ERD, the conceptual diagram incorporates all necessary attributes and details to support the complete design and implementation of the database.

### SQL Scripts
The project includes SQL scripts for:

- Table creation: Scripts define tables with integrity constraints.
- Data insertion: Insertion scripts load a set of initial data into each entity.
- Sequences: Oracle sequences are used to auto-increment primary keys.

## Stored Procedures, Functions, and Triggers
The project demonstrates advanced PL/SQL features including:

- Subprograms using collections: For managing student competition participation.
- Cursors (including parameterized ones): To fetch and display instructor course details.
- Functions with exception handling: For retrieving student details based on competition awards.
- Procedures with custom exception handling: For fetching instructor details by dance style.
- Triggers: Several triggers are implemented to enforce rules at both the row and statement level, as well as a DDL trigger for auditing schema modifications.

## Package for Competition Management
A PL/SQL package (pkg_gestionare_competitii) has been created to manage competition processes. This package includes:

- Complex Data Types: Nested tables and record types.
- Functions: To calculate total awards per school and check competition eligibility (avoiding overlaps).
- Procedures: To register new competitions and generate detailed competition reports.

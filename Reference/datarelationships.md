In PostgreSQL (and relational databases in general), the main types of relationships between tables are:

### 1. **One-to-Many (1:N)**
- **Description:** This is the most common type of relationship. One record in the first table can relate to multiple records in the second table, but each record in the second table can only relate to one record in the first table.
- **Example:** A table of `authors` (one) can have many related `books` (many), but each book is written by only one author.
- **Implementation:** Typically implemented using a foreign key in the "many" table that references the primary key of the "one" table.

### 2. **Many-to-One (N:1)**
- **Description:** This is essentially the reverse of a one-to-many relationship. Multiple records in the first table can relate to one record in the second table.
- **Example:** Multiple `books` (many) can be written by the same `author` (one).
- **Implementation:** Like one-to-many, it's implemented using a foreign key in the "many" table that references the primary key of the "one" table.

### 3. **Many-to-Many (N:M)**
- **Description:** This relationship allows records in the first table to relate to multiple records in the second table and vice versa.
- **Example:** A table of `students` (many) can enroll in multiple `courses` (many), and each course can have multiple students enrolled.
- **Implementation:** This is typically implemented using a junction table (also known as a join table) that contains foreign keys referencing the primary keys of both related tables.

### 4. **One-to-One (1:1)**
- **Description:** In this relationship, one record in the first table corresponds to exactly one record in the second table, and vice versa.
- **Example:** A table of `users` might have a corresponding `profile` table, where each user has exactly one profile, and each profile belongs to exactly one user.
- **Implementation:** Implemented by adding a unique foreign key constraint in one of the tables that references the primary key of the other table.

### Summary:
- **One-to-Many (1:N):** One record relates to multiple records in another table.
- **Many-to-One (N:1):** Multiple records relate to one record in another table.
- **Many-to-Many (N:M):** Multiple records in both tables relate to each other, typically through a junction table.
- **One-to-One (1:1):** One record relates to exactly one record in another table.
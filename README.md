# Fall 2024 Principles of Databases — Assignment 4

* **Do not start this project until you’ve read and understood these instructions. If something is not clear, ask.**

---

## ❖ Introduction ❖

For this assignment, you will write responses to nine questions based on different topics from our textbook, *Database Systems — The Complete Book* and to one question based on your notes. Reply to each question in the provided region using Markdown syntax.

---

## ❖ Questions ❖

### 1. [2.4] What is the difference between a Cartesian Product, a Natural Join, and Theta-Joins?

Cartesian Product: Combines all tuples from two relations, resulting in every possible pair of tuples. The output includes all attributes from both relations, and its size equals the product of the number of tuples in each relation.
Natural Join: Matches tuples from two relations based on shared attributes with the same values. It filters the Cartesian Product to include only relevant combinations and removes duplicate columns in the output.
Theta Join: Extends the Cartesian Product by applying a condition (e.g., attributes meeting a specific comparison), retaining only tuples that satisfy that condition.

### 2. [2.5] What is a Referential Integrity Constraint?

A Referential Integrity Constraint ensures a foreign key in one relation matches a primary key in another relation. For example, an order table with a CustomerID must reference a valid CustomerID in the customer table, ensuring there are no "orphaned" entries.



###  3. [2.5] What is a Key Constraint?

A Key Constraint ensures that a set of attributes in a relation has unique values across all tuples, which helps identify each tuple uniquely. For example, a student database might use StudentID as a key, ensuring no two students share the same ID, even if other attributes (e.g., name) are identical.

### 4. [4.1] What is an Entity/Relationship Model? What purpose does it serve in the process of creating/designing databases?

The ER Model provides a graphical representation of a database's structure, using three main components:

Entity Sets (e.g., Student, Teacher): Represent tables in the database and are depicted as rectangles.
Attributes (e.g., Name, Age): Represent properties of entities and are shown as ovals connected to their entity.
Relationships (e.g., Teaches, Enrolls): Represent associations between entities and are shown as diamonds.
The ER Model simplifies database design by organizing entities and their relationships before implementation.


### 5. [4.4] What is a Weak Entity Set?

A Weak Entity Set cannot be uniquely identified using only its own attributes. It requires a related entity (via a foreign key) and additional attributes to form a unique identifier. For example, dependents in an insurance database rely on the policyholder for identification. In ER diagrams, weak entities are represented by rectangles with double borders.



### 6. [5.2.7; 6.3.8] Explain the concepts of Outerjoin, Natural Right Outer Joins, Natural Left Outer Joins, and Full Outer Joins.

Outer Join: Extends a join by including unmatched tuples from one or both relations and fills missing attributes with NULL.
Left Outer Join: Retains all tuples from the left relation, including those with no match in the right relation.
Right Outer Join: Retains all tuples from the right relation, including those with no match in the left relation.
Full Outer Join: Includes all tuples from both relations, even those without matches, with unmatched values replaced by NULL.

### 7. [6.6.3] What is the difference between the SQL command `TRANSACTION` and the execution of any statement in SQL?

The TRANSACTION command groups multiple SQL operations into a single logical unit, allowing them to be committed or rolled back together. Regular SQL statements execute immediately, while transactions provide control to ensure either all operations succeed or none are applied, preventing partial updates.



### 8. [8] What is a Virtual View and what are its advantages?

A Virtual View is a stored SQL query that acts like a temporary table but does not store data itself. Its advantages include simplifying complex queries by reusing the stored query, improving security by restricting access to specific data, and enhancing performance for frequently used queries. Virtual Views only last for the duration of the SQL session.



### 9. [8.3] What is an *index* and what are its advantages?
An Index is a data structure that optimizes data retrieval by sorting and organizing data based on selected attributes. It accelerates queries by reducing the time needed to search large datasets. For example, indexing the city attribute in a table of restaurants allows faster lookups when searching for restaurants in a specific city.

### 10. Explain the concept of an MVC, or model, view, controller, framework for designing full stack applications

The MVC (Model-View-Controller) framework divides an application into three interconnected parts:

Model: Manages data, business logic, and interactions with the database.
View: Displays data and provides the user interface.
Controller: Acts as the intermediary, processing user input, updating the Model, and refreshing the View.
This structure separates concerns, making the application easier to maintain, scale, and update.

---

## ❖ Due ❖

Sunday, 15 December 2024, at 10:00 AM.

---

## ❖ Grading ❖

| Item        | Points |
|-------------|:------:|
| Question 1  | `10`   |
| Question 2  | `10`   |
| Question 3  | `10`   |
| Question 4  | `10`   |
| Question 5  | `10`   |
| Question 6  | `10`   |
| Question 7  | `10`   |
| Question 8  | `10`   |
| Question 9  | `10`   |
| Question 10 | `10`   |

---

## ❖ Submission ❖

**NO late submissions will be accepted.**

You will need to issue a pull request back into the original repo, the one from which your fork was created for this project. See the **Issuing Pull Requests** section of [this site](http://code-warrior.github.io/tutorials/git/github/index.html) for help on how to submit your assignment.

**Note**: This assignment may **only** be submitted via GitHub. **No other form of submission will be accepted**.

# Fall 2024 Principles of Databases — Assignment 4

* **Do not start this project until you’ve read and understood these instructions. If something is not clear, ask.**

---

## ❖ Introduction ❖

For this assignment, you will write responses to nine questions based on different topics from our textbook, *Database Systems — The Complete Book* and to one question based on your notes. Reply to each question in the provided region using Markdown syntax.

---

## ❖ Questions ❖

### 1. [2.4] What is the difference between a Cartesian Product, a Natural Join, and Theta-Joins?

A Cartesian Product is an algebraic operation that produces all possible combinations of tuples from two relations. So for example each tuple from relation 1 pairs with every tuple of relation 2. The final relation is going to contain all of the tuples and attributes from both of the relations and be the size of (# of tuples in 1 x # of tuples in 2).

A Natural Join is an operation that merges tuples from 2 relations based on if the values of the attributes are the same or not. You will be left with only the tuples with the common attributes.

A Theta Join selects tuples from the cartesian product of 2 relations that will meet a specific condition. So its kind of like the cartensian product with another step.

### 2. [2.5] What is a Referential Integrity Constraint?

A Referential Integrity Constraint ensures that a value in one relation's attribute of a tuple will also appear in another corresponding attribute of a tuple in a different relation. This is kind of like how a foreign key's values must match a value in the referenced primary key. Referential Integrity constraints prevent dangling tuples to maintain logical consistency between tables.

###  3. [2.5] What is a Key Constraint?

A Key Constraint is a constraint that will ensure a set of attributes in a relation will not repeat. These attributes that wont repeat are all going to be unqiue values and are usually identifiers in a relation. For example if you have a lot of students you might give them all unique numbers to identify them by because there is a chance they have the same name, height, major, etc. So their unqiue number you give them will have a key constraint to ensure no student has the same number.

### 4. [4.1] What is an Entity/Relationship Model? What purpose does it serve in the process of creating/designing databases?

An Entity Relationship Model (ER Model) graphically represents a struce of a database using 3 main elements: Entity Sets, Attributes, and Relationships. This is usually used before designing a database to have a simplified structure to build schema from.

Entity Sets represents your database tables/relation. It will be shown in the diagram as rectangles and nouns are used to describe them (Ex. Student, Teacher, College). 
Attributes are the characteristics of the entity set and are going to be the attributes of the relation. These are denoted in the diagram as bubbles branched off from the entity set rectangle and are usually labeled as adjectives or descriptions (Ex. height, weight, eye color, studentID, name, etc).
Relationships are the connections between 2 entity sets and they can also have their own attributes. They are denoted as diamonds in the diagram and are usually labeled with verbs (Ex. Teaches, Enrolls in, Extends, etc).

### 5. [4.4] What is a Weak Entity Set?

A Weak Entity Set is an entity set that cannot be uniquely identified by its own attributes. They do not have their own independant key so they require their own attributes along with the attributes of a related entity set to form a unique identifier. These are depicted in the ER diagram using rectagles with double borders. For example my father's our insurance policy holder through his work and as his dependant I get insurance coverage through him. I do not exist on that insurance without my father, I do not have my own insurance so if he were to get off of that insurance I would not be there as well. I exist in that insurance database through my father so I am a weak entity set in that example.

### 6. [5.2.7; 6.3.8] Explain the concepts of Outerjoin, Natural Right Outer Joins, Natural Left Outer Joins, and Full Outer Joins.

An Outerjoin preserves dangling tuples by finding the tuples from one or both relations to the join operation and it fills in the missing attribute values with NULL.

A Natural Right Outer Join is a natural join which will then add the dangling tuples from the RIGHT relation and fills in the missing attribute values with NULL. This is to preserve all of the information from the RIGHT relation.

A Natural Left Outer Join is a natural join which will then add the dangling tuples from the LEFT relation and fills in the missing attribute values with NULL. This is to preserve all of the information from the LEFT relation.

A Full Outer Join is a natural join that will add the dangling tuples from BOTH of the relations and fill the missing attribute values with NULL. This is to preserve all of the information from BOTH relations.

### 7. [6.6.3] What is the difference between the SQL command `TRANSACTION` and the execution of any statement in SQL?

The TRANSACTION command groups SQL statements together into a single unit while other statements in SQL are executed immediately. The TRANSACTION statements are executed as a block and will either be saved to the database or discarded in case of errors.

### 8. [8] What is a Virtual View and what are its advantages?

A Virtual View is a SQL query that is stored as its own temporary table. It doesn't store data itself but it stores the query that contains the data. Its advantages are that it simplifies complex queries into one place and it enhances security by restricting you only to the data from the query (and not the full tables). It also makes things quicker if you are using that specific query over and over again (I like to think of it as making a shortcut for the query). These Views are only temporary beacuse once you exit your SQL session they go away.

### 9. [8.3] What is an *index* and what are its advantages?

An Index is a data structure to improve the speed/efficiency of data retrieval operations on a database table. Indexes will have an index key which is a unique attribute value or values that will be used to sort through the database. This key is placed on the attribute that is expected to be searched the most form the database. For example if you have a table; Restaurants(name, city, street) and you think that when people are looking for where they might want to eat they will search by city to see whats in their city, you will make an index with city being your key. This will then sort the searches by city so when looking at the table it will be sorted by city. I like to think of it as grouping by matching attributes. This data structure will make your queries faster, sort your data efficiently and filter out uneeded data. This works very well in large data sets.

### 10. Explain the concept of an MVC, or model, view, controller, framework for designing full stack applications

MVC (Model View Controller) is a framework that splits an application into 3 interconnected components; View, Controller, and Model. It will also flow in that same way. This is used to make the application easier to maintain, update, and increase the size.

The Model manages and stores data, logic, and rules of the application interacting with the database.

The View displays the data of the application to the user.

The Controller (being in the middle) acts as a pathway inbetween the Model and View and will handle user input that will interact with the model and update the view. 

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

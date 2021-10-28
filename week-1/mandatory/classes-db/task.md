# Class Database

## Submission

Below you will find a set of tasks for you to complete to set up a databases of students and mentors.

To submit this homework write the correct commands for each question here:

```sql


```

When you have finished all of the questions - open a pull request with your answers to the `Databases-Homework` repository.

## Task

1. Create a new database called `cyf_classes` (hint: use `createdb` in the terminal)

CREATE DATABASE cyf_classes owner postgres;

2. Create a new table `mentors`, for each mentor we want to save their name, how many years they lived in 
Glasgow, their address and their favourite programming language.

CREATE TABLE mentors(
id SERIAL PRIMARY KEY,
name VARCHAR(50) NOT NULL,
yearsInGlasgow int,
address VARCHAR(120),
favProgramLanguage VARCHAR(100)
);

3. Insert 5 mentors in the `mentors` table (you can make up the data, it doesn't need to be accurate ;-)).

INSERT INTO mentors (name, yearsinglasgow, address, favprogramlanguage) VALUES (Wendy Andrade', 0, 'Barcelona', 'JavaScript');

INSERT INTO mentors (name, yearsinglasgow, address, favprogramlanguage) VALUES ('Robert Andrade', 0, 'Barcelona', 'JavaScript');

INSERT INTO mentors (name, yearsinglasgow, address, favprogramlanguage) VALUES ('Flor Maria', 0, 'Barcelona', 'JavaScript');

INSERT INTO mentors (name, yearsinglasgow, address, favprogramlanguage) VALUES ('Juan', 0, 'Barcelona', 'JavaScript');

INSERT INTO mentors (name, yearsinglasgow, address, favprogramlanguage) VALUES ('Yelitza', 0, 'Barcelona', 'JavaScript');

4. Create a new table `students`, for each student we want to save their name, address and if they have graduated from Code Your Future.

CREATE TABLE students(
id SERIAL PRIMARY KEY,
name VARCHAR(50) NOT NULL,
address VARCHAR(120),
graduated BOOL
);


5. Insert 10 students in the `students` table.

INSERT INTO students (name, address, graduated) VALUES ('Maria Alejandra', 'Passeig de Fabra i Puig, 330. Madrid', 'true');

INSERT INTO students (name, address, graduated) VALUES ('Juan Pablo', 'Passeig de Fabra i Puig, 330. Madrid', 'true');

INSERT INTO students (name, address, graduated) VALUES ('Ulises Rodriguez', 'Passeig de Fabra i Puig, 330. Madrid', 'true');

INSERT INTO students (name, address, graduated) VALUES ('Daniel Andrade', 'Passeig de Fabra i Puig, 330. Madrid', 'true');

INSERT INTO students (name, address, graduated) VALUES ('Yesenia Rodriguez', 'Passeig de Fabra i Puig, 330. Madrid', 'true');

INSERT INTO students (name, address, graduated) VALUES ('Nelly Rodriguez', 'Passeig de Fabra i Puig, 330. Madrid', 'true');

INSERT INTO students (name, address, graduated) VALUES ('Jenelly Parra', 'Passeig de Fabra i Puig, 330. Madrid', 'true');

INSERT INTO students (name, address, graduated) VALUES ('Natalia Montoya', 'Passeig de Fabra i Puig, 330. Madrid', 'true');

INSERT INTO students (name, address, graduated) VALUES ('Jesus Martin', 'Passeig de Fabra i Puig, 330. Madrid', 'true');

INSERT INTO students (name, address, graduated) VALUES ('Marta Gomez', 'Passeig de Fabra i Puig, 330. Madrid', 'true');

6. Verify that the data you created for mentors and students are correctly stored in their respective tables (hint: use a `select` SQL statement).

SELECT * FROM students;
SELECT * FROM mentors;

7. Create a new `classes` table to record the following information:

   - A class has a leading mentor
   - A class has a topic (such as Javascript, NodeJS)
   - A class is taught at a specific date and at a specific location

   CREATE TABLE classes(
id SERIAL PRIMARY KEY,
leadingmentor VARCHAR(50) NOT NULL,
topic VARCHAR(120) NOT NULL,
date DATE NOT NULL,
location VARCHAR(30) NOT NULL
);


8. Insert a few classes in the `classes` table

INSERT INTO classes (leadingmentor, topic, date, location) VALUES ('Carlos Marcos', 'JavaScript', '2021/10/15', 'Madrid');

INSERT INTO classes (leadingmentor, topic, date, location) VALUES ('Brenda Maria', 'JavaScript', '2021/10/15', 'Madrid');

INSERT INTO classes (leadingmentor, topic, date, location) VALUES ('Bruno Jose', 'JavaScript', '2021/10/15', 'Madrid');

INSERT INTO classes (leadingmentor, topic, date, location) VALUES ('Teresa Carolina', 'JavaScript', '2021/10/15', 'Madrid');

9. We now want to store who among the students attends a specific class. How would you store that? Come up with a solution and insert some data if you model this as a new table.
10. Answer the following questions using a `select` SQL statement:
    - Retrieve all the mentors who lived more than 5 years in Glasgow
    - Retrieve all the mentors whose favourite language is Javascript
    - Retrieve all the students who are CYF graduates
    - Retrieve all the classes taught before June this year
    - Retrieve all the students (retrieving student ids only is fine) who attended the Javascript class (or any other class that you have in the `classes` table).

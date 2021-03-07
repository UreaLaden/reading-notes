# Database Normalization
[Home](./README.md)

#### Definition
There are three common forms of database normalization: **1st**, **2nd**, and **3rd** normal form. They are also abbreviated as **1NF**, **2NF**, and **3NF** respectively. 

The forms are progressive, meaning that to qualify for 3rd normal form a table must first satisfy the rules for 2nd normal form, and 2nd normal form must adhere to those for 1st normal form. Before we discuss the various forms and rules in detail, let’s summarize the various forms:

- `First Normal Form` – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
- `Second Normal Form` – The table is in first normal form and all the columns depend on the table’s primary key.
- `Third Normal Form` – the table is in second normal form and all of its columns are not transitively dependent on the primary key
If the rules don’t make too much sense, don’t worry. I’ve linked to article to help you understand them.

For now it’s important to understand there are three rules for database normalization that upon each other.  Some people make database normalization seem complicated.

There are three main reasons to normalize a database:
- To minimize duplicate data
- To minimize or avoid data modification issues
- To simplify queries. 


#### Source
[Kris Wenzel: Database Normalization (Explained in Simple English) ](https://www.essentialsql.com/get-ready-to-learn-sql-database-normalization-explained-in-simple-english/)
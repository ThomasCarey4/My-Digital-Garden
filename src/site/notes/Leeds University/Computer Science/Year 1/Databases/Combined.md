---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/databases/combined/"}
---


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/databases/1-introduction/1-introduction/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




#### File-Based Processing
![F-B P.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/1.%20Introduction/images/F-B%20P.png)
##### Limitations
- Separation and isolation of data
	- Each program maintains its own set of data
	- Users of one program ma be unaware of potentially useful data held by other programs
- Duplication of data
	- Same data is held by different programs
	- Wasted space and potentially different values and/or different formats for the same item
- Data dependence
	- File structure is defined in the program code
- Incompatible file formats
	- Programs are written in different languages, and so cannot easily access each other’s files
- Fixed queries/proliferation of application programs
	- Programs are written to satisfy particular functions
	- Any new requirement needs a new program
	- No provision for concurrent access
#### Database
The limitations in a file-based approach leads to database/**d**ata**b**ase **m**anagement **s**ystem (**DBMS**)
*Database*
	- A shared collection of logically related data (and a description of this data), designed to meet the information needs of an organisation
***DBMS***
	- A software system that enables users to define, create, maintain and control access to the database
***Database** Application Program*
	- A computer program that interacts with databases by issuing an appropriate request (SQL statement) to the **DBMS**
##### History of Database Systems
###### $1^{st}$ Generation: Hierarchical and Network
![1st Gen.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/1.%20Introduction/images/1st%20Gen.png)
###### $2^{nd}$ Generation: Relational
![2nd Gen.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/1.%20Introduction/images/2nd%20Gen.png)
###### $3^{rd}$ Generation: Object-Relational, Object-Oriented
![3rd Gen.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/1.%20Introduction/images/3rd%20Gen.png)

##### Advantages of DBMS
- Control of data redundancy
- Data consistency
- More information from the same amount of data
- Sharing of data
- Improved data integrity
- Improved security
- Enforcement of standards
- Economy of scale
- Balance conflicting requirements #what
- Improved data accessibility and responsiveness
- Increased productivity
- Improved maintenance through data independence
- Increased concurrency
- Improved backup and recovery services
##### Disadvantages of DBMS
- Complexity
- Size
- Cost of DBMS
	- There are free ones lol, PostgreSQL
- Additional hardware costs
- Cost of conversion
- Performance
- Higher impact of failure
#### Summary
- Limitations in file-based systems leads to database approach
- DBMS allows users to interact with databases
- There are many components and roles in database environments
- Before implementing databases, you need to be aware of advantages and disadvantages of DBMSs

</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/databases/2-database-environment-and-architecture/2-database-environment-and-architecture/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




**External**
- The user, completely independent of the database designer
***Conceptual***
- The schema for the database
	- The design of the tables, their relations
	- All the SQL that *makes* the database
**Internal**
- *Where* the data is, how to find it and how it is compressed
- The communications between the DBMS and the Database
![ANSI-SPARC 3-Level Architecture.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/2.%20Database%20Environment%20&%20Architecture/images/ANSI-SPARC%203-Level%20Architecture.png)
![External-Conceptual-Internal.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/2.%20Database%20Environment%20&%20Architecture/images/External-Conceptual-Internal.png)
#### Data Independence
![Data Independence.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/2.%20Database%20Environment%20&%20Architecture/images/Data%20Independence.png)**Logical Data Independence**
- Allows you to edit the database without needing to change anything in the External Schema
	- *Unless!* you $\color{red} \textit{remove}$ a column from a table
		- Then the External Schema will break
**Physical Data Independence**
- You can modify the Internal Schema massively without needing to change the Conceptual Schema
- If you:
	- Move the database to a new storage location (bigger hard drive)
	- Rearrange the layout of the files
	- Change the hashing algorithm
	- Change the compression techniques
- The conceptual level remains unchanged

#### Database Languages
***DDL***
- To *Create*, *Update* or *Delete* database objects with,
- **Data Definition Language**
***DML***
- To *Add*, *Update*, *Delete* or *Retrieve* data from a database with,
- **Data Manipulation Language**
#### Data Models
Model – representation of real-world objects and events, and their associations
##### Object-Based
###### Entity-Relationship
![Entity-Relationship.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/2.%20Database%20Environment%20&%20Architecture/images/Entity-Relationship.png)
###### Object-Oriented
![Object-Oriented.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/2.%20Database%20Environment%20&%20Architecture/images/Object-Oriented.png)
###### Semantic, Functional
![Semantic-Functional.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/2.%20Database%20Environment%20&%20Architecture/images/Semantic-Functional.png)
##### Record-Based
###### Relational
![Relational.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/2.%20Database%20Environment%20&%20Architecture/images/Relational.png)
###### Hierarchical
![Hierarchical.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/2.%20Database%20Environment%20&%20Architecture/images/Hierarchical.png)
###### Network
![Network.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/2.%20Database%20Environment%20&%20Architecture/images/Network.png)
##### Physical
![Physical.png|200](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/2.%20Database%20Environment%20&%20Architecture/images/Physical.png)

#### Functions of a DBMS
- Data *Storage*, *Retrieval*, and *Updation*
- A User-Accessible Catalog
	- A catalog is the hierarchy above a schema
		- e.g. A catalog is a collection of schema’s, which are collections of tables
- Transaction Support
	- A *unit of work* performed within a database
	- Generally represents any change in a database
- *Concurrency Control* Services
	- Prevent simultaneous transactions from interfering with each other
- *Recovery*
- *Authorisation*
- Support for Data Commutation
- Integrity Services
- Services to *Promote Data Independence*
- Utility Services
#### Multi-User DBMS Architectures
Most common: **Client-Server Architecture**
**Client**
- Manages the user interface and runs applications
**Server**
- Holds database and DBMS
- Controls data validation and Database access
*Flaws*
- Client requires considerable resources to run effectively (Data processing)
- Significant client-side admin overhead
##### A 3rd tier is proposed
***1* - Client**
- Manages user interface
***2* - Application Server**
- Manages data processing and business logic
***3* - Database Server**
- Same as before
*Pros*
- Supports data independence

</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/databases/3-relational-data-model/3-relational-data-model/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




#### Components of a Data Model
**Structural Part** - A set of rules
**Manipulative Part** - Operations allowed on data
**A set of integrity constraints**
#### Terminology
**Relation** $\rightarrow$ *Table* $\rightarrow$ *File*
**Tuple** $\rightarrow$ *Row* $\rightarrow$ *Record*
**Attribute** $\rightarrow$ *Column* $\rightarrow$ *Field*
**Cardinality** $\rightarrow$ The row number
**Degree** $\rightarrow$ The column number
**Attribute Domain** $\rightarrow$ The set of values allowed in an attribute
	- Not necessarily a ‘set’ of values but a definition of what is allowed (e.g. ```character: size 8```)
#### Defining a Relation (The Schema)
${\color{lightgreen}R}=\set{{\color{blue} A}_{1}:{\color{red} D}_{1},{\color{blue} A}_{2}:{\color{red} D}_{2},\dots,{\color{blue} A}_{n}:{\color{red} D}_{n}}$
$\implies$ $\color{lightgreen} R$: A Relation
$\implies$ $\color{blue} A$: An Attribute
$\implies$ $\color{red} D$: An Attribute **Domain**
For example:
${\color{lightgreen} \text{Branch}} = \set{{\color{blue} branchNo}:{\color{red} BranchNumbers},{\color{blue} street}:{\color{red} StreetNames},\dots}$
**A Database Schema**: $\color{lavender} R=\set{{\color{lightgreen} R}_{1},{\color{lightgreen} R}_{2},\dots,{\color{lightgreen} R}_n}$
#### Properties of Relations
- **Relation Name** $\rightarrow$ ***DISTINCT**
- **Cell** $\rightarrow$ Contains ***ONE*** value
- **Attribute Name** $\rightarrow$ ***DISTINCT***
- **Attribute Value** $\rightarrow$ All from the ***SAME DOMAIN***
- **Tuple** $\rightarrow$ ***DISTINCT***
- **Order of Attributes** $\rightarrow$ ***NO*** Significance
- **Order of Tuples** $\rightarrow$ ***NO*** Significance, theoretically
#### Relational Keys
**Super Key** $\rightarrow$ *Any* set of attributes that uniquely identifies a row
**Candidate Key** $\rightarrow$ A *minimal* Super Key
	- e.g. A super key where if any attribute was removed it would no longer be a super key
**Primary Key** $\rightarrow$ The chosen Candidate Key to be used
**Foreign Key** $\rightarrow$ The primary key of a different table being used in the current table
#### Integrity Constraints
**Entity Integrity** $\rightarrow$ Each primary key should be unique
**Referential Integrity** $\rightarrow$ A foreign key must be a valid primary key of the referred relation
**Multiplicity Constraints**
- One-To-One,
- One-To-Many,
- Many-To-One, 
- Many-To-Many
**General Constraints** $\rightarrow$ The constraints of a domain (e.g. Age is a positive integer)
#### Views
A view is a virtual relation that does not necessarily actually exist in the database but is produced upon request, at the time of request
- Provides powerful and flexible security mechanism by hiding parts of a database from certain users
- Permits users to access data in a customised way, so that the same data can be seen by different users in different ways, a the same time
- Can simplify complex operations on base relations
##### Updating Views
All updates to a base relation should be immediately reflected in all views that reference that base relation
- If a view is updated, underlying base relation should also reflect the change
- There are restrictions on the types of modifications that can be made through views
	- Updates are allowed if query involves a single base relation and contains a candidate key the base relation
	- Updates are not allowed involving multiple base relations
	- Updates are not allowed involving aggregation or grouping operations


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/databases/4-relational-algebra/4-relational-algebra/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




Relational algebra operations work on *one or more relations* to **define another relation** ***without*** changing the original relations
- Both operands and results are relations, so output from one operation can become input to another operation
- Five basic operations in relational algebra:
	- Selection
	- Projection
	- Cartesian Product
	- Union
	- Set Difference
	- Rename?
- Three secondary operations (Defined using the basic operations)
	- Join
	- Intersection
	- Division
##### Selection
$\rightarrow$ Single relation $\color{blue} R$, the predicate
$\implies$ Returns a smaller relation with only *tuples* satisfying the predicate are displayed
**For Example:** List all staff with a salary > 10,000
$\large{\color{red} \sigma}_{salary\ >\ 10,000}({\color{blue} Staff})$
##### Projection
$\rightarrow$ Single relation $\color{blue} R$, the desired attributes
$\implies$ Returns a relation with specific *attributes* removed ***AND*** duplicate *tuples* removed
**For Example**: Produce a list of salaries for all staff, showing only staffNo, fName , lName and salary details
$\large{\color{red} \Pi}_{staffNo,fName,lName,slary}({\color{blue} Staff})$
##### Union
$\rightarrow$ Two relations $\color{blue} R$ and $\color{blue} S$
$\implies$ Returns a relation that contains the *tuples* of $\color{blue} R$ ***OR*** $\color{blue} S$ ***OR*** both, ***AND*** duplicate *tuples* removed
**For Example**: List all cities where there is either a branch office or a property for rent
$\large\Pi_{city}({\color{blue} Branch})\ {\color{red} \bigcup}\ \Pi_{city}({\color{blue} PropertyForRent})$
##### Cartesian Product
$\rightarrow$ Two relations $\color{blue} R$ and $\color{blue} S$
$\implies$ Returns a relation that is the concatenation of every tuple of $\color{blue} R$ with every tuple in $\color{blue} S$
![Cartesian Product.png|250](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/4.%20Relational%20Algebra/images/Cartesian%20Product.png)
**For Example**: List the names and comments of all clients who have viewed a property for rent
$\large\Pi_{clientNo,fName,lName}({\color{blue} Client})\ {\color{red} \bigtimes}\ \Pi_{clientNo, propertNo, comment}({\color{blue} Viewing})$
$\small \text{Pretty sure this is wrong, cartesian product DOES NOT allow common attributes}$
##### Intersection
$\rightarrow$ Two relations $\color{blue} R$ and $\color{blue} S$
$\implies$ Returns a relation with *tuples* that are in both $\color{blue} R$ ***AND*** $\color{blue} S$
**For Example**: List all cities where there is both a branch office and at least one property for rent
$\large\Pi_{city}({\color{blue} Branch})\ {\color{red} \bigcap}\ \Pi_{city}({\color{blue} PropertyForRent})$
##### Set Difference
$\rightarrow$ Two relations $\color{blue} R$ and $\color{blue} S$
$\implies$ Returns a relation of the tuples that are in relation $\color{blue} R$ but ***NOT*** in relation $\color{blue} S$
**For Example**: List all cities where there is a branch office but no properties for rent
$\large\Pi_{city}({\color{blue} Branch}){\color{red} -}\Pi_{city}({\color{blue} PropertForRent})$
##### Rename
$\rightarrow$ Single relation $\color{blue} R$, the new name(s)
$\implies$ Returns the same $\color{blue} R$ but with changed attribute name(s) or relation name
**For Example, Relation Name**:
${\color{red} \rho}\ NewName({\color{blue} R})$
**For Example, Attribute Name**:
${\color{red} \rho}\ oldAttr\rightarrow newAttr,oldAttr2\rightarrow newAttr2(\color{blue} R)$
##### Natural Join
$\rightarrow$ Two relations $\color{blue} T$ and $\color{blue} U$
$\implies$ Returns a Cartesian Product with common attribute(s) used as a primary/foreign key
![Natural Join.png|300](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/4.%20Relational%20Algebra/images/Natural%20Join.png)
**For Example**: $ClientViewing = Client\ {\color{blue} \bowtie}\ Viewing$
##### Theta Join
$\rightarrow$ Two relations $\color{blue} R$ and $\color{blue} S$, a predicate $\color{lightgreen} \theta$
$\implies$ Returns a combination of Natural Join and Selection
- If $\color{lightgreen} \theta$ only contains equality operations $=$ then the term **Equijoin** is used
**For Example**: List all students exams where they got above 70%
$GoodGrades = {\color{blue} Student}\ {\color{red} \bowtie} ({\color{lightgreen} Result.grade > 70})\ {\color{blue} Result}$
#### Semi-Join
$\rightarrow$ Two relations $\color{blue} R$ and $\color{blue} S$, a predicate $\color{lightgreen} \theta$
$\implies$ Returns a Theta Join with:
	- Only the columns of $\color{blue} R$
	- Each *tuple* in $\color{blue} R$ is returned once even if there is multiple matches
##### (Left) Outer Join
$\rightarrow$ Two relations $\color{blue} R$ and $\color{blue} S$, a predicate $\color{lightgreen} \theta$
$\implies$ Returns the same as Theta Join **However!** if there is no foreign key in $\color{blue} S$ for the primary key in $\color{blue} R$ then the tuple is added *once* with the other attributes set to NULL
- Also, if a predicate is given, it becomes the new primary key to be used
![(Left) Outer Join.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/4.%20Relational%20Algebra/images/(Left)%20Outer%20Join.png)
**For Example**: ${\color{blue} R}$ $\huge ⟕$ $\color{blue} S$
##### (Right) Outer Join
$\rightarrow$ Two relations $\color{blue} R$ and $\color{blue} S$, a predicate $\color{lightgreen} \theta$
$\implies$ Literally the same as (Left) Outer Join but the ‘primary key’ is in $\color{blue} S$ and the ‘foreign key’ is in $\color{blue} R$
##### Full Outer Join
$\rightarrow$ Two relations $\color{blue} R$ and $\color{blue} S$, a predicate $\color{lightgreen} \theta$
$\implies$ The same as the other outer joins, if there isn’t a match from ${\color{blue} R}\rightarrow {\color{blue} S}$ then the $\color{blue} R$ tuple appears with all the $\color{blue} S$ attributes NULL and if their isn’t a match from ${\color{blue} S}\rightarrow {\color{blue} R}$ then the $\color{blue} S$ tuple appears with all the $\color{blue} R$ attributes NULL
#### Aggregation
$\rightarrow$ One relations $\color{blue} R$ and function(s) $\color{lightgreen} AL$
$\rightarrow$ $\color{lightgreen} AL$: COUNT, SUM, AVG, MIN, MAX
$\implies$ Iterates the function(s) over a list (e.g. an attribute) in $\color{blue} R$
**For Example**:
$_{\color{lightgreen} sum(balance)}({\color{blue} credit\_acct})$
#### Grouping
$\rightarrow$ One relations $\color{blue} R$, function(s) $\color{lightgreen} AL$ and grouping attribute(s) $\color{red} GA$
$\rightarrow$ $\color{lightgreen} AL$: COUNT, SUM, AVG, MIN, MAX
$\rightarrow$ $\color{red} GA$: An attribute
$\implies$ Performs an aggregation but groups together the attributes in the $\color{red} GA$, returning a graph with column(s) for the $\color{red} GA$’s and column(s) for the $\color{lightgreen} AL$
**For Example**:
$_{{\color{red} person\_name}\ \color{lightgreen} count(puzzle\_name)}({\color{blue} completed})$


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/databases/5-entity-relationship-modelling/5-entity-relationship-modelling/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




**The Life-cycle**
![Database System Development Lifecycle.png|400](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/5.%20Entity-Relationship%20Modelling/images/Database%20System%20Development%20Lifecycle.png)
**Conceptual Database Design**
- The process of constructing a model of the data used in an enterprise, independent of all physical considerations
#### Building the *Conceptual Model*
1. Identify Entities
2. Identify Relationships
3. Identify and associate Attributes with Entities or Relationships
4. Determine Attribute Domains
5. Determine Keys
6. Consider enhanced modelling
   (optional step)
7. Check model for redundancy
8. Validate model against user transactions
9. Review data model with user
##### Entity-Relationship Modelling
- Entity-relationship modelling analyses data requirements in a systematic way to help produce a well-designed database
- ER modelling should always be completed before  you implement your database
- Everything is modelled in terms of three basic concepts: *Entity*, *Attribute*, *Relationship*
###### Notations
**UML (Unified Modelling Language)**
![UML.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/5.%20Entity-Relationship%20Modelling/images/UML.png)
**Chen’s Notation**
![Chen's Notation.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/5.%20Entity-Relationship%20Modelling/images/Chen's%20Notation.png)
**Crow’s Feet Notation**
![Crow's Feet Notation.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/5.%20Entity-Relationship%20Modelling/images/Crow's%20Feet%20Notation.png)
**Others**
- Bachman Notation, Barker’s Notation, IDEF1X, etc…
###### ***Entity***
A group of objects with the same properties (Attributes), having an independent existence
- Physical entity (Car, Staff, Product, Influencer)
- Conceptual entity (Timetable, Sale, Viewing, Spending)
- Entity occurrence or instance of an entity
	- Uniquely identifiable instance of an entity such as Nigel Ng (Uncle Roger) is an instance of the entity Influencer
**Strong Entity**: An entity that *is not* existence-dependent another entity
**Weak Entity**: An entity that *is* existence-dependent on another entity
###### ***Attribute***
A property of an entity or a relationship
- Attribute Domain
	- A set of allowable values for one or more attributes
	- e.g. Age, 1 to 150 years
- Example: An Influencer entity with attributes firstName and lastName
**Simple Attribute**: An attribute composed of a single component with an independent existence,
e.g. ID
**Composite Attribute**: An attribute composed of multiple components, each with an independent existence,
e.g. deliveryAddress can be subdivided into Street, City and Postcode
**Derived Attribute**: An attribute that represents a value that is derivable from a value of a related attribute, or set of attributes, not necessarily in the same entity,
e,g, Age can be calculated from DOB
###### ***Relationship***
Entities take part in relationships.
- Identify relationships from **verbs** or **verb phrases**
- A set of meaningful associations among entities
- Shown as a line connecting associated entities together with the name of the relationship
- Example: a student **registers** a course
![Relationship.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/5.%20Entity-Relationship%20Modelling/images/Relationship.png)
**Degree of a Relationship**
The number of participating entities in a relationship
**Unary** (degree 1) - One entity
**Binary** (degree 2) - Two entities
**Ternary** (degree 3) - Three entities
**Quaternary** (degree 4) - Four entities
***N*-ary** (degree 5) - *n* entities
###### Step 1: Identify Entity (types)
- Examine user’s requirements specification
- Identity nouns or noun phrases,
  e.g. Staff Number, Staff Name, Property Number
- Look for major objects, such as People, Places or Concepts of Interest, excluding nouns that are Attributes
- Look for objects with an independent existence
- If possible, the users should be involved
- Document entities in a data dictionary

| Entity Name | Description | Aliases  | Occurence |
| ----------- | ----------- | -------- | --------- |
| **Staff**   | …           | Employee | …         |
|             |             |          |           |
###### Step 6: Identify Relationships
- Look for **verbs** or **verb phrases**
- Determine multiplicity constraints (section 3) of relationships
- Document relationships

| Entity Name | Multiplicity | Relationship | Multiplicity | Entity Name         |
| ----------- | ------------ | ------------ | ------------ | ------------------- |
| **Staff**   | 0..1         | *Manages*    | 0..100       | **PropertyForRent** |
$\small0\leftrightarrow1\text{ Staff Manages }0\leftrightarrow100\text{ PropertForRent}$
**Many-to-Many** (\*..\*) $\implies$ ***BAD!***
Create a Composite Entity:
![Composite Entity.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/5.%20Entity-Relationship%20Modelling/images/Composite%20Entity.png)
###### Step 3: Identify Attributes
Look for **nouns** or **noun phrases** that are a property, quality, identifier, or characteristic of entities or relationships
- Document the attributes in a data dictionary

| Entity Name | Attributes   | Description | Data Type & Length    | Nulls? | Multi-valued? |
| ----------- | ------------ | ----------- | --------------------- | ------ | ------------- |
| **Staff**   | staffNo<br>… | …           | 5 variable characters | No     | No            |
###### Step 5: Determine Keys
Identify the candidate key(s) for an entity and then select the primary key
Some general guideline in choosing a primary key:
- The key with the minimal set of attributes
- The key with values least likely to change
- The Key with the fewest characters or smallest maximum value
- The key that is easiest to use from the user’s point of view
Document the keys
###### Step 7: Check Model for Redundancy
- Re-examine one-to-one (1..1) relationships
	- Merge entities if needed
- Removed redundant relationships
	- Between same entities
- Consider time dimensions
	- Potential influence in the future
###### Step 8: Validate Model with User Transactions
- Attempt to perform the operations manually using the model
- Can all transactions be done? If not, there must be a problem with the model
---
##### Problems with ER Models
Problems may arise when designing a conceptual data model called connection traps
- Often due to a <u>misinterpretation of the meaning of certain relationships</u>
- Two main types of connection traps are called **fan traps** and **chasm traps**
###### Fan Trap
This is where a model represents a relationship between entity types, but **the pathway between certain entity occurrences is ambiguous**
- A fan trap may exists where two or more 1:* relationships fan out from the same entity

![fan trap.png|700](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/5.%20Entity-Relationship%20Modelling/images/fan%20trap.png)
At which branch does staff number SG37 work?
**Remove Fan Trap:**
![remove fan trap.png|700](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/5.%20Entity-Relationship%20Modelling/images/remove%20fan%20trap.png)
SG37 works at branch B003
###### Chasm Trap
This is where a model suggests the existence of a relationship between entity types, but a pathway does not exist between certain entity types
- May occur with relationships with a minimum multiplicity of 0 forming part of the pathway between related entities

![chasm trap.png|700](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/5.%20Entity-Relationship%20Modelling/images/chasm%20trap.png)
At which branch office is property PA14 available?

**Remove Chasm Trap**
![remove chasm  trap.png|700](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/5.%20Entity-Relationship%20Modelling/images/remove%20chasm%20%20trap.png)


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/databases/6-logical-database-design/6-logical-database-design/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




### Database Design
**Conceptual Design**:
- See ER-Modelling
**Logical Design**
- The process of constructing a model of the data used in an enterprise based on a specific data model (e.g. relational), but independent of a particular DBMS and other physical considerations
**Physical Design**
- The process of producing a description of the implementation of the database on secondary storage; it describes the base relations, file organisations, and index design use to achieve efficient access to the data, and any associated integrity constraints and security measures
#### Critical Success Factors in DB Design
- Work interactively **with the users!**
- Follow a structured methodology throughout
- Employ a data-driven approach
- Incorporate structural and integrity considerations
- Combine conceptualisation, normalisation, and transaction validation techniques
- Use diagrams to represent data models
- Use a Database Design Language (DbDL) to represent additional data semantics
- Build a data dictionary to supplement the data model diagrams
#### Logical DB Design
Conceptual Model $\rightarrow$ Logical Model
1. Derive Relations
2. Validate Relations using normalisation
3. Validate relations against user transactions
4. Define integrity constraints
5. Review logical data model with user
6. (optional) Merge logical data models into global model
7. Check for future growth
##### Derive Relations
**Strong Entities**
- For each strong entity in the data model, create a relation that includes all the simple attributes of that entity
- For composite attributes, include only the constituent simple attributes
![strong entities.png|400](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/6.%20Logical%20Database%20Design/images/strong%20entities.png)

**Weak Entities**
- For each weak entity, create a relation with the primary key partially or full derived from each owner entity after all relationships with the owner entities have been mapped
![weak entities.png|400](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/6.%20Logical%20Database%20Design/images/weak%20entities.png)

**One-to-Many (1:\*) Binary Relationships**
- For each 1:\* binary relationship, the entity on the ‘one side’ is designated as the parent entity and the entity on the ‘many side’ is designated as the child entity. A copy of the primary key attribute(s) of the parent entity is placed in the relation for the child entity as a foreign key
![one-to-many binary.png|400](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/6.%20Logical%20Database%20Design/images/one-to-many%20binary.png)

**One-to-One (1:1) Binary Relationships**
More complex as the cardinality cannot be used to identify to parent and child identities in a relationship
- Instead, the participation constraints are used to decide whether
	- To represent the relationship by combining the entities involved into one relation or
	- by creating two relations and posting a copy of the primary key from one relation to the other
- Consider the following
	- **(a) Mandatory** participation on **both** sides
		- Combine entities into one relation and choose one of the primary keys of the entity to be primary key and the other as an alternate key
		- ![mandatory both one-to-one.png|400](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/6.%20Logical%20Database%20Design/images/mandatory%20both%20one-to-one.png)
	- **(b) Mandatory** participation on **one** side
		- The entity with optional participation is designated as the parent entity, and the entity with mandatory participation is designated as the child entity.
		- A copy of the primary key of the parent entity is places in the relation for the child entity
		- ![mandatory one one-to-one.png|400](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/6.%20Logical%20Database%20Design/images/mandatory%20one%20one-to-one.png)
	- **(c) Optional** participation on **both** sides
		- Arbitrary designation of the parent and child entities unless we can find out more about the relationship that can help a decision be made one way or the other
		- ![optional one-to-one.png|400](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/6.%20Logical%20Database%20Design/images/optional%20one-to-one.png)

**One-to-One (1:1) Recursive Relationships**
For 1:1 recursive relationships, follow the same rules for participation as in a 1:1 relationship

**Superclass/Subclass Relationships**
Identify superclass entity as the parent and the subclass entity as the child
There are options to represent such relationships depending on participation and disjoint constraints
![superclass-subclass.png|600](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/6.%20Logical%20Database%20Design/images/superclass-subclass.png)

**Many-to-Many (\*:\*) Binary Relationships**
Create a relation for the relationship with all the attributes of the relationship, with a copy of the primary key of the participating entities as foreign keys. These foreign keys will also form the primary key of the new relation
![many-to-many.png|500](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/6.%20Logical%20Database%20Design/images/many-to-many.png)

**Complex Relationships**
Create a relation to represent the relationship. Copy the primary key of the participating entities as foreign keys.
Any foreign keys that represent a ‘many’ relationship (for example, 1..\*, 0..\*) generally will also form the primary key of this new relation
![Complex.png|500](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/6.%20Logical%20Database%20Design/images/Complex.png)

**Multi-Valued Attributes**
Create a new relation for the multi-valued attribute with the primary key of the entity as a foreign key.
Unless the multi-valued attribute is itself an alternate key of the entity, the primary key of the new relation is the combination of the multi-valued attribute and the primary key of the entity
![multi-valued attributes.png|500](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/6.%20Logical%20Database%20Design/images/multi-valued%20attributes.png)
$\small\text{The branch could have more than one phone number!}$
##### Validate Relations with Normalisation
To validate the relations in the logical data model using normalisation to ensure that the set of relations has a minimal yet sufficient number of attributes necessary to support the data requirements of the enterprise
##### Validate Relations Against User Transactions
Attempt to perform the operations manually using the relations, and the primary key/foreign key links in the relations
If we are unable to perform a transaction manually, there must be a problem with the data model that must be resolved
##### Check Integrity Constraints
Identifying:
- Required data
- Attribute domain constraints
- Multiplicity
- Entity integrity
- Referential integrity
- General constraints
Referential integrity considerations when a tuple in parent relation is deleted:
- NO ACTION, CASCADE, SET NULL, SET DEFAULT, NO CHECK
##### Step 5 – Step 7
**Review the Logical Data Model with the User**
- Review the logical data model with the users to ensure that they consider the model to be a true representation of the data requirements of the enterprise
**Merge Logical Data Models into Global Model (Optional Step)**
- To merge logical data models into a single global logical data model that represents all user views of a database
**Check for Future Growth**
- To determine whether there are any significant changes likely in the foreseeable future and to assess whether the logical data model can accommodate these changes


#### Physical DB Design
Logical Model $\rightarrow$ Physical Model
1. Translate logical data model for target DBMS
2. Design file organisations and indexes
3. Design user views
4. Design security mechanisms
5. Consider the introduction of controlled redundency
6. Monitor and tune the operational system
##### Translate Logical Data Model for Target DBMS
**Design Base Relations**
From the data dictionary, produce the DbDL to define domains, default values, and null indicators
![Design base Relations.png|500](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/6.%20Logical%20Database%20Design/images/Design%20base%20Relations.png)
**Design Representation of Derived Data**
To decide how to represent any derived data present in the logical data model in the target DBMS
- Examine the logical data model and data dictionary, then produce a list of all the derived attributes
- Each derived attribute can be stored in the database or calculated every time it is needed
**Design General Constraints**
To design the general constraints for the target DBMS
- Some DBMS provide more facilities than others for defining enterprise constraints, Example:
![Design General Constraints.png|600](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/6.%20Logical%20Database%20Design/images/Design%20General%20Constraints.png)
##### Design File Organisations & Indexes
To determine \[optimal file organisations to store the base relations in and] the indexes that are required to achieve acceptable performance; that is, the way in which relations and tuples will be held on secondary storage
**Analyse Transactions**
To understand the functionality of the transactions that will run on the database and to analyse the import transactions
- Attempt to identify performance criteria, such as:
	- Transactions that run frequently and will have a significant impact on performance
	- Transactions that are critical to the business
	- Times during the day/week when there will be a high demand on the database (called the **peak load**)
**Choose file Organisations**
To determine an efficient file organisation for each base relation
- File organisations such as
	- Heap
	- Hash
	- Indexed Sequential Access Method (ISAM)
	- Some DBMSs may not allow selection of file organisations
**Choose Indexes**
To determine whether adding indexes will improve the performance of the system
- One approach is to keep tuples unordered and create as many secondary indexes as necessary
- Another approach is to order tuples in the relation by specifying a primary or clustering index
**Estimate Disk Space Requirements**
yeah
##### Design User Views
To design the user views that were identified during the Requirements Collection and Analysis stage of the database system development life-cycle
##### Design Security Measures
To design the security measures for the database as specified by the users
##### Consider the Introduction of Controlled Redundancy
- To determine whether introducing redundancy in a controlled manner by relaxing the normalisation rules will improve the performance of the system
##### Monitor and Tune the Operational System
- To monitor the operational system and improve the performance of the system to correct inappropriate design decisions or reflect changing requirements


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/databases/7-normalisation/7-normalisation/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




**Why Normalisation?**
To prevent data redundancy
- **Minimal** number of attributes required
- Attributes with a close logical relationship in the same relation
- **Minimal redundancy** $\rightarrow$ Less storage

### The ‘Approaches’
***Approach 1***: Use normalisation as a **bottom-up technique** to create a set of relations
***Approach 2***: Use normalisation as a **validation technique** to check structure of relations
#### Approach 1
![Approach 1.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/7.%20Normalisation/images/Approach%201.png)
##### Unnormalised Form (UNF)
A relation that contains one/more repeating groups
To create an unnormalised relation
- Transform the data from the information source (e.g. a form) into table format with columns and rows
![UNF.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/7.%20Normalisation/images/UNF.png)
##### First Normal Form (1NF)
A relation in which the **intersection** of each row and column contains **one and only one value**
UNF $\rightarrow$ 1NF
- Nominate an attribute or group of attributes to act as the primary key for the unnormalised table
- Identify the repeating group(s) in the unnormalised table which repeats for the key attribute(s)
- Remove the repeating group by
	- Entering appropriate data into the empty columns of rows containing the repeating data (‘flattening’ the table)
	- Or, by placing the repeating data along with a copy of the original key attribute(s) into a separate relation
![UNF-1NF.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/7.%20Normalisation/images/UNF-1NF.png)
##### Functional Dependency (FD)
If $\color{lightgreen} A$ and $\color{lightgreen} B$ are attributes of relation $\color{blue} R$, $\color{lightgreen} B$ is functionally dependent on $\color{lightgreen} A$ (denoted ${\color{lightgreen} A}\ \rightarrow \ {\color{lightgreen} B}$), if each value of $\color{lightgreen} A$ in $\color{blue} R$ is associated with exactly one value of $\color{lightgreen} B$ in $\color{blue} R$ (one-to-one relationship)
![Functional Dependency.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/7.%20Normalisation/images/Functional%20Dependency.png)
**Full Functional Dependency**: The dependent is functionally dependent on the determinant, but not any proper subset of the determinant
###### Partial & Transitive Dependencies
**Partial Dependency**
- $\color{red}\text{staffNo}$, staffName $\rightarrow$ warehouseNo, warehouseAddress, sales
-  ${\color{red}\text{staffNo}}\rightarrow$ warehouseNo, warehouseAddress, sales
Here warehouseNo, etc are *partially dependent* on $\textquoteleft\color{red}\text{staffNo}$, staffName’ as they don’t really need staffName
**Transitive Dependency**
- staffNo $\rightarrow \color{red}\text{warehouseNo}$, warehouseAddress, sales
- ${\color{red}\text{warehouseNo}}\rightarrow$ warehouseAddress
Here warehouseAddress is *transitively dependent* on staffNo
**Identify FD?**
- Users and/or documentation
- Common sense
- Sample data
##### Second Normal Form (2NF)
A relation that is in 1NF and every non-primary-key attribute is fully functionally dependent on the primary key/(any candidate key?)
1NF $\rightarrow$ 2NF
- Identify the functional dependencies in the relation
- Identify the primary key for the 1NF relation
- If the partial dependencies exist on the primary key, remove them by placing them in a new relation along with a copy of their determinant
![1NF-2NF.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/7.%20Normalisation/images/1NF-2NF.png)
##### Third Normal Form (3NF)
- A relation that is in 1NF and 2NF and in which no non-primary-key attribute is transitively dependent on the primary key/(any candidate key?)
2NF $\rightarrow$ 3NF
- Identify the primary key in the 2NF relation
- Identify functional dependencies in the relation
If transitive dependencies exist on the primary key, remove them by placing them in a new relation along with a copy of their determinant
##### Boycee-Codd Normal Form (BCNF)
A relation is in BCNF if and only if **every determinant is a candidate key**
- Every relation in BCNF is also in 3NF. However, a relation in 3NF is not necessarily in BCNF
##### More Function Dependencies?
The complete set of functional dependencies for a given relation can be very large
The set of all functional dependencies that are implied by a given set of functional dependencies *F* is called the **closure of *F***, written $\color{blue} \boldsymbol{F^{\tiny+}}$ 
- Armstrong’s axioms is used to find $\color{blue} \boldsymbol{F^{\tiny+}}$ 
###### Interference Rules for FDs
A set of interference rules, called **Armstrong’s axioms**, specifies how new functional dependencies can be inferred from given ones
- Let $\color{lightgreen} A$, $\color{lightgreen} B$, and $\color{lightgreen} C$ be subsets of the attributes of the relation $\color{blue} R$. Armstrong’s axioms are as follows:
1. **Reflexivity**
   If $\color{lightgreen} B$ is a subset of $\color{lightgreen} A$, then ${\color{lightgreen} A}\rightarrow{\color{lightgreen} B}$
2. **Augmentation**
   If ${\color{lightgreen} A}\rightarrow{\color{lightgreen} B}$, then ${\color{lightgreen} A},{\color{lightgreen} C}\rightarrow {\color{lightgreen} B},{\color{lightgreen} C}$
3. **Transitivity**
   If ${\color{lightgreen} A}\rightarrow{\color{lightgreen} B}$ and ${\color{lightgreen} B}\rightarrow{\color{lightgreen} C}$, then ${\color{lightgreen} A}\rightarrow{\color{lightgreen} C}$
Further rules can be derived from the first three rules. Let $\color{lightgreen} D$ be another subset of the attributes of relation $\color{blue} R$, then
4. **Self-determination**
   ${\color{lightgreen} A}\rightarrow{\color{lightgreen} A}$
5. **Decomposition**
   If ${\color{lightgreen} A}\rightarrow{\color{lightgreen} B},{\color{lightgreen} C}$ then ${\color{lightgreen} A}\rightarrow {\color{lightgreen} B}$ and ${\color{lightgreen} A}\rightarrow {\color{lightgreen} C}$
6. **Union**
   If ${\color{lightgreen} A}\rightarrow {\color{lightgreen} B}$ and ${\color{lightgreen} A}\rightarrow {\color{lightgreen} C}$, then ${\color{lightgreen} A}\rightarrow {\color{lightgreen} B},{\color{lightgreen} C}$
7. **Composition**
   If ${\color{lightgreen} A}\rightarrow{{\color{lightgreen} B}}$ and ${\color{lightgreen} C}\rightarrow {\color{lightgreen} D}$ then ${\color{lightgreen} A},{\color{lightgreen} C}\rightarrow {\color{lightgreen} B},{\color{lightgreen} D}$
**Example?**:
![Example.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/7.%20Normalisation/images/Example.png)
###### Closure
The closure of attribute set $\{{\color{lightgreen} A}\}$, denoted by $\{{\color{lightgreen} A}\}^{\tiny+}$ can also be inferred with Armstrong’s axioms
Given relation ${\color{blue} R}({\color{lightgreen} A},{\color{lightgreen} B},{\color{lightgreen} C},{\color{lightgreen} D},{\color{lightgreen} D})$ with function dependencies ${\color{red} F}\set{{\color{lightgreen} A}\rightarrow {\color{lightgreen} B},{\color{lightgreen} B}\rightarrow {\color{lightgreen} C},{\color{lightgreen} D}\rightarrow {\color{lightgreen} E},{\color{lightgreen} E}\rightarrow {\color{lightgreen} D}}$
**Closure of attributes:**
- $\{{\color{lightgreen} A}\}^{\tiny+}=\set{{\color{lightgreen} A},{\color{lightgreen} B},{\color{lightgreen} C}}$
- $\{{\color{lightgreen} B}\}^{\tiny+}=\set{{\color{lightgreen} B},{\color{lightgreen} C}}$
- $\{{\color{lightgreen} C}\}^{\tiny+}=\set{{\color{lightgreen} C}}$
- $\{{\color{lightgreen} D}\}^{\tiny+}=\set{{\color{lightgreen} D,{\color{lightgreen} E}}}$
- $\{{\color{lightgreen} E}\}^{\tiny+}=\set{{\color{lightgreen} D},{\color{lightgreen} E}}$
- $\{{\color{lightgreen} AB}\}^{\tiny+}=\set{{\color{lightgreen} A},{\color{lightgreen} B},{\color{lightgreen} C}}$
- etc…
###### Finding Candidate Keys with Attribute Closure
Given relation ${\color{blue} R}({\color{lightgreen} A},{\color{lightgreen} B},{\color{lightgreen} C},{\color{lightgreen} D},{\color{lightgreen} D})$ with function dependencies ${\color{red} F}\set{{\color{lightgreen} A}\rightarrow {\color{lightgreen} B},{\color{lightgreen} B}\rightarrow {\color{lightgreen} C},{\color{lightgreen} D}\rightarrow {\color{lightgreen} E},{\color{lightgreen} E}\rightarrow {\color{lightgreen} D}}$
**Closure of attributes**
- $\{{\color{lightgreen} A}\}^{\tiny+}=\set{{\color{lightgreen} A},{\color{lightgreen} B},{\color{lightgreen} C}}$
- $\{{\color{lightgreen} D}\}^{\tiny+}=\set{{\color{lightgreen} D,{\color{lightgreen} E}}}$
- $\{{\color{lightgreen} E}\}^{\tiny+}=\set{{\color{lightgreen} D},{\color{lightgreen} E}}$
Since a single attribute is unable to determine all the attributes on its own, we combine two or more attributes to determine the candidate keys
- $\set{{\color{lightgreen} A},{\color{lightgreen} D}}^{\tiny+}=\set{{\color{lightgreen} A},{\color{lightgreen} B},{\color{lightgreen} C},{\color{lightgreen} D},{\color{lightgreen} E}}$
- $\set{{\color{lightgreen} A},{\color{lightgreen} E}}^{\tiny+}=\set{{\color{lightgreen} A},{\color{lightgreen} B},{\color{lightgreen} C},{\color{lightgreen} D},{\color{lightgreen} E}}$
###### Minimal Sets of FDs
A set of functional dependencies ${\color{red} X}$ is minimal if it satisfies the following conditions
- Every dependency in ${\color{red} X}$ has a single attribute on its right-hand side (C1)
- We cannot replace any dependency ${\color{lightgreen} A}\rightarrow {\color{lightgreen} B}$ in ${\color{red} X}$ with dependency ${\color{lightgreen} C}\rightarrow {\color{lightgreen} B}$, where ${\color{lightgreen} C}$ is a proper subset of ${\color{lightgreen} A}$ and still have a set of dependencies that is equivalent to ${\color{red} X}$ (C2)
- We cannot remove any dependency from ${\color{red} X}$ and still have a set of dependencies that is equivalent to ${\color{red} X}$ (C3)
– Note that there can be several minimal covers for a set of functional dependencies


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/databases/8-database-security-and-administration/8-database-security-and-administration/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




**Why do we care?**
Data is valuable! it must be strictly controlled and managed, as with any corporate resource
The DBMS must ensure that the database is secure
Database security covers not only DBMS, but also its environment,
- Hardware, software (DBMS, application software, OS, etc…), people data, procedures
### Security
- **Confidentiality** – Secrecy over data
- **Integrity** – Protect against invalid or corrupted data
- **Availability** – Data or systems available to legitimate users
- Authentication
- Non-repudiation
**CIA** of security
![CIA.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/8.%20Database%20Security%20and%20Administration/images/CIA.png)
#### Database Security
**Protect against**:
- Loss of confidentiality on the secrecy over data critical to the organisation
- Loss of privacy on data about individuals
- Loss of integrity with invalid or corrupted data
- Loss of availability as data or systems are unavailable to legitimate users
- Theft and fraud of data, identity, programs, or hardware
**Threat** – Any situation or event, whether intentional or unintentional, that will adversely affect a system and consequently an organisation
- Need to consider not only the data held in a database but the whole ecosystem
- Failure to protect could lead to loss of confidentiality, loss of competitiveness, loss of privacy, legal action, corrupted data, financial loss, etc…
![Threats.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/8.%20Database%20Security%20and%20Administration/images/Threats.png)
![Threat Examples.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/8.%20Database%20Security%20and%20Administration/images/Threat%20Examples.png)
**Countermeasures**:
- Physical Controls
- Procedures
- Computer-Based Controls
##### Computer-Based Controls
###### Authorisation
The granting of a right or privilege, which enables a subject to legitimately have access to a system or a system’s object
- Involves authentication which determines whether a user is, who he or she claims to be
- A common authentication method is through the user of a password (we recommend a passphrase)
- How strong is your password
- Other methods? Multi-factor authentication such as *Duo*
###### Access Control
Methods used to enforce authorisation
- Based on the granting and revoking privileges
- A privilege allows a user to create or access (that is read, write, or modify) some database object (such as a relation, view, or index) or to run certain DBMS utilities
- Privileges are granted to users to accomplish the tasks required for their jobs

- **Most** DBMSs provide an approach called Discretionary Access Control (DAC)
- SQL standard supports DAC through the **GRANT** and **REVOKE** commands\*
- The GRANT command gives privileges to users, and the REVOKE command takes away privileges
\*SQLite does not support GRANT and REVOKE.
Access control is through the API at the application level
***Examples***:
```sql
GRANT SELECT, UPDATE (salary)
ON Staff
TO Personnel, Director;

GRANT SELECT
ON Branch
TO PUBLIC
```
###### Views
Hiding parts of the database from certain users
###### Backup & Recovery
Backup data at regular intervals to a secure location
**Journaling**
- Keep and maintain a log file (or journal) of all changes made to the database to enable effective recovery in the event of failure
###### Integrity Constraints
Through enforcing integrity constraints
- Domain constraints
- Entity integrity
- Referential integrity
###### Encryption
- Applying an encryption algorithm on data
- The encoding of the data by a special algorithm that renders the data unreadable by any program without the decryption key
- Four components: encryption key, encryption algorithm, decryption key, decryption algorithm
- Symmetric encryption – same key
		- Caesar cipher, Vigenere, DES, 3DES, Blowfish, AES, ChaCha
- Asymmetric encryption – different key
		- RSA (Rivest–Shamir–Adleman), Elliptical Curve, Cryptography (ECC), Diffie-Hellman
**Asymmetric Encryption**:
A set of keys: secrete/private key, public key
**Challenges**:
	- Key generation
	- Authentication of the public key $\rightarrow$ Public key infrastructure (PKI)
**Usage**:
	- Public key encryption
	- Digital signatures

**Public-key Infrastructure (PKI)**
A set of roles, policies, hardware, software and procedures needed to create, manage, use, store, and revoke digital certificates and manage public-key encryption
**CA** - Certificate Authority
- Creates, issues and manages the PKs as a trusted third party
**RA** - Registration Authority
- Ensures an authorised identity is requesting a certificate
**VA** - Validation Authority
- Authenticates and validates issued certificates
![PKI.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/8.%20Database%20Security%20and%20Administration/images/PKI.png)
###### Hashing
Process of taking a group of characters, apply a hash function to it, to generate a fixed length hash value
- One way encryption as the hashes are irreversible
**Examples**: MD5, SHA, SHA-2, SHA-3, DSA, Whirlpool, BLAKE, BLAKE-2, BLAKE-3
**Usage**:
	- Verify integrity of files and messages
	- Digital signatures
	- Password verification
###### DBMSs and Web Security
Internet communication relies on TCP/IP as the underlying protocol. However, TCP/IP and HTTP were not designed with security in mind. Without special software, all internet traffic travels ‘in the clear’ and anyone who monitors traffic can read it

You must ensure transmission over the Internet is:
- Inaccessible to anyone but the send and receiver (privacy/confidentiality?)
- Not changed during transmission (integrity)
- Receiver can be sure it came from the sender (authenticity)
- Sender can be sure receiver is genuine (non-fabrication)
- Sender cannot deny they sent it (non-repudiation)

**Security measures include**:
- Proxy servers
- Firewalls
- Message digest algorithms and digital signatures
- Digital certificates
- Kerberos
- Secure Sockets Layer (SSL) and Secure HTTP (S-HTTP)
- Secure Electronic Transactions (SET) and Secure Transaction Technology (SST)
###### Data & DB Administration
**Data administrator (DA)**
- Managing data resources, including database planning, development, maintenance of standards, policies, procedures, and conceptual and logical database design
**Data*base* administrator (DBA)**
- Application/physical database design to operational management including setting security and integrity control, and monitoring system performance
###### Data Administration Tasks
- Selecting appropriate productivity tasks
- Assisting in the development of the corporate IT/IS and enterprise strategies
	- $\small\text{Information Tech and Information Systems}$
- Undertaking feasibility studies and planning for database development
- Developing a corporate data model
- Determining the organisation’s data requirements
- Setting data collection standards & data formats
- Estimating volumes of data and likely growth
- Determining patterns and frequencies of data usage
- Determining data access requirements and safeguards for both legal and enterprise requirements
- Undertaking conceptual and logical database design
- Liaising with other parties involved with the database to ensure all requirements are met.
- Educating users on data standards & legal responsibilities
- Keeping up to date with IT/IS and enterprise developments
- Ensuring the documentation is up to data and complete
- Managing the data dictionary
- Liasing with users to determine new requirements and to resolve difficulties over data access or performance
- Developing a security policy
###### Data*base* Administration Tasks
- Evaluating and selecting DBMS products
- Physical database designs and implementation on target DBMS
- Defining security and integrity constraints
- Liasing with database application developers
- Developing test strategies
- Training users
- “Signing off” on the implemented database system
- Monitoring system performance and tuning the database
- Performing routine backups
- Ensuring recovery mechanisms & procedures are in place
- Ensuring that documentation is complete
- Keeping software & hardware up to date, including cost
![Data vs DB Admin.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/8.%20Database%20Security%20and%20Administration/images/Data%20vs%20DB%20Admin.png)


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/databases/9-transaction-management/9-transaction-management/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




**Why do we care?**
- How many users/database operations are accessing the database system at one time
- How sure are you that there won’t be any incidents affecting the data in the database? e.g. system crash, media failure, error in program? How about sabotage?
- DBMS provides concurrency control and database recovery
#### Transaction Support
**What is a transaction?**
- An action, or series of actions, carried out by a user or application, which reads or updates contents of a database
- Logical unit of work on the database
- An/The? Application program is a series of transactions with non-database processing in between
- Transforms the database from one consistent state to another, although consistency may be violated during transaction

- Can have one or two outcomes:
	- **Success** – the transaction commits and the database reaches a new consistent state
	- **Failure** – the transaction aborts, and the database must be restored to a consistent state before it is started
		- Such a transaction is rolled back or undone
- A committed transaction cannot be aborted
- An aborted transaction that is rolled back can be restarted later
![Example Transaction.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/9.%20Transaction%20Management/images/Example%20Transaction.png)
#### Properties of Transactions
There are four basic (***ACID***) properties that define a transaction:
- **Atomicity** – ‘All or nothing’ property
- **Consistency** – Must transform the database from one consistent state to another
- **Isolation** – Partial effects of incomplete transactions should not be visible to other transactions
- **Durability** – Effects of a committed transaction are permanent and must not be lost because of later
#### Concurrency Control
The process of managing simultaneous operations on the database without having them interfere with one another
- Prevents interference when two or more users are accessing database simultaneously and at least one is updating data
- Although two transactions may be correct in themselves, interleaving of operations may produce an incorrect result
**Need for Concurrency Control**
Three examples of potential problems caused by concurrency:
- Lost update problem
- Uncommitted dependency problem
- Inconsistent analysis problem
##### Lost Update Problems
A successfully completed update is overridden by another user
![Lost Update Problem.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/9.%20Transaction%20Management/images/Lost%20Update%20Problem.png)
	- Loss of $T_{2}$’s update avoided by preventing $T_{1}$ from reading $\text{bal}_{x}$ until after update
##### Uncommitted Dependency Problem
Occurs when one transaction can see intermediate results of another transaction before it has committed
![Uncommitted dependency problem.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/9.%20Transaction%20Management/images/Uncommitted%20dependency%20problem.png)
	- Problem avoided by preventing $T_{3}$ from reading $\text{bal}_{x}$ until after $T_{4}$ commits or aborts
##### Inconsistent Analysis Problems
Occurs when a transaction reads several values but a second transaction updates some of them during the execution of the first
![Inconsistent Analysis Problem.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/9.%20Transaction%20Management/images/Inconsistent%20Analysis%20Problem.png)
	- Problem avoided by preventing $T_{6}$ from reading $\text{bal}_{x}$ and $\text{bal}_{z}$ until after $T_{5}$ completed updates
##### Serialisability
The objective of a concurrency control protocol is to schedule non-interfering transactions
- Serialisability as a means of helping to identify those executions of transactions that are guaranteed to ensure consistency, as if the transactions are run in serial execution
**Why all these troubles? Recovery!**
- If a transaction in a schedule fails, it should be undone
- The DBMS does not test for serialisability of a schedule as the interleaving of operations is determined by the OS
- DBMS $\rightarrow$ concurrency control techniques to achieve serialisability
##### Concurrency Control Techniques
Two basic concurrency control techniques
- Locking
- Time-stamping
Both are conservative approaches: delay transactions in case they conflict with other transactions
Optimistic methods assume conflict is rare and only check for conflicts at commit
###### Locking
Transactions use locks to deny access to other transactions and to therefore prevent incorrect updates
Two types
- **Shared lock** for reading a data item
- **Exclusive lock** for both reading & writing a data item
Reads cannot conflict, so more than one transaction can hold shared locks simultaneously on the same item
**Exclusive lock** gives a transaction exclusive access to that item
Some systems allow transactions to upgrade a **shared lock** to an **exclusive lock**, or downgrade an **exclusive lock** to a **shared lock**

**Locks are used in the following way**:
- Any transaction that need to access a data item must first lock the item
- If the item is not already locked by another transaction, the lock will be granted
- If the item *is* locked, the DBMS determines whether the request is compatible with the existing lock. If a shared lock is requested on an item with a shared lock, the request will be granted; otherwise, the transaction must wait until the existing lock is released
- A transaction continues to hold a lock until it explicitly release it. It is only when the exclusive lock has been released that the effects of the write operation will be made visible to other transactions
###### Two-Phase Locking (2PL)
A transaction follows the 2PL protocol if all locking operations precede the first unlock operations in the transaction
**Two phases for the transaction**:
- ***Growing Phase*** – acquires all locks but cannot release any locks
- ***Shrinking Phase*** – releases the locks but cannot acquire any new locks

**Cascading Rollback**
If every transaction in a schedule follows 2PL, the schedule is serialisable
- However, problems can occur with the interpretation of when locks can be released
![Cascading Rollback.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/9.%20Transaction%20Management/images/Cascading%20Rollback.png)
$T_{14}$ aborts, since $T_{15}$ is dependent of $T_{14}$, $T_{15}$ must also be rolled back. Since $T_{16}$ is dependent on $T_{15}$, it too must be rolled back
**To prevent this with 2PL, you can:**
- ***Rigorous 2PL*** $\rightarrow$ Leave the release of **all** locks until the end of the transaction
- ***Strict 2PL*** $\rightarrow$ Hold only the **exclusive locks** until the end of the transaction
###### Deadlock
An impasse that may result when two (or more) transactions are each waiting for locks held by the other to be released
![Deadlock.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/9.%20Transaction%20Management/images/Deadlock.png)
There is only one way to break a deadlock: Abort all but one of the transactions
A deadlock should be transparent to the user, so the DBMS should restart the transaction(s)
However, in practice the DBMS cannot restart the aborted transaction since it is unaware of transaction logic even if it was aware of the transaction history (unless there is no user input in the transaction or the input is not a function of the database state)

**Three general techniques for handling a deadlock:**
- Timeouts
	- A transaction that requests a lock will only wait for a system defined period of time
	- If the lock has not been granted within this period, the lock request times out
	- In this case, the DBMS assumes the transaction may be deadlocked, even though it may not be, and it aborts and automatically restarts the transaction
- Deadlock prevention
	- The DBMS looks ahead to see if the transaction would cause a deadlock and never allows a deadlock to occur
**Deadlock detection and recovery**
The DBMS allows the deadlock to occur but recognises it and breaks it
- Usually handled by the construction of a wait-for graph (WFG) showing transaction dependencies
	- Create a node for each transaction
	- Create edge $T_{a}\rightarrow T_{b}$ if $T_{a}$ if waiting to lock an item locked by $T_{b}$
- A deadlock exists if and only if the WFG contains a cycle
![Deadlock WFG.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/9.%20Transaction%20Management/images/Deadlock%20WFG.png)
**Recovery**
There are several issues:
- Choice of the deadlock victim
	- How long has the transaction been running?
	- How many data items have been updated?
	- How many data items still need to be updated?
- How far to rollback a transaction?
- Avoiding starvation
	- Don’t make the same transaction a victim every time!
###### Time-stamping
A different approach to locking, with timestamps
- Transactions are ordered globally so that older transactions will smaller timestamps, get priority in the event of conflict
- Conflict is resolved by rolling back and restarting the transaction. No locks so no deadlock
- **Time-stamp**
	- A unique identifier that indicates the relative starting time of a transaction
	- Generated by using the system clock, or a logical counter
- A read/write will proceed only if the last update on that data item was carried out by an older transaction
- Otherwise, the transaction requesting the read/write is restarted and given a new timestamp
- Also timestamps for data items:
	- **read_timestamp** – The timestamp of the last transaction to read the item
	- **write_timestamp** – The timestamp of the last transaction to write to the item

**Basic Timestamp Ordering**
Consider a transaction ${\color{lightgreen} T}$ with timestamp $ts({\color{lightgreen} T})$ requesting to $read({\color{red} x})$
- $ts({\color{lightgreen} T}) < write\_timestamp({\color{red} x})$
	- ${\color{red} x}$ is already updated by a younger (later) transaction
	- The transaction must be aborted and restarted with a new timestamp
- Otherwise, update $read\_timestamp({\color{red} x})$

Consider a transaction ${\color{lightgreen} T}$ with timestamp $ts({\color{lightgreen} T})$ requesting to $write({\color{red} x})$
- $ts({\color{lightgreen} T}) < read\_timestamp({\color{red} x})$
	- ${\color{red} x}$ is already read by a younger transaction
	- Roll back the transaction and restart it using a later timestamp
- $ts({\color{lightgreen} T}) < write\_timestamp({\color{red} x})$
	- ${\color{red} x}$ is already written by a younger transaction
	- Roll back the transaction and restart it using a later timestamp
- Otherwise update $write\_timestamp({\color{red} x})$

**Strict time-stamping…**
When writing or reading, the transaction must also wait for the last transaction to write to the data item to abort/commit to avoid a cascading rollback

**Thomas’ Write Rule**
A variation to the basic timestamp ordering protocol that increase concurrency by relaxing strict serialisability
- Thomas’ write rule is that the write can safely be ignored – ignore obsolete write rules
	- When the current transaction wants to update a value that has been updated by a younger transaction, that write operation can be ignored and the current transaction does not need to be aborted

##### Optimistic Techniques
In some environments, conflicts are rare and it is more efficient to proceed without delays
- Checking for conflict before commit
- If there is a conflict, the transaction must be rolled back and restarted
- **Three phases**:
	- Read
	- Validation
	- Write
###### Read Phase
Extends from the start until immediately before the commit
- The transaction reads the values from the database and stores them in local variables. Updates are applied to a local copy of the data
###### Validation Phase
After the read phase,
For a read-only transaction, it checks that the data it read is still the same values. If no interference, the transaction is committed, otherwise it is aborted and restarted
- For an update transaction, it checks whether the transaction leaves the database in a consistent state (adheres to rules, constraints, and integrity requirements), with serialisability maintained

Each transaction ${\color{lightgreen} T}$ is assigned a time-stamp at
- The start of its execution, $start({\color{lightgreen} T})$
- The start of its validation phase, $validation({\color{lightgreen} T})$
- Its finish time, $finish({\color{lightgreen} T})$
Given transaction ${\color{lightgreen} T}_{x}$ at ${\color{blue} t}_{1}$ and transaction ${\color{lightgreen} T}_{y}$ at ${\color{blue} t}_{2}$ with $({\color{blue} t}_{2}>{\color{blue} t}_{1})$, to **pass** the validation test, either:
1. $finish({\color{lightgreen} T}_{x})<start({\color{lightgreen} T}_y)$, or
2. $start({\color{lightgreen} T}_{y})<finish({\color{lightgreen} T}_x)$, and
	1. The set of data items written by ${\color{lightgreen} T}_x$ are not the ones read by ${\color{lightgreen} T}_{y}$; and
	2. $start({\color{lightgreen} T}_y)<finish({\color{lightgreen} T}_{x})<validation({\color{lightgreen} T}_y)$
###### Write Phase
After a successful validation phase for an update transaction, the updates made to the local copy are applied to the database
##### Granularity of Data Items
The size of data items chosen as the unit of protection by the concurrency control protocol
**Ranging from coarse to fine:**
- The entire database
- A file (relation)
- A page
	- A unit of predetermined size (typically 4KB, 8KB, 16KB or more)
- A record (tuple)
- A field value of a record
**Trade-off:**
- Coarser, the lower the degree of concurrency
- Finer, more locking information than is needed is stored
The best item size depends on the types of transactions
![Granularity Heirarchy.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/9.%20Transaction%20Management/images/Granularity%20Heirarchy.png)
###### Hierarchy of Granularity
When a node is locked, all its descendants are also locked
- The DBMS should check the hierarchical path before granting a lock
- To reduce searching involved in locating locks, an intention lock could be used to lock all ancestors of a locked node
	- Intention locks can be read/write.
	  Applied top-down, released bottom-up
###### Multiple-Granularity Locking
**Intention Shared (IS)**: explicit locking at a lower level of the tree but only with shared locks
**Intention Exclusive (IX)**: explicit locking at a lower level with exclusive or shared locks
**Shared and Intention Exclusive (SIX)**: the sub tree rooted by that node is locked explicitly in shared mode and explicit locking is being done at a lower level with exclusive mode locks
![Multiple-Granularity Locking.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/9.%20Transaction%20Management/images/Multiple-Granularity%20Locking.png)
![Granular example.png|500](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/9.%20Transaction%20Management/images/Granular%20example.png)
4 Transactions ${\color{lightgreen} T}1$, ${\color{lightgreen} T}2$, ${\color{lightgreen} T}3$, ${\color{lightgreen} T}4$
${\color{lightgreen} T}1$ wants an ${\color{red} S}$ lock on $\text{Record}_{2}$
${\color{lightgreen} T}2$ wants an ${\color{red} X}$ lock on $\text{Record}_{2}$
${\color{lightgreen} T}3$ wants an ${\color{red} X}$ lock on $\text{Record}_{1}$
${\color{lightgreen} T}4$ wants an ${\color{red} S}$ lock on $\text{Page}_{2}$

#### Types of Failures
**System Crashes**: due to hardware/software errors, loss in main memory
**Media Failure**: such as head crashes or unreadable media, resulting in a loss of parts of secondary storage
**Application Software Errors**: such as logical errors
**Natural Physical Disasters**: such as fires, floods, etc…
**Carelessness or Unintentional Destruction of Data or Facilities**
**Sabotage**: intentional corruption/destruction
#### Transactions and Recovery
Transactions represent the basic unit of recovery
- **Recovery manager** responsible for atomicity and durability
- If failure occurs between a commit and the database buffers being flushed to secondary storage then, to ensure durability, **recovery manager** has to redo (roll-forward) the transaction’s updates
- If the transaction had not committed at failure time, **recovery manager** has to undo (rollback) any effects of that transaction for atomicity
##### Recovery Facilities
The DBMS should provide the following facilities to assist with recovery:
- **Backup Mechanism** – which make periodic backup copies of the database
- **Logging Facilities** – which keep track of the current state of the transactions and database changes
- **Checkpoint Facility** – which enables updates to the database in progress to be made permanent
- **Recovery Manager** – which allows the DBMS to restore the database to a consistent state following a failure
###### Log File
Contains information about all updates to the database:
- Transaction records
- Checkpoint records
Often used for other purposes (for example, auditing)
![Log file example.png|400](/img/user/Leeds%20University/Computer%20Science/Year%201/Databases/9.%20Transaction%20Management/images/Log%20file%20example.png)
- Log file may be duplexed or triplexed (2 or 3 copies)
- The log file is sometimes split into two separate random-access files
- Potential bottleneck; critical in determining overall performance
###### Checkpointing
- **Checkpoint** – the point of synchronisation between database and log file. All buffers are force-written to secondary storage
- A checkpoint record is created containing identifiers of all active transactions
- When failure occurs, redo all transactions that committed since the checkpoint and undo all transactions active the time of the crash
###### Recovery Techniques
If the database has been damaged:
- Need to restore the last backup copy of the database and reapply updates of the committed transactions using the log file
If the database is only inconsistent:
- Need to undo all changes that caused inconsistency. May also need to redo some transactions to ensure the updates reach secondary storage
- Do not need the backup, but can restore the database using before- and after-images in the log file
- Thee main recovery techniques:
	- **Deferred update** – till commit
	- **Immediate update** – immediately
	- **Shadow Paging** – two pages


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/databases/10-ethics/10-ethics/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




all my homies hate ethics!
###### SoMe GeNeRaL GuIdElInEs
- **Transparency** – Making sure the algorithms used, data collected, uses of the tools and so on is transparent to other peers and to the public
- **Communication** – Making clear to users and other for what purposed their data is being collected for, so that data subjects can give informed consent, and hold organisations accountable if the use this data in another way
- **Data Stewardship** – Making sure that data is securely kept, and also that it is not forwarded or sold to any dodgy third parties
- **Professional Responsibility** – Data scientists making sure that the projects they work on are ethical, and thinking about the uses that developed tools could be put to
- **Public and Professional Oversight** – Accountability of people in control of databases and data analytic tools to public and professional oversight
- **Legitimacy** – Making sure the purposes for and the contexts of the data collection mean that it is legitimate


</div></div>

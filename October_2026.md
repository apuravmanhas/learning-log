# October 2026

**2026-10-16**
* **Hours:** 4
* **Academic Engineering (DBMS — Relational Algebra):**
  * Covered the complete formal query language underlying SQL, in dependency order from primitive to derived operators:
    1. *Primitive Unary Operators:* Selection (sigma) for horizontal filtering by condition, Projection (pi) for vertical filtering by attribute columns, and Rename (rho) for schema aliasing.
    2. *Primitive Set Operators:* Union, Intersection, and Set Difference applied to union-compatible relations. Studied cardinality behavior for each operation.
    3. *Relational Comparison & Conditions:* Compound predicates using AND, OR, NOT. Comparison operators across attribute domains and their mapping to SQL WHERE clauses.
    4. *Join Operators:* Cartesian Product (base), Theta Join (generalised condition), Equi-Join (equality-only condition), Natural Join (automatic attribute matching), Semi-Join, and Anti-Join. Studied output schema and tuple count for each.
    5. *Division Operator:* Relational division for queries of the form find tuples related to ALL values in another relation. Mapped to its SQL equivalent using NOT EXISTS / EXCEPT.
    6. *Extended Operators:* Grouping (gamma) with aggregate functions and Ungrouping. How these map to GROUP BY and ROLLUP/CUBE in SQL.

---

**2026-10-15**
* **Hours:** 6
* **Code & Data Science (Data Visualization Stack + NumPy Deep Dive):**
  * Covered the complete Python visualization ecosystem in structured order from foundational charts to statistical distributions:
    1. *Core Chart Types (Matplotlib):* Bar charts, pie charts, scatter plots, and histograms. Practised axis labeling, text alignment, title placement, and custom tick formatting.
    2. *Statistical Distribution Plots (Matplotlib + Seaborn):* Box plots (IQR, whiskers, outlier detection), violin plots (kernel density estimation mirrored around a center axis), and swarm plots (non-overlapping jittered points showing full data distribution).
    3. *Seaborn Integration:* Layering Seaborn statistical plots on Matplotlib Axes objects. Understood how Seaborn is a high-level wrapper around Matplotlib using the same Figure/Axes architecture under the hood.
    4. *Text Annotation & Layout:* Word clouds for frequency-weighted text visualization. Axis text alignment controls, annotation placement, and multi-subplot layout management.
    5. *NumPy (Mathematical & Statistical Functions):* Revisited and deepened understanding of array attributes (shape, dtype, ndim, size, strides). Practiced mathematical ufuncs (np.sqrt, np.log, np.exp, np.power) and statistical aggregations (np.mean, np.median, np.std, np.var, np.percentile, np.corrcoef).

---

**2026-10-14**
* **Hours:** 6
* **Academic Engineering (DBMS — Foundations to Indexing for University Exams):**
  * Covered the full DBMS stack in sequential order from relational theory to physical storage structures:
    1. *Relational Model Foundations:* Relations, attributes, degree (number of attributes), cardinality (number of tuples), and static vs. dynamic relations.
    2. *Keys & Constraints:* Super key, candidate key, primary key, foreign key, and composite key. Enforcing referential integrity and constraint propagation across tables.
    3. *SQL Command Architecture:* DDL (CREATE, ALTER, DROP), DML (INSERT, UPDATE, DELETE), TCL (COMMIT, ROLLBACK), and DCL (GRANT, REVOKE) — reviewed their execution context within transaction boundaries.
    4. *Storage & Indexing — B-Trees and B+ Trees:* Structural differences between B-Trees (data stored at all nodes) and B+ Trees (data only at leaf nodes, linked list at leaves). Insertion, deletion, and search time complexity. Why RDBMS engines (MySQL InnoDB, PostgreSQL) exclusively use B+ Trees for secondary indexing.
    5. *Hashing & Collision Resolution:*
       * Static Hashing: Open addressing (linear probing, quadratic probing, double hashing) vs. Separate chaining.
       * Dynamic/Extensible Hashing: Global depth, local depth, bucket splitting, and directory doubling mechanics. All associated formulas and bit-manipulation concepts for bucket address calculation.
  * Studied all standard formulas for hashing, tree height, and space utilization across indexing methods.

---

**2026-10-13**
* **Hours:** 3
* **Code & Data Science Foundations (NumPy & Matplotlib Deep Dive):** 
  * *NumPy (Array Manipulation & Vectorization):*
    * Practiced multi-dimensional slicing and advanced boolean masking (filtering arrays via conditional indexing).
    * Experimented with array broadcasting rules across mismatched shapes to understand memory layout and dimension expansion.
    * Implemented axis-specific aggregations (\xis=0\ vs \xis=1\) and basic matrix operations (p.dot\, matrix transpositions).
  * *Matplotlib (Visualization & Object-Oriented API):*
    * Transitioned from standard stateful plotting to the Object-Oriented API using \plt.subplots()\, manipulating \Figure\ and \Axes\ objects directly.
    * Built multi-panel plots, distribution histograms, and scatter plots mapped to synthetic datasets.
    * Configured plot aesthetics: custom markers, gridlines, axis scaling, legends, and layout padding via \plt.tight_layout()\.
  * *Key Takeaway:* Practiced feeding vectorized NumPy transformations directly into visualization pipelines without relying on inefficient Python loops.

---

**2026-10-12**
* **Hours:** 7
* **Academic Engineering (OOP & C++ Deep Dive for University Exams):** 
  * Structured and revised Object-Oriented Programming concepts from foundational mechanics to runtime dispatch:
    1. *Object Mechanics & Lifecycle:* Member functions, friend functions, constructors (types, initialization lists), and destructors.
    2. *Inheritance Hierarchies:* Single, multiple, multilevel, hierarchical, and hybrid inheritance; member access control (public, protected, private).
    3. *Compile-Time (Static) Polymorphism:* Function overloading, unary operator overloading, and binary operator overloading.
    4. *Run-Time (Dynamic) Polymorphism:* Function overriding, virtual functions (vtable/vptr mechanics), and virtual base classes (resolving the diamond problem).
    5. *Robustness & Control Flow:* Exception handling fundamentals (	ry, catch, 	hrow) and defining custom user-defined exceptions.
  * Wrote and analyzed concrete code implementations exploring edge cases for each paradigm.

---

**2026-10-11**
* **Hours:** 6
* **Academic Engineering (Software Engineering Exam Prep):** 
  * Completed an intensive, structured revision of the Software Engineering lifecycle:
    1. *Requirements Engineering:* Requirements analysis, Software Requirements Specification (SRS), and Data Dictionaries.
    2. *System Design & Modeling:* Data Flow Diagrams (DFD), Entity-Relationship (ER) diagrams, and Unified Modeling Language (UML).
    3. *Estimation & Project Management:* Software Project Management (SPM), size estimation, effort/cost modeling via the COCOMO model, and project scheduling using Gantt charts.
    4. *Risk Management:* Risk identification, assessment, and mitigation planning.

---

**2026-10-10**
* **Hours:** 1
* **Code (NumPy):** 
  * Transitioned from theory to practical code execution (prep for upcoming university exams).
  * Practiced creating, reshaping, and manipulating 1D and 2D 
p.array structures.
  * Wrote scripts to test array slicing, vectorization concepts, and core mathematical/statistical functions.

---

**2026-10-09**
* **Hours:** 5
* **Code (Data Science Stack):** 
  * Studied the theoretical foundations of NumPy: explored 
darray attributes, data types, array creation methods, and core applications.
  * Reviewed Matplotlib fundamentals: understanding the hierarchy of figures, subplots, and basic charting/graphing capabilities.
  * *Note:* Heavy theory day. Need to ensure this is immediately followed up by practical coding implementation tomorrow so the concepts don\'t fade.

---

**2026-10-08**
* **Hours:** 1
* **Code (SQL):** 
  * Practiced the core SQL command categories: DDL (Definition), DML (Manipulation), TCL (Transaction Control), and DCL (Data Control).
* **Blocker / Status:** 
  * University exams, assignments, and projects are heavily starting to eat into my time and focus. 
  * *Note:* Experiencing the classic collision between the academic workload and actual engineering skill-building. Need to tightly manage my time so this doesn\'t derail my daily momentum.

---

**2026-10-07**
* **Hours:** 1
* **Code (SQL):** 
  * Studied fundamental SQL aggregate functions: COUNT(), SUM(), AVG(), and MIN().
  * Practiced using the GROUP BY clause to aggregate data across categories.
  * Reinforced basic database querying structures and syntax.

---

**2026-10-06**
* **Hours:** 1
* **Code (Python):** 
  * Practiced foundational coding questions centered on functions.
  * Reviewed the mechanics of function definitions, syntax, and execution flow.
  * *Blocker:* Still experiencing some confusion around function definitions—specifically how parameters map to arguments and how the code execution jumps when a function is called.

---

**2026-10-05**
* **Hours:** 2
* **Code (Python):** 
  * Continued practicing * pattern loops and studying the underlying mathematical logic. 
  * *Blocker:* Confused about how to dynamically handle user input for sizing the pattern grids.
  * Started learning functions: definitions, calling, default arguments, and parameters. 
  * Explored the concept of recursion and base cases, and how functions improve code reusability.

---

**2026-10-04**
* **Hours:** 6
* **Code (Python):** Practiced nested loops by building `*` pattern shapes. 
  * *Blocker:* Found it difficult to manage indentation, calculate exact spaces, and set the correct `range()` boundaries for inverted shapes. 
  * *Status:* Still working on fully grasping how the inner and outer loops interact with spaces.
* **Reading (Research):** Studied YOLO object detection models applied to weapon detection. Focused on understanding their performance metrics and current limitations. Also read up on global market insights.
* **Side Quest (Sniptoolkit):** 
  * Polished the UI for our team's website (`sniptoolkit`). 
  * Stress-tested the compiler using extreme AI-generated edge cases. 
  * Deployed the changes to a `workers.dev` preview environment.

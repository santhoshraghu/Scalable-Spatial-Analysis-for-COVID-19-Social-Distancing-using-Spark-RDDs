# Scalable-Spatial-Analysis-for-COVID-19-Social-Distancing-using-Spark-RDDs
Big Data 
Step 1 – Synthetic Data Creation:
Create three datasets using python — PEOPLE-large, INFECTED-small, and PEOPLE-SOME-INFECTED-large. Each dataset consists of 2D points (x, y) with unique identifiers (id) and additional attributes. 

*PEOPLE-large:* A large dataset including everyone with random points. The infection status is unknown.

*INFECTED-small:* A subset of PEOPLE-large with individuals infected with COVID-19.

*PEOPLE-SOME-INFECTED-large:* Two assumptions:
1. This dataset is the same as PEOPLE-large, but with an additional "INFECTED" column based on records in INFECTED-small.
2. This dataset is independent of PEOPLE-large and INFECTED-small, with its own "INFECTED" column.

Step 2 – Executed these Queries on the synthetic dataset:
Query 1: Close Contacts Identification
Given PEOPLE-large and INFECTED-small, identify close contacts (within 6 units) for each infected person from INFECTED-small in PEOPLE-large.
- Output: List of pairs (pi, infect-i) representing people pi from PEOPLE-large in close contact with infect-i.

Query 2: Unique Close Contacts
Building on Query 1, remove duplicate entries of close contacts. Even if a person was close to multiple infected individuals, include them only once.
- Output: List of unique pi.id representing people from PEOPLE-large who were close contacts at the concert.

Query 3: Count of Close Contacts
Given PEOPLE-SOME-INFECTED-large, count the number of close contacts (within 6 feet) for each infected person based on the "INFECTED" attribute.
- Output: Pairs (infect-i, count-of-close-contacts-of-infect-i)Step 1 – Synthetic Data Creation: Create three datasets using python — PEOPLE-large, INFECTED-small, and PEOPLE-SOME-INFECTED-large. Each dataset consists of 2D points (x, y) with unique identifiers (id) and additional attributes. *PEOPLE-large:* A large dataset including everyone with random points. The infection status is unknown. *INFECTED-small:* A subset of PEOPLE-large with individuals infected with COVID-19. *PEOPLE-SOME-INFECTED-large:* Two assumptions: 1. This dataset is the same as PEOPLE-large, but with an additional "INFECTED" column based on records in INFECTED-small. 2. This dataset is independent of PEOPLE-large and INFECTED-small, with its own "INFECTED" column. Step 2 – Executed these Queries on the synthetic dataset: Query 1: Close Contacts Identification Given PEOPLE-large and INFECTED-small, identify close contacts (within 6 units) for each infected person from INFECTED-small in PEOPLE-large. - Output: List of pairs (pi, infect-i) representing people pi from PEOPLE-large in close contact with infect-i. Query 2: Unique Close Contacts Building on Query 1, remove duplicate entries of close contacts. Even if a person was close to multiple infected individuals, include them only once. - Output: List of unique pi.id representing people from PEOPLE-large who were close contacts at the concert. Query 3: Count of Close Contacts Given PEOPLE-SOME-INFECTED-large, count the number of close contacts (within 6 feet) for each infected person based on the "INFECTED" attribute. - Output: Pairs (infect-i, count-of-close-contacts-of-infect-i)
Skills: PySpark · SparkRDD · Python (Programming Language)

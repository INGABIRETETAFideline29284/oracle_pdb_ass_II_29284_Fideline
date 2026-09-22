# oracle_pdb_ass_II_29284_Fideline
# Oracle PDB Assignment II

Student Information

| Item               | Details                             |
| ------------------ | ----------------------------------- |
| Student Name       | Fideline                            |
| Student ID         | 29284                               |
| Oracle Version     | Oracle Database 21c Express Edition |
| Main PDB Name      | FI_PDB_29284                        |
| PDB Username       | FIDELINE_PLSQLAUCA_29284            |
| Temporary PDB Name | FI_TO_DELETE_PDB_29284              |
| Repository Name    | oracle_pdb_ass_II_29284_fideline    |

1. Assignment Overview

This assignment demonstrates the practical administration of an Oracle multitenant database environment using Oracle Database 21c Express Edition.

These are the overview tasks to be done in assignment II:

1.Create a new Pluggable Database (PDB) using the required naming convention.
2.Create an administrative user inside the PDB.
3.Verify the PDB creation and its open state.
4.Create a temporary PDB.
5.Verify and completely delete the temporary PDB.
6.Access Oracle Enterprise Manager (OEM/EM Express).
7.Display the Oracle database environment and PDB information.
8.Document the activities and provide evidence through screenshots.

2. Oracle Environment

The assignment was completed using:

Database: Oracle Database 21c Express Edition
Operating System: Windows
Database Tool: Oracle SQL Developer
Database Management Interface: Oracle Enterprise Manager Express
Oracle Listener Port: 1521
EM Express HTTPS Port: 5500

The Oracle multitenant environment contains a Container Database (CDB) and Pluggable Databases (PDBs).

The main PDB created for this assignment is:

FI_PDB_29284

The PDB was created inside the Oracle Container Database and opened in `READ WRITE` mode.

3. Task 1 – Create a New PDB

3.1 PDB Creation

The required PDB naming convention was:

FirstTwoLettersOfFirstName_pdb_StudentID

For this assignment:

FI_PDB_29284

3.2 Verify PDB Creation

The PDBs were checked using:

SHOW PDBS;

The created PDB was identified as:

FI_PDB_29284

Initially, the PDB was in `MOUNTED` state.

3.3 Open the PDB

The PDB was opened using:

ALTER PLUGGABLE DATABASE FI_PDB_29284 OPEN;

The PDB status was then verified using:

SHOW PDBS;

The expected state was:

FI_PDB_29284    READ WRITE

This confirmed that the PDB was successfully created and opened.

3.4 Verify the PDB User

The PDB administrator username created for the assignment was:

FIDELINE_PLSQLAUCA_29284

The username was verified from a connection to the created PDB using:

SELECT USER FROM DUAL;

The result confirmed the required user.

4. Task 2 – Create and Delete a Temporary PDB

4.1 Create Temporary PDB

The temporary PDB required by the assignment was:

FI_TO_DELETE_PDB_29284

The temporary PDB was then verified using:

SHOW PDBS;

The PDB appeared in the list of available PDBs.

4.2 Delete Temporary PDB

After confirming its existence, the temporary PDB was completely removed.

4.3 Confirm Deletion

The PDB list was checked again:

SHOW PDBS;

The result confirmed that:

FI_TO_DELETE_PDB_29284

was no longer present.

Therefore, the temporary PDB was successfully created, verified, and completely deleted.

5. Task 3 – Oracle Enterprise Manager

Oracle Enterprise Manager Express was accessed using:

https://localhost:5500/em

The Oracle environment was accessed through the root container:

CDB$ROOT

As we've seen above the PDB created for the assignment was:

FI_PDB_29284

The Oracle environment and PDB information were checked using Oracle Enterprise Manager and SQL Developer.

6. Screenshots and Evidence

Screenshots have been organized into separate folders for easier verification.

7. Challenges Encountered and Solutions

Challenge 1: Connecting to the PDB

Initially, connecting to the newly created PDB was not possible before the PDB had been created and opened.

Solution:

The PDB was first created and opened from the "CDB$ROOT" container. A separate SQL Developer connection was then created using:

Hostname: localhost
Port: 1521
Service Name: FI_PDB_29284

This allowed the PDB user to connect successfully.

Challenge 2: PDB Open State

After creation, the PDB initially appeared as:

MOUNTED

Solution:

The PDB was opened using:

ALTER PLUGGABLE DATABASE FI_PDB_29284 OPEN;

It was then verified using:

SHOW PDBS;

The PDB subsequently appeared as:

READ WRITE

Challenge 3: Viewing the Oracle Environment

The PDB dashboard and the overall Oracle environment are different levels of the Oracle multitenant architecture.

Solution:

The overall Oracle environment was accessed through:

CDB$ROOT

while the assignment PDB was:

FI_PDB_29284

Conclusion:

The Oracle PDB Assignment II was completed using Oracle Database 21c Express Edition. The required PDB "FI_PDB_29284" was created with the specified administrative user and successfully opened. A temporary PDB, "FI_TO_DELETE_PDB_29284", was also created, verified, and completely deleted. Oracle Enterprise Manager Express was used to access and display the Oracle database environment and PDB information.

Repository Link: [https://github.com/INGABIRETETAFideline29284/oracle_pdb_ass_II_29284_Fideline]
PDB Name Created: [FI_PDB_29284]
Issues Encountered: [Yes]

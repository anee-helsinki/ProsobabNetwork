## Social Networks of Prosobab

This repository contains the network of people and documents mined from the database dump of The Prosobab - an open access prosopography of Babylonia in the Neo-Babylonian and Persian periods (c. 620-330 BCE) https://prosobab.leidenuniv.nl/index.php. The database was created in a ERC Consolidator Grant project at the University of Leiden. The database can be browsed online but, as it is a university project, the continuance of the the site cannot be guaranteed. 

A dump of the SQL database was published in DANS  https://doi.org/10.17026/dans-zvn-eece. To access the data in the dump we created an empty database in MySql:

```sql
CREATE DATABASE DB
```
Then from the command line we inserted the dump into the new database:
```Bash
mysql -u <user> -p DB < include/prosobab-dump-2022-06-03.sql
```
The password for the database in DB.

From the MySql database, we extracted all persons, their attestations in documents, and the documents. We publish here three spreadsheets in a xlsx-file:
- Individual persons with all the information in the database + all the attestations (ids) of the individual in texts
- Documents with all the information in the database + all the attestations (ids) of individuals in the document
- The attestation of individuals (with ids) in documents (with ids) with information on that occasion.

The tables are also available as separate tsv-files.

We also extracted networks with...

<p align="center">
<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a><br />These files are licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/">Creative Commons Attribution-NonCommercial 4.0 International License</a>.</p>

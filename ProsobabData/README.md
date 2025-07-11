### The data extracted from the Prosobab database dump

A dump of the SQL database was published by Prosobab in DANS  https://doi.org/10.17026/dans-zvn-eece. To access the data in the dump we created an empty database in MySql:

```sql
CREATE DATABASE DB
```
Then from the command line we inserted the dump into the new database:
```Bash
mysql -u <user> -p DB < prosobab-dump-2022-06-03.sql
```
The password for the database is DB.

From the MySql database, we extracted all persons, their attestations in documents, and the documents. We publish here three TSV-files (tab-separated-values):
- Documents with all the information in the database + all the attestations (ids) of individuals in the document
- Individual persons with all the information in the database + all the attestations (ids) of the individual in texts
- The attestation of individuals (with ids) in documents (with ids) with information on that occasion.

We extracted from the database all the information that is available also on the online service of Prosobab for each of the three views on the data. Since, in the Prosobab database, it is the documents that have the date with the name of the king, year, month, and day whenever feasable but online each individual has a date range, we extracted the earliest and latest documents for all the individuals and added their date as that persons min date and max date. 

These files contain also some additions. From the min and max dates of an individual, we extracted the min and max reigns the person is attested in. The reigns of the kings also have a serial number (see SupplementaryFiles/reignNumbers). We have added modified id-numbers with a letter to distinguish the tablets (T), individuals (P for personal id) and attestations (A) from each other. We also added zeros in front of the number. Thus the tablet with id 151 became T00151 and the individual with personal id 5983 was given id P05983. The original ids can also be found in the tables. The modified id-numbers are used in the networks of relations and roles that we created (see Networks folder). Each document also has the id-numbers of all the attestations found in it and all individuals have all the id-numbers of their attestations.

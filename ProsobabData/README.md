# The data extracted from the Prosobab database dump

A dump of the SQL database was published by Prosobab in DANS (Waerzeggers and Groß 2022). To access the data in the dump we started MySql with the command:
```bash
mysql -u root -p
```
...and  created an empty database (you can use any name) in MySql:
```sql
mysql> CREATE DATABASE DB;
```
Using the command line, we inserted the dump into the new database:
```Bash
mysql -u root -p DB < prosobab-dump-2022-06-03.sql
```
Once back in MySql, we started using the the database:
```sql
mysql> USE DB;
```

From the MySql database, we extracted all individuals, their attestations in tablets (cuneiform documents), and the tablets. We publish the extracted data here in two formats, as three TSV files (tab-separated values) and as an Excel worksheet:
- Attestations.tsv: The attestations of individuals (with IDs) in tablets (with IDs) with information on that attestation.
- Individuals.tsv: Individual persons with all the attribute information available in the database. We have also added attestation IDs for each individual. This is the same file as /Networks/individuals.tsv, but two column titles have been changed: Personal ID = ID and Name = Label. **New file coming shortly!**
- Tablets.tsv: Tablets with all the metadata in the database + all the attestation IDs of individuals in the tablet.

From the database, we extracted all the information that is also available on the online portal of Prosobab in the attestation, individual, and tablet views. The online portal provides a date range for each individual, showing when the person is attested for the first and last time in a dated tablet. The dates are available for each tablet in the database, and from there we extracted the dates for the earliest and latest tablets for each individual and added these dates as that person's min date and max date. 

These files also contain some additions. Using the min and max dates of an individual, we extracted information about the kings who were ruling when a person was attested for the first (min reign) and the last time (max reign). To facilitate automatic processing of the data, we gave a running number for each king from the earliest to the latest ("Min reign order" and "Max reign order"; see /SupplementaryFiles/reignNumbers). Finally, we added modified ID numbers preceded by a letter to distinguish tablets (T), individuals (P for personal ID), and attestations (A) from each other. We also added zeros in front of the number. Thus the tablet with ID 151 became T00151, and the individual with personal ID 5983 was given ID P05983. The original IDs can also be found in the TSV files. The modified ID numbers are used in the networks we created (see the folder Networks).

To aid automatic processing of the data, Babylonian months are given running numbers from first to last. This means that intercalary months (Ululu and Addaru, normally referred to as VIb and XIIb) affect the numbering. In this data, intercalary Ululu (normally VIb) is month 7, Tašritu (normally VII) is month 8, and so forth. Intercalary Addaru (XIIb) is thus month 14. The numbering follows the same system regardless of the presence or absence of an intercalary month in a given year.

The MySql queries can found in the folder _Queries/_.

## References 
Waerzeggers, C., & Groß, M. (2022). Prosobab (version 1.0). DANS Data Station Archaeology. https://doi.org/10.17026/dans-zvn-eece.

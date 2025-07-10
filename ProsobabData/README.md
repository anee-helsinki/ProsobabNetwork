### The data extracted from the Prosobab database dump


Individuals.tsv: Individual persons with all the information in the database + all the attestations (ids) of the individual in texts

Tablets.tsv: Tablets (or other documents) with all the information in the database + all the attestations (ids) of individuals in the document

Attestations.tsv: The attestation of individuals (with ids) in documents (with ids) with information on that occasion.

We have added modified id-numbers with a letter to distinguish the tablets (T), individuals (P for personal id) and attestations (A) from each other. We also added zeros in front of the number. Thus Tablet id 151 became T00151 and Individual with personal id 5983 was given id P05983. The original ids are also in the tables. The modified id-numbers are used in the networks of relations and roles that we created.

We extracted from the database all the information that is available also on the online service of Prosobab for each of the three views on the data. Since, in the Prosobab database, it is the documents that have the date with the name of the king, year, month, and day whenever feasable but online each individual has a date range, we extracted for all the individuals the earliest and latest documents and added their date as that persons min date and max date. We also extracted from that the min and max reigns the person is attested in. Each tablet also has id-numbers of all the attestations found in it and all individuals have all the id-numbers of their attestations.

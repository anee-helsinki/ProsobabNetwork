### Networks of Neo-Babylonian people

The dataset is intended to be used primarily in social network analysis. It contains a nodelist of persons and an edgelist for persons attested in the same documents. There are also several directed networks from the information on the relations and roles of the individuals as specified in Prosobab. We connected people to each other on the basis of various social roles such as creditor and debtor, bride and groom, and father and child. Each type of relation is presented in a single edge list that also contains attribute data about the social relation and the tablet in which it is documented. All the data about persons is presented in a separate file which one can use as a node list.

- **individuals.tsv** = Nodelist of all persons in the network. Can be used with the edgelists.
- **connections.tsv** = Edgelist of nodes (persons) attested in the same documents. Weight is the number of co-occurrences. _Undirected_.
- **relations.tsv** = Edgelist of nodes (persons) that have a relation such as 'X brother of Y'. _Directed_.
- **legalRoles.tsv** = Edgelist of nodes (persons) in legal role pairs with each other (e.g. judge and litigant or creditor and debtor). For the list of role pairs see SupplementaryFiles/RolePairs.csv. _Directed_.
- **sameRoles.tsv** = Edgelist of nodes (persons) that have the same role in the same document. For the list of roles see SupplementaryFiles/Roles.txt. _Directed both ways_.
- **rolesWithWitnessesScribes.tsv** = Edgelist between nodes (persons) that have a role from the SupplementaryFiles/Roles.txt list and nodes (persons) designated as witnesses or scribes who have been attested in the same document. _Directed_.
- **witnessScribeConnections.tsv** = Edgelist between nodes (persons) designated as witnesses or scribes who have been attested in the same document. _Undirected_.

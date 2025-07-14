### Networks of Neo-Babylonian people

The dataset contains a nodelist of all persons and an edgelist for persons attested in the same documents. That attribute data for the individuals comes from the Prosobab database. We have also build several directed networks from the relations and roles of the individuals as specified in Prosobab. Each edgelist contains one types of relations/roles with the attribute data about the social relations/roles and the tablets in which it they are attested. The nodelist of all persons can used with these edgelists.

#### Files
- **individuals.tsv** = Nodelist of all persons in the network with the attribute data. Can be used with the edgelists.
- **connections.tsv** = Edgelist of nodes (persons) attested in the same documents. Weight is the number of co-occurrences. _Undirected_.
- **relations.tsv** = Edgelist of nodes (persons) that have a relation such as 'X brother of Y'. _Directed_.
- **legalRoles.tsv** = Edgelist of nodes (persons) in legal role pairs with each other (e.g. judge and litigant or creditor and debtor). For the list of role pairs see SupplementaryFiles/RolePairs.csv. _Directed_.
- **sameRoles.tsv** = Edgelist of nodes (persons) that have the same role in the same document. For the list of roles see SupplementaryFiles/Roles.txt. _Directed both ways_.
- **rolesWithWitnessesScribes.tsv** = Edgelist between nodes (persons) that have a role from the SupplementaryFiles/Roles.txt list and nodes (persons) designated as witnesses or scribes who have been attested in the same document. _Directed_.
- **witnessScribeConnections.tsv** = Edgelist between nodes (persons) designated as witnesses or scribes who have been attested in the same document. _Undirected_.

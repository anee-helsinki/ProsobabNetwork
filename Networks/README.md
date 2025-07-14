### Networks of Neo-Babylonian people

The dataset is intended to be used primarily in social network analysis. It contains a nodelist of persons and an edgelist for persons attested in the same documents. There are also several directed networks from the information on the relations and roles of the individuals as specified in Prosobab. The networks allows the researcher to study questions about who knew whom and which persons were in interaction with each other. 

- **individuals.tsv** = Nodelist of all persons in the network. Can be used with the edgelists to visualise the network so that it contains node attributes
- **connections.tsv** = Edgelist of nodes (persons) attested in the same documents. Weight is the number of co-occurrences. _Undirected_.
- **relations.tsv** = Edgelist of nodes that have a relation such as 'X brother of Y'. _Directed_.
- **legalRoles.tsv** = Edgelist of nodes in legal role pairs with each other (e.g. judge and litigant or creditor and debtor). For the list of role pairs see SupplementaryFiles/RolePairs.csv. _Directed_.
- **sameRoles.tsv** = Edgelist of nodes that have the same role in the same document. For the list of roles see SupplementaryFiles/Roles.txt. _Directed both ways_.
- **rolesWithWitnessesScribes.tsv** = Edgelist between nodes that have a role from the SupplementaryFiles/Roles.txt list and witnesses or scribes attested in the same document. _Directed_.
- **witnessScribeConnections.tsv** = Edgelist between scribes and witnesses attested in the same document. _Undirected_.

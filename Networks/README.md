### Networks of Neo-Babylonian people

The dataset contains a node list of all persons and an edge list for persons attested in the same documents. The attribute data for the individuals comes from the Prosobab database. We have also built several directed networks from the relations and roles of the individuals as specified in Prosobab. Each edgelist contains one types of relations/roles with the attribute data about the social relations/roles and the tablets in which it they are attested. The node list of all persons can used with these edgelists.

#### Files
- **connections.tsv** = Edge list of nodes (persons) attested in the same document. Weight is the number of documents in which two nodes co-occur. _Undirected_.
- **individuals.tsv** = Node list of all persons in the network. Includes rich attribute data on each person. Can be used with the edge lists. This is the same file as /ProsobabData/Individuals.tsv, but two column titles have been changed: Personal ID = ID and Name = Label.
- **relations.tsv** = Edge list of nodes (persons) that have a relation such as 'X brother of Y'. _Directed_.
- **legalRoles.tsv** = Edge list of nodes (persons) in legal role pairs with each other (e.g. judge and litigant or creditor and debtor). For the list of role pairs see SupplementaryFiles/RolePairs.csv. _Directed_.
- **sameRoles.tsv** = Edge list of nodes (persons) that have the same role in the same document. For the list of roles see SupplementaryFiles/Roles.txt. _Directed both ways_.
- **rolesWithWitnessesScribes.tsv** = Edge list between nodes (persons) that have a role from the SupplementaryFiles/Roles.txt list and nodes (persons) designated as witnesses or scribes who have been attested in the same document. _Directed_.
- **witnessScribeConnections.tsv** = Edge list between nodes (persons) designated as witnesses or scribes who have been attested in the same document. _Undirected_.

# Node and edge lists for creating networks

The dataset contains a node list of all persons and an edge list for persons attested in the same documents. The attribute data for the individuals comes from the Prosobab database. We have also built several directed networks from the relations and roles of the individuals as specified in Prosobab. Each edgelist contains one types of relations/roles with the attribute data about the social relations/roles and the tablets in which it they are attested. The node list of all persons can used with these edgelists.

## Files
- **co-occurrencesPersons.tsv** = Edge list of nodes (persons) attested in the same document. Each edge has information on the tablet in which the two persons co-occur. _Undirected_.
- **co-occurrencesPersons_simple.tsv** = Edge list of nodes (persons) attested in the same documents. Weight is the number of documents in which two nodes co-occur. _Undirected_.
- **co-occurrencesTexts.tsv** = Edge list of texts linked by persons who are attested in two or more texts. Each edge has information on the individual linking the tabelts. Attestations "king in date", "king in oath", and "king on coin" are excluded. _Undirected_.
- **individuals.tsv** = Node list of all persons in the network. Includes rich attribute data on each person. Can be used with the edge lists. This is the same file as /ProsobabData/Individuals.tsv, but two column titles have been changed: Personal ID = ID and Name = Label. See the readme file in /ProsobabData/ for more detailed notes.
- **legalRoles.tsv** = Edge list of nodes (persons) in legal role pairs with each other (e.g. judge and litigant or creditor and debtor). For the list of role pairs see SupplementaryFiles/RolePairs.csv. _Directed_.
- **relations.tsv** = Edge list of nodes (persons) that have a relation such as "X brother of Y". Relations such as "Broken/Unclear Gimil-Šamaš" indicate that there is a relation mentioned in the text but its nature remains unclear. _Directed_.
- **sameRoles.tsv** = Edge list of nodes (persons) that have the same role in the same document. For the list of roles see SupplementaryFiles/Roles.txt. _Directed both ways_.
- **rolesWithWitnessesScribes.tsv** = Edge list between nodes (persons) that have a role from the SupplementaryFiles/Roles.txt list and nodes (persons) designated as witnesses or scribes who have been attested in the same document. _Directed_.
- **tablets.tsv** = Node list of all tablets in the network. Includes rich attribute data on each text. Can be used with the co-occurrencesTexts.tsv edge list. This is the same file as /ProsobabData/Tablets.tsv, but two column titles have been changed: Personal ID = ID and Museum no. = Label. See the readme file in /ProsobabData/ for more detailed notes.
- **twoMode.tsv** = Edge list of a two-mode network of persons and tablets. If a person is attested in a tablet, there is an edge between them. Persons are in the source column and tablets in the target column. _Undirected_.
- **witnessScribeConnections.tsv** = Edge list between nodes (persons) designated as witnesses or scribes who have been attested in the same document. _Undirected_.

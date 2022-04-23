# AssociationKG
This is the repository for the "Extraction of Object-Action and Object-State Associations from Knowledge Graphs" journal paper, submitted at the Journal of Web Semantics

This repository contains the files (1) _YAGO KG_, (2) _ATOMIC KG_, (3) _ConceptNet KG_, (4) _ConceptNet (without RelatedTo) KG_, (5) _DBpedia KG_ and (6) _WebChild KG_  

![kgs.png](https://github.com/valexande/AssociationKG/blob/main/kgs.png)

each one of this files contains the files: (1) _action_ with all the files for the object-action association pipeline, (2) _state_ with all the files for the object-state association pipeline and (3) the _labels X_ (where X is one of the aforementioned graphs) with the labels of action-object-state from something-something which exist in the X graph.

![info_kg.png](https://github.com/valexande/AssociationKG/blob/main/info_kg.png)


In more detail the folder action (and similarly the folder state) contains the folders: (1) _context graphs_ with all the subgraphs that are descibed in the paper for the KG at hand, after pair merging, (2) _cross validation_ with the folds of object-action (or state) relations, (3) _patterns_ that contains the relation patterns for the problem at hand along with their weight of importance, (4) _positive-negative relations_ with all the positive and negative object action (or state) relations and (5) _scores_ with the final results for the path-node-wup metrics as well as for the simple relation pattern and relation pattern with clusters.

![more_info.png](https://github.com/valexande/AssociationKG/blob/main/more_info.png)

Moreover, the file _(3) ConceptNet KG_ shown in the second picture contains all the pipeline files when evaluating ConceptNet but with the labels existing in YAGO, ATOMIC, DBpedia and WebChild

![different_label_cn.png](https://github.com/valexande/AssociationKG/blob/main/different_label_cn.png)

Notice that the WebChild and YAGO KGs had the same number of object action labels. Therefore evaluating ConceptNet with the object-action relations existing in these two would return the same scores with ConceptNet.

Similar is the case for each KG when evaluting object-state relations.



Additionally, the repository contains the source code of our whole pipeline and evaluation method in the _AssociationKG source code_ and the clusters that were created from the relation patterns of each KG, in the txt file _allClusters_

![source_cluster.png](https://github.com/valexande/AssociationKG/blob/main/source_cluster.png)

Finally, in the picture below we can see what the _AssociationKG source code_ file contains

![source_all.png](https://github.com/valexande/AssociationKG/blob/main/source_all.png)

the _atomic_, _dbpedia_, _webchild_ and _yago_ files with the scripts to find the labels and create the subgraphs without contextual infromation for each KG, respectively. Similarly, _dataCleaning_ has the scripts that find the labels in ConceptNet and _graphContructor_ has the scripts that construct the subgraphs without contextual information for ConceptNet. 

All the graphs without contextual information are stored in the _subgraph_ file. Next, the _relation creator_ contains some scripts that help us create the positive and negative relations given a set of labels. Furthermore, _graphContext_ contains scripts that help us insert contextual information in the subgraphs. Afterwards, the subgraphs related to positive relations are stored in _subgraphContextPositive_ (analogously the  subgraphs related to positive relations are stored in _subgraphContextNegative_). The user must move them (both positive and negative) to the _subgraphContextFinal_ file for the evaluation. 

The _crossValidation_ file has the script that creates the folds for testing and training. Finally, _thresholds_ is the file with the scripts that find the optimal thresholds for the path-node-wup metrics, and the weights of importance for the relation patterns with and without clusters. Moreover, it computes the Accuracy, Precision, Recall and F1 scores for each method as described in the paper.

# GitHub does not allow us to upload big files, please find the aforementioned code here: [http://lpis.csd.auth.gr/ontologies/2022/AssociationKG/code.zip](http://lpis.csd.auth.gr/ontologies/2022/AssociationKG/code.zip) and the subgraphs + results + patterns + relations here: [http://lpis.csd.auth.gr/ontologies/2022/AssociationKG/dataset_results.zip](http://lpis.csd.auth.gr/ontologies/2022/AssociationKG/dataset_results.zip). Copy-paste the links to a new tab.

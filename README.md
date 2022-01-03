# AssociationKG
This is the repository for the "A Comparison of Methods for Object-Action and Object-State Association Extraction from Knowledge Graphs" journal paper, submitted at the Journal of Web Semantics

This repository contains the files (1) YAGO KG, (2) ATOMIC KG, (3) ConceptNet KG, (4) ConceptNet (without RelatedTo) KG, (5) DBpedia KG and (6) WebChild KG  

![kgs.png](https://github.com/valexande/AssociationKG/blob/main/kgs.png)

each one of this files contains the files (1) action that contains all the files for the object-action association pipeline, (2) state that contains all the files for the object-state assocation pipeline and (3) the label X-graph (where X is one of the aforementioned graphs) that contains the labels of action-object-state from something-something which exist in the X graph.

![info_kg.png](https://github.com/valexande/AssociationKG/blob/main/info_kg.png)


In more detail the folder action (and similarly the folder state) contain the folders: (1) _context graphs_ with all the subgraphs that are descibed in the paper, after pair merging, (2) _cross validation_ with the folds of object-action (or state relations), (3) _patterns_ that contain the most important relation patterns for the problem at hand, (4) _positive-negative relations_ with all the positive and negative object action (or state) relations and (5) _scores_ with the final results for the path-node-wup metrics as well as for the simple relation pattern and relation pattern with clusters.

![more_info.png](https://github.com/valexande/AssociationKG/blob/main/more_info.png)

Moreover, the file _(3) ConceptNet KG_ shown in the second picture contains all the pipeline files when evaluating ConceptNet but with the labels existing in YAGO, ATOMIC, DBpedia and WebChild

![different_label_cn.png](https://github.com/valexande/AssociationKG/blob/main/different_label_cn.png)

Notice that the WebChild and YAGO KGs had the same number of object action labels. Therefore evaluating CN with the object-action relations existing in these two would return the same scores with CN.

Similar is the case for each KG when evaluting object-state relations.



Additionally, the repository contains the source code of our whole pipeline and evaluation method in the _AssociationKG source code_ and the clusters that were created from the relation pattern of each KG, in the txt file _allClusters_

![source_cluster.png](https://github.com/valexande/AssociationKG/blob/main/source_cluster.png)

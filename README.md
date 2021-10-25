# Detection d'objet Model
Un de modèle de détection pré-entraînés sur l'ensemble de données **[Kitti dataset](http://www.cvlibs.net/datasets/kitti/)** et l'ensemble de données **[Open Images dataset](https://storage.googleapis.com/openimages/web/index.html)**.
Ce modèle peuvent être utiles pour l'inférence prête à l'emploi si vous êtes intéressé par les catégories déjà présentes dans ces ensembles de données. Ils sont également utiles pour initialiser vos modèles lors de l'entraînement sur de nouveaux ensembles de données.

Vous pouvez décompresser le fichier tar.gz via, par exemple :

```
tar -xzvf faster_inception_v2.tar.gz
```
Dans le répertoire , vous trouverez :

* un proto de graphe (`graph.pbtxt`)
* un point de contrôle (`model.ckpt.data-00000-of-0001`, `model.ckpt.index`,
     `modèle.ckpt.meta`)
* un proto de graphique frozen avec des poids intégrés au graphique en tant que constantes
     (`frozen_inference_graph.pb`) à utiliser pour l'inférence prête à l'emploi (essayez
     ceci dans le cahier Jupyter !)
* un fichier de configuration (`pipeline.config`) qui a été utilisé pour générer le graphique.
     Ceux-ci correspondent directement à un fichier de configuration dans le
     [samples/configs](https://github.com/tensorflow/models/tree/master/research/object_detection/samples/configs))
     répertoire mais souvent avec un seuil de score modifié. Dans le cas de la
     modèles plus lourds Faster R-CNN, nous fournissons également une version du modèle qui
     utilise un nombre très réduit de propositions pour la vitesse.


## Conguration du modèle

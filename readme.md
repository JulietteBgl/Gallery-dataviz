# Introduction

Objectif : Faire une galerie de viz, pour mettre en relation un graphique avec le code correspondant (en R et Python).

### Pour la partie R
Les librairies à installer sont les suivantes : @Juliette

### Pour la partir Python 

Pour faire tourner du code python dans un R markdown, il faut installer la librairie R **reticulate**. 

Pour pouvoir utiliser les librairies installer dans un environnement virtuel conda dans le Rmarkdown, voici la démarche : 

+ Créer un environnement virtuel conda nommé *gallery* (en supposant qu'anaconda est installé, sinon il faut l'installer) : 
	+ créer l'env : `conda create --name gallery python=3.6`
	+ activer l'env : `source activate gallery` ou `conda activate gallery`
	+ installer les lib nécessaires : `pip install matplotlib pandas seaborn numpy`
	
+ Il faut ensuite spécifier le path vers le fichier binaire python . Pour cela, on regarde quel python est utilisé avec la commande `which python` et on met le résultat dans la fonction `use_python()`. Par exemple : `use_python("/usr/local/anaconda3/envs/dataviz/bin/python")`.
+ De même, il faut spécifier le nom de l'env et le path vers cet env. De même, on utilise la commande `which conda` et la fonction `use_condaenv`. Exemple :  `use_condaenv(condaenv = "gallery", conda = "/usr/local/anaconda3/bin/conda")`. 
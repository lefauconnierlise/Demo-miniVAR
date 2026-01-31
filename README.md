# Démonstration d'un mini VAR - Génération d'images par résolution suivante 

Cette démonstration vise à expliquer le principe de VAR: Visual Autoregressive model. 
La démonstration est volontairement simplifiée, et a pour but de rendre fluide la compréhension de ce modèle autorégressif de génération d'images. 

Pour l'utiliser, vous pouvez cloner ce repo entier. 

Le fichier "demo_miniVAR.ipynb" est le notebook du mini VAR, qui doit être lancé sur Google Colab avec un GPU. Il peut tourner sur une machine classique mais cela prendra trop de temps. 


## Installation si vous souhaitez quand même le lancer en local

1. Créer un environnement python 3.10 : `conda create -y -n myenvVAR -c conda-forge python=3.10`.
2. Installer `torch>=2.0.0`.
3. Installer les autres packages via `pip install -r requirements.txt`.


## Démonstration par les auteurs du papier 

Les auteurs du papier ont fourni une démonstration du VAR, bien plus complexe que mon mini-VAR. Cette démonstration est dans le dossier "VAR_papier". 
Le modèle est déjà entraîné et les paramètres sont directement utilisés. 

Le fichier demo_VAR.ipynb peut être exécuter pour générer des images. Les images générées appartiennent à des classes qui peuvent être choisies dans la 2ème cellule du notebook, dans la variable "class_labels". Vous pouvez les changer pour tester. 

Le fichier demo_zero_shot_edit.ipynb peut être exécuter pour comprendre la capacité de généralisation du VAR, sur une image de perroquet. Il y a dans la troisième et dernière cellule la possibilité d'indiquer au modèle la tâche de généralisation souhaitée: le paramètre "class_label" est actuellement sur 1000, le modèle effectue une tâche de "in-painting" comme évoquée dans la vidéo. Pour tous les labels inférieurs, l'image va être éditée avec un style particulier. Vous pouvez essayer de changer de labels pour tester. 


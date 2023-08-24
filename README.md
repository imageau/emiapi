# Installation

Depuis votre console python, lancer la commande :
```
pip install emiapi
```
# Exemple d'utilisation

Téléchager le fichier `config_example.cfg`. Renommer le `config.cfg` et éditez son contenu en remplaçant l'`email` et le `password` par vos identifiants EMI. Placer ensuite le fichier dans un dossier, et créer le script suivant dans ce même dossier : 

```
from emiapi import EmiApi
from emiapi import plot_dataraw
#Set id
i=10239
#EMI API connect
api=EmiApi('config.cfg')
df=api.get_data(i,'dataraw')
plot_dataraw(df)
```

Ce script permet de charger les données de la station 10239 et d'afficher sa donnée brute. Les données brutes sont stockées dans le dataframe `df`.

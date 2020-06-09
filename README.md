garder les logs de changement
1 liste de tous les fichiers depuis le début (bdd)
1 journal avec les erreurs et conflits de toutes les opérations faites depuis le début (log)
maintenance de la database (quand effacer les logs? prompt user ou automatiquement apres un certain moment etc)
1 comparateur: comparaison des metadata de l'arb1 ET de l'arb2 avec les metadata de la db

scan branche A --> créé fichier avec liste de tout les dossiers et fichiers de la branche A
Idem pour B

charge dans la ram la base de donnée

compare A et DB --> créé un fichier toutes les modifs (diff entre A et DB)
pareil B et DB


ligne par ligne pour le fichier des diff entre A et DB :
recherche si la modif n'est pas dans le fichier des modifs de B et DB (vérifier si pas de conflit)
si pas de conflit copier fichier de A dans B + update metadata (de A) dans la DB
pareil avec B

Pour conflits : fichier le plus ancien on le renomme avec conflit et on garde me fichier le plus récent

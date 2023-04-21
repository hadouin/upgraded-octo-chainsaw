# upgraded-octo-chainsaw

## Import de la BDD

![Alt text](images/brave_tyeonrENUb.png)

## SQL

### 1 Ajoutez une contrainte qui permet de dire que la colonne id_specialite de la table specialite_personne est une clé secondaire et correspond à la clé primaire id_specialite de la table specialite

```sql
ALTER TABLE specialite_personne
ADD CONSTRAINT FK_PersonOrder
FOREIGN KEY (id_specialite) REFERENCES specialite(id_specialite);
```

![Alt text](images/brave_jZxCM6XDTD.png)

### Listez par ordre alphabétique sur la designation et sans redondance tous les jouets.

``
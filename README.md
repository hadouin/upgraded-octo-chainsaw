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

### Listez par ordre alphabétique sur la designation et sans redondance tous les jouets

```sql
SELECT * FROM `jouet` ORDER BY `jouet`.`designation` ASC
```

![Alt text](images/brave_VR3KZrQQon.png)


### Comptez le nombre de personnes mineures

```sql
SELECT COUNT(age)
FROM personne
WHERE age<18;
```

### Ajoutez dans la table theme un nouveau thème appelé « jeux de sociétés »

```sql
INSERT INTO `theme` (`id_theme`, `nom`) VALUES (NULL, 'jeux de sociétés')
```
![Alt text](images/brave_qglke2AMt2.png)

### Martin Pascale change d’orientation professionnelle et quitte son travail actuel. Supprimez-la de la table personne. Est-ce qu’il y a un changement dans la table specialite_personne ? Expliquez.

```sql

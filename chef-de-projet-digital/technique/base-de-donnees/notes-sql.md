# Notes SQL — Base de données

## Ressources

- Référence SQL : https://sql.sh/

## Exemples de serveurs

- APACHE : https://httpd.apache.org/
- NGINX : https://nginx.org/
- IIS : https://www.iis.net/

## Notions clés

### Vocabulaire de base
- SQL
- PK : primary key
- FK : foreign key
- Relations : one to one / one to many / many to many
- Base de données / database
- Requête / requêtage
- Moteur de base de données
- CSV
- Colonne / ligne / attribut / table / base de données

### Outils
- Logiciel Looping
- phpMyAdmin
- VS Code
- MySQL
- HeidiSQL
- W3C validator → extension VS Code

### Syntaxe et règles
- Une requête SQL se finit toujours par un point-virgule

### Mots-clés SQL
`select` / `from` / `as` / `where` / `like` / `not` / `between` / `or` / `and` / `is` / `in` / `not like` / `not in`

### Raccourcis et opérateurs
- `*` = tout
- `%` = n'importe quel caractère de 0 à x fois
- `_` = n'importe quel caractère 1 fois
- `!`
- `<>`

### Conditions et contraintes
- Les conditions
- Contraintes
- Regroupements

### Agrégats
`count` / `max` / `min` / `AVG` (somme, mini, maxi, moyennes)

### Formatage
`floor` / `ceil` / `round`

### Ordre au sein d'une requête
`having` / `group by` / `order by` / `asc` - `desc` / `limit` / `offset`

### Manipulation de données
`insert into` / `default` / `update` / `set` / `delete`

### Divers
- Alias

---

## CRUD

Les 4 fonctions de base :

| Objectif | Fonction SQL |
|----------|--------------|
| Create   | `insert`     |
| Read     | `select`     |
| Update   | `update`     |
| Delete   | `delete`     |

---

## Jointures (plusieurs tables)

**Règle des conditions de jointure :**
- Si 3 tables → 2 jointures
- Si 2 tables → 1 jointure
- Toujours une jointure de moins que le nombre de tables

**Fonctions de jointure :**
- `join`
- `inner join` / `left join` / `right join`
- `on`

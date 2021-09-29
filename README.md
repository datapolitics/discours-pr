<div align="center" id="top"> 


  <!-- <a href="https://{{app_url}}.netlify.app">Demo</a> -->
</div>

<h1 align="center">discours-pr</h1>

<br>

## :dart: A propos ##

Ce projet contient l'ensemble des discours et communications officielles du président de la république française depuis 1974 et jusqu'à mi-septembre 2021 environ.

Les données sont issues de [Vie Publique](http://vie-publique.fr) qui maintient à jour une base de donnéee exceptionnelle.

## :white_check_mark: Pré-requis ##

- Aucun (fichier CSV)

## Contenu du fichier ##

Le fichier CSV contient l'ensemble des meta données des discours (date, titre, circomstances, mots clés...). 

Les colonnes suivantes sont issues de calculs de notre algorithme de reconnaissance de pays:
country_title,country_what_keywords,main_country
- _country_title_: les noms de pays identifiés dans le champ "titre" du discours
- _country_what_keywords_: les noms de pays identifiés dans le champ "mots-clés" du discours
- _country_circumstances_: les noms de pays identifiés dans le champ "circonstances" du discours.
- _main_country_ : le nom de pays retenu pour notre analyse, qui correspond au pays identifié dans circonstance s'il est unique, ou à défaut du pays dont le nombre d'occurences est le plus élevé dans les champs précédents.

L'identification de pays s'effectue sur la base d'une liste de pays et d'adjectifs de nationalité, puis par un peu de NLP. Merci à [alain.j.scheider](http://alain.j.schneider.free.fr/pays.htm) d'avoir mise en ligne une base de vocabulaire de nationalités.


## Mise à jour ##

Nous ne garantissons pas la mise à jour régulière de ce dépot, aussi si vous souhaitez utiliser des données fraiches, nous vous recommandons d'aller jeter un oeil au [scraper](https://github.com/datapolitics/scraper-vie-publique) pour vous constituez votre propre ressource.

## :memo: License ##

This project is under license from MIT. For more details, see the [LICENSE](LICENSE.md) file.

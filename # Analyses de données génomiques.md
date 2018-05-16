# Analyses de données génomiques

Dr Anne-Sophie Denommé-Pichon
2018-05-17

## Consignes

- Réponses des exercices à écrire dans un fichier texte au format Markdown (CommonMark, extension .md)
	Formatage des réponses https://frama.link/example-md

```md
# UE génétique médicale 2017-04-05
* Prénom1 Nom1 
* Prénom2 Nom2
## Exercice 1
### Q1
*TCF4*
### Q2
NC_000018.9:g.52895514_52895515delGA
## Exercice 2
### Q1
* item1
* item2
* item3
### Q2
[NM_001083962.1:c.1957_1958delTC in UCSC](http://example.com)
```

- Suivez le lien [https://classroom.github.com/a/wpZGfpx-](https://classroom.github.com/a/wpZGfpx-
)
- FIXME consignes Après avoir créé un compte GitHub, déposer le texte dans un Gist (https://gist.github.com/) 
- FIXME consignes Envoyer le lien à as.denomme@outlook.com avant 18 heures
- FIXME ajouter image

## Exercice 1

Identification de trois variations chez un patient avec un syndrome de Pitt-Hopkins :
NC_000018.9:g.52895531T>C
NC_000018.9:g.52999284delC
NC_000018.9:g. 53331929C>A

- Q1 À quelle séquence de référence ces notations se réfèrent-elles ? 
- Q2 Sur quel chromosome se trouvent ces variants ?
- Q3 Quelle est la fréquence de chacun de ces variants dans la population générale ? GnomAD
- Q4 Quelle est la conséquence protéique de chacun de ces variants ? GnomAD
- Q5 Lequel de ces variants semble mériter une étude approfondie ? Argumentez.
FIXME Note : pour chercher une délétion dans gnomAD, il faut préciser la base qui précède. Par exemple, pour recherche NC_000018.9: g.11111delA, le format d’entrée dans gnomAD est 18-11110-TA-T
La séquence autour du nucléotide délété NC_000018.9:g.52999284delC est  GCAT*C*ACAC dans le sens de transcription du gène (3’5’)
Le nucléotide en gras est le nucléotide délété.
FIXME ajouter images

# Analyses de données génomiques

Dr Anne-Sophie Denommé-Pichon - 2018-05-17

## Consignes

Écrivez les réponses aux exercices dans un fichier texte au format Markdown (CommonMark, extension `.md`). Respectez ce [modèle de formatage](https://raw.githubusercontent.com/Oodnadatta/Exercises/master/exemple.md) des réponses (reproduit ci-dessous), pour ce [rendu final](https://github.com/Oodnadatta/Exercises/blob/master/exemple.md).

```
# UE génétique médicale 2018-05-17
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

Vous avez jusqu'à aujourd'hui, jeudi 17 mai 2018 à 18 h 00 CEST pour répondre aux questions. Toute réponse apportée ultérieurement sera ignorée.

<kbd>
  <img src="https://raw.githubusercontent.com/Bioinformatics-classroom/Genomic-analysis/master/Deadline.png" alt="Deadline">
</kbd>

## Exercices

### Exercice 1

Trois variations sont identifiées chez un patient avec un syndrome de Pitt-Hopkins :
1. `NC_000018.9:g.52895531T>C`
2. `NC_000018.9:g.52999284delG`
3. `NC_000018.9:g. 53331929C>A`

- Q1 À quelle séquence de référence ces notations se réfèrent-elles ?
- Q2 Sur quel chromosome se trouvent ces variants ?
- Q3 Convertissez la notation génomique (g.) des ces variants en notation nucléotidique (c.). Que remarquez vous ? Que pouvez-vous en conclure quant au sens de transcription du gène ? `Mutalyzer`

Pour chercher une délétion dans gnomAD, il faut préciser la **base qui précède** la délétion **dans le sens génomique (5′3′)**. Par exemple, pour rechercher <code>NC_000018.9: g.1111<b>1</b>delA</code>, le format d’entrée dans gnomAD est <code>18-1111<b>0</b>-TA-T</code>.

Ci-dessous se trouve la région génomique autour de la variation `NC_000018.9:g.52999284delG`, dans le sens génomique et dans le sens de transcription du gène.
![Capture d'écran d'Alamut, sens génomique](https://raw.githubusercontent.com/Bioinformatics-classroom/Genomic-analysis/master/sens-g%C3%A9nomique.png)

![Capture d'écran d'Alamut, sens de transcription du gène](https://raw.githubusercontent.com/Bioinformatics-classroom/Genomic-analysis/master/sens-de-transcription.png)
D'après Alamut Visual v.2.9 © Interactive Biosoftware.

- Q4 Quelle est la fréquence de chacun de ces variants dans la population générale ? `GnomAD`
- Q5 Quelle est la conséquence protéique de chacun de ces variants ? `GnomAD`
- Q6 Lequel de ces variants semble mériter une étude approfondie ? Argumentez.

### Exercice 2

Une variation hétérozygote est identifiée chez un patient avec petite taille à -3 DS et déformation de Madelung : `NM_000451.3:c.399G>C`. Le variant est également présent chez la mère, qui présente une petite taille à -2,5 DS. Il est absent chez le père, qui n’a pas de petite taille.

- Q1 Dans quel gène se trouve la variation ?
- Q2 Quelles sont les maladies associées à ce gène et quels sont leurs modes de transmission ? `OMIM`
- Q3 Quel est le lien entre ce gène et le syndrome de Turner ? `OMIM` `PubMed`
- Q4 Quelle est la notation HGVS de cette variation au niveau génomique (en utilisant GRCh37) ? `Mutalyzer`
- Q5 Quelle est la signification des différentes parties de cette notation ?
- Q6 Quelle est la notation HGVS de cette variation au niveau protéique ? `Mutalyzer`
- Q7 Quelle est la signification des différentes parties de cette notation ?
- Q8 Quel est le type de variation au niveau protéique : faux-sens, non-sens, synonyme, variant d’épissage ? `Mutalyzer`
- Q9 Visualisez la variation dans UCSC. Copiez l’URL de cette visualisation dans le fichier de réponses. `Mutalyzer`
- Q10 Le gène est-il sur le brin sens ou anti-sens ? `UCSC`
- Q11 Combien d’exons ce gène comporte-t-il (transcrit `NM_000451.3`) ? `UCSC`
- Q12 Dans quel exon ce variant se trouve-t-il ? `UCSC`
- Q13 Le variant se trouve-t-il dans une région conservée ? `UCSC (track 100 Vert. Cons)`
- Q14 Dans quel domaine fonctionnel protéique se trouve le variant ? `NCBI (protein)`
- Q15 Dans quelle publication ce variant a-t-il déjà été décrit ? `LOVD` `Pubmed`
- Q16 Analysez ce variant dans VEP (Variant Effect Predictor) en utilisant GRCh37.
Il existe plusieurs formats d’entrée dans VEP. Vous pouvez utiliser celui-ci : `SHOX:c.399G>C`
Ajoutez l’option pour avoir les numéros de transcrits Ensembl et RefSeq. Laissez les autres options par défaut. `VEP`
- Q17 Pourquoi existe-t-il plusieurs lignes alors que vous n’avez saisi qu’un seul variant ?
- Q18 Exportez le résultat de cette requête au format VCF.
- Q19 Analysez ce VCF dans wAnnovar. Utilisez votre adresse mail universitaire. Collez l’URL de l’analyse dans le fichier de réponse. `wAnnovar`
- Q20 Trouver l’article des recommandations de l’ACMG sur l’interprétation des variants de séquence (*Standards and guidelines for the interpretation of sequence variants*, Richards *et al.*, Genet. Med., 2015). Quel est le DOI de l’article ? `Pubmed`
- Q21 D’après cet article, quels sont les critères déterminant une variation pathogène ou probablement pathogène ? (100 mots maximum, environ 8 à 10 critères attendus, exemple : « ségrégation du variant dans la famille »).
- Q22 Dans quelle catégorie classez-vous le variant `NM_000451.3:c.399G>C` (pathogène, probablement pathogène, probablement bénin, bénin, VOUS) ? Sur quels critères ? `VEP` `wANNOVAR`
Voici quelques éléments d'orientation pour certains de ces critères :
  - PS1 : `LOVD` `ClinVar`
  - PS2 : énoncé
  - PS3 : `PubMed`
  - PS4 : `GnomAD` `1000 Genomes` `Exome Variant Server`
  - PM1 : `NCBI (protein)`
  - PP3 : `VEP` `wANNOVAR`
  - Autres : `VEP` `wANNOVAR`

### Exercice 3

Vous voulez analyser les résultats d’exome d’un enfant de 6 ans avec obésité morbide et diarrhée chronique sévère. Les parents sont cousins germains. Les résultats ont été chargés [sur wANNOVAR](http://wannovar.wglab.org/FIXME).

 - Q1 Quel variant est responsable de la pathologie de ce patient ?

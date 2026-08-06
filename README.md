# L'Épopée de Gilgamesh — corpus multilingue

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21819525.svg)](https://doi.org/10.5281/zenodo.21819525)

**Lecture en ligne : [https://l0d0v1c.github.io/gilgamesh](https://l0d0v1c.github.io/gilgamesh)**

Traduction française intégrale du corpus de l'Épopée de Gilgamesh — les **4 268 vers** des **39 témoins** connus : la version standard en douze tablettes (« *Celui qui a vu l'Abîme* », attribuée à Sîn-lēqi-unninni), les quatorze sources paléo-babyloniennes (~1800 av. J.-C.), les onze fragments médio-babyloniens (Boğazköy, Émar, Megiddo, Ougarit, Nippur, Ur) et les deux fragments néo-assyriens.

Chaque vers est donné en **cunéiforme Unicode**, en **translittération akkadienne normalisée**, en **anglais** (édition eBL), en **français** (traduction critique, avec crochets de restitution) et en **français littéraire** (texte lissé pour la lecture), accompagné le cas échéant d'une note philologique.

## Le lecteur (`index.html`)

Application web sans dépendance, pensée pour mobile :

- navigation par tablette et par **strophes de quatre vers** (boutons ◀ ▶, balayage tactile, flèches clavier), avec enchaînement automatique d'une tablette à l'autre ;
- affichage à la carte des cinq couches (cunéiforme, translittération, français, littéraire, anglais) ;
- **citations** : toucher un vers l'ajoute à une liste persistante, exportable en un geste ;
- **reprise de lecture** : la position est mémorisée localement.

## Le corpus (`corpus.json`)

Un tableau JSON, une entrée par vers :

| champ | contenu |
|---|---|
| `reference` | témoin (ex. `Standard-Babylonian XI`, `Old-Babylonian III`) |
| `vers` | numéro de vers dans l'édition |
| `babylonien` | texte akkadien composite normalisé (eBL) |
| `cuneiforme` | vers en cunéiforme Unicode |
| `anglais` | traduction anglaise de la ligne (eBL / A. R. George) |
| `francais` | traduction française, appareil critique conservé (`[...]` = restitution) |
| `frlitt` | version littéraire lissée du français |
| `comment` | note philologique (facultatif) |

Le cunéiforme est produit **algorithmiquement** : pour chaque vers, la translittération signe à signe (ATF) du manuscrit le mieux conservé est convertie via la liste de signes OSL d'Oracc ; `□` note un signe visible mais illisible, `…` une lacune ; pour les vers entièrement restitués (refrains), la graphie est empruntée au vers parallèle identique le mieux conservé. Couverture : 4 244 vers sur 4 268.

La traduction française a été établie sur l'akkadien normalisé. Elle conserve les conventions suivantes : les termes sans équivalent sûr restent en akkadien (*šār*, *pukku*, *mikkû*, *ballukku*, *elammaku*…) ; les formes onomastiques propres à chaque tradition sont respectées (Huwawa en paléo-babylonien, Humbaba dans la version standard, Hubbebe en néo-assyrien ; Sursunabu / Ur-šanabi ; Ūta-naʾištim / Ūta-napišti).

## Ce que la mise en regard des colonnes révèle

L'étude systématique du corpus (comparaison akkadien / anglais / français) a mis au jour quelques faits notables :

**Les vers à double témoin.** 47 vers existent en deux états du texte akkadien (variantes de la même ligne). La traduction anglaise d'eBL étant attachée **à la ligne**, et non à chaque témoin, une cinquantaine de variantes n'avaient aucune traduction propre — le français est ici la seule traduction publiée de ces états du texte (ex. SB II 278–279 « afin de préserver les cèdres / Enlil lui a donné pour destin d'être la terreur des gens » ; VIII 173 *inaqqīšu* « il fait libation » ; VI 163, où un témoin pèse les bordures des cornes en *mines* et l'autre les mesure en *doigts*). Dans `corpus.json`, le champ `anglais` reproduit donc la traduction de ligne d'eBL sur chaque variante, tandis que `francais` traduit chaque témoin pour lui-même.

**Là où le français suit l'akkadien de plus près.** Quelques choix assumés : les *quatre* fléaux de XI 129 (*šāru, rādu, mehû, abūbu* — vent, averse, tempête, Déluge) ; « aux quatre vents » (XI 157, *ana erbet šārī*) ; « vêtement de sa dignité » (XI 267, sans le « royal » ajouté par l'anglais) ; « la stupeur d'Adad » (XI 106, *šuharratu*) ; *urnu* rendu « pin » et non « cèdre » (X 158) ; *rebītu* « Grand-Place » et non « rue » (OB II 214) ; « la vie, ils l'ont retenue entre leurs mains » (VA+BM, l'image des mains conservée) ; *kurunnu* « bière fine » distingué de *hīqu* « bière coupée » (VIII).

**Registre.** *ṣēru* est rendu « la steppe », *harimtu* « la courtisane », *sābītu* « la cabaretière » — des choix moins connotés que « the wild », « harlot », « ale-wife ».

## Sources et licences

- **Éditions et traduction anglaise** : [electronic Babylonian Library (eBL)](https://www.ebl.lmu.de), Ludwig-Maximilians-Universität München / Bayerische Akademie der Wissenschaften, dir. Enrique Jiménez. Édition du Gilgamesh standard et traduction anglaise fondées sur les travaux d'**Andrew R. George** (*The Babylonian Gilgamesh Epic*, Oxford, 2003). Citation recommandée : *Gilgameš, eBL edition ([https://www.ebl.lmu.de/corpus](https://www.ebl.lmu.de/corpus)), accessed 2026*. Contenu eBL publié sous licence [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).
- **Liste de signes cunéiformes** : [OSL — Oracc Sign List](https://github.com/oracc/osl) (domaine public, CC0).
- **Traduction française, notes, cunéiforme dérivé et lecteur web** : © 2026 — publiés sous la même licence **[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)** (attribution, pas d'usage commercial, partage dans les mêmes conditions), conformément à la clause de partage à l'identique de la source.

Le texte akkadien antique appartient, lui, à l'humanité depuis plus de trois mille ans.

> *De la mort et de la vie il me dira le secret.* — SB IX 77




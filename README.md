<div align="center">
    <h2>Simon</h2>
</div>

### Description du jeu 
> A la base, le jeu du Simon est un petit jeu électronique qui met au défi la mémoire du joueur. Le jeu est constitué de 4 couleurs (vert, rouge, bleu, jaune) qui sont combinées pour produire une suite de couleurs  
>
> Le joueur a pour mission de reproduire une suite de couleurs générées aléatoirement  par  le  jeu  sachant  que  cette  suite  s’allonge  au  fur  et  à mesure  de  la  progression  du  jeu.  L’objectif  pour  le  joueur  est  de reproduire la plus longue suite possible de couleurs sans se tromper. 

### Spécification du besoin 
> La version du jeu à élaborer s’excécutera dans un terminal et la suite de couleurs sera représentée par des caractères colorés : caractère ‘v’ affiché  en  vert,  caractère  ‘r’  affiché  en  rouge,  caractère  ‘b’  affiché  en bleu et caractère ‘j’ affiché en jaune. 
> Pour saisir ses couleurs, le joueur utilisera les touches ‘v’ pour saisir la couleur verte, ‘r’ pour rouge, ‘b’ pour bleu et ‘j’ pour jaune. 
> Le déroulement d’une partie est le suivant : 
>> 1.  Le  jeu  commence  par  afficher  une  première  couleur  choisie aléatoirement parmi les couleurs vert, rouge, bleu et jaune ; 
>> 2.  Le  joueur  dispose  d’environ  3  secondes  pour  mémoriser  la couleur affichée ; 
>> 3.  Une  fois  le  temps  de  mémorisation  écoulé  l’écran  s’efface  et  le joueur est invité à saisir la couleur qu’il a mémorisée ; 
>> 4.  Si le joueur se trompe le jeu est terminé, sinon la partie continue ; 
>> 5.  L’écran s’efface puis le Simon réaffiche la première couleur qu’il avait sélectionné puis en affiche une seconde tirée aléatoirement ; 
>> 6.  A  nouveau,  le  joueur  dispose  d’environ  3  secondes  pour mémoriser les deux couleurs affichées ; 
>> 7.  A la fin du temps de mémorisation, l’écran s’efface et le joueur est invité à saisir les deux couleurs précédemments affichées ; 
>> 8.  Si le joueur se trompe le jeu est terminé, sinon la partie continue avec une 3ème couleur ajoutée par le Simon et ainsi de suite. Lorsque le joueur se trompe et que la partie prend fin, le jeu précise sur quelle saisie l’utilisateur s’est trompé puis il ré-affiche : 
>>> • la série de couleurs proposées par le Simon 
>>> • la  série  de  couleurs  saisie  par  le  joueur  jusqu’à  la  couleur  pour laquelle il s’est trompé ; 
>>
>>En  comparant  les  deux  séries,  le  joueur  est  capable  de  voir  à  quel moment il s’est trompé et quelle était la couleur attendue. 
>> Le programme affiche également le score du joueur, à savoir, le nombre de  couleurs  composant  la  série  la  plus  longue  qu’il  a  saisi  sans  se tromper. 

### Scénario nominal : Le joueur se trompe sur la dernière couleur de la série 
> Ce scénario décrit le comportement du jeu lorsque le joueur se trompe en  saisissant  la  dernière  couleur  de  la  saisie.  Dans  cet  exemple,  le joueur fait une erreur en saisissant la 4ème couleur : il saisit la couleur jaune alors que le simon avait affiché la couleur bleu en 4ème couleur... 
> A  la  fin  du  jeu,  le  programme  affiche  que  le  joueur  s’est  trompé  en saisissant la 4ème couleur puis il ré-affiche : 
>> • les 4 couleurs générées par le Simon ; 
>> • les 4 couleurs saisies par le joueur. 
> Le programme présente également le score du joueur, à savoir, 3 points car il a pu saisir au maximum 3 couleurs correctes sans se tromper. 

### Scénario alternatif : Le joueur se trompe sur une couleur autre que la dernière 
> Ce scénario décrit le comportement du jeu lorsque le joueur se trompe en saisissant une couleur qui n’est pas la dernière de la série. Dans cet exemple, le joueur a réussi à saisir 4 couleurs sans se tromper mais au moment  de  saisir  la  série  suivante,  il  fait  une  erreur  de  frappe (d’étourderie ?) au moment de saisir la 3ème couleur : il saisit la couleur rouge alors que le Simon attendait la couleur verte.
> A  la  fin  du  jeu,  le  programme  affiche  que  le  joueur  s’est  trompé  en saisissant la 3ème couleur puis il ré-affiche : 
>> • les 5 couleurs générées par le Simon ; 
>> • les couleurs du joueur jusqu’à l’erreur lors de la 3ème saisie. 
>
> Le  programme  précise  néanmoins  que  le  score  du  joueur  est  de  4 points  car  il  avait  préalablement  réussi  à  saisir  4  couleurs  correctes sans se tromper. 

### Scénario d’exception : Le joueur saisit une couleur inexistante 
> Ce scénario décrit la réaction du programme lorsque, au moment de sa saisie, le joueur entre une couleur inexistante. 
>
>> • le  joueur  saisit  le  caractère  ‘a’  dès  la  1ère  saisie  ce  qui  ne correspond à aucune couleur. Le programme signale l’erreur de saisie puis demande à l’utilisateur de saisir une nouvelle couleur ; 
>>
>> • lors de la 2ème saisie, il saisit la lettre ‘v’ (correcte) puis la lettre ’t".  Le  programme  signale  l’erreur  puis  demande  une  nouvelle couleur. 

### Ressources à disposition 
> Vous pouvez utiliser (si vous le souhaitez) les fonctionnalités proposées dans le module game-tools : 
https://github.com/TomPlanche/game-tools-univ
> Ce  module  met  à  disposition  des  fonctionnalités  simples  permettant d’effacer le terminal, de mettre le programme en pause, d’afficher des éléments en couleur ou encore de générer un nombre entier aléatoire. 
>
> Attention :  Rappelez-vous  que  votre  production  doit  respecter  les spécifications  fournies  dans  la  section Spécification du besoin.  Les fonctionnalités  de  la  librairie game-tools doivent  être  utilisées avec parcimonie : 
>> • soit  pour  répondre  à  un  besoin  clairement  spécifié  dans  la section Spécification du besoin et les scénarios décrits; 
>>
>> • soit pour agrémenter l’interface du jeu, sans toutefois dénaturer à l’excès  le  comportement  attendu  et  décrit  dans  les  différents scénarios. 
>
> En cas de doute, n’hésitez pas à en discuter avec votre enseignant. 

### Extension possible 
> Cette  extension,  si  elle  est  modélisée  (algorithme)  et  programmée correctement,  peut  rapporter  des  points  bonus  mais  vous  n’êtes  pas obligé de la traiter. 
>
> Attention :  Cette  extension  est secondaire et  ne  doit  pas  prendre  le pas  sur  les  spécifications  fournies.  L’élaboration  d’une  extension  ne pourra  en  aucun  cas  compenser  l’absence  d’une  fonctionnalité demandée dans la Spécification du besoin et/ou dans les scénarios. 
> Le  but  de  cette  extension  est  de  fournir  une  aide  au  joueur  en  lui permettant  d’utiliser  un  joker  par  série  :  Lorsque  le  joueur  hésite  au moment  de  saisir  une  couleur,  il  peut  saisir  un  caractère  “joker” représenté par une étoile qui sera remplacé par la couleur attendue par le simon. 
>
> Ce caractère joker n’est utilisable qu’une seule fois par série de couleur à  saisir  :  Si  le  joueur  tente  de  l’utiliser  plus  d’une  fois,  le  programme indiquera que le joker a déjà été utilisé et invitera le joueur à saisir une couleur valide.
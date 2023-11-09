# Lean Software Development

On a choisi de présenter la Lean Software Devlopment 
Pourquoi ce choix ? : Après s'être rapidement documenté sur les différentes méthode agiles à présenter, on a compris de la méthode du Lean Software Development qu'elle avait une approche basée sur l'efficacité, la flexibilité et l'orientation client, et donque c'était un choix judicieux pour les projets axés sur la satisfaction du client ce qui nous a semblé très important et donc très intéressant. De plus, la LSD vise à éliminer les activités qui n'ajoutent pas de valeur au produit final ce qui permet d'optimiser le processus de développement et d'utiliser les ressources de manière bien plus efficace.

# L'organisation du projet 
## 08/09 - 15/09 - 22/09 

On a fait le choix d'utiliser Github plutôt que Gitlab pour notre projet.
Pendant les premiers cours on a donc continué notre apprentissage de l'utilisation de Git. 

La façon dont on configure le repository etc, comment on push, à quoi sert de pull, a quoi servent les différentes branches... 
On connaissait tous les deux git mais on n'avait jamais utilisé pour des projets à plusieurs, uniquement pour des projets solo ce qui fait qu'on n'avait jamais eu des branches différentes. 

On a compris les modalités et les bonnes pratiques à avoir pour travailler en groupe.  

Aussi on a compris les clés ssh pour pouvoir push etc. 
-> d'abord générer une paire de clés ssh sur la machine via le terminal 
Par defaut la clé est sauvegarder dans le repertoire : <b> /home/user/.ssh/id_rsa </b> 
On ne va pas changer ca.
(C'est dans un dossier caché (on le voit car c dans /user/.ssh/) or dossier/fichier qui commence par . est caché)

-> Ensuite il demande d'entrer un mdp en plus si on veut (meme sans ce sera sécurisé) 
-> si pas de mdp sécurisé quand meme mais juste pas besoin de ressaisir le mdp a chaque push/pull 
-> La clé est généré. Pour retoruver les fichiers générés on va dans le repertoire .ssh (caché) (-> /home/user/.ssh/ ) puis on ouvre le fichier id_rsa.pub (ATTENTION important de prendre id_rsa.pub et non id_rsa car c la privée cell la) et on voit toute la clé la.

-> puis copier le contenu et aller sur github 
-> dans github aller dans settings / ssh et GPG keys 
-> ajouter une clé ssh 

On poursuit notre apprentissage de git en se documentant sur différents sites et sur les différents github comme celui de M.Launnay ou encore sur celui de la classe avec les premieres modifications de celui-ci. 

On a fait un `git clone` du repository de cours de M.Launnay pour avoir sur notre machine les cours et également tester la commande. Tout va bien on a eu sur nos machines respectives tous les dossiers/fichiers.
Dans le même temps on commence à se documenter sur la Lean Software Devlopment 
## 29/09

Les commandes git sont assez claires on a fait un fichier pour clarifier la situation et surotut avoir les commandes essentielles de git. Celui-ci sera sur notre repo. 
Voici des commandes git importantes :
-> git --version = version et verif que bien installé 
-> git init  = Premiere commande a taper sur chaque projet si on veut l'initialiser en tant que depot git  => et enft ca crée un dossier caché .git (qu'on peut voir si on fait ls -a (et pas ls tout simple))
-> git add = tracker des fichiers 
-> git add -A = track tous les fichiers existants 
-> git commit -m "initialisation [par exemple]" capture l'etat d'un projet à un point dans le temps
-> git remote
-> git push 

-> dans un fichier (avec vim) pour quitter et sauvegarder faire echap puis ':wq' 

-> rm -rf .git => supprimer le depot git local initialisé 

-> git pull = quand on a un fichier qui a ete update sur github par qq d'autre par exemple et bah si on veut push un travail on peut pas avant d'avoir pull c a d récup le travail et l'update de l'autre. 
donc git pull origin master par exemple si c le chemin origin de la branche master puis git push origin master 

git ignore => fichier/dossier qu'on veut pas prendre dans le depot. 

## 06/10 

Problème : 
Je n'arrivais pas à pull puis push les modifs d'un fichier sur la branche master sur github 
on arrive pas a pull un fichier test de la branche main [master] en local et à le modifier pour ensuite le re-push sur la branche main du depot git. 

<i> "user@user-Latitude-3420:~/Documents/Cours/L2/Gestion de projet/projetMethodesAgiles$ git push origin master
To github.com:hugohebbinckuys/notes_hugo_yazid.git
 ! [rejected]        master -> master (non-fast-forward)
error: impossible de pousser des références vers 'github.com:hugohebbinckuys/notes_hugo_yazid.git'
astuce: Les mises à jour ont été rejetées car la pointe de la branche courante est derrière
astuce: son homologue distant. Extrayez cette branche et intégrez les changements distants
astuce: (par exemple 'git pull ...') avant de pousser à nouveau.
astuce: Voir la 'Note à propos des avances rapides' dans 'git push --help' pour plus d'information." </i> 

Alors que j'avais deja pull et mis a jour et donc que tout etait à jour. 

Problème : 
1. Objectif : crée un fichier md dans notre répo et pouvoir le modifié a deux afin de travailler sur des taches differente mais sur le meme fichier.
	1.1 Etape suivie pour la réalisation de l'objectif:
		1.1.1 Une personne "A" crée un fichier sur la répo.
		1.1.2 Une personne "B" pull la répo pour avoir accés au nouveau 		fichier crée
		1.1.3 La personne B modifie le nouveau fichier.
		1.1.4 La personne B  add le fichier a la répo , ajoute un commit, et push le fichier
		1.1.5 La personne "A" a accés a la répo avec sont fichier crée mais avec les modification de la Personne "B"
        1.2 Problème rencontré : durant la réalisation de l'objectif: On arrivait pas a ce que je vois le fichier qu'il pushait alors qu'on le faisait en direct et après avoir refresh la page impossible de voir ses nouveaux fichiers. 

## 13/10

On poursuit notre présentation du LSD (Lean Software Dev). 

## 20/10

-> go apprendre qq trucs en markdwon pour faire une presentation un peu carré 
estimation de temps : 30min 
=> finalement a peu pres 45min pour apprendre les bases et les utilisations basiques du markdown

-> la j'ai voulu initialiser un depot local pour envoyer mon fichier apprentissage.md au depot en ligne 
=> erreurs concernant les branches que je veux pousser faut que je crée en local la branche hugo pour la push ensuite et j'avais pas compris (pas sur que j'aie vraimebt compris actuellement)

- commande git branch pour afficher les branches locales 
- commande git branch *nom branche* = création de branche 
- ou alors git checkout -b *nom branche*
- git checkout *nom branche* = basculer vers la branche 
labranche active est précédée d'une asterisque et de couleur différentelors d'un git branch 

C'est un fail 
ca marche pas j'arrive pas a pull et je comprend pas prq donc je peux pas push car y a des conflits 

temps estimé = 5 min 
temps réel = pas encore fini 




sources : https://www.varonis.com/fr/blog/git-branching
https://docs.framasoft.org/fr/grav/markdown.html

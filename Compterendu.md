*Exercice 1*

1- Dans quels dossiers bash trouve-t-il les commandes tapées par l’utilisateur?
printenv PATH/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin

2-Quelle variable d’environnement permet à la commande cd tapée sans argument de vous ramener dans votre répertoire personnel?
cd $HOME

3.Explicitez le rôle des variablesLANG,PWD,OLDPWD,SHELL et_.
Lang = détermine la langue que les logiciels utilisent pour communiquer avec l’utilisateur
PWD = Affiche le chemin absolu du répertoire courant
OLDPWD = Contient le dernier répertoire avant le cd
SHELL= Le schell utilisé par l'utilisateur connecté
_ = La dernière commande saisie par l'utilisateur

4.Créez une variable localeMY_VAR(le contenu n’a pas d’importance). Vérifiez que la variable existe.
Création --> My_Var='abcd'  ( Si on veut une variable d'environnement on ajoute export devant)
Visualisation --> echo $My_Var --> Retourne la valeur de la variable

5.Tapez ensuite la commande bash. Que fait-elle? La variable MY_VARexiste-t-elle? Expliquez.
A la fin de cette question, tapez la commande exitpour revenir dans votre session initiale.
La commande BASH créer un nouveau SHELL, chaque SHELL créer est le fils du SHELL précédent. La variable locale n'existe pas par conséquent on ne pas accéder au variable locale de l'ancien 
shell (mais on peut accèder au variable d'environnement); 
Avec la commande echo $SHLVL on peut voir le niveau d'imbrication des shell 

6.Transformez MY_VAR en une variable d’environnement et recommencez la question précédente. Expli-quez.
Transofrmer en variable d'environnement --> Export My_Var; 
Par contre cette fois ci dans le nouveau Shell la variable d'environnement est hérité de son père.

7.Créer la variable d’environnement NOM Sayant pour contenu vos noms de binômes séparés par un espace.
Aﬀicher la valeur deNOMSpour vérifier que l’affectation est correcte.

8.Ecrivez une commande qui aﬀiche ”Bonjour à vous deux, binôme1 binôme2!” (où binôme1 et binôme2sont vos deux noms) en utilisant la variableNOMS.
echo BOnjour à vous deux, $NOMS ! 

9.Quelle différence y a-t-il entre donner une valeur vide à une variable et l’utilisation de la commande unset?
Unset permet de supprimer une valeur tandis que si on affecte une chaine vide à une variable elle existe elle est juste vide. 

10.Utilisez la commande echo pour écrire exactementla phrase :$HOME =chemin(où chemin est votredossier personneld’après bash)
echo '$HOME =' $HOME

Exercice 2
Ecrivez un script testpwd.shqui demande de saisir un mot de passe et vérifie s’il correspond ou non aucontenu 
d’une variablePASSWORDdont le contenu est codé en dur dans le script. Le mot de passe saisi par l’utilisateur 
ne doit pas s’aﬀicher.

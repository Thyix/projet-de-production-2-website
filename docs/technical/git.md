# Commandes utiles pour Git !

Git est un outil très utile qui vous permet de faire de la gestion de source code. Le but de cette page est donc de montrer des commandes qui vous permettront de vous débrouiller avec des cas plus complexes pour git.

Avant de commencer, je veux juste séparer certains concepts pour qu'on comprenne quelle commande va faire quoi.

1. Local

Lorsque vous allez développer sur votre machine, vous allez développer du code qui sera stocké _localement sur votre machine_. Lorsque vous faites un **git add**, les changements seront sauvegardés localement sur votre machine. Tant que vous n'aurez pas fait un git push, tous les commits créés et les changements sauvegardés seront présents uniquement sur votre machine.

2. Serveur

Les changements sur le serveur seront effectués seulement lorsqu'un **git push** sera effectué à partir de l'ordinateur d'un des collaborateurs du repository.

## git add `<nom de votre fichier>`

Cette commande va sauvegarder les changements faits localement dans le but de faire un _commit_. Les changements ne sont pas _coulés dans le béton_ et peuvent être mis à jour en refaisant un **git add**.

## git commit -m `<message de commit>`

Lorsque vous créez un commit, vous créez une commande de votre code source qui sera packagé sous forme d'un commit. Celui-ci ne pourra pas être modifié par la suite, il pourra seulement être appliqué au serveur, ammend ou effacé. De ce fait, vous devez être certains de vos changements avant de faire un commit.

## git push

Va envoyer les **commits** qui ont été faits localement vers le serveur. Les changements qui ont été faits sur votre machine et sur le repository distants seront au même niveau.

## git push --set-upstream origin master

Lorsque vous n'avez jamais fait de **push** sur une certaine branche, cette commande va vous permettre de faire un premier push.

## git checkout `<nom de votre branche>`

Lorsque vous voulez aller vers une branche existante, cette commande est ce qu'il vous faut.

## git checkout -b `<nom de votre nouvelle branche>`

Lorsque vous voulez aller sur une nouvelle branche que vous voulez créer. La branche sera disponible uniquement sur votre poste **local** tant que vous n'effectuez pas de **push** sur le serveur.

## git pull origin `<nom de la branche principale>`

Lorsque vous voulez aller chercher les commits d'une certaine branche et de les appliquer dans votre branche locale, vous pouvez utiliser cette commande. Il se peut que vous soyez obligés d'aller chercher les changements en faisant un checkout sur le master localement et d'effectuer un pull. Suite à cela, revenez à votre branche et réessayez de faire la commande pour voir si les changements sont appliqués sur votre branche.

# Lectures intéressantes

Il existe plusieurs types de flow pour utiliser git. Celui que je préfère personnellement utiliser est le _Trunk Based Development_, qui nous pousse à avoir une branche principale stable et que les branches ne s'éloignent jamais trop de celui-ci.

https://www.optimizely.com/optimization-glossary/trunk-based-development/

Pour voir les différences entre les merge et les rebase, c'est ici:

https://www.atlassian.com/fr/git/tutorials/merging-vs-rebasing#:~:text=Le%20merge%20est%20une%20solution,la%20branche%20principale%20(%20main%20).

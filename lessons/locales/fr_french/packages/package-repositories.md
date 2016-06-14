# Dépôt de paquets

## Lesson Content

Comment est-ce que les paquets, qui ont été téléversés sur internet, se retrouve-t-ils sur nos ordinateurs? Allez-vous sur la page de téléchargement de chacun des paquets que vous voulez et cliquez vous sur télécharger et installer? Eh bien, en fait, vous pouvez le faire, mais il existe une meilleure solution que l'on appelle les dépôts de paquets (<i>package repositories</i>). Les dépôts de paquets sont simplement un emplacement central où sont stockés les paquets. Il existe une tonnes de dépôts qui contiennent eux aussi une tonnes de paquets et le plus génial dans tout cas c'est qu'ils se trouvent tous sur internet sans recourir à des disques d'installation inutiles. Votre machine ne sait pas où regarder pour trouver ces dépôts si vous ne lui indiquez pas explicitement leur emplacement.

Par exemple, disons que je veux le logiciel WackyWidgets sur ma machine. Eh bien, WackyWidgets maintiennent leur propre dépôt pour les paquets de leurs widgets. À l'intérieur de ce dépôt se trouve 10 paquets qui sont CoolWidget, SuperWidget, etc. WackyWidgets héberge ce dépôt à du lien de la source suivante: http://download.widgets/linux/deb/

Maintenant, à la place d'aller sur leur site internet pour télécharger directement le paquet, vous pouvez indiquer à votre machine comment trouver le logiciel WackyWidgets à partir du lien de la source.

Votre distribution contient par défaut une liste de sources pré-approuvées dans lesquels vous pouvez récupérer des logiciels et c'est de cette manière que les paquets de base que vous avez sur votre système sont installés. Sur un système Debian, ce fichier source est <b>/etc/apt/sources.list</b>. Votre machine va savoir qu'elle doit regarder dans ce fichier et elle regardera toutes les dépôts de source que vous ajouterez dans ce fichier.

## Exercise

Aucun exercise pour cette leçon.

## Quiz Question

Where is the sources file in a Debian system?
Où est le fichier des sources dans un système Debian?

## Quiz Answer

/etc/apt/sources.list

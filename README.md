# 2020-04_UE-neurosciences-computationnelles
matériel pour le cours de modélisation
# From the retina to action: Understanding visual processing

* Où: Marseille (France) - et principalement de faaçon virtuelle

* Quoi: Master Neurosciences et Sciences Cognitives

* But de ce travail: lire un article scientifique et pouvoir à la fois le reproduire avec des simulations de neurones.

* Modalités: les étudiants s'organisent seuls, en binome ou en trinome pour fournir un mémoire sous forme de `notebook` complété à partir de celui qui est fourni. Les commentaires doivent être fait en français (ou en anglais si nécessaire).

* Forum de questions: https://spik.xyz/nc/index.php/call/xuswegwv (pas de logiciel / login nécessaire)

# reproduction de l'article de Mainen & Sejnowski, 1995

## contexte

* en premier lieu, un article à lire sur le temps dans le cerveau: https://laurentperrinet.github.io/publication/perrinet-19-temps/ [lien direct](https://theconversation.com/temps-et-cerveau-comment-notre-perception-nous-fait-voyager-dans-le-temps-127567)

* Le but de cette première tache est de créer un "raster plot" qui montre la reproducibilité d'un train de spike avec des répétitions du même stimulus, comme dans ce travail dans la [rétine de rongeurs](https://laurentperrinet.github.io/2019-04-03_a_course_on_vision_and_modelization/#/1/3) ou dans le [cortex (V1) du chat](https://laurentperrinet.github.io/2019-04-03_a_course_on_vision_and_modelization/#/1/6).

Ici, nous allons essayer de répliquer la figure 1 de [Mainen & Sejnowski (1995)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.299.8560&rep=rep1&type=pdf):

![Mainen Sejnowski 1995](http://i.stack.imgur.com/ixnrz.png "figure 1")

Et pour celà, nous allons procéder à plusieures étapes progressives à rédiger dans le [noteboook](src/A_0_IntegrateAndFire.ipynb):

## prise en main des outils: numpy et matplotlib

- on va créer des vecteurs représentant la dynamique d'un valeur en fonction du temps
- pour cela, on crée un vecteur `time, 1995 représentant 2 secondes avec une précision de dt=1ms
- dans un premier temps, on va créer un plot d'un spike, d'un créneau & d'une sinusoïde

## définition du problème: leaky-integrate and fire neuron

- on va simuler 1 neurone pour 2 secondes avec une précision de dt=1ms
- pour cela, on utilise l'équation d'un lIF
- on montre alors sa réponse aux stimuli créés ci-dessus

## injection d'un bruit

- Comme dans la figure 1 de Mainen & Sejnowski (1995), on ajoute un bruit à l'injection de courant
- ce bruit peut être caractisé par son amplitude et son temps caractéristique: quel est l'impact sur le résultat?
- que se passe-t-il quand on inclut un bruit interne à la dynamique du neurone?

## bonus: utilisation de pyNN / brian

- on va utiliser [brian](http://briansimulator.org/) pour écrire l'équation du lIF et refaire les mêmes simulations
- on compare avec d'autres modèles de neurone

## références

* http://e.guigon.free.fr/rsc/article/BretteGuigon03.pdf


# Annexe

## d'autre cours sur le même sujet

* [Des illusions aux hallucinations visuelles: une porte sur la perception](https://laurentperrinet.github.io/talk/2019-04-18-jnlf/) - ([slides](https://laurentperrinet.github.io/2019-04-18_JNLF/)) - article sur la perception visuelle : https://laurentperrinet.github.io/post/2019-06-06-theconversation/ [lien direct](https://theconversation.com/illusions-et-hallucinations-visuelles-une-porte-sur-la-perception-117389)


* [Modelling spiking neural networks using Brian, Nest and pyNN](https://laurentperrinet.github.io/talk/2019-04-03-a-course-on-vision-and-modelization/) - ([slides](https://laurentperrinet.github.io/2019-01-14_LACONEU/))

* [Tutorial on predictive coding](https://laurentperrinet.github.io/talk/2018-03-26-cours-neuro-comp-fep/)  https://laurentperrinet.github.io/talk/2017-06-30-telluride/ https://laurentperrinet.github.io/sciblog/files/2017-06-30_Telluride.html

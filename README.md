# 2021_UE-neurosciences-computationnelles, matériel pour le cours de modélisation


* Où: Marseille (France)

* Quoi: [Master 1 Neurosciences et Sciences Cognitives](https://ametice.univ-amu.fr/course/view.php?id=70136)


1. _Réseaux neuronaux artificiels pour la vision_

  * Mercredi 24/03/2021 de 9h-12h
  * Introduction aux Neurosciences de la Vision
  * Réseaux de neurones artificiels et apprentissage machine

2. _Neurones impulsionnels et modèles des fonctions visuelles_
  * Mercredi 24/03/2021 de 13h30-16h30
  * TP via notebook
  * https://github.com/laurentperrinet/2021_UE-neurosciences-computationnelles/

Rendez-vous sur https://univ-amu-fr.zoom.us/j/95045077273?pwd=Y2Y2Q2VWbEUrd3lFRlUrdjlsczRVdz09


# TP: reproduction de l'article de Mainen & Sejnowski, 1995


* But de ce travail: lire un article scientifique, pouvoir le reproduire avec des simulations d'un neurone et afin d'améliorer sa compréhension.

* Modalités: les étudiants s'organisent seuls, en binome ou en trinome pour fournir un mémoire sous forme de [notebook](https://jupyter.org/) complété à partir [du modèle qui est fourni](https://raw.githubusercontent.com/laurentperrinet/2021_UE-neurosciences-computationnelles/master/C_MainenSejnowski1995.ipynb)). Suivez les balises `TODO` dans le notebook pour vous guider dans cette rédaction. Les commentaires doivent être fait en français (ou en anglais si nécessaire) dans le notebook (n'oubliez-pas de sauver vos changements) et envoyé par e-mail à mailto:laurent.perrinet@univ-amu.fr une fois votre travail fini (de préférence *avant* le 31 avril).

* Outils nécessaires: [Jupyter](https://jupyter.org/), avec [numpy](https://numpy.org/) et [matplotlib](https://matplotlib.org/). Ce sont des outils standard et qui sont facilement installables sur toute plateforme. D'autres solutions hébergées existent:
  * [ebrains / HBP](https://wiki.ebrains.eu/bin/view/Collabs/neuromorphic/SpiNNaker/)
  * https://deepnote.com/
  * sur  [GoogleColab](https://colab.research.google.com)  https://colab.research.google.com/github/laurentperrinet/2021_UE-neurosciences-computationnelles/blob/master/C_MainenSejnowski1995.ipynb

## contexte

* Le but de cette première tache est de créer un "raster plot" qui montre la reproducibilité d'un train de spike avec des répétitions du même stimulus, comme dans ce travail dans la [rétine de rongeurs](https://laurentperrinet.github.io/2019-04-03_a_course_on_vision_and_modelization/#/1/3) ou dans le [cortex (V1) du chat](https://laurentperrinet.github.io/2019-04-03_a_course_on_vision_and_modelization/#/1/6).

Ici, nous allons essayer de répliquer la figure 1 de [Mainen & Sejnowski (1995)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.299.8560&rep=rep1&type=pdf):

![Mainen Sejnowski 1995](http://i.stack.imgur.com/ixnrz.png "figure 1")

## prise en main des outils: numpy et matplotlib

- on va créer des vecteurs représentant la dynamique d'un valeur en fonction du temps
- pour cela, on crée un vecteur `time' représentant 1 seconde avec une précision de dt=.5ms
- dans un premier temps, on va créer un plot d'un spike, d'un créneau & d'une sinusoïde

## définition du problème: leaky-integrate and fire neuron

- on va simuler 1 neurone pour 2 secondes avec une précision de dt=1ms
- pour cela, on utilise l'équation d'un leaky-IF
- on montre alors sa réponse aux stimuli créés ci-dessus

## injection d'un bruit

- Comme dans la figure 1 de Mainen & Sejnowski (1995), on ajoute un bruit à l'injection de courant
- ce bruit peut être caracterisé par son amplitude et son temps caractéristique: quel est l'impact sur le résultat?
- que se passe-t-il quand on inclut un bruit interne à la dynamique du neurone?

# Annexes

* un article à lire sur le temps dans le cerveau: https://laurentperrinet.github.io/publication/perrinet-19-temps/ [lien direct](https://theconversation.com/temps-et-cerveau-comment-notre-perception-nous-fait-voyager-dans-le-temps-127567)

* [Des illusions aux hallucinations visuelles: une porte sur la perception](https://laurentperrinet.github.io/talk/2019-04-18-jnlf/) - ([slides](https://laurentperrinet.github.io/2019-04-18_JNLF/)) - article sur la perception visuelle : https://laurentperrinet.github.io/post/2019-06-06-theconversation/ [lien direct](https://theconversation.com/illusions-et-hallucinations-visuelles-une-porte-sur-la-perception-117389)

* [Modelling spiking neural networks using Brian, Nest and pyNN](https://laurentperrinet.github.io/talk/2019-04-03-a-course-on-vision-and-modelization/) - ([slides](https://laurentperrinet.github.io/2019-01-14_LACONEU/))

* [Tutorial on predictive coding](https://laurentperrinet.github.io/talk/2018-03-26-cours-neuro-comp-fep/)  https://laurentperrinet.github.io/talk/2017-06-30-telluride/ https://laurentperrinet.github.io/sciblog/files/2017-06-30_Telluride.html

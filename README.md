# GardenMapBot (GaMBo🌸)

## À propos du projet

<img align="left" src="https://github.com/THE07s/GarderMapBot/assets/101391118/45ccf17c-52ff-4c6a-bc98-bd0e7e535424" alt="GMD logo" width="70%" />

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**GaMBo🌸** est un robot conçu pour cartographier les jardins en mesurant la température, l'humidité et l'ensoleillement. Ces données lui permettent de fournir des conseils pour optimiser la croissance et la santé des plantes.

<br clear="left"/>

## Sommaire

[I. Qui sommes-nous?](#i-qui-sommes-nous-)

[II. Pourquoi ce projet?](#ii-pourquoi-ce-projet-)

[III. Fonctionnalités](#iii-fonctionnalités)

[IV. Liste du matériel du projet final](#iv-liste-du-matériel-du-projet-final)

[V. Installation du projet final](#v-installation-du-projet-final)

[VI. Notre parcours](#vi-notre-parcours)

[VII. Contributions](#vii-contributions)

[VIII. Contacts](#viii-contacts)

[IX. Remerciements](#ix-remerciements)

## I. Qui sommes-nous ?

Nous sommes un groupe de 4 étudiants passionnés, inscrits en classe préparatoire au cycle ingénieur à ESEO - Cours Lumière, située au Togo. L'équipe est constituée de GNASSINGBE Emilie, DOUMBIA Aïchata, KORDOHOU Errath et LEENAERTS Loïc (chef de projet). 

## II. Pourquoi ce projet ?

Inspirés par l'événement mondial Arduino Day, notre équipe a saisi l'opportunité offerte par nos enseignants de concevoir des projets de robotique. Nous aspirons à améliorer la culture des plantes et à encourager l'utilisation de la tech pour faciliter et optimiser l'agriculture sur notre continent.

## III. Fonctionnalités

- **Prise en charge de formes de jardins quelconques**
- **Cartographie thermique**
- **Cartographie de l'humidité**
- **Cartographie de l'ensoleillement**
- **Conseils de jardinage**

## IV. Liste du matériel du projet final

| **Système**     | **Arduino**                     | **Espressif**                        |
| --------------- | ------------------------------- | ------------------------------------ |
| 🖥️ **Microcontrôleur** | Arduino NANO                | ESP-32-CAM                       |
| 📡 **Capteurs** | - 🌡️💧DHT22 × 1               | - 🌡️💧DHT22 × 1                       |
|                 | - 🌅 Photorésistance × 1      | - 🌅 Photorésistance × 1             |
|                 | - 🔊 Capteur ultrason × 3     | - 🔊 Capteur ultrason × 3            |
|                 | - 📷 Module caméra             |                                      |
|                 | - 🌍 Module GPS                | - 🌍 Module GPS                      |
| 🛠️ **Autres**  | - ⚙️ Servomoteurs débridés × 4~6 | - ⚙️ Servomoteurs débridés × 4~6 (dépendant de la charge totale) |
|                 | - 🔋 Batterie : rechargeable et légère | - 🔋 Batterie : rechargeable et légère |
|                 | - 🛡️ Châssis : PLA             | - 🛡️ Châssis : PLA                   |

## V. Installation du projet final
😶‍🌫️

## VI. Notre parcours

<img align="right" src="https://github.com/THE07s/GardenMapBot/assets/162814213/61cb331c-02a5-4488-8f8d-96ea3b070785" alt="schémaGMB" width="50%" />

Le projet final implique un robot entièrement autonome, capable de cartographier un jardin de forme complexe. Mais avant d'atteindre ce résultat final, nous devons adopter une méthode itérative. Ainsi, dans un premier temps, le projet se limitera à ces fonctionalités :

- **Prise en charge de formes de jardins rectangulaires**
- **Cartographie thermique**
- **Cartographie de l'humidité**
- **Cartographie de l'ensoleillement**



Nous avons eu à realiser un schéma pour avoir une idée de le forme du robot et de l'emplacement des différents composants

<br clear="right"/>
<br>

 <video autoplay loop playsinline src="https://github.com/THE07s/GardenMapBot/assets/101391118/6161aa29-c9dc-4e73-8f62-6bf7b1b91bbf">  video </video>
<br>

Lors de la phase de conception de notre robot, nous avons dû réaliser un schéma détaillé pour visualiser la forme du robot et planifier l'emplacement optimal des différents composants. Cette étape cruciale nous permet de garantir une intégration efficace et une fonctionnalité optimale de chaque élément.

### Schéma du Robot

Pour débuter, nous avons utilisé le [🌡️💧DHT22](https://grabcad.com/library/dht22-module-1), un capteur d'humidité et de température, afin de réguler l'environnement interne du robot. Ce composant essentiel a été placé stratégiquement pour assurer une mesure précise dans toutes les conditions.

Ensuite, nous avons intégré le [⚙️Servomoteur](https://grabcad.com/library/servo-motor-sg90-6) pour contrôler les mouvements mécaniques du robot. Son positionnement a été soigneusement étudié pour garantir une manipulation précise des éléments externes.

Un autre composant crucial est le [🔊Capteur ultrason](https://grabcad.com/library/ultrasonic-sensor-hc-sr04-3), utilisé pour la détection d'obstacles. Nous avons choisi son emplacement de manière à maximiser la couverture de détection tout en minimisant les interférences.

### Composants Supplémentaires

Le [🌍 Module GPS](https://grabcad.com/library/ublox-m6-with-ceramic-antenna-1) a été intégré pour permettre au robot de naviguer efficacement dans son environnement. Son placement a été optimisé pour assurer une réception satellite optimale.

La [🌅 Photorésistance](https://grabcad.com/library/gl5528-photoresistor-1) a également été incluse pour détecter les variations de luminosité, permettant au robot de s'adapter à différentes conditions d'éclairage. Son emplacement a été choisi avec soin pour garantir une mesure précise de la lumière ambiante.

### Contrôle et Alimentation

Pour coordonner toutes ces fonctions, nous avons intégré l'[🖥️Arduino NANO](https://grabcad.com/library/arduino-nano--1), une carte de développement compacte et puissante. Son positionnement central facilite la connexion avec tous les autres composants.

Enfin, pour protéger et faciliter la connexion de l'Arduino Nano, nous avons ajouté un [Shield Arduino NANO](https://grabcad.com/library/arduino-nano-2), assurant ainsi une intégration propre et sécurisée.

### Problèmes & Solutions

Lors de la réalisation de ce projet, nous avons eu à faire face à une flopée de problèmes à savoir :

**Pendant la modélisation 3D** :
- Centrer les extrusions (destinées à la carte) horizontalement au milieu de la face, même en remontant dans l’historique
- Établir une connexion claire entre les esquisses et la modélisation 3D
- Gérer les contraintes lors de l’application d’une projection sans surcontraindre l’esquisse

**Après la modélisation 3D** :
- Le DHT22 et le module GPS ne rentraient pas dans l'espace qui leur était réservés
- Les Servomoteurs flottaeint dans l'espace qui leur était réservés

**Pendant la conception du circuit** :
 - Importer le DHT22 dans Fritzing
 - Importer le Shield adapté à l'Arduino NANO dans Fritzing
 - L'absence du NANO, du module GPS et du DHT22 dans Tinkercad

Pour résoudre ces problèmes, nous avons "innover" c'est-à-dire que dans le cas du circuit, nous avons fait les tests avec l'Arduino UNO puisque le NANO et l'UNO sont les "mêmes".

### Images du modèle 3D

# place ceci au bon endroit s’il te plait et réorganise-le :
# Code de test des servos après les avoir débridé, ici en mettant un angle de 90 les servos sont à l'arrêt, ensuite je vais procéder à une programmation fonctionnelle en lieu et place d'une programmation orientée objet en raison du manque de temps et d'entraînement en cpp 
```cpp
#include <Servo.h>

Servo avant_gauche, arriere_gauche, avant_droit, arriere_droit;

void setup() {
  avant_gauche.attach(2);
  arriere_gauche.attach(3);
  avant_droit.attach(4);
  arriere_droit.attach(5);
}

void loop() {
  avant_gauche.write(90);
  arriere_gauche.write(90);
  avant_droit.write(90);
  arriere_droit.write(90);
}
```


## VII. Contributions

M. Sylvestre OLANLO

M. Josaphat BANKAÏ

## Licence

Distribué sous la Licence Apache-2.0. Voir `LICENSE` pour plus d'informations.

## VIII. Contacts

- <img align="right" src="https://github.com/THE07s/GardenMapBot/assets/162814213/7ce17a51-531f-4dd5-ab0d-2510791ebc77" alt="Loïc" width="14%"/> LEENAERTS Loïc Harry - 📞 +228 79 62 67 84 <br clear="right"/>
<br>

- <img align="right" src="https://github.com/THE07s/GardenMapBot/assets/162814213/47a21ab6-4af5-423a-b38b-64732f9e6863" alt="Émilie" width="14%"/> GNASSINGBE Emilie Koboyo - 📞 +228 93 26 69 57 <br clear="right"/>
<br>

- <img align="right" src="https://github.com/THE07s/GardenMapBot/assets/162814213/64d60790-987e-49c4-a338-266067e54d52" alt="Aïchata" width="14%"/> DOUMBIA Aïchata  - 📞 +228 70 90 99 77 <br clear="right"/>
<br>

- <img align="right" src="https://github.com/THE07s/GardenMapBot/assets/162814213/1ca73ac7-0029-4b0b-93ad-0a4ae5e75d6e" alt="Errath" width="14%"/> KORDOHOU Errath - 📞 +228 91 02 15 05 <br clear="right"/>
<br>

Lien du projet : [GitHub - GaMBo 🌸](https://github.com/THE07s/GarderMapBot.git)

## IX. Remerciements

M. Sylvestre OLANLO, qui nous a accompagné depuis le tout début.

M. Giovanni KAMEKPO, qui nous a montré comment utiliser Git et GitHub.

M. Josaphat BANKAÏ, qui nous a montré ce qu'est la modélisation paramétrée.

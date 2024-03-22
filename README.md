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

Inspirée par l'événement mondial Arduino Day, notre équipe a saisi l'opportunité offerte par nos enseignants de concevoir des projets de robotique. Nous aspirons à améliorer la culture des plantes et à encourager l'utilisation de la tech pour faciliter et optimiser l'agriculture sur notre continent.

## III. Fonctionnalités

- **Prise en charge de formes de jardins quelconques**
- **Cartographie thermique**
- **Cartographie de l'humidité**
- **Cartographie de l'ensoleillement**
- **Conseils de jardinage**

## IV. Liste du matériel du projet final

| **Système**             | **Arduino**                            | **Espressif**                                                    |
|-------------------------|----------------------------------------|------------------------------------------------------------------|
| 🖥️ **Microcontrôleur** | Arduino NANO                           | ESP-32-CAM                                                       |
| 📡 **Capteurs**         | - 🌡️💧DHT22 × 1                       | - 🌡️💧DHT22 × 1                                                 |
|                         | - 🌅 Photorésistance × 1               | - 🌅 Photorésistance × 1                                         |
|                         | - 🔊 Capteur ultrason × 3              | - 🔊 Capteur ultrason × 3                                        |
|                         | - 📷 Module caméra                     |                                                                  |
|                         | - 🌍 Module GPS                        | - 🌍 Module GPS                                                  |
| 🛠️ **Autres**          | - ⚙️ Servomoteurs débridés × 4~6       | - ⚙️ Servomoteurs débridés × 4~6 (dépendant de la charge totale) |
|                         | - 🔋 Batterie : rechargeable et légère | - 🔋 Batterie : rechargeable et légère                           |
|                         | - 🛡️ Châssis : PLA                    | - 🛡️ Châssis : PLA                                              |

## V. Installation du projet final
😶‍🌫️

## VI. Notre parcours

Le projet final implique un robot entièrement autonome, capable de cartographier un jardin de forme complexe. Mais avant d'atteindre ce résultat final, nous devons adopter une méthode itérative. Ainsi, dans un premier temps, le projet se limitera à ces fonctionnalités :

- **Prise en charge de formes de jardins rectangulaires**
- **Cartographie thermique**
- **Cartographie de l'humidité**
- **Cartographie de l'ensoleillement**



Nous avons eu à réaliser le schéma que voici pour avoir une idée de la forme du robot et de l'emplacement des capteurs et composants pour optimiser l'espace efficacement afin d'accueillir l'ensemble du câblage. 

<img align="right" src="https://github.com/THE07s/GardenMapBot/assets/162814213/61cb331c-02a5-4488-8f8d-96ea3b070785" alt="schémaGMB" width="68%" />

- Nous avons donc placé le [🌡️💧DHT22](https://grabcad.com/library/dht22-module-1) tourné vers le sol et sur la face inférieure du robot pour pouvoir prendre nos mesures le plus près possible du sol. 
- Les 4 [⚙️Servomoteur](https://grabcad.com/library/servo-motor-sg90-6) et les 3 [🔊Capteur ultrason](https://grabcad.com/library/ultrasonic-sensor-hc-sr04-3) ont eux, étés logés sur les côtés symétriquement par rapport à l'axe passant par le milieu des faces inférieur et supérieur. 
- La [🌅 Photorésistance](https://grabcad.com/library/gl5528-photoresistor-1) est quant à elle placée de sorte que le milieu de sa face supérieur soit confondus avec l'axe de symétrie. 
- L'antenne du [🌍 Module GPS](https://grabcad.com/library/ublox-m6-with-ceramic-antenna-1) a été placée au-dessus de l'[🖥️Arduino NANO](https://grabcad.com/library/arduino-nano--1) pour des raisons d'esthétiques. 
- La carte [🖥️Arduino NANO](https://grabcad.com/library/arduino-nano--1) est elle-même placée de telle sorte que ces ports soient exposés et facilement accéssibles de l'extérieur.

<br clear="right"/>
<br>
Voici les étapes de la modélisation du corps de notre robot :
<br>
 <video autoplay loop playsinline src="https://github.com/THE07s/GardenMapBot/assets/101391118/6161aa29-c9dc-4e73-8f62-6bf7b1b91bbf">  video </video>
<br>

Après la modélisation, nous avons procédé à l'impression du corps et en raison d'un certain nombre de problèmes d'encadrement, nous avons dû procéder au limage de certaines bordures pour permettre l'accueil des capteurs.

Nous avons ensuite débridé les servomoteurs pour permettre leur rotation en continu. Pour des raisons de logiques, nous avons choisi de prendre un angle de 90° comme position d'arrêt. Voici le code de test que nous avons écrit :

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

À présent, nous allons procéder à une programmation fonctionnelle en lieu et place d'une programmation orientée objet en raison du manque de temps et d'entraînement en C++.

### Problèmes & Solutions

Lors de la réalisation de ce projet, nous avons eu à faire face à une flopée de problèmes à savoir :

**Pendant la modélisation 3D** :
- Centrer les extrusions (destinées à la carte) horizontalement au milieu de la face réservée en utilisant la modélisation paramétrique.
- Établir une connexion claire entre les esquisses et la modélisation 3D.
- Éviter les sur-contraintes de l’esquisse.

**Après la modélisation 3D** :
- Le DHT22 et le module GPS ne rentraient pas dans l'espace qui leur était réservés.
- Les Servomoteurs flottaient dans l'espace qui leur était réservés.

**Pendant la conception du circuit** :
 - Importer le DHT22 dans Fritzing.
 - Importer le Shield adapté à l'Arduino NANO dans Fritzing.
 - L'absence du NANO, du module GPS et du DHT22 dans Tinkercad.

Pour résoudre ces problèmes, nous avons "innover" faisant les tests nécessaires avec l'Arduino UNO étant donné les nombreuses similitudes entre cette carte et l'arduino NANO.

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

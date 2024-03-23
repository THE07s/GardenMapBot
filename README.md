# GardenMapBot (GaMBo🌸)

## À propos du projet

<img align="left" src="https://github.com/THE07s/GarderMapBot/assets/101391118/45ccf17c-52ff-4c6a-bc98-bd0e7e535424" alt="GMD logo" width="70%" />

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**GaMBo🌸** est un robot conçu pour cartographier les jardins en mesurant la température, l'humidité et l'ensoleillement. Ces données lui permettent de fournir des conseils pour optimiser la croissance et la santé des plantes.

<br clear="left"/>

## Sommaire

[I. Qui sommes-nous ?](#i-qui-sommes-nous-)

[II. Pourquoi ce projet ?](#ii-pourquoi-ce-projet-)

[III. Fonctionnalités](#iii-fonctionnalités)

[IV. Liste du matériel du projet final](#iv-liste-du-matériel-du-projet-final)

[V. Installation du projet final](#v-installation-du-projet-final)

[VI. Notre parcours](#vi-notre-parcours)

[VII. Licence](#vii-licence)

[VIII. Contacts](#viii-contacts)

[IX. Contributions](#ix-contributions)

[X. Remerciements](#x-remerciements)

## I. Qui sommes-nous ?

Nous sommes un groupe de 4 étudiants passionnés, inscrits en classe préparatoire au cycle ingénieur à ESEO - Cours Lumière, située au Togo. L'équipe est constituée de GNASSINGBE Émilie, DOUMBIA Aïchata, KORDOHOU Errath et LEENAERTS Loïc (chef de projet). 

## II. Pourquoi ce projet ?

Inspirée par l'événement mondial Arduino Day, notre équipe a saisi l'opportunité offerte par nos enseignants de concevoir des projets de robotique. Nous aspirons à améliorer la culture des plantes et à encourager l'utilisation de la tech pour faciliter et optimiser l'agriculture sur notre continent.

## III. Fonctionnalités

- **Prise en charge de formes de jardins quelconques**
- **Cartographie thermique**
- **Cartographie de l'humidité**
- **Cartographie de l'ensoleillement**
- **Conseils de jardinage**

```mermaid
graph TD;
    A[Capteurs de température, humidité et luminosité] --> B(Analyse des données);
    B --> C{Conditions de jardinage};
    C -->|Température élevée| D(Arrosage plus fréquent);
    C -->|Humidité basse| E(Augmenter l'arrosage ou ajouter du paillis);
    C -->|Ensoleillement insuffisant| F(Déplacer les plantes vers des zones plus ensoleillées ou ajouter des lampes de croissance);
    C -->|Conditions optimales| G(Aucun conseil nécessaire);
    D --> H{Connecté à un ordinateur};
    E --> H;
    F --> H;
    G --> H;
    H --> I(Interface utilisateur);
    I --> J[Tableau de données];
    I --> K[Graphiques de tendances];
```

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

Voici les différentes parties qui forment le boitier de notre robot :
<br>
<p>
    <img src="https://github.com/THE07s/GardenMapBot/assets/162814002/96229055-2d68-4da5-b596-8e4f06e4de6f" alt="Dessous" width="47%" hspace="10" >
    <img src="https://github.com/THE07s/GardenMapBot/assets/162814002/d35b4b35-3c79-444f-ae4d-81c1af8201e7" alt="Dessus" width="47%" hspace="10" >
</p>

### Servomoteurs

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

J'ai donc commencé à créer les fonctions de base du robot, autrement dit avancer, reculer et tourner. Pour la fonction *tourner()* il me fallait trouver le nombre de millisecondes au bout duquel le robot faisait une rotation sensiblement égale à 90°. Voici donc le programme de test qui traduit mes déductions :

```cpp
#include <Servo.h>

Servo avant_gauche, arriere_gauche, avant_droit, arriere_droit;

void stop() {
  avant_gauche.write(90);
  arriere_gauche.write(90);
  avant_droit.write(90);
  arriere_droit.write(91);
}

void avancer(int duree) {
  avant_gauche.write(180);
  arriere_gauche.write(96);
  avant_droit.write(0);
  arriere_droit.write(0);
  delay(duree);
  stop();
}

void reculer(int duree) {
  avant_gauche.write(0);
  arriere_gauche.write(0);
  avant_droit.write(180);
  arriere_droit.write(180);
  delay(duree);
  stop();
}

void tourner_moins_90() {
  avant_gauche.write(0);
  arriere_gauche.write(0);
  avant_droit.write(0);
  arriere_droit.write(0);
  delay(650);
  stop();
};

void tourner_plus_90() {
  avant_gauche.write(180);
  arriere_gauche.write(180);
  avant_droit.write(180);
  arriere_droit.write(180);
  delay(650);
  stop();
};

void carre() {
  for (int i = 0; i < 4; i++) {
    avancer(1750);
    tourner_plus_90();
  };
};

void setup() {
  avant_gauche.attach(2);
  arriere_gauche.attach(3);
  avant_droit.attach(4);
  arriere_droit.attach(5);
}

void loop() {
  carre();
}
```
Voici un aperçu du déplacement du robot :

<br>
<video autoplay loop playsinline src="https://github.com/THE07s/GardenMapBot/assets/162814002/8494161b-c6f6-4778-b160-64e97f9adee7" width="30%" hspace="10"> video </video>
<br>

### Ultrason HC-SR04

**Fonctionnement individuel**

```cpp
#include <Ultrasonic.h>

const int trigPin = 9;
const int echoPin = 8;

const int ledPin = 13;

Ultrasonic ultrasonic(trigPin, echoPin);

void setup() {
  Serial.begin(9600);

  pinMode(ledPin, OUTPUT);
}

void loop() {
  float distance = ultrasonic.read();

  Serial.print("Distance: ");
  Serial.print(distance);
  Serial.println(" cm");

  if (distance > 20) {
    digitalWrite(ledPin, HIGH);
  } else {
    digitalWrite(ledPin, LOW);
  }

  delay(1000);
}

```

**Fonctionnement des 3 ultrasons**

```cpp
#include <Ultrasonic.h>

const int trigPin1 = 4; 
const int echoPin1 = 3; 
const int trigPin2 = 6;
const int echoPin2 = 5; 
const int trigPin3 = 9; 
const int echoPin3 = 8; 

const int ledPin = 13;

Ultrasonic ultrasonic1(trigPin1, echoPin1);
Ultrasonic ultrasonic2(trigPin2, echoPin2);
Ultrasonic ultrasonic3(trigPin3, echoPin3);

void setup() {
  Serial.begin(9600);

  pinMode(ledPin, OUTPUT);
}

void loop() {
  float distance1 = ultrasonic1.read();
  float distance2 = ultrasonic2.read();
  float distance3 = ultrasonic3.read();

  Serial.print("Distance 1: ");
  Serial.print(distance1);
  Serial.println(" cm");
  Serial.print("Distance 2: ");
  Serial.print(distance2);
  Serial.println(" cm");
  Serial.print("Distance 3: ");
  Serial.print(distance3);
  Serial.println(" cm");

  if (distance1 > 20 || distance2 > 20 || distance3 > 20) {
    digitalWrite(ledPin, HIGH); // Allumez la LED
  }
  
  else {
    digitalWrite(ledPin, LOW);
  }
  delay(1000);
}

```

### DHT

En parallèle de l'ultrason, nous avons testé le DHT22 qui, nous le rappellons, devait servir à mesurer la température et l'humidité. Totefois lors des tests, il s'est grillé et nous l'avons remplacé par le DHT11. Voici le code qui nous a permis d'effectuer les tests :

```cpp
#include <Arduino.h>
#include "DHT_Async.h"

#define DHT_SENSOR_TYPE DHT_TYPE_11

static const int DHT_SENSOR_PIN = 10;
DHT_Async dht_sensor(DHT_SENSOR_PIN, DHT_SENSOR_TYPE);


void setup() {
    Serial.begin(115200);
}

static bool measure_environment(float *temperature, float *humidite) {
    static unsigned long measurement_timestamp = millis();

    if (millis() - measurement_timestamp > 4000ul) {
        if (dht_sensor.measure(temperature, humidite)) {
            measurement_timestamp = millis();
            return (true);
        }
    }

    return (false);
}

void loop() {
    float temperature;
    float humidite;

    if (measure_environment(&temperature, &humidite)) {
        Serial.print("T = ");
        Serial.print(temperature, 1);
        Serial.print(" deg. C, H = ");
        Serial.print(humidite, 1);
        Serial.println("%");
    }
}

```
### Code "Final"

```cpp
#include <Servo.h>
#include <Arduino.h>
#include "DHT_Async.h"
#include <VARSTEP_ultrasonic.h>


Servo avant_gauche, arriere_gauche, avant_droit, arriere_droit;
#define DHT_SENSOR_TYPE DHT_TYPE_11
#define trigger_pin 8
#define echo_pin 9
double distance_cm, distance_m;
VARSTEP_ultrasonic HCSR04(trigger_pin, echo_pin);
static const int DHT_SENSOR_PIN = 7;
DHT_Async dht_sensor(DHT_SENSOR_PIN, DHT_SENSOR_TYPE);

float temperature;
float humidity;

void stop() {
  avant_gauche.write(90);
  arriere_gauche.write(90);
  avant_droit.write(90);
  arriere_droit.write(91);
}

void avancer(int duree) {
  avant_gauche.write(180);
  arriere_gauche.write(96);
  avant_droit.write(0);
  arriere_droit.write(0);
  delay(duree);
  stop();
}

void reculer(int duree) {
  avant_gauche.write(0);
  arriere_gauche.write(0);
  avant_droit.write(180);
  arriere_droit.write(180);
  delay(duree);
  stop();
}

void tourner_moins_90() {
  avant_gauche.write(0);
  arriere_gauche.write(0);
  avant_droit.write(0);
  arriere_droit.write(0);
  delay(650);
  stop();
};

void tourner_plus_90() {
  avant_gauche.write(180);
  arriere_gauche.write(180);
  avant_droit.write(180);
  arriere_droit.write(180);
  delay(650);
  stop();
};

static bool measure_environment(float *temperature, float *humidity) {
    static unsigned long measurement_timestamp = millis();

    /* Measure once every four seconds. */
    if (millis() - measurement_timestamp > 4000ul) {
        if (dht_sensor.measure(temperature, humidity)) {
            measurement_timestamp = millis();
            return (true);
        }
    }

    return (false);
}

void T_H() {
  distance_cm = HCSR04.distance_cm();
  distance_m = HCSR04.distance_m();
  if (measure_environment(&temperature, &humidity)) {
    Serial.print("T = ");
    Serial.print(temperature, 1);
    Serial.print(" deg. C, H = ");
    Serial.print(humidity, 1);
    Serial.println("%");
  }
}

void check_obstacle() {
  if(distance_cm <= 3.0) {
    Serial.print("Distance: ");
    Serial.print(distance_cm);
    Serial.print("cm | ");
    Serial.print(distance_m);
    Serial.println("m");
    reculer(875);
    tourner_plus_90();
    check_obstacle();
  }
}

void carre() {
  for (int i = 0; i < 4; i++) {
    check_obstacle();
    avancer(1750);
    tourner_plus_90();
    T_H();
  };
};

void setup() {
  while(!Serial);
  Serial.begin(9600);
  avant_gauche.attach(2);
  arriere_gauche.attach(3);
  avant_droit.attach(4);
  arriere_droit.attach(5);
}

void loop() {
  carre();
}
```
> [!NOTE]
> ### Problèmes & Solutions
> Lors de la réalisation de ce projet, nous avons eu à faire face à une flopée de problèmes à savoir :
> **Pendant la modélisation 3D** :
> - Centrer les extrusions (destinées à la carte) horizontalement au milieu de la face réservée en utilisant la modélisation paramétrique.
> - Établir une connexion claire entre les esquisses et la modélisation 3D.
> - Éviter les sur-contraintes de l’esquisse.

> [!WARNING]
> **Après la modélisation 3D** :
> - Le DHT22 et le module GPS ne rentraient pas dans l'espace qui leur était réservés.
> - Les Servomoteurs flottaient dans l'espace qui leur était réservés.

> [!NOTE]
> **Pendant la conception du circuit** :
> - Importer le DHT22 dans Fritzing.
> - Importer le Shield adapté à l'Arduino NANO dans Fritzing.
> - L'absence du NANO, du module GPS et du DHT22 dans Tinkercad.

> [!TIP]
> Pour résoudre ces problèmes, nous avons "innover" et fait les tests nécessaires avec l'Arduino UNO étant donné les nombreuses similitudes entre cette carte et l'arduino NANO. Quant aux pièces, nous avons limé les contours pour pouvoir placer le DHT22 et utiliser le pistolet à colle pour fixer les servomoteurs.

### Références

- [Inspiration pour la conception du corps 🧰](https://www.youtube.com/watch?v=E0NVC8xhf3I)
- [Roues pour le servomoteur SG90 ⚙️](https://cults3d.com/fr/mod%C3%A8le-3d/art/wheel-for-sg90-servo)
- [Configuration du capteur ultrason 🔊](https://arduino-france.site/ultrason-hc-sr04/)
- [Aide à la rédaction de la documentation 📑](https://github.com/miyujach/Projet-Robot/blob/9f384fafb67974cea4fc9b659ff7004661033b75/README.md#projet-ascyloom)

## VII. Licence

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

## IX. Contributions

- M. Sylvestre OLANLO (Disposition des matériels dans le boitier)

- M. Josaphat BANKAÏ (Fusion 360)

- Kenneth K. NONVIGNON (Diagramme)

- Pierre K. ATADEGNON & Adama NADJOMBE (Servomoteurs débridés)


## X. Remerciements

- M. Sylvestre OLANLO, qui nous a suivi depuis le tout début.

- M. Giovanni KAMEKPO, qui nous a initié à Git & GitHub.

- M. Josaphat BANKAÏ, qui nous entretenu sur la modélisation paramétrique.

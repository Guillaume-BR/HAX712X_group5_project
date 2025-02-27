# Occitanie air quality explorer
L'objectif du projet est de créer une application web dans laquelle il sera possible de visualiser un graphique ou plusieurs graphiques simultanément décrivant l'évolution d'une valeur de polluant en fonction d'une donnée du climat. Tout ceci pourra être conditionné en amont par d'autres choix.

```mermaid
flowchart TD
    A[Zone] --> B[Condition]
    B --> D[Pollution]
    B --> E[Climat]
    E --> G[Graphique]
    D --> G
```

De plus, nous créerons une carte intéractive cliquablede la région Occitanie à la précision du canton pour obtenir un traitement suffisamment fin, l'échelle du département étant trop grande. 

Pour faire tout ça, nous nous organiserons en trois équipes 
 - équipe 1 : le traitement des données
 - équipe 2 : le visuel
 - équipe 3 : le lien

```mermaid
gantt
    title Occitanie air quality explorer
    dateFormat YYYY-MM-DD
    section Phase 1
        Brainstrorming 1 :a1, 2023-10-01, 10d
        Brainstorming 2  :after a1, 10d
        Snpashot : 2023-10-22
    section Development
        Traitements des données : a2, 2023-10-22, 30d
        Visualiation   : 2023-11-01, 30d
        Coordination : 2023-11-15 , 25d
        Documentation : a3, after a2 , 10d
        Beamer : after a3, 5d
```

## Le traitement des données

Les packages standarts de traitements des données seront utilisés ici : pandas, numpy, scipy. 
Il s'agira dans un premier temps de nettoyer les données pour obtenir des dataframes utilisables.

## Le visuel

Pour créer cette carte, nous utiliserons le package Python : folium ou choropleth. Nous introduirons un fichier Geojson pour obtenir une carte cliquable à la précision du canton.

Pour définir nos choix de variables à utiliser pour tracer les grahiques, nous utiliserons le package python dash. Cela nous permettra d'obtenir de l'intéractivité dans nos graphiques.

Pour les graphiques, plusieurs choix s'offrent à nous : matplotlib, seaborn. Nous ne sommes pas encore fixés dessus.
Enfin pour la page web nous utiliserons le framework django.

## L'analyse et interprétation des résultats

## Membres et contact

- Abchiche Thiziri : thiziri.abchiche@etu.umontpellier.fr
- Bernard-Reymond Guillaume : guillaume.bernard-reymond@etu.umontpellier.fr
- Hamomi Majda : majda.hamomi@etu.umontpellier.fr
- Gaggini Lorenzo : lorenzo.gaggini@etu.umontpellier.fr
- Ollier Julien : julien.ollier@etu.umontpellier.fr

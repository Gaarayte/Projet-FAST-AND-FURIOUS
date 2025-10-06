# Projet-FAST-AND-FURIOUS
Projet effectué dans mon école, notre travail été de réalisé un code fonction pour la simulation des temps d'un parcours type HOTWHEELS avec des loopings et saut. Les différentes stats des voitures étaient prises en compte à tout point du parcours.

# Fast and Furious - Simulateur de Course 🏎️

## Description

Simulation physique d'une course automobile inspirée de Fast and Furious où Dom Toretto doit battre Owen Shaw en complétant un parcours extrême en moins de 8 secondes.

## Le Circuit

Le parcours comprend 4 sections critiques :

1. **Piste d'élan** (31m, pente 3.699°) - Avec nitro activé
2. **Looping vertical** (rayon 6m) - Nécessite une vitesse minimale
3. **Saut du ravin** (minimum 9m) - Vol parabolique
4. **Sprint final** (10m) - Ligne droite

## Voitures Disponibles

- **Dodge** - Lourde et puissante (1760 kg)
- **Toyota** - Équilibrée et rapide (1615 kg)
- **Chevrolet** - Intermédiaire (1498 kg)
- **Mazda** - Légère et agile (1385 kg)
- **Nissan** - Stable (1540 kg)
- **Mitsubishi** - Performante (1600 kg)

Chaque voiture possède des caractéristiques uniques : masse, accélération, dimensions, coefficients aérodynamiques (Cx, Cz) et friction (mu).

## Physique Simulée

- **Forces appliquées** : gravité, accélération moteur, friction, résistance aérodynamique
- **Méthode numérique** : Intégration d'Euler (dt = 0.001s)
- **Modélisation** : 
  - Mouvement rectiligne avec résistance de l'air
  - Mouvement circulaire pour le looping
  - Trajectoire de projectile pour le saut

## Utilisation

```bash
python FASTANDFURIOUS.py
```

Le programme vous demandera de choisir une voiture parmi la liste affichée.

## Conditions de Victoire

- ✅ Compléter le looping sans tomber
- ✅ Franchir le ravin (≥ 9m)
- ✅ Temps total < 8 secondes

## Visualisations

Le programme génère automatiquement :
- Graphique de vitesse dans le looping
- Trajectoire de la voiture lors du saut

## Dépendances

```python
numpy
matplotlib
```

## Notes Techniques

- Le nitro augmente l'accélération de 30%
- La vitesse minimale pour le looping est calculée en fonction de l'énergie et du travail des forces résistives
- La résistance de l'air varie avec le carré de la vitesse
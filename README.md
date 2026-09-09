# Tip Calculator

Une application Android simple construite avec **Jetpack Compose** qui calcule le pourboire à laisser en fonction du montant de l'addition et du niveau de service.

Ce projet a pour objectif d'illustrer les bases de la gestion d'état en Compose (remember, mutableStateOf), la création de composables réutilisables, ainsi que la construction d'une interface simple et fonctionnelle avec Material 3.

## Aperçu

L'application permet à l'utilisateur de :
- Saisir le montant de l'addition
- Indiquer le pourcentage de pourboire souhaité (en fonction de la qualité du service)
- Arrondir le pourboire à l'entier supérieur grâce à un interrupteur (switch)
- Voir le montant du pourboire calculé, formaté selon la devise locale

## Fonctionnalités

- Calcul automatique du pourboire en temps réel
- Clavier numérique adapté pour la saisie des montants
- Option "Arrondir le pourboire" via un `Switch`
- Formatage automatique de la devise selon la locale de l'appareil (`NumberFormat.getCurrencyInstance()`)
- Interface construite entièrement en Jetpack Compose avec Material 3

## Architecture du code

| Composant | Rôle |
|---|---|
| `MainActivity` | Point d'entrée de l'application, initialise le thème et l'UI |
| `TipTimeLayout` | Composable principal qui gère l'état (montant, pourcentage, arrondi) et assemble l'écran |
| `EditNumberField` | Composable réutilisable pour les champs de saisie numérique (montant, pourcentage) |
| `RoundTheTipRow` | Composable affichant le libellé et le switch pour arrondir le pourboire |
| `calculateTip` | Fonction utilitaire qui calcule et formate le montant du pourboire |

## Prérequis

- Android Studio (version récente recommandée)
- SDK Android configuré
- Kotlin

## Installation

1. Cloner le dépôt :
   ```bash
   git clone <url-du-repo>
   ```
2. Ouvrir le projet dans Android Studio
3. Laisser Gradle synchroniser les dépendances
4. Lancer l'application sur un émulateur ou un appareil physique

## Utilisation

1. Entrer le montant de l'addition dans le champ **Bill Amount**
2. Entrer le pourcentage de pourboire dans le champ **How was the service?**
3. Activer l'interrupteur si vous souhaitez arrondir le pourboire au dollar/euro supérieur
4. Le montant du pourboire s'affiche automatiquement en bas de l'écran

## Technologies utilisées

- **Kotlin**
- **Jetpack Compose** (UI déclarative)
- **Material 3**
- **State management** avec `remember` / `mutableStateOf`

## Pistes d'amélioration

- Validation des entrées (valeurs négatives, formats invalides)
- Ajout de préréglages de pourcentage de pourboire (ex : boutons 10% / 15% / 20%)
- Tests unitaires sur `calculateTip`
- Support de plusieurs devises indépendamment de la locale système

## Licence

Ce projet est fourni à des fins d'apprentissage (issu du cursus Android Basics with Compose).

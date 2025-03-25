# Projet d'Analyse et de Prédiction de la Consommation Électrique

## Auteurs
- **Cavaliere Luca**  
- **Alan Casasnovas**  
- **Arthur Da Costa Vieira**  

## Objectif du Projet
L’objectif principal de ce projet est d’analyser et de prédire la consommation électrique en région (exemple : Nouvelle-Aquitaine) à partir de données temporelles, tout en identifiant des anomalies potentielles. Les aspects clés incluent :

- **Visualisation** des tendances de consommation et de production énergétique.
- **Modélisation prédictive** pour anticiper la consommation horaire.
- **Détection d’anomalies** via des algorithmes non supervisés.
- **Explicabilité des modèles** pour comprendre les facteurs influençant la consommation.

---

## 📊 Résultats Clés

### 🔍 Analyse Exploratoire
- La consommation électrique présente des variations **journalières** (pics en journée) et **saisonnières** (hausse en hiver).
- Les **énergies renouvelables** (éolien, solaire) contribuent de manière significative mais sont variables selon les périodes.
- **Corrélations fortes** entre la consommation et la production thermique/nucléaire.

### 🤖 Modélisation Prédictive
- **Modèle utilisé :** Ridge Regression
- **Variables explicatives :** heure, jour de la semaine, production thermique
- **Performance du modèle sur la région Nouvelle-Aquitaine** :
  - **MAE (Erreur Absolue Moyenne) :** 655.66 MW
  - **RMSE (Racine de l’Erreur Quadratique Moyenne) :** 834.77 MW

### ⚠️ Détection d’Anomalies
- **Méthodes utilisées :** Isolation Forest et Local Outlier Factor
- **Résultats :** Environ **1% des données sont marquées comme anomalies** (consommation anormalement élevée ou faible).

### 📈 Visualisations Interactives
- Graphiques temporels (Plotly) montrant l’évolution de la consommation et des anomalies.
- Comparaison des sources de production énergétique avec des palettes de couleurs personnalisées.

---

## 📂 Sources Utilisées

### 📊 Dataset Principal
- **Nom du fichier :** `eco2mix-regional-tr.csv`
- **Source Officielle :** RTE (Réseau de Transport d’Électricité)
  - **Lien :** [Données ÉCO2Mix](https://odre.opendatasoft.com/explore/dataset/eco2mix-regional-tr/information/?utm_source=chatgpt.com&disjunctive.nature&disjunctive.libelle_region)
  - **Description :** Ce dataset contient des données horaires sur la consommation et la production électrique par région française, incluant :
    - **Consommation (MW)**
    - **Production par filière** : thermique, nucléaire, éolien, solaire, hydraulique, bioénergies
    - **Échanges commerciaux et taux de CO₂**
  - **Période Couverte :** Données mises à jour quotidiennement

### 🛠️ Librairies Python utilisées
- `pandas`, `numpy` pour la manipulation des données
- `scikit-learn` pour la modélisation et la détection d’anomalies
- `matplotlib`, `seaborn`, `plotly` pour les visualisations
- `prophet` pour l’analyse avancée de séries temporelles

---

## 🔑 Détails du Dataset
| **Colonne**          | **Description**                                           | **Type de Donnée** |
|----------------------|-------------------------------------------------------|------------------|
| `Date - Heure`       | Timestamp horaire (AAAA-MM-JJ HH:MM)                  | Datetime         |
| `Région`            | Région française (ex : Nouvelle-Aquitaine)            | Catégorielle     |
| `Consommation (MW)` | Consommation électrique totale                        | Numérique        |
| `Thermique (MW)`    | Production d’origine fossile (gaz, charbon)           | Numérique        |
| `Nucléaire (MW)`    | Production d’origine nucléaire                        | Numérique        |
| `Éolien (MW)`       | Production éolienne                                   | Numérique        |
| `Solaire (MW)`      | Production solaire                                    | Numérique        |
| `Hydraulique (MW)`  | Production hydroélectrique                            | Numérique        |
| `Bioénergies (MW)`  | Production à partir de biomasse                       | Numérique        |

---

## ⚙️ Traitement des Données
- **Nettoyage :** Gestion des valeurs manquantes via imputation médiane.
- **Feature Engineering :**
  - Création de **variables temporelles** (heure, jour de la semaine, weekend).
  - Calcul de la **part d’énergies renouvelables** dans la production totale.
- **Normalisation :** Standardisation des données pour les modèles ML.

---

## 🎯 Conclusion
Ce projet illustre comment l’**IA et l’analyse de données** peuvent éclairer les **décisions énergétiques**. Les modèles développés permettent **de prédire la consommation**, mais aussi **d’identifier des comportements anormaux**, facilitant une **gestion proactive des réseaux électriques**.

Les données **RTE** offrent une **base fiable et riche** pour des analyses approfondies, tout en nécessitant un **prétraitement rigoureux** pour garantir leur exploitation optimale.

---


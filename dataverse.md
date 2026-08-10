# Microsoft Dataverse — Résumé PL-900

## 1. Qu'est-ce que Dataverse ?

**Microsoft Dataverse** est la plateforme de données de Microsoft Power Platform.

Elle permet de :

* stocker des données métier ;
* structurer les données ;
* créer des relations entre les données ;
* appliquer des règles métier ;
* gérer la sécurité ;
* connecter les données à Power Apps, Power Automate, Power BI et Copilot Studio.

> **Dataverse = le socle de données de Power Platform.**

---

## 2. Les tables

Le principal élément de Dataverse est la **table**.

Une table contient :

* des **lignes (Rows)** → enregistrements ;
* des **colonnes (Columns)** → attributs.

### Exemple

```text
Table : Clients

| ID | Nom         | Email              | Ville |
|----|-------------|--------------------|-------|
| 1  | Jean Dupont | jean@email.com     | Lyon  |
| 2  | Marie Martin| marie@email.com    | Paris |
```

* **Table** → Clients
* **Row** → Jean Dupont
* **Column** → Email
* **Value** → [jean@email.com](mailto:jean@email.com)

---

## 3. Types de colonnes

Dataverse propose différents types de données :

* Texte
* Nombre
* Devise
* Date et heure
* Oui/Non
* Choix
* Lookup
* Image
* Fichier

### Exemple

```text
Client
├── Nom → Texte
├── Email → Texte
├── Date de naissance → Date
├── Actif → Oui/Non
└── Pays → Choix
```

---

## 4. Relations entre les tables

Dataverse permet de créer des relations entre les tables.

### 1:N — One-to-Many

Un enregistrement peut être associé à plusieurs enregistrements.

```text
1 Client
   │
   ├── Commande 1
   ├── Commande 2
   └── Commande 3
```

### N:1 — Many-to-One

Plusieurs enregistrements sont associés à un seul enregistrement.

```text
Commande 1 ─┐
Commande 2 ─┼──→ Client
Commande 3 ─┘
```

### N:N — Many-to-Many

Plusieurs enregistrements peuvent être associés à plusieurs autres.

```text
Étudiants ↔ Cours
```

> **PL-900 : connaître les concepts 1:N, N:1 et N:N.**

---

## 5. Lookup

Une colonne **Lookup** permet de référencer un enregistrement d'une autre table.

### Exemple

```text
Table : Commandes

Numéro
Montant
Client → Lookup vers la table Clients
```

La commande peut ainsi être associée à un client existant.

> **Lookup = référence vers une autre table.**

---

## 6. Clé primaire

Une clé primaire permet d'identifier de manière unique un enregistrement.

```text
Client

ID    Nom
001   Jean
002   Marie
003   Paul
```

Chaque enregistrement possède un identifiant unique.

---

## 7. Business Rules

Les **Business Rules** permettent d'appliquer une logique métier sans forcément écrire du code.

### Exemple

```text
Si Client = Professionnel
        ↓
Afficher "Numéro TVA"
```

Autre exemple :

```text
Si Statut = Inactif
        ↓
Désactiver certains champs
```

> **Business Rules = logique métier appliquée aux données.**

---

## 8. Sécurité

Dataverse permet de contrôler l'accès aux données.

Les principaux concepts sont :

* utilisateurs ;
* équipes ;
* rôles de sécurité ;
* permissions ;
* niveaux d'accès.

### Exemple

```text
Commercial
→ Lecture des clients

Manager
→ Lecture + modification

Administrateur
→ Accès étendu
```

> **Security Roles = contrôler qui peut accéder aux données et ce qu'il peut faire.**

---

## 9. Environnements

Dataverse fonctionne dans des **Power Platform environments**.

Exemple :

```text
Development
    ↓
   Test
    ↓
   UAT
    ↓
Production
```

Chaque environnement peut avoir ses propres :

* applications ;
* flows ;
* tables Dataverse ;
* données ;
* connexions ;
* configurations.

> **Environment = isolation des ressources.**

---

## 10. Dataverse + Power Apps

Power Apps peut utiliser Dataverse comme source de données.

```text
Utilisateur
     ↓
Power Apps
     ↓
Dataverse
```

Exemple :

Une application permet de gérer les clients.

```text
Power Apps
├── Nom
├── Email
├── Téléphone
└── Adresse
        ↓
   Dataverse
```

---

## 11. Dataverse + Power Automate

Power Automate peut lire et modifier les données Dataverse.

```text
Nouvelle ligne Dataverse
        ↓
Power Automate
        ↓
Créer une tâche
        ↓
Envoyer une notification
```

Ou :

```text
Demande
   ↓
Dataverse
   ↓
Power Automate
   ↓
Approval
   ↓
Mise à jour Dataverse
```

> **Dataverse stocke → Power Automate automatise.**

---

## 12. Dataverse + Power BI

Power BI peut analyser les données Dataverse.

```text
Dataverse
    ↓
Power BI
    ↓
Rapport
    ↓
Dashboard
```

Exemples :

* chiffre d'affaires ;
* ventes par commercial ;
* ventes par produit ;
* évolution mensuelle.

> **Dataverse = stockage → Power BI = analyse.**

---

## 13. Dataverse + Model-driven Apps

Les **Model-driven Apps** sont fortement basées sur Dataverse.

```text
Dataverse
    ↓
Tables
    ↓
Relations
    ↓
Formulaires
    ↓
Vues
    ↓
Model-driven App
```

### À comparer

| Canvas App                     | Model-driven App                         |
| ------------------------------ | ---------------------------------------- |
| Interface très personnalisable | Interface basée sur le modèle de données |
| Contrôle des écrans            | Génération basée sur Dataverse           |
| Très flexible                  | Adaptée aux processus métier complexes   |

> **Model-driven Apps → Dataverse est central.**

---

## 14. Solutions

Les **Solutions** permettent de regrouper et transporter des composants Power Platform.

Une solution peut contenir :

```text
Solution
├── Tables Dataverse
├── Colonnes
├── Applications
├── Power Automate flows
├── Business Rules
└── autres composants
```

Elles sont importantes pour l'**ALM (Application Lifecycle Management)**.

### Exemple

```text
Development
      ↓
   Solution
      ↓
     Test
      ↓
   Solution
      ↓
  Production
```

> **Solution = packaging + transport + déploiement des composants.**

---

## 15. Dataverse vs Excel

### Excel

Adapté à :

* petits volumes ;
* calculs ;
* analyses individuelles ;
* feuilles de calcul.

### Dataverse

Adapté à :

* applications métier ;
* données relationnelles ;
* sécurité ;
* processus métier ;
* intégration Power Platform ;
* plusieurs utilisateurs.

> Application métier complexe → **Dataverse** est généralement plus adapté qu'Excel.

---

## 16. Dataverse vs SharePoint Lists

### SharePoint Lists

Adaptées notamment à :

* listes simples ;
* collaboration Microsoft 365 ;
* données relativement simples.

### Dataverse

Adapté notamment à :

* données métier structurées ;
* relations entre tables ;
* sécurité avancée ;
* logique métier ;
* applications Power Platform.

---

# 🧠 Tableau PL-900

| Concept              | À retenir                              |
| -------------------- | -------------------------------------- |
| **Dataverse**        | Stockage et gestion des données métier |
| **Table**            | Structure contenant les données        |
| **Row**              | Enregistrement                         |
| **Column**           | Attribut                               |
| **Lookup**           | Référence vers une autre table         |
| **Relationship**     | Relation entre tables                  |
| **1:N**              | Un vers plusieurs                      |
| **N:N**              | Plusieurs vers plusieurs               |
| **Business Rule**    | Logique métier                         |
| **Security Role**    | Contrôle des permissions               |
| **Environment**      | Isolation des ressources               |
| **Solution**         | Packaging et déploiement               |
| **Power Apps**       | Crée les applications                  |
| **Power Automate**   | Automatise les processus               |
| **Power BI**         | Analyse les données                    |
| **Model-driven App** | Application basée sur Dataverse        |

---

# 🎯 Schéma à mémoriser

```text
                    ┌──────────────┐
                    │  POWER APPS  │
                    └──────┬───────┘
                           │
                           ↓
                    ┌──────────────┐
                    │  DATAVERSE   │
                    │              │
                    │    TABLES    │
                    │    ROWS      │
                    │   COLUMNS    │
                    │  RELATIONS   │
                    └──────┬───────┘
                           │
             ┌─────────────┼─────────────┐
             ↓             ↓             ↓
      Power Automate   Power BI   Copilot Studio
             │             │             │
       Automatisation   Analyse          IA
```

# ⭐ Les 5 points à absolument retenir

1. **Dataverse = données**
2. **Table = structure de données**
3. **Lookup = relation/référence entre tables**
4. **Security Roles = contrôle des accès**
5. **Solutions = gestion et déploiement des composants**

## 🏆 Phrase PL-900

> **Power Apps crée l'application → Dataverse stocke les données → Power Automate automatise → Power BI analyse.**

**Dataverse = plateforme de données sécurisée et relationnelle de Power Platform.**

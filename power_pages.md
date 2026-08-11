# 🌐 Power Pages — Résumé PL-900

## 1. Qu'est-ce que Power Pages ?

**Microsoft Power Pages** permet de créer des **sites web métier** accessibles à des utilisateurs internes ou externes à l'organisation.

Exemples :

* portail client ;
* portail fournisseur ;
* portail partenaire ;
* site de support ;
* formulaire public ;
* espace de self-service.

> **Power Pages = créer des sites web métier accessibles depuis un navigateur.**

---

# 2. À quoi sert Power Pages ?

Power Pages est particulièrement adapté lorsque des personnes doivent **consulter ou saisir des données métier via un site web**.

### Exemple

Une entreprise possède des clients externes.

```text
Client
   ↓
Power Pages
   ↓
Formulaire
   ↓
Dataverse
```

Le client peut :

* consulter ses informations ;
* créer une demande ;
* modifier certaines données ;
* suivre l'état d'une demande.

Les données peuvent être stockées dans **Dataverse**.

---

# 3. Power Pages + Dataverse

C'est une association très importante pour la PL-900.

```text
                    ┌──────────────┐
                    │ Power Pages  │
                    │    Site Web  │
                    └──────┬───────┘
                           ↓
                    ┌──────────────┐
                    │  Dataverse   │
                    │    Tables    │
                    └──────────────┘
```

Power Pages fournit principalement **l'expérience web**.

Dataverse fournit principalement **les données métier**.

### Exemple

```text
Client
  ↓
Portail Power Pages
  ↓
"Créer une demande"
  ↓
Dataverse
  ↓
Nouvelle ligne dans la table Demandes
```

---

# 4. Utilisateurs internes vs externes

Power Pages est particulièrement intéressant pour les **utilisateurs externes**.

### Exemple

Une entreprise crée un portail pour ses clients :

```text
Client externe
      ↓
Power Pages
      ↓
Consulter ses commandes
      ↓
Dataverse
```

Il n'est donc pas nécessaire que tous les utilisateurs soient des employés utilisant directement les applications internes de l'entreprise.

### Exemples d'utilisateurs

* clients ;
* fournisseurs ;
* partenaires ;
* citoyens ;
* utilisateurs externes.

---

# 5. Sites web

Power Pages permet de créer des sites web avec notamment :

* pages ;
* navigation ;
* formulaires ;
* listes ;
* contenu ;
* authentification ;
* autorisations.

Le site peut être personnalisé selon les besoins de l'organisation.

---

# 6. Pages

Une **page web** constitue une partie du site.

Exemple :

```text
Portail client
│
├── Accueil
├── Mon profil
├── Mes commandes
├── Nouvelle demande
└── Contact
```

Chaque page peut présenter du contenu ou permettre d'interagir avec les données.

---

# 7. Forms — Formulaires

Les formulaires permettent aux utilisateurs de **consulter ou saisir des données**.

Exemple :

```text
Nouvelle demande

Nom :        Jean Dupont
Email :      jean@email.com
Sujet :      Problème de livraison
Description: ...
                 ↓
              Envoyer
```

Les informations peuvent ensuite être enregistrées dans Dataverse.

> **Form = interface permettant de saisir ou consulter des données.**

---

# 8. Lists — Listes

Les listes permettent d'afficher plusieurs enregistrements provenant notamment de Dataverse.

Exemple :

```text
Mes demandes

ID     Sujet                 Statut
001    Livraison             Ouverte
002    Facture               Résolue
003    Produit défectueux    En cours
```

L'utilisateur peut ainsi consulter les données qui lui sont accessibles.

---

# 9. Sécurité

La sécurité est une notion **très importante** dans Power Pages.

Il faut contrôler quelles données les utilisateurs peuvent voir ou modifier.

Exemple :

```text
Client A
   ↓
Power Pages
   ↓
Voir uniquement ses demandes
```

Le client A ne doit pas pouvoir consulter les demandes du client B.

Power Pages utilise notamment :

* authentification ;
* permissions ;
* web roles ;
* table permissions.

---

# 10. Web Roles

Les **Web Roles** permettent d'associer des utilisateurs à des rôles sur le site.

Exemple :

```text
Client
   ↓
Web Role : Customer

Fournisseur
   ↓
Web Role : Supplier

Administrateur
   ↓
Web Role : Administrator
```

Les rôles permettent de déterminer ce que les utilisateurs peuvent faire sur le site.

---

# 11. Table Permissions

Les **Table Permissions** permettent de contrôler l'accès aux données Dataverse depuis Power Pages.

Exemple :

```text
Utilisateur
     ↓
Power Pages
     ↓
Table Permissions
     ↓
Dataverse
```

On peut contrôler les opérations telles que :

* Read ;
* Create ;
* Write ;
* Delete.

### Exemple

```text
Client

Read   → ✅
Create → ✅
Write  → ✅
Delete → ❌
```

Le client peut donc consulter et créer certaines données, mais ne peut pas les supprimer.

> **Table Permissions = contrôle de l'accès aux données Dataverse depuis Power Pages.**

---

# 12. Authentification

Power Pages peut permettre aux utilisateurs de **s'authentifier**.

Exemple :

```text
Utilisateur
     ↓
Login
     ↓
Power Pages
     ↓
Accès personnalisé
```

L'authentification permet ensuite d'appliquer les permissions correspondant à l'utilisateur.

---

# 13. Anonymous access

Un site Power Pages peut également exposer certaines informations publiquement selon sa configuration.

Exemple :

```text
Internet
   ↓
Power Pages
   ↓
Page publique
```

Mais les données sensibles doivent être protégées par les mécanismes de sécurité appropriés.

🎯 **PL-900 :**

Ne pas confondre :

* **site accessible publiquement** ;
* **données accessibles publiquement**.

Les permissions déterminent ce que l'utilisateur peut réellement consulter ou modifier.

---

# 14. Power Pages + Power Automate

Power Pages peut être combiné avec Power Automate.

Exemple :

```text
Client
  ↓
Power Pages
  ↓
Créer une demande
  ↓
Dataverse
  ↓
Power Automate
  ↓
Notification
  ↓
Équipe support
```

Cela permet de créer des processus métier complets.

---

# 15. Power Pages + Power BI

Power Pages peut également être intégré dans des scénarios d'analyse.

Exemple :

```text
Dataverse
    ↓
Power BI
    ↓
Rapport
    ↓
Power Pages
```

Cela peut permettre d'afficher certaines informations analytiques dans un portail, selon les besoins et la configuration.

---

# 16. Power Pages vs Power Apps

C'est une comparaison importante.

| Power Apps                           | Power Pages                       |
| ------------------------------------ | --------------------------------- |
| Applications métier                  | Sites web métier                  |
| Utilisateurs internes principalement | Utilisateurs internes ou externes |
| Canvas Apps                          | Sites web                         |
| Model-driven Apps                    | Portails / sites                  |
| Interface applicative                | Expérience web                    |
| Dataverse possible                   | Dataverse très important          |

### Exemple

**Application interne pour les employés :**

→ Power Apps

**Portail permettant aux clients de suivre leurs demandes :**

→ Power Pages

---

# 17. Power Pages vs SharePoint

Il ne faut pas les confondre.

### SharePoint

Très adapté à :

* collaboration ;
* documents ;
* intranet ;
* listes ;
* partage de contenu.

### Power Pages

Très adapté à :

* portails métier ;
* utilisateurs externes ;
* interaction avec les données métier ;
* self-service ;
* scénarios basés sur Dataverse.

---

# 18. Design Studio

Power Pages fournit des outils permettant de construire et personnaliser les sites avec une approche **low-code**.

Le **Design Studio** permet notamment de travailler sur :

* les pages ;
* la navigation ;
* le style ;
* les données ;
* les formulaires ;
* les listes.

L'objectif est de permettre la création d'un site sans devoir développer entièrement celui-ci en code traditionnel.

---

# 19. Cas d'utilisation typiques

### 🧑‍💼 Portail client

```text
Client
 ↓
Power Pages
 ↓
Consulter commandes
 ↓
Dataverse
```

### 🛠️ Portail support

```text
Client
 ↓
Créer ticket
 ↓
Power Pages
 ↓
Dataverse
 ↓
Power Automate
 ↓
Équipe support
```

### 🏢 Portail fournisseur

```text
Fournisseur
 ↓
Power Pages
 ↓
Informations fournisseur
 ↓
Dataverse
```

### 🏛️ Formulaire public

```text
Citoyen
 ↓
Power Pages
 ↓
Formulaire
 ↓
Dataverse
```

---

# 🧠 Tableau PL-900

| Concept              | À retenir                              |
| -------------------- | -------------------------------------- |
| **Power Pages**      | Création de sites web métier           |
| **Site**             | Portail web                            |
| **Page**             | Page du site                           |
| **Form**             | Saisie / consultation de données       |
| **List**             | Affichage de plusieurs enregistrements |
| **Dataverse**        | Stockage des données métier            |
| **Web Role**         | Rôle de l'utilisateur sur le site      |
| **Table Permission** | Contrôle de l'accès aux données        |
| **Authentication**   | Identification de l'utilisateur        |
| **Power Automate**   | Automatisation des processus           |
| **Power Apps**       | Applications métier                    |
| **Power BI**         | Analyse et visualisation               |

---

# 🎯 Schéma à mémoriser

```text
                 UTILISATEUR
                      ↓
              ┌───────────────┐
              │  POWER PAGES  │
              │    SITE WEB   │
              └───────┬───────┘
                      ↓
             Authentification
                      ↓
                Web Roles
                      ↓
             Table Permissions
                      ↓
              ┌───────────────┐
              │   DATAVERSE   │
              │    TABLES     │
              └───────┬───────┘
                      ↓
             Power Automate
                      ↓
              Processus métier
```

# ⭐ Les 7 points à absolument retenir

1. **Power Pages = sites web métier**
2. **Utilisateurs internes ET externes**
3. **Dataverse = données derrière le portail**
4. **Forms = saisir/consulter des données**
5. **Lists = afficher plusieurs enregistrements**
6. **Web Roles + Table Permissions = sécurité**
7. **Power Automate = automatiser les processus déclenchés autour du portail**

# 🏆 Phrase PL-900

> **Power Pages permet de créer des sites web métier low-code donnant aux utilisateurs internes ou externes un accès contrôlé aux données et processus de l'organisation.**

## 🔥 Mémo ultra-court

```text
Power Pages → SITE WEB
Dataverse   → DONNÉES
Web Roles   → RÔLES
Permissions → ACCÈS
Forms       → SAISIE
Lists       → AFFICHAGE
Power Automate → AUTOMATISATION
```

### Question type PL-900

**Une entreprise veut permettre à ses clients externes de consulter leurs demandes et d'en créer de nouvelles depuis un navigateur. Quelle technologie utiliser ?**

✅ **Power Pages + Dataverse**

❌ Power BI → analyse de données
❌ Power Automate → automatisation
❌ Power Apps → application métier
❌ Copilot Studio → agent conversationnel

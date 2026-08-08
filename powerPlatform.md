
# Microsoft Power Platform — Résumé

## Qu'est-ce que Power Platform ?

Microsoft Power Platform est une plateforme **low-code/no-code** qui permet de créer des applications, automatiser des processus, analyser des données et développer des assistants intelligents avec peu ou pas de développement traditionnel.

Elle s'intègre nativement avec **Microsoft 365**, **Azure**, **Dynamics 365** ainsi qu'à de nombreux services tiers via des connecteurs.

---

# Les composants principaux

## Power BI

Power BI est l'outil de **Business Intelligence** de Microsoft.

Il permet de :

* connecter plusieurs sources de données ;
* transformer les données avec Power Query ;
* modéliser les données ;
* créer des tableaux de bord interactifs ;
* partager des rapports au sein de l'entreprise.

Cas d'usage :

* suivi des ventes ;
* indicateurs métiers ;
* tableaux de bord financiers ;
* reporting RH.

---

## Power Apps

Power Apps permet de créer rapidement des applications métier sans développer une application complète en code.

Deux principaux types d'applications :

### Canvas Apps

* Interface entièrement personnalisable.
* Le développeur contrôle chaque écran.
* Idéal pour les applications mobiles et métiers.

### Model-driven Apps

* Interface générée automatiquement à partir des données.
* Basées sur Microsoft Dataverse.
* Adaptées aux processus métiers complexes.

---

## Power Automate

Power Automate permet d'automatiser des tâches répétitives.

Exemples :

* envoyer un e-mail lorsqu'un fichier est ajouté dans SharePoint ;
* approuver automatiquement une demande de congés ;
* copier des données entre plusieurs applications ;
* déclencher des workflows.

Types de flux :

* Automated Cloud Flow
* Instant Cloud Flow
* Scheduled Cloud Flow
* Desktop Flow (RPA)

---

## Power Pages

Power Pages permet de créer des sites web sécurisés accessibles aux utilisateurs internes ou externes.

Utilisations :

* portail client ;
* portail fournisseur ;
* portail partenaire ;
* formulaires publics.

---

## Microsoft Copilot Studio

Copilot Studio permet de créer des assistants conversationnels et des agents d'IA personnalisés.

Fonctionnalités :

* conception de chatbots ;
* intégration avec Microsoft Teams ;
* utilisation de l'IA générative ;
* automatisation via Power Automate ;
* connexion aux données métier.

Depuis les dernières mises à jour, Copilot Studio remplace progressivement Power Virtual Agents.

---

# Microsoft Dataverse

Dataverse est la base de données relationnelle de Power Platform.

Il fournit :

* stockage sécurisé des données ;
* tables relationnelles ;
* règles métier ;
* sécurité basée sur les rôles ;
* API et intégrations.

Dataverse constitue le socle de nombreuses applications Power Platform.

---

# Les connecteurs

Les connecteurs permettent de communiquer avec des services externes.

Exemples :

* Microsoft 365
* SharePoint
* Outlook
* SQL Server
* Azure
* Salesforce
* SAP
* GitHub
* Dropbox

Deux catégories :

* Connecteurs standard
* Connecteurs premium (licence supplémentaire)

Il est également possible de créer des **connecteurs personnalisés** pour des API REST.

---

# AI Builder

AI Builder permet d'ajouter facilement de l'intelligence artificielle dans les applications et les flux.

Exemples :

* reconnaissance de documents ;
* lecture de factures ;
* analyse de sentiments ;
* prédictions ;
* extraction de texte.

Aucune expertise en Machine Learning n'est nécessaire.

---

# Sécurité

Power Platform s'appuie sur plusieurs mécanismes :

* Microsoft Entra ID pour l'authentification ;
* rôles de sécurité ;
* environnements (Development, Test, Production) ;
* prévention contre la perte de données (Data Loss Prevention Policies) ;
* gestion des licences.

---

# Environnements

Les environnements permettent d'isoler les ressources.

On retrouve généralement :

* Development
* Test
* UAT
* Production

Chaque environnement possède :

* ses applications ;
* ses flux ;
* ses connexions ;
* sa base Dataverse ;
* ses politiques de sécurité.

---

# Low-code vs No-code

**Low-code**

* Quelques expressions ou formules.
* Personnalisation avancée.
* Destiné aux développeurs et utilisateurs avancés.

**No-code**

* Création entièrement graphique.
* Aucune programmation.
* Destiné aux utilisateurs métier (Citizen Developers).

---

# Cas d'utilisation

Power Platform est adaptée à :

* la dématérialisation de formulaires ;
* l'automatisation des processus métier ;
* la création d'applications internes ;
* les tableaux de bord décisionnels ;
* les portails clients ;
* les assistants IA.

---

# Points clés pour la PL-900

À retenir :

* **Power BI** → Analyse et visualisation des données.
* **Power Apps** → Création d'applications métier.
* **Power Automate** → Automatisation des processus.
* **Power Pages** → Création de portails web.
* **Copilot Studio** → Création d'agents conversationnels et assistants IA.
* **Dataverse** → Stockage et gestion des données.
* **AI Builder** → Ajout de fonctionnalités d'IA sans développement ML.
* **Connecteurs** → Intégration avec Microsoft et des services tiers.
* **Environnements** → Isolation des ressources et gestion du cycle de vie.
* **DLP Policies** → Protection des données entre les connecteurs.

La PL-900 évalue principalement la compréhension des cas d'usage de chaque composant, de leur intégration et des scénarios dans lesquels ils sont les plus adaptés.

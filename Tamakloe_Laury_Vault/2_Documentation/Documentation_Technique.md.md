
## 🧠 Justification du choix d'Obsidian

Le choix d'**Obsidian** répond à une volonté de structurer ma recherche de manière dynamique et rigoureuse :

- **Pensée en réseau** : Grâce aux liens bidirectionnels (backlinks), j'ai relié mes recherches théoriques (ONISEP/CIDJ) à mes enquêtes de terrain (Mazars/UJM). Mon **Canvas** visualise ce maillage entre compétences et métiers.
- **Automatisation (Dataview)** : L'utilisation de métadonnées YAML permet de générer des tableaux comparatifs de salaires qui s'actualisent automatiquement selon mes sources.
- **Littérate Programming** : Le format Markdown permet de faire cohabiter mes analyses textuelles et mes scripts de **scraping R**. Le Vault devient un outil _stand-alone_ où la méthode technique est aussi documentée que le contenu.

## 1. Organisation du Projet
Le projet est structuré pour répondre aux critères de la grille d'évaluation de l'Université Jean Monnet.
- **01_Documentation** : Contient le `Readme.md` qui définit la problématique de recherche sur les salaires.
- **02_fiche_metier** : Notes structurées avec des propriétés YAML pour l'extraction de données.
- **03_Entretiens** : Comptes-rendus liant la théorie à la réalité du terrain.
- **06_Attachements** : Notes de synthèse et bilans personnels.

## 2. Choix Techniques (Critère 2)
J'ai utilisé plusieurs outils avancés pour enrichir ce travail :
- **Dataview** : Ce plugin permet de générer automatiquement un tableau comparatif (`Synthese_Salariale.md`) à partir des métadonnées de mes fiches métiers.
- **Backlinks** : J'ai créé un réseau de liens internes entre les métiers et les entretiens professionnels (ex: [[Actuaire]] ↔ [[Entretien_Agbedjinou]]).
- **LaTeX** : Utilisé pour la mise en forme de concepts mathématiques et de rapports scientifiques, conformément aux attentes du métier d'enseignant-chercheur.


## 🗺️3. Modélisation visuelle via Obsidian Canvas

En complément de l'organisation par dossiers, j'ai utilisé l'outil **Canvas** (`tableau_de_bord.canvas`) pour créer une cartographie interactive de mon projet.

### Pourquoi utiliser le Canvas ?

- **Visualisation de l'architecture** : Il permet de voir d'un seul coup d'œil les connexions entre la problématique initiale, les fiches métiers et les preuves de terrain (entretiens).
    
- **Navigation intuitive** : Chaque nœud du Canvas est un lien direct vers la note correspondante, facilitant l'exploration du Vault pour l'évaluateur.
    
- **Complémentarité avec Excalidraw** : Alors qu'Excalidraw modélise ma réflexion logique, le Canvas sert de structure physique montrant comment les fichiers sont réellement liés dans mon système de connaissances.


## 4. Méthodologie de Recherche (Scraping)
Conformément à ma problématique, j'ai exploré des sources numériques variées :
- **Sources institutionnelles** : CIDJ et ONISEP pour les données de référence.
- **Webscraping manuel** : Extraction de données salariales depuis l'Institut des Actuaires et Glassdoor pour comparer les écarts de rémunération.

L'analyse comparative a été automatisée sous **R** via le package `pdftools`. Ce script a permis d'isoler la page 17 de l'enquête de l'Institut des Actuaires pour extraire les moyennes salariales par niveau d'ancienneté, facilitant ainsi la mise à jour de mes fiches métiers.

![[Pasted image 20251223030132.png]]

Pour répondre à ma problématique sur la fiabilité des données salariales, j'ai automatisé la collecte d'informations via le langage **R**. Cette démarche se décompose en deux axes techniques :

- **Extraction Web (rvest)** : J'ai utilisé la bibliothèque `rvest` pour extraire le texte des balises HTML `<p>` sur des sites comme Superprof. Cette méthode permet de récupérer rapidement les paragraphes traitant de la rémunération sans saisie manuelle.
- **Extraction PDF (pdftools)** : Pour l'enquête de l'**Institut des Actuaires 2024**, j'ai employé `pdftools` afin de cibler précisément la page 17, isolant ainsi les données de salaires moyens (92k€) directement depuis le document source.
- **Fiabilisation des données** : Les scripts incluent des fonctions de formatage (YAML) pour transformer les données brutes en propriétés exploitables par mon plugin **Dataview**.
Cette approche garantit que les chiffres présentés dans mon tableau comparatif sont issus de sources vérifiables et reproductibles.


## 🚀 Procédure de Publication et Versioning

Pour garantir l'accessibilité, la pérennité et la transparence de mon travail, j'ai mis en place une procédure de publication professionnelle utilisant le versioning.

### 1. Choix de la plateforme

J'ai sélectionné **GitHub** pour héberger mon Vault Obsidian. Cette plateforme permet une consultation claire des fichiers Markdown et conserve l'historique complet de mes modifications.

### 2. Étapes techniques de mise en ligne

- **Initialisation** : Création d'un dépôt local via Git pour suivre l'évolution des fichiers.
    
- **Nettoyage** : Vérification de la structure des dossiers (00 à 05) pour une navigation fluide.
    
- **Synchronisation** : Utilisation de `Git push` pour envoyer le contenu local vers le serveur distant.
    
- **Accessibilité** : Configuration du dépôt en mode "Public" pour permettre l'évaluation.
    

### 3. Lien d'accès au projet

Le Vault complet est consultable à l'adresse suivante :

> [!info] Publication & Versioning
> Le projet est hébergé et versionné sur GitHub pour garantir la transparence de la démarche scientifique.
> **Lien direct :** [Cliquez ici pour consulter le dépôt](https://github.com/laurytamakloe-create/Tamaklo_Laury_Vault)
### 4. Suivi des modifications (Versioning)

Conformément aux critères de réflexivité, chaque étape majeure (intégration du scraping R, création du Canvas, rédaction des entretiens) a fait l'objet d'un "commit" spécifique. Cela prouve l'authenticité du travail et la progression de la réflexion sur le semestre


## 📝 Conclusion et Réflexion Finale

Ce projet m'a permis de confronter ma vision initiale de l'actuariat à la réalité du terrain.
- **Synthèse des écarts** : L'analyse a révélé des disparités entre les sources institutionnelles (3 300 € brut selon l'ONISEP) et la réalité des cabinets de conseil (51k€/an chez Mazars), soulignant l'importance du secteur d'activité.
- **Validation du projet professionnel** : L'entretien avec M. Agbedjinou a confirmé mon attrait pour la dimension technique et la forte responsabilité du métier d'**Actuaire**, malgré les contraintes de charge de travail identifiées.
- **Compétences acquises** : Au-delà des connaissances métiers, ce travail a renforcé ma maîtrise d'outils d'ingénierie numérique (Obsidian, R, Dataview), essentiels pour ma future carrière en économie quantitative.
# TP Conception d'une application avec UML - Fromagerie DigiCheese

**Auteur :** Baptiste Rouault  
**Formation :** M1 CYBER-RESSOURCE  
**TP :** Conception d'une application avec UML  
**Version :** 1.2  

## 📋 Description

Ce projet contient les livrables du TP de conception d'application avec UML pour la fromagerie DigiCheese. L'objectif est de modéliser une application de gestion pour une fromagerie en utilisant les différents diagrammes UML.

## 🎯 Livrable principal

**📊 PowerPoint de présentation**  
`baptiste-rouault_powerpoint_fromagerie_digicheese_v1.pptx`  
*Document le plus important - Présentation complète du projet*

## 📁 Structure du projet

```
fromagerie_digicheese_baptiste_rouault/
├── README.md                                    # Ce fichier
├── .gitignore                                   # Fichiers ignorés par Git
├── 📊 baptiste-rouault_powerpoint_fromagerie_digicheese_v1.pptx  # Présentation principale
├── 📄 01_acteurs_roles.md                       # Identification des acteurs et rôles
├── 📄 04_scenario_gestion_colis.md              # Scénario de gestion des colis
├── 📁 puml/                                     # Fichiers source PlantUML
│   ├── 02_architecture.puml                     # Diagramme d'architecture
│   ├── 03_use_cases.puml                        # Diagramme des cas d'utilisation
│   ├── 05_activity.puml                         # Diagramme d'activité
│   ├── 06_sequence.puml                         # Diagramme de séquence
│   └── 07_class_diagram.puml                    # Diagramme de classes (v1.2 avec Emplacements)
└── 📁 images/                                   # Images des diagrammes générés
    ├── 02_architecture.png                      # Architecture système
    ├── 02_architecture_blanc.png                # Architecture (version blanche)
    ├── 03_use_cache.png                         # Cas d'utilisation
    ├── 05_activity.png                          # Diagramme d'activité
    ├── 05_activityback.png                      # Diagramme d'activité (backup)
    ├── 06_sequence.png                          # Diagramme de séquence
    ├── 07_class_diagram.png                     # Diagramme de classes
    └── architecture.png                         # Architecture (version alternative)
```

## 📐 Diagrammes UML réalisés

1. **🎭 Diagramme des acteurs et rôles** - Identification des différents acteurs du système
2. **🏗️ Diagramme d'architecture** - Vue globale de l'architecture système (client léger / intranet)
3. **📋 Diagramme des cas d'utilisation** - Fonctionnalités principales du système
4. **⚡ Diagramme d'activité** - Flux de processus métier (gestion des colis)
5. **🔄 Diagramme de séquence** - Interactions entre les composants
6. **🏛️ Diagramme de classes** - Structure des données et relations (v1.2 avec Emplacements)

## 🛠️ Technologies utilisées

- **📊 PlantUML** - Génération des diagrammes UML
- **📝 Markdown** - Documentation technique
- **💾 Git** - Versioning et suivi des modifications
- **🎯 PowerPoint** - Présentation finale du projet

## ⚙️ Compilation des diagrammes

Pour générer les diagrammes à partir des fichiers PlantUML :

```bash
# Installation de PlantUML (si nécessaire)
# Utiliser un éditeur supportant PlantUML comme VS Code avec l'extension PlantUML
# Ou utiliser la ligne de commande :
java -jar plantuml.jar puml/*.puml
```

## 📊 Consultation du projet

**🎯 Document prioritaire à consulter :**
- `baptiste-rouault_powerpoint_fromagerie_digicheese_v1.pptx` - Présentation complète du projet

**📁 Documentation technique :**
- `01_acteurs_roles.md` - Analyse des acteurs et leurs responsabilités
- `04_scenario_gestion_colis.md` - Scénario détaillé de gestion des colis

**🖼️ Diagrammes générés :**
- Dossier `images/` - Tous les diagrammes UML au format PNG

## 👨‍💻 Auteur

**Baptiste Rouault**  
Étudiant en M1 CYBER-RESSOURCE  
TP de Conception d'une application avec UML  
📧 Contact : [disponible sur demande]

---

**🔗 Repository GitHub :** https://github.com/RouaultBaptiste/uml-projet

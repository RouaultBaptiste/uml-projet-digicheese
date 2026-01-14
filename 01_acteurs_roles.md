# DIGICHEESE — Acteurs & rôles (périmètre **gestion des colis**)  
Référence : *LA FROMAGERIE DIGICHEESE V1.0*.

## 1) Acteurs principaux (internes)

### A1 — Opérateur colis (rôle métier principal)
**Mission :** gérer le cycle de vie des commandes/colis, depuis la création de commande jusqu’à l’envoi.  
**Droits (fonctionnels) :**
- Créer / rechercher / modifier un **client**
- Créer / modifier une **commande**
- Ajouter / retirer des **lignes de commande (objets)**
- Lancer le **calcul de conditionnement** (choix emballage selon règles min/max)
- Lancer le **calcul d’affranchissement** (poids total → tarif)
- Saisir / associer un **numéro de suivi** (Lettre suivie) et mettre à jour le **statut**
- Consulter et alimenter l’**historique** (mouvements / événements)
- Générer impressions (bon de préparation, liste d’expédition, etc.)
- Envoyer des **emails** (notification / info client)
- Export **mailing** (fichier texte) si prévu par l’organisation

**Responsabilités :**
- Assurer la cohérence « commande ↔ colis ↔ suivi ↔ statut »
- Contrôler le poids (articles + emballage) avant affranchissement

---

### A2 — Opérateur stock
**Mission :** gérer les stocks d’objets/goodies et disponibilités.  
**Droits :**
- Consulter **catalogue objets**
- Consulter / mettre à jour **stock**
- Réaliser inventaire / ajustements
- Consulter commandes (lecture) pour anticiper la préparation

**Responsabilités :**
- Garantir la disponibilité des objets et la fiabilité des quantités

---

### A3 — Administrateur (administration fonctionnelle)
**Mission :** paramétrer l’application et les référentiels.  
**Droits :**
- Gérer **utilisateurs** et **profils** (droits)
- Gérer **référentiels** : objets, catégories, emplacements, enseignes (si utilisés)
- Gérer **emballages** et **règles de conditionnement** (min/max par objet ou groupe d’objets)
- Gérer **tarifs postaux** (tranches de poids, prix)
- Paramétrer modèles d’email, exports, impressions

**Responsabilités :**
- Maintenir à jour les règles métier (conditionnement / affranchissement)

---

### A4 — Direction / Manager (consultation)
**Mission :** piloter l’activité via indicateurs.  
**Droits :**
- Accéder aux **statistiques** (par mois/année, volumes, coûts, etc.)
- Exporter rapports
- Lecture seule sur clients/commandes (selon politique)

**Responsabilités :**
- Analyse & reporting

---

## 2) Acteurs externes (hors SI, mais influencent le flux)

### E1 — Client final (expéditeur du chèque / points / choix cadeaux)
**Rôle :** déclenche l’existence d’une commande.  
**Interactions :** indirectes (saisie par opérateur), réception d’email/suivi.

---

### E2 — La Poste / Service d’expédition
**Rôle :** fournit les règles de prix (tarifs) et le suivi “Lettre suivie”.  
**Interactions :**
- Consultation des **tranches de poids** et **tarifs** (paramétrés ou synchronisés)
- Enregistrement / utilisation d’un **numéro de suivi**

---

## 3) Profils & matrice de droits (résumé)
| Fonctionnalité | Opérateur colis | Opérateur stock | Admin | Direction |
|---|---:|---:|---:|---:|
| Gérer clients |(lecture possible) | (lecture) |
| Gérer commandes/colis (lecture) | (lecture) |
| Conditionnement / affranchissement |  (paramétrage) |
| Stocks | (lecture) |
| Paramétrage (objets/emballages/tarifs)  |
| Statistiques / rapports | (selon besoin) |  (selon besoin) | 

Légende :  autorisé /  limité /  non autorisé

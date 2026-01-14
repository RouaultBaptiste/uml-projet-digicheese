# DIGICHEESE — Scénario “Gestion des colis” (texte)

## Préconditions
- L’utilisateur (opérateur colis) est **authentifié** et dispose du rôle “Opérateur colis”.
- Les référentiels sont en place : **objets**, **emballages**, **règles min/max**, **tarifs postaux**.

## Déclencheur
- Une demande arrive (ex. choix cadeaux/points/chèque) → l’opérateur doit créer ou compléter une commande et expédier.

## Scénario nominal (happy path)
1. **Rechercher ou créer le client**
   - L’opérateur cherche le client (nom/email/code client).
   - Si absent, il crée la fiche client (coordonnées, email, newsletter…).
2. **Créer une commande**
   - L’opérateur crée une commande liée au client (date, commentaires, statut initial “À préparer”).
3. **Ajouter les lignes de commande (objets)**
   - L’opérateur ajoute les objets/goodies et quantités.
4. **Calculer le conditionnement**
   - Le système sélectionne un **emballage** adapté, en respectant les **règles min/max** (quantités/compatibilités).
   - Si aucune solution n’est trouvée : alerte et proposition d’alternatives (changement emballage, scinder en plusieurs colis).
5. **Calculer le poids total**
   - Poids total = somme(poids objets * quantités) + poids emballage.
6. **Calculer l’affranchissement**
   - Le système identifie la **tranche de poids** et le **tarif postal** correspondant.
7. **Finaliser l’expédition**
   - L’opérateur saisit ou associe le **numéro de suivi (Lettre suivie)**.
   - Le statut passe à “Expédié” (ou “Affranchi” puis “Expédié” selon politique).
   - Le système enregistre un événement d’historique.
8. **Impressions / notifications**
   - L’opérateur imprime les documents nécessaires.
   - Le système envoie un email au client (optionnel) avec le suivi.

## Extensions / erreurs
- **Client incomplet** : champs manquants → blocage ou avertissement (selon règles).
- **Conditionnement impossible** : aucun emballage compatible → proposer scission en plusieurs colis ou choix manuel.
- **Tarif postal absent** : aucune tranche correspondante → avertir l’admin (paramétrage).
- **N° de suivi non fourni** : expédition possible mais suivi absent → statut “Expédié sans suivi”.

## Postconditions
- Commande/colis enregistrés avec statut à jour.
- Historique alimenté.
- Affranchissement calculé, n° de suivi éventuellement associé.

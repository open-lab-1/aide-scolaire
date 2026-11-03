# Aide Scolaire

Application web responsive de révision scolaire. Dépôt indépendant du projet L'Atelier de Noël 3D.

## État actuel

Cette première version contient une interface responsive et des interactions locales :
- navigation entre les espaces ;
- ajout de cours dans l'état de la page (sans envoi du fichier) ;
- ajout d'examens et affichage des échéances ;
- pages bibliothèque, planning, entraînement et progression ;
- base visuelle compatible avec une future PWA.

**Important :** aucune donnée n'est encore envoyée vers un serveur. Les cours et examens ajoutés sont perdus au rechargement. La génération IA, l'authentification, Supabase Storage et la sauvegarde cloud ne sont pas encore connectés.

## Déploiement GitHub Pages

1. Ouvrir les paramètres du dépôt GitHub.
2. Aller dans **Pages**.
3. Dans **Build and deployment**, choisir **Deploy from a branch**.
4. Choisir la branche `main` et le dossier `/ (root)`.
5. Enregistrer. GitHub affichera l'adresse publiée après quelques instants.

## Prochaines étapes

1. Créer un projet Supabase séparé, sans réutiliser celui de L'Atelier de Noël.
2. Définir le schéma SQL, les politiques RLS et le bucket privé de documents.
3. Ajouter l'authentification et la persistance des cours/examens.
4. Déployer une Edge Function pour l'analyse IA (clé fournisseur uniquement côté serveur).
5. Ajouter génération PDF, cartes mentales, quiz, flashcards et planification adaptative.

## Sécurité

Ne jamais placer une clé Supabase `service_role`, une clé secrète ou une clé de fournisseur IA dans les fichiers servis par GitHub Pages. Le navigateur ne doit utiliser qu'une clé publishable/anon, avec RLS activé sur toutes les tables exposées.

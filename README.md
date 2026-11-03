# Aide Scolaire

Application web responsive de révision scolaire. Dépôt indépendant du projet L'Atelier de Noël 3D.

## Fonctionnalités actuellement intégrées

- Interface responsive avec tableau de bord, cours, planning, entraînement et progression.
- Authentification Supabase par e-mail et mot de passe.
- Sauvegarde cloud des cours et des examens.
- Importation de documents dans un bucket privé (20 Mo maximum).
- Ouverture des documents via des liens temporaires signés.
- Suppression des cours et examens.
- Protection des tables et fichiers par utilisateur (RLS).

## Déploiement GitHub Pages

Le workflow GitHub Actions est prêt. Dans le dépôt, ouvrir **Settings > Pages**, choisir **GitHub Actions** comme source de déploiement. Le workflow publiera ensuite le site à chaque mise à jour de la branche main.

## Configuration Supabase

Le projet Supabase indépendant est configuré dans la région Paris (eu-west-3).

Dans **Authentication > URL Configuration**, ajouter l'URL GitHub Pages du site aux Redirect URLs autorisées, puis la définir comme Site URL. Exemple : `https://open-lab-1.github.io/aide-scolaire/`.

Le navigateur utilise uniquement une clé publishable. Ne jamais placer de clé `service_role` ou de clé de fournisseur IA dans les fichiers publics.

## Limites de cette version

- La génération de fiches, cartes mentales, PDF, quiz et flashcards par IA n'est pas encore connectée.
- Le planning enregistre les examens ; la génération automatique de séances sera développée ensuite.
- Les notifications de rappel ne sont pas encore actives.
- L'authentification par e-mail peut nécessiter une confirmation d'adresse selon les réglages Supabase.

## Vie privée et sécurité

Les documents sont privés et chaque élève ne peut lire que ses propres données. Avant une ouverture publique à des mineurs, compléter les informations légales, la politique de confidentialité, les règles de conservation et les réglages de consentement adaptés au droit français.

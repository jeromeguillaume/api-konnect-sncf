# Modèle pour construire et déployer une API dans Konnect
Le modèle de l'OAS (OpenAPI Specification) se trouve dans `mon-api/openapi.yaml`. Les policies de la Kong Gateway sont dans `mon-api/policies`

Lorsque le développeur effectue un commit sur ce dépôt, un pipeline est exécuté pour publier l'API dans Konnect - environnement de Développement pour Kong Gateway, le Catalog et le Developer Portal

## Équipe Plateforme
L'équipe Plateforme contrôle et applique la gouvernance et la sécurité en ajoutant des politiques dans le pipeline CI. Voir l'application des politiques dans `platform/`. Les politiques portent le flag Kong Gateway `platform-repo-managed`

## Cycle de vie de l'API
Lors du commit, une PR est créée pour déployer l'API dans l'environnement de Développement. Le propriétaire de l'API fusionne la PR pour déployer l'API dans un environnement de Développement

`Promote API to Konnect Environments` est le workflow Git qui promeut l'API du Développement vers le Test, puis du Test vers la Production

## Pays
La PR est exécutée pour `environment: FRANCE_DEV`. À adapter pour les autres pays

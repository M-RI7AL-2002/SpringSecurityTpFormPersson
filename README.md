# TP : Personnalisation de l'authentification Spring Security

## Objectif du TP

Ce mini-projet a pour objectif de **maîtriser le mécanisme d’authentification de Spring Security** et de personnaliser entièrement le flux de connexion.  
L’idée est de remplacer la page de connexion par défaut par un **formulaire HTML personnalisé**, tout en gérant :

- Les erreurs de connexion
- Les redirections après authentification selon les rôles
- La déconnexion
- La restriction d’accès aux pages selon les rôles (`USER`, `ADMIN`)

Ce TP permet de mieux comprendre comment Spring Security gère l’**authentification et l’autorisation**, et comment l’application peut contrôler ce flux de manière fine.

---

## Description du mini-projet

Dans ce projet, vous trouverez un exemple concret d’application sécurisée avec les fonctionnalités suivantes :

- **Formulaire de connexion personnalisé**  
  Un formulaire HTML intégré à Spring Security pour remplacer la page par défaut, avec des messages d’erreur clairs et un message de déconnexion réussie.

- **Gestion des utilisateurs et rôles**  
  Les utilisateurs sont définis en mémoire pour simplifier le TP, avec deux rôles : `USER` et `ADMIN`.  
  Chaque rôle a accès à des pages spécifiques.

- **Pages sécurisées par rôle**  
  - `/user/dashboard` : accessible aux rôles `USER` et `ADMIN`  
  - `/admin/dashboard` : accessible uniquement au rôle `ADMIN`

- **Redirections après connexion**  
  Après authentification, l’utilisateur est automatiquement redirigé vers sa page selon son rôle.

- **Déconnexion**  
  Fonctionnalité de logout qui redirige l’utilisateur vers la page de connexion avec un message de confirmation.

- **Filtres de sécurité**  
  Le projet inclut la vérification du bon fonctionnement des filtres de sécurité, qui protègent les endpoints et contrôlent l’accès aux pages selon les rôles.

---

## Résumé des étapes réalisées dans le TP

1. Création d’un formulaire de connexion HTML personnalisé.  
2. Intégration du formulaire à Spring Security via l’endpoint `/authenticate`.  
3. Gestion des messages d’erreur et de succès lors de la connexion et de la déconnexion.  
4. Mise en place de redirections personnalisées après connexion selon les rôles.  
5. Sécurisation des endpoints et vérification du fonctionnement des filtres de sécurité.

---

## Résultat attendu

À la fin de ce mini-projet, vous serez capables de :

- Personnaliser entièrement la page de connexion Spring Security  
- Gérer le flux complet d’authentification et de redirection  
- Sécuriser les pages et les endpoints selon les rôles  
- Comprendre et contrôler le processus d’authentification dans une application Spring Boot

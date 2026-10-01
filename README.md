# locale-fr-FR

Ce dépôt contient les fichiers de traduction française des enquêtes State of JS, State of CSS, State of HTML et d'autres enquêtes Devographics. Vous trouverez la liste de [tous les dépôts de traduction ici](https://github.com/orgs/Devographics/repositories?q=locale-&type=all&language=&sort=name).

## Comment contribuer

#### 1. Devenir traducteur ou traductrice

Pour commencer à traduire une enquête, rejoignez le [serveur Discord](https://discord.com/invite/zRDb35jfrt), puis envoyez un message privé à `SachaG` avec votre nom d'utilisateur GitHub et le code de locale souhaité (`fr-FR`, `zh-Hant`, etc.).

Vous recevrez ensuite les droits de maintenance sur le dépôt correspondant. Vous pourrez alors gérer les fichiers de traduction YAML avec les autres membres de l'équipe.

#### 2. Repérer les textes à traduire

Vous pouvez parcourir l'application de réponse aux enquêtes et le site des résultats pour repérer les textes manquants. Vous pouvez aussi utiliser notre API pour consulter le taux d'avancement d'une locale ou la liste des clés non traduites :

- https://graphiql.devographics.com/

Exemple de requête :

```graphql
query GetLocaleData {
  locale(localeId: fr_FR) {
    completion
    totalCount
    translatedCount
    translators
    untranslatedKeys
  }
}
```

#### 3. Être crédité

Les personnes qui contribuent aux traductions sont créditées sur les sites qui les utilisent, à commencer par l'application des enquêtes. Pour apparaître dans les crédits, ajoutez votre nom d'utilisateur GitHub au tableau `translators` du fichier `config.yml` de la locale.

Voici un exemple pour la locale `de-DE` :

- https://github.com/Devographics/locale-de-DE/blob/main/config.yml#L3

#### 4. Publier vos modifications

La mise à jour des applications de production n'est pas encore automatisée après une modification de traduction. Pour le moment, prévenez-nous sur Discord lorsque vos changements sont prêts.

## Fichiers de traduction

Les fichiers partagés se trouvent dans `shared/` :

- `accounts.yml` et `surveys.yml` : comptes et application des enquêtes
- `common.yml` : textes communs aux applications
- `homepage.yml` : page d'accueil
- `results.yml` : site des résultats
- `countries.yml`, `how_to_help.yml` et `legacy.yml` : autres textes partagés

Les fichiers propres aux enquêtes sont regroupés dans leur répertoire, par exemple `state_of_js/`, `state_of_css/` ou `state_of_html/`. Ils contiennent les textes de l'enquête et de ses pages de résultats.

## Équipes de traduction

Nous vous recommandons de rejoindre l'[équipe de traduction](https://github.com/orgs/Devographics/teams/translators/teams) correspondant à votre langue.

## Développement local

Il n'existe pas encore de moyen simple de visualiser les traductions dans leur contexte pendant le développement local. Cette fonctionnalité est en cours de préparation.

## Besoin d'aide ?

Rejoignez [notre serveur Discord](https://discord.gg/zRDb35jfrt).

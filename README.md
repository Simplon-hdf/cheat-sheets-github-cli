# Cheat-sheets-github-cli

# Introduction à GitHub CLI

Bienvenue dans la documentation dédiée à GitHub CLI, l'outil en ligne de commande qui vise à améliorer et à optimiser votre flux de travail avec GitHub directement depuis votre terminal.

## Qu'est-ce que GitHub CLI?

GitHub CLI est une interface de ligne de commande puissante conçue pour faciliter l'utilisation des fonctionnalités de GitHub sans jamais quitter votre console. Que vous soyez sous Windows, Mac ou Linux, GitHub CLI vous permet d'interagir avec les issues, les pull requests, les dépôts et plus encore, offrant une expérience GitHub fluide et intégrée directement dans votre environnement local.

Avec GitHub CLI, vous pouvez effectuer presque toutes les opérations que vous feriez sur le site web de GitHub, mais avec l'efficacité et la rapidité que seul le terminal peut offrir. Cet outil est spécialement conçu pour les développeurs qui préfèrent utiliser le clavier plutôt que la souris, et qui souhaitent rester concentrés sur leur code sans se laisser distraire par le changement de contexte qu'implique le passage à un navigateur web.

## Pourquoi utiliser GitHub CLI?

Voici quelques avantages clés qui pourraient vous inciter à adopter GitHub CLI:

1. **Efficacité accrue**: Effectuez des tâches courantes en moins de commandes et sans quitter le contexte de votre projet.
2. **Automatisation simplifiée**: Intégrez facilement des opérations GitHub dans vos scripts pour automatiser votre workflow.
3. **Moins de context switching**: Réduisez les interruptions en restant dans le terminal, l'outil que vous utilisez déjà pour le développement.
4. **Prise en charge complète des fonctionnalités GitHub**: Interagissez avec presque toutes les parties de GitHub, y compris les forks, les issues, les pull requests, et bien plus encore.
5. **Personnalisation et extension**: Étendez les fonctionnalités de GitHub CLI avec des alias pour les commandes personnalisées, adaptant l'outil à vos besoins spécifiques.
6. **Expérience unifiée**: Que vous travailliez en solo ou en équipe, GitHub CLI offre une expérience cohérente pour tous les membres du projet.

Dans les sections suivantes, nous explorerons comment installer GitHub CLI, le configurer, et commencer à l'utiliser pour accélérer et simplifier votre interaction avec vos dépôts GitHub. Que vous soyez nouveau sur GitHub ou un vétéran cherchant à optimiser votre flux de travail, GitHub CLI est un outil indispensable à ajouter à votre arsenal de développement.

# Installer GitHub CLI

## Windows

### Avec Scoop

```bash
scoop install gh
```

### Avec Chocolatey

Ouvrez PowerShell en tant qu'administrateur et exécutez :

```bash
choco install gh
```

### Installation manuelle

Téléchargez le fichier **.msi** depuis la [page des releases de GitHub CLI](https://cli.github.com/), exécutez-le et suivez les instructions.

## MacOS

### Avec Homebrew

```bash
brew install gh
```

### Avec MacPorts

```bash
sudo port install gh
```

### Installation manuelle

Téléchargez le fichier **.pkg** depuis la [page des releases de GitHub CLI](https://cli.github.com/), ouvrez-le et suivez les instructions.

## Linux

### Sur Debian/Ubuntu (et dérivés) avec apt

```bash
sudo apt update
sudo apt install gh
```

### Sur Fedora avec dnf

```bash
sudo dnf install gh
```

### Sur CentOS avec yum

```bash
sudo yum install gh
```

### Sur Arch Linux avec pacman

```bash 
sudo pacman -S github-cli
```

### Installation manuelle

Téléchargez le fichier **.tar.gz** depuis la [page des releases de GitHub CLI](https://cli.github.com/), décompressez-le et suivez les instructions du README.

## Vérification de l'installation

Après installation, vérifiez en tapant :
```bash
gh --version
```

## Authentification

Pour vous connecter à GitHub via gh :

```bash
gh auth login
```

Suivez les instructions à l'écran pour authentifier.


# CONFIGURATION

### Step 1: GitHub Authentication

Pour vous connecter à votre compte GitHub via la ligne de commande, utilisez la commande suivante :

```
gh auth login
```

Suivez les instructions à l'écran pour vous authentifier à votre compte GitHub.

***

### Step 2 : Code Editor Configuration

Définir votre éditeur pour les opérations en ligne de commande, utilisez la commande `gh config set editor` suivi du nom de votre éditeur. 

``
gh config set editor code
``

***

### Step 3 : Alias

Déclarer des alias pour les commandes que vous utilisez fréquemment, utilisez la commande `gh alias set`. 
Si vous souhaitez créer un alias pour la commande `gh repo create`, vous pouvez le faire de la manière suivante :

``
gh alias set creer-repo 'repo create'
``

## Les bases de l'utilisation de GitHub CLI

Les lignes de commandes GitHub CLI, doivent être utilisée pour gagner du temps et éviter de changer de contexte, et d'interface.

### Les commandes de bases

Entrez <code>gh status</code> pour voir les détails de votre travail actuel sur GitHub dans tous les référentiels.

``` 
gh status
```
Entrez <code>gh help</code> pour obtenir de l'aide directement dans l'application.
```
gh help
 ```

### personnaliser son GitHub CLI

Pour adapter son GitHub CLI de la manière qui convient le mieux, il est possible de configurer et ajouter des alias et des extensions.

pour configurer les paramètres de GitHub CLI, entrez <code>gh config set SUBCOMMANDS</code>, en remplacant SUBCOMMANDS par le paramètre à ajuster.

Par exemple, pour redéfinir votre éditeur de texte préféré sur Visual Studio Code, entrez:
```
 gh config set editor "code -w" 
 ```
Dans ce cas l'indicateur <code>-w</code> fait en sorte que la commande attende que le fichier soit fermé dans Visual Studio Code avant de passer à l'étape suivante dans votre terminal.

### Travailler sur les repo GitHub

Pour créer un nouveau dépôt, utilisez la commande <code>gh repo create</code>.
```
gh repo create
```



Pour fork un dépôt, utilisez la commande <code>gh repo fork</code>.
```
gh repo create
```

 <code>--add-readme</code>: cré un fichier README dans le dépôt.

 <code>-c </code>, <code>--clone </code>: Clone le dépôt.

 <code>-d </code>, <code>--description < string > </code>: Description du dépôt.

 <code>-g </code>, <code>--gitignore < string > </code>: génère un gitignore pour le dépôt.

<code>--private </code> ou <code>--public </code>: rend le dépôt privé/public.

<code>--push </code> Push le commits dans le dépôt.

### Génération des Issue

Pour générer un "issue" utilisez la commande <code>gh issue create</code>.
Il est possible d'y ajouter un titre (<code>--title "text"</code>), un corp (<code>--body "text"</code>), ou encore un label (<code>--label "text"</code>).
```
gh issue create
```

### Création des Pull Request

Pour créer un Pull Request utilisez la commande <code>gh pr create</code>, puis suivre les instructions dans le Terminal.
```
gh pr create
```

Il est possible de lister les Pull Request en cour avec la commande <code>gh pr list</code>. 
```
gh pr list
```
La liste indiquera le numéro de la Pull Request à utilister dans le Terminal. Par exemple pour voir le Pull Request dans le Terminal utilisez la commande <code>gh pr view 1</code>, pour voir la première Pull Request.

Pour voir les conflits entre la branche principale et la Pull Request, utilisez la commande <code>gh pr diff 1</code> (pour le premier Pull Resquest).

Il est aussi possible de commenter la commande <code>gh pr comment 1 "votre commentaire"</code>.

Lorsque le  Pull Request est terminée, il est possible de le fermer avec la commande  <code>gh pr close 1</code> (pour le premier Pull Request).
```
gh pr close 1 -d
```
Il sera possible de réouvrire le Pull Request avec <code>gh pr reopen 1</code>.

A tout moment, il est possible de verifier le status du Pull Request avec la commande <code>gh pr status</code>


## Les extensions CLI


Les extensions CLI GitHub sont des dépôts qui fournissent des commandes gh supplémentaires.



Les noms d'extensions comment par <code>gh-</code> et doivent contenir un executable du même nom. 

La commande <code>gh extension brows [flags]</code> permet de rechercher, ajouter ou retirer vos extensions GitHub.
 ```
gh extension brows
```
Elles sont utilisées pour chatouiller la rétine de l'utilisateur, avoir des informations complémenteur depuis GitHub CLI, ou même pour chater et faire des graphiques! Les extensions sont nombreuses, et vous y trouverez forcement votre bonheur pour pimper votre CLI.

Vous trouverez une liste d'extensions à ce lien:  https://github.com/topics/gh-extension

# Installer des extensions

Pour installer une extensions, utilisez la commande <code>gh extensions install (url du repo)</code>. par exemple, pour l'extention "whoami":
```
gh extension install https://github.com/mislav/gh-branch
```

Vous trouverez de super extensions sur ce dépôt :https://github.com/kodepandai/awesome-gh-cli-extensions




# Astuces pour GitHub CLI

Utiliser GitHub CLI (`gh`) peut rendre votre flux de travail plus rapide et plus direct. Voici quelques astuces pour les développeurs qui débutent avec `gh`.

## Authentification simplifiée

Utilisez SSH pour l'authentification pour éviter de saisir vos identifiants à chaque fois :

```bash
gh auth login -h github.com -p ssh
```

## Navigation rapide

Ouvrez le dépôt actuel dans votre navigateur avec :

```bash
gh repo view --web
```

## Travail avec les issues

Listez les issues assignées à vous dans le dépôt actuel :

```bash
gh issue list --assignee @me
```

Créez une issue en spécifiant un titre et le corps directement :

```bash
gh issue create --title "Titre de l'issue" --body "Description de l'issue"
```

## Gestion des Pull Requests (PR)

Créez une pull request et remplissez automatiquement le titre et le corps avec les informations du commit :

```bash
gh pr create --fill
```

Listez les PRs qui demandent votre avis (en tant que reviewer) :

```bash
gh pr list --reviewer @me
```

## Alias pour les commandes longues

Créez des alias pour simplifier les commandes longues ou fréquentes. Par exemple, définissez un alias pour lister les PRs :

```bash
gh alias set prl 'pr list --limit 10'
gh prl
```

## Scripts et automatisation

Intégrez `gh` dans vos scripts pour automatiser les tâches GitHub. Par exemple, un script pour cloner et naviguer dans un dépôt :

```bash
#!/bin/bash

# Cloner et ouvrir un dépôt
gh repo clone utilisateur/repo && cd repo && gh repo view --web
```

## Consulter et télécharger les Releases

Listez les dernières releases :

```bash
gh release list
```

Téléchargez des assets spécifiques de la dernière release :

```bash
gh release download --pattern "*.zip"
```
GitHub CLI (`gh`) est un outil puissant pour interagir avec GitHub directement depuis votre terminal. Voici un "cheat sheet" des commandes de base et quelques alias que vous pouvez configurer pour raccourcir ces commandes.

### Cheat Sheet de Commandes `gh`

**Authentification:**

- `gh auth login` : Se connecter à GitHub CLI.
- `gh auth logout` : Se déconnecter de GitHub CLI.

**Gestion des issues:**

- `gh issue list` : Lister les issues.
- `gh issue view <numéro>` : Voir une issue spécifique.
- `gh issue create` : Créer une nouvelle issue.
- `gh issue close <numéro>` : Fermer une issue.
- `gh issue reopen <numéro>` : Réouvrir une issue fermée.

**Gestion des pull requests:**

- `gh pr list` : Lister les Pull Requests.
- `gh pr view <numéro>` : Voir une PR spécifique.
- `gh pr diff <numéro>` : Voir les différences d'une PR.
- `gh pr checkout <numéro>` : Faire un checkout d'une PR.
- `gh pr create` : Créer une nouvelle PR.
- `gh pr edit <numéro>` : Éditer une PR existante.
- `gh pr merge <numéro>` : Fusionner une PR.
- `gh pr close <numéro>` : Fermer une PR.
- `gh pr reopen <numéro>` : Réouvrir une PR fermée.

**Gestion des repos:**

- `gh repo clone <repo>` : Cloner un dépôt.
- `gh repo create` : Créer un nouveau dépôt.
- `gh repo fork <repo>` : Forker un dépôt.
- `gh repo view [--web]` : Voir le dépôt actuel.

**Gestion des workflows (Actions GitHub):**

- `gh workflow list` : Lister les workflows.
- `gh workflow view <workflow_id>` : Voir un workflow.
- `gh workflow run <workflow_id>` : Exécuter un workflow.
- `gh workflow disable <workflow_id>` : Désactiver un workflow.
- `gh workflow enable <workflow_id>` : Activer un workflow.

**Alias:**

GitHub CLI vous permet de créer des alias pour les commandes, afin de réduire la quantité de frappe nécessaire pour les exécuter.

Pour configurer un alias dans `gh`, utilisez la commande suivante:

```sh
gh alias set <alias> '<commande>'
```

Par exemple:

- `gh alias set prl 'pr list'` : Crée un alias `prl` pour `gh pr list`.
- `gh alias set vic 'issue create'` : Crée un alias `vic` pour `gh issue create`.
- `gh alias set vpr 'pr view'` : Crée un alias `vpr` pour `gh pr view`.

Pour utiliser un alias, tapez simplement `gh` suivi de l'alias:

```sh
gh prl
```

Pour voir tous vos alias:

```sh
gh alias list
```

Pour supprimer un alias:

```sh
gh alias delete <alias>
```

Ces alias sont personnalisables, donc vous pouvez les configurer comme bon vous semble pour correspondre à votre workflow.
# Gestion des Gists GitHub avec GitHub CLI

## Qu'est-ce qu'un Gist ?

Les gists sont un moyen simple de partager des extraits de code et d'autres petits morceaux de texte avec d'autres. Tandis que les dépôts GitHub sont destinés à des projets plus grands, les gists sont idéaux pour des morceaux de code isolés, des scripts, des notes ou des snippets. Chaque gist est sauvegardé dans un dépôt Git, ce qui signifie qu'ils peuvent être versionnés, forkés et clonés.

Les gists peuvent être créés soit en tant que fichiers publics que tout le monde peut voir et partager, soit en tant que fichiers privés accessibles uniquement à l'utilisateur.

## Création d'un Gist

Pour créer un nouveau gist :

```bash
gh gist create <filename>
```

- `<filename>` : le fichier que vous souhaitez télécharger en tant que gist.

Pour créer un gist avec du contenu directement depuis la ligne de commande :

```bash
echo "Votre contenu ici" | gh gist create -
```

- Le `-` indique à `gh` de lire le contenu du standard input.

## Lister vos Gists

Pour voir la liste de vos gists :

```bash
gh gist list
```

## Voir un Gist

Pour afficher le contenu d'un gist :

```bash
gh gist view <gist-id>
```

- `<gist-id>` : l'identifiant du gist que vous souhaitez visualiser.

## Éditer un Gist

Pour éditer un gist existant :

```bash
gh gist edit <gist-id>
```

- `<gist-id>` : l'identifiant du gist que vous souhaitez éditer.

## Cloner un Gist

Pour cloner un gist dans un répertoire local :

```bash
gh gist clone <gist-id>
```

- `<gist-id>` : l'identifiant du gist que vous souhaitez cloner.

## Supprimer un Gist

Pour supprimer un gist :

```bash
gh gist delete <gist-id>
```

- `<gist-id>` : l'identifiant du gist que vous souhaitez supprimer.

## Conclusion

L'utilisation de `gh` pour les gists permet une intégration fluide et rapide avec votre flux de travail en ligne de commande. Pour plus de détails sur les commandes `gh gist`, vous pouvez toujours exécuter :

```bash
gh gist --help
```

Utilisez les gists pour partager rapidement des bouts de code ou pour sauvegarder des fragments de texte pour un usage futur, tout cela directement depuis votre terminal.
  
Ces alias sont personnalisables, donc vous pouvez les configurer comme bon vous semble pour correspondre à votre workflow. N'oubliez pas que chaque alias devrait rendre votre utilisation de `gh` plus efficace et plus ra## Les bases de l'utilisation de GitHub CLI

Les lignes de commandes GitHub CLI, doivent être utilisée pour gagner du temps et éviter de changer de contexte, et d'interface.

 GitHub CLI est un outil open source permettant d’utiliser GitHub à partir de la ligne de commande de votre ordinateur.
 Lorsque vous travaillez à partir de la ligne de commande, vous pouvez utiliser l’interface de ligne de commande GitHub pour gagner du temps et éviter de changer de contexte.
 GitHub CLI inclut des fonctionnalités GitHub telles que : Afficher, créer, cloner et dupliquer des dépôts Créer, fermer, modifier et afficher des problèmes et des demandes de tirage.
 GitHub CLI est un outil de ligne de commande qui apporte les demandes de tirage, les problèmes, les actions GitHub et d’autres fonctionnalités GitHub à votre terminal, afin que vous puissiez effectuer tout votre travail en un seul endroit.
 Quelle est la différence entre GitHub CLI et Git sur la ligne de commande ?
 L’interface de ligne de commande Git (git) vous permet de travailler avec un référentiel Git local ou distant. Le dépôt distant peut être hébergé sur GitHub ou par un autre service.
 GitHub CLI (gh) est spécifiquement destiné à l’utilisation de GitHub. Il vous permet d’utiliser la ligne de commande pour interagir avec GitHub de toutes sortes de façons, comme illustré par la liste précédente. Si vous avez tendance à travailler sur la ligne de commande, vous préférerez peut-être utiliser GitHub CLI plutôt que d’utiliser GitHub dans un navigateur. GitHub CLI vous permet également de créer plus facilement des scripts pour automatiser les opérations GitHub.
 Comparaison avec le hub: Pendant de nombreuses années, hub a été l’outil CLI GitHub non officiel. gh est un nouveau projet qui nous aide à explorer à quoi peut ressembler un outil CLI GitHub officiel avec un design fondamentalement différent. Alors que les deux outils apportent GitHub au terminal, hub se comporte comme un proxy de git, et gh est un outil autonome. Consultez notre explication plus détaillée pour en savoir plus.

 ***


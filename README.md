# cheat-sheets-github-cli

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
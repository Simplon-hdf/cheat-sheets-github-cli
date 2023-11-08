<a href="README.md">Table des Matières</a>

# Installer GitHub CLI

### Windows

#### Avec Scoop

```bash
scoop install gh
```

#### Avec Chocolatey

```bash
choco install gh
```

#### Installation manuelle

Téléchargez le fichier **.msi** depuis la [page des releases de GitHub CLI](https://cli.github.com/), exécutez-le et suivez les instructions.

### MacOS

#### Avec Homebrew

```bash
brew install gh
```

#### Avec MacPorts

Téléchargez le fichier **.pkg** depuis la [page des releases de GitHub CLI](https://cli.github.com/), ouvrez-le et suivez les instructions.

```bash
sudo port install gh
```

### Linux

#### Sur Debian/Ubuntu (et dérivés) avec apt

```bash
sudo apt update
sudo apt install gh
```

#### Sur Fedora avec dnf

```bash
sudo dnf install gh
```

#### Sur CentOS avec yum

```bash
sudo yum install gh
```

#### Sur Arch Linux avec pacman

Téléchargez le fichier **.tar.gz** depuis la [page des releases de GitHub CLI](https://cli.github.com/), décompressez-le et suivez les instructions du README.

```bash 
sudo pacman -S github-cli
```

### Vérification de l'installation 

```bash
gh --version
```

<br>

***
## CONFIGURATION

### GitHub Authentication

Pour vous connecter à votre compte GitHub via la ligne de commande, utilisez la commande suivante :

```
gh auth login
```

Suivez les instructions à l'écran pour vous authentifier à votre compte GitHub.



###  Code Editor Configuration

Définir votre éditeur pour les opérations en ligne de commande, utilisez la commande `gh config set editor` suivi du nom de votre éditeur. 

```
gh config set editor code
```

###  Alias

Déclarer des alias pour les commandes que vous utilisez fréquemment, utilisez la commande `gh alias set`. 

Par exemple, si vous souhaitez créer un alias pour la commande `gh repo create`, vous pouvez le faire de la manière suivante :

```
gh alias set creer-repo `____`
```

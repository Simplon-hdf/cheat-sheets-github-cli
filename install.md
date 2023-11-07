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
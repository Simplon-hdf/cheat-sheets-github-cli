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

***
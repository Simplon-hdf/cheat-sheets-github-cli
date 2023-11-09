# Table des matières

- [Table des matières](#table-des-matières)
- [Gestion des Gists GitHub avec GitHub CLI](#gestion-des-gists-github-avec-github-cli)
    - [Qu'est-ce qu'un Gist ?](#quest-ce-quun-gist-)
    - [Création d'un Gist](#création-dun-gist)
    - [Lister vos Gists](#lister-vos-gists)
    - [Voir un Gist](#voir-un-gist)
    - [Éditer un Gist](#éditer-un-gist)
    - [Cloner un Gist](#cloner-un-gist)
    - [Supprimer un Gist](#supprimer-un-gist)
    - [Gist Help](#gist-help)

# Gestion des Gists GitHub avec GitHub CLI

### Qu'est-ce qu'un Gist ?

Les gists sont un moyen simple de partager des extraits de code et d'autres petits morceaux de texte avec d'autres. Tandis que les dépôts GitHub sont destinés à des projets plus grands. Les gists sont idéaux pour des morceaux de code isolés, des scripts, des notes ou des snippets. 

Chaque gist est sauvegardé dans un dépôt Git, ce qui signifie qu'ils peuvent être versionnés, forkés et clonés.

Les gists peuvent être créés soit en tant que fichiers publics que tout le monde peut voir et partager, soit en tant que fichiers privés.

### Création d'un Gist

Pour créer un nouveau gist :

```sh
gh gist create <filename>
```

- `<filename>` : Le fichier que vous souhaitez uploader en tant que gist.

### Lister vos Gists

Pour voir la liste de vos gists :

```sh
gh gist list
```

### Voir un Gist

Pour afficher le contenu d'un gist :

```sh
gh gist view <gist-id>
```
 `<gist-id>` : L'identifiant du gist que vous souhaitez visualiser.

### Éditer un Gist

Pour éditer un gist existant :

```sh
gh gist edit <gist-id>
```

`<gist-id>` : L'identifiant du gist que vous souhaitez éditer.

### Cloner un Gist

Pour cloner un gist dans un répertoire local :

```sh
gh gist clone <gist-id>
```
`<gist-id>` : L'identifiant du gist que vous souhaitez cloner.

### Supprimer un Gist

Pour supprimer un gist :

```sh
gh gist delete <gist-id>
```

- `<gist-id>` : L'identifiant du gist que vous souhaitez supprimer.

### Gist Help 

L'utilisation de `gh` pour les gists permet une intégration fluide et rapide avec votre flux de travail en ligne de commande. Pour plus de détails sur les commandes `gh gist`, vous pouvez exécuter :

```sh
gh gist --help
```

<div align="center">
  <img src="images/gistHelp.png"/>
</div>
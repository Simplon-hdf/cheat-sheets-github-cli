  <p align="center"><img src="ghcli.png" /></p>

# GitHub CLI


## Table des matières


<br>

<ul>
    <li><a href="introduction.md">Introduction</a></li>
    <li><a href="installation.md">Installation</a></li>
    <li><a href="utilisation.md">Bases de l'utilisation</a></li>
    <li><a href="gist.md">GitHub Gist</a></li>
</ul>

<br>



# Cheat-Sheet de Commandes `gh`

### **Authentification:**

- `gh auth login` : Se connecter à GitHub CLI.
- `gh auth logout` : Se déconnecter de GitHub CLI.

### **Gestion des issues:**

- `gh issue list` : Lister les issues.
- `gh issue view <numéro>` : Voir une issue spécifique.
- `gh issue create` : Créer une nouvelle issue.
- `gh issue close <numéro>` : Fermer une issue.
- `gh issue reopen <numéro>` : Réouvrir une issue fermée.

### **Gestion des pull requests:**

- `gh pr list` : Lister les Pull Requests.
- `gh pr view <numéro>` : Voir une PR spécifique.
- `gh pr diff <numéro>` : Voir les différences d'une PR.
- `gh pr checkout <numéro>` : Faire un checkout d'une PR.
- `gh pr create` : Créer une nouvelle PR.
- `gh pr edit <numéro>` : Éditer une PR existante.
- `gh pr merge <numéro>` : Fusionner une PR.
- `gh pr close <numéro>` : Fermer une PR.
- `gh pr reopen <numéro>` : Réouvrir une PR fermée.

### **Gestion des repos:**

- `gh repo clone <repo>` : Cloner un dépôt.
- `gh repo create` : Créer un nouveau dépôt.
- `gh repo fork <repo>` : Forker un dépôt.
- `gh repo view [--web]` : Voir le dépôt actuel.

### **Gestion des workflows (Actions GitHub):**

- `gh workflow list` : Lister les workflows.
- `gh workflow view <workflow_id>` : Voir un workflow.
- `gh workflow run <workflow_id>` : Exécuter un workflow.
- `gh workflow disable <workflow_id>` : Désactiver un workflow.
- `gh workflow enable <workflow_id>` : Activer un workflow.
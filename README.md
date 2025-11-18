# Cours d'introduction au RL

Ce répertoire contient une série de notebooks Jupyter qui présentent les concepts d'Apprentissage par Renforcement (Reinforcement Learning, RL) de manière accessible. Le premier notebook (`rl_intro.ipynb`) couvre les deux grandes familles fondatrices du RL : les méthodes basées sur la valeur et les méthodes basées sur la politique.

## Prérequis

- [uv](https://github.com/astral-sh/uv), le gestionnaire ultra-rapide d'environnements et de paquets Python.
- Un terminal en ligne de commande (instructions ci-dessous pour Windows et pour Mac/Linux).

## Installer uv (si nécessaire)

### Mac/Linux

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Le script ajoute `uv` à votre PATH shell. Redémarrez le terminal (ou rechargez le profil indiqué) afin que la commande `uv` soit reconnue.

### Windows

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

Le script ajoute `uv` à votre PATH. Redémarrez votre terminal (PowerShell ou Invite de commandes) pour rendre la commande `uv` disponible.

## Préparer l'environnement Python avec uv

Exécutez ces commandes depuis la racine du projet :

### Mac/Linux

```bash
uv venv --python 3.13
source .venv/bin/activate
uv pip install -r requirements.txt
```

### Windows

```powershell
uv venv --python 3.13
.venv\Scripts\activate
uv pip install -r requirements.txt
```

**Explications :**
- `uv venv --python 3.13` crée un environnement virtuel local dans `.venv` avec Python 3.13. Si cette version n'est pas déjà installée, `uv` la télécharge et l'installe automatiquement.
- Le script d'activation dépend de la plateforme (`source .venv/bin/activate` sur Mac/Linux contre `.venv\Scripts\activate` sur Windows).
- `uv pip install -r requirements.txt` installe toutes les dépendances listées dans le fichier. Actuellement il contient `numpy`, `ipykernel` et `jupyter`, nécessaires au premier notebook, mais vous pouvez y ajouter d'autres paquets au fil du cours.

## Lancer les notebooks avec uv

La commande est identique sur toutes les plateformes :

```bash
uv run jupyter notebook
```

`uv run` garantit que l'interpréteur et les paquets provenant de `.venv` sont utilisés. Lorsque Jupyter s'ouvre dans votre navigateur, vous pouvez parcourir tous les notebooks du répertoire. Commencez par `rl_intro.ipynb` et exécutez les cellules de haut en bas. Chaque expérience (value iteration et bandit avec gradient de politique) affiche sa progression directement dans la sortie.

## Mettre à jour les dépendances

Si vous ajoutez de nouveaux paquets en avançant dans les notebooks, continuez d'utiliser le même environnement :

### Mac/Linux

```bash
source .venv/bin/activate
uv pip install <nom-du-paquet>
```

### Windows

```powershell
.venv\Scripts\activate
uv pip install <nom-du-paquet>
```

Cette approche garantit la reproductibilité et évite de recréer manuellement des environnements.

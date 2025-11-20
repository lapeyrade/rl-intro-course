# Cours d'introduction au RL

Ce répertoire contient une série de notebooks Jupyter qui présentent les concepts d'Apprentissage par Renforcement (Reinforcement Learning, RL) de manière accessible. Le premier notebook (`rl_intro.ipynb`) couvre les deux grandes familles fondatrices du RL : les méthodes basées sur la valeur et les méthodes basées sur la politique.

## Prérequis

- Un terminal en ligne de commande (Mac/Linux ou Windows).
- Python 3.13.9 recommandé.
- Le gestionnaire de paquets [uv](https://github.com/astral-sh/uv) est facultatif mais vivement conseillé pour accélérer l'installation et isoler l'environnement. Vous pouvez aussi utiliser l'outillage Python standard (`python -m venv`, `pip`).

## Installer uv (facultatif mais recommandé)

- **Mac/Linux**

  ```bash
  curl -LsSf https://astral.sh/uv/install.sh | sh
  ```

  Le script ajoute `uv` à votre PATH. Redémarrez le terminal ou rechargez votre profil.

- **Windows**

  ```powershell
  powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
  ```

  Le script ajoute `uv` à votre PATH PowerShell/Invite de commandes.

## Préparer l'environnement Python

Depuis la racine du projet, choisissez l'approche qui vous convient.

### Avec uv (recommandé)

- **Mac/Linux**

  ```bash
  uv venv --python 3.13
  source .venv/bin/activate
  uv pip install -r requirements.txt
  ```

- **Windows**

  ```powershell
  uv venv --python 3.13
  .venv\Scripts\activate
  uv pip install -r requirements.txt
  ```

### Sans uv (outil standard Python)

- **Mac/Linux**

  ```bash
  python3 -m venv .venv
  source .venv/bin/activate
  python -m pip install --upgrade pip
  python -m pip install -r requirements.txt
  ```

- **Windows**

  ```powershell
  python -m venv .venv
  .venv\Scripts\activate
  python -m pip install --upgrade pip
  python -m pip install -r requirements.txt
  ```

**Notes :**
- `requirements.txt` inclut Gymnasium (avec extras Atari), PyGame, PyTorch, Matplotlib, Pandas, etc.

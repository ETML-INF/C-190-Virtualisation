# GitHub Actions – Workflows

Ce répertoire contient les workflows GitHub Actions du module.

---

## `marp.yml` – Build & Deploy GitHub Pages

Déclenché sur `push` ou `pull_request` quand un fichier `.md` ou une image change dans `b-UnitesEnseignement/Presentations/`, ou qu'un exercice PDF change dans `b-UnitesEnseignement/Exercices/`.

- Convertit chaque `.md` en HTML et PDF avec MARP CLI.
- Copie les images et les exercices PDF.
- Génère un `index.html` listant présentations et exercices.
- Déploie sur **GitHub Pages**.

---

## `ref-marp-to-section-inf.yml` – TARDIS : déploiement présentations

Déclenché sur `push` vers `main` quand `b-UnitesEnseignement/Presentations/**` change.

- Compile les slides avec les thèmes ETML (depuis `ETML-INF/tardis-pipelines`).
- Génère un `index.html` avec le nom du module (`ICT_MODULE`).
- Synchronise le résultat vers le serveur Section INF via FTP.

**Variables requises :**

| Nom | Type | Description |
|-----|------|-------------|
| `ICT_MODULE` | Variable | Code du module (`C190`) |
| `ICT_ROOT_FOLDER` | Variable | Dossier racine FTP |
| `FTP_PRESENTATIONS_DIR` | Variable | Sous-dossier FTP présentations |
| `FTP_SERVER` | Variable | Adresse du serveur FTP |
| `FTP_USERNAME` | Secret | Identifiant FTP |
| `FTP_PASSWORD` | Secret | Mot de passe FTP |

---

## `ref-sync-exercices.yml` – TARDIS : synchronisation exercices

Déclenché sur `push` vers `main` quand `b-UnitesEnseignement/Exercices/*.pdf` change.

- Génère un `index.html` listant les PDF disponibles.
- Synchronise les PDF + index vers le serveur Section INF via FTP.

**Variables requises :** mêmes que ci-dessus, plus :

| Nom | Type | Description |
|-----|------|-------------|
| `FTP_EXO_DIR` | Variable | Sous-dossier FTP exercices |

---

📌 **Auteur :** AGR

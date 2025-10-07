## Enoncé de l'exercice: 
Exercice N°2
Branching & Merging
L'ensemble des instructions suivantes doivent ètre réalisés exclusivement via le terminal, sauf la dernière.

Notez que vous devrez surement installez Github CLI pour cet exercice.

Objectifs : Apprendre à créer des branches, y effectuer des changements et les merger dans la branche main

Depuis un repo clonez du nom: git-learning-2 que vous aurez créez créez une nouvelle branche du nom de myself.
Créez un fichier about.txt avec des infos sur vous (nom, prénom, lieu de naissance...)
Faites un commit puis, puis pushez la branche myself.
Faites un pull request de git-learning-2/myself -> main.
Mergez le pull request.
Sur GitHub, vérifier l'historique.

# git-learning-2

Ce projet montre comment utiliser Git et GitHub CLI pour gérer un flux de travail avec branches et Pull Requests.

## 1. Créer un nouveau dépôt GitHub

```bash
gh repo create git-learning-2 --public --clone
cd git-learning-2
```
- `gh repo create ...` : crée un nouveau dépôt public nommé **git-learning-2** sur GitHub et le clone localement.
- `cd git-learning-2` : entre dans le dossier du projet.

---

## 2. Créer une branche `myself`

```bash
git checkout -b myself
```
- Crée et bascule sur une nouvelle branche appelée `myself`.

---

## 3. Créer un fichier `about.txt` avec vos informations

```bash
echo "Nom : Soumana yayé, Prénom: Issaka, Lieu de naissance: Niamey" > about.txt
```
- Crée un fichier `about.txt` et y ajoute vos informations personnelles.

---

## 4. Commit et push de la branche

```bash
git add about.txt
git commit -m "Ajout du fichier about.txt avec mes infos personnelles"
git push origin myself
```
- `git add about.txt` : prépare le fichier pour le commit.
- `git commit -m ...` : enregistre les modifications localement avec un message.
- `git push origin myself` : envoie la branche `myself` sur GitHub.

---

## 5. Créer une Pull Request de `myself` vers `main`

```bash
gh pr create --base main --head myself --title "Ajout de about.txt" --body "Ce PR ajoute mes informations personnelles."
```
- Crée une Pull Request pour fusionner la branche `myself` dans `main`.

---

## 6. Merger la Pull Request

```bash
gh pr merge --merge
```
- Fusionne la Pull Request avec un merge classique (`--merge`).

## 7.Voici un capture de mon travail:
![](./Exo2-github.png)
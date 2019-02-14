
# Crear repositorio

```
git init
git commit --allow-empty -m "Initial commit"
git checkout -b dev master
git branch
git remote add origin git@github.com:RaulKite/ejemplogitflow.git
```


# Features

```
# Crear la rama a partir de dev
git checkout -b feature/<issue_id>[-short_description] dev

# Compartir la rama (en caso necesario)
git checkout feature/<issue_id>[-short_description]
git push origin feature/<issue_id>[-short_description]

# Finalizar una rama Feature
git checkout dev
git pull origin dev
git merge --no-ff feature/<issue_id>[-short_description]
git branch -d feature/<issue_id>[-short_description]
git push origin dev

# Si se compartió la rama en el servidor
git push origin :feature/<issue_id>[-short_description]
```

# Releases

```
# Crear la rama a partir de dev
git checkout -b release/x.y.z dev

# Compartir la rama (en caso necesario)
git checkout release/x.y.z
git push origin release/x.y.z

# Finalizar una rama Release
git checkout master
git pull origin master
git merge --no-ff release/x.y.z
git tag -a x.y.z
git checkout dev
git pull origin dev
git merge --no-ff release/x.y.z
git branch -d release/x.y.z
git push origin master
git push origin dev
git push origin --tags

# Si se compartió la rama
git push origin :release/x.y.z
```



# Comandos utiles en git

## Área de trabajo

```
git add archivo (Añade un archivo para versionar)
git add . (Añade todos los archivos del directorio donde ejecutes este comando)
git add *.py (Añade todos los archivos que terminan con .py)

git rm –cached archivo (Elimina el track del archivo en git sin eliminarlo del sistema)
git reset HEAD (Vuelve al último commit)
git checkout — archivo (Deshace los cambios realizados en el archivo llamado archivo)
```

## Branches

```
git branch (Muestra la lista de branches locales)
git branch -r (Muestra la lista de branches remotos)
git branch -a (Muestra todos los branches, tanto locales como remotos)
git checkout -b nuevobranch (Crea un nuevo branch llamado nuevobranch)
git checkout branchacambiar (Cambiarse al branch bancheacambiar)
git branch -d nuevobranch (Elimina un branch llamada nuevobranch)
```

## Repositorios
```
git remote -v (Muestra repositorios remotos)
git remote add nombre url (Agrega un repositorio remoto con el alias nombre a partir de la url)
git push origin master (Actualizar el repositorio remote a parte del repositorio actual)
git pull origin master (Actualiza el repositorio local a partir del remoto)
```

# Stash
```
git stash (Mueve todos los cambios a Stash)
git stash list (Muestra la lista de todos los stash)
git stash apply (Aplicar los archivos del último stash aplicado)
```

## Commits
```
git commit -m “Crea un commit”. (Genera un commit)
git commit -am “Genera un commit.” (Crea un commit adicionando los archivos sin pasar por staging)
git commit -m –amend (Adiciona nuevos archivos al commit actual)
```

## Logs
```
git log (Muestra una lista de todos los commits realizados)
git reflog (Muestra estados anteriores de los branches)
```

## Patches
```
git format-patch nombredelbranch (Crea un patch sobre el branch actual)
```

## Tags
```
git tag v1.0 (Crea una etiqueta llamada v1.0)
```


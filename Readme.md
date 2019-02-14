
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

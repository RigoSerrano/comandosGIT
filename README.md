## Página oficial de GIT
https://git-scm.com/

## Configuración inicial
```
git config --global user.email "tu_correo@correo.com"
git config --global user.name "nombre_de_usuario"
```

## Configuración de proxy
```
git config --global http.proxy 192.168.241.14:8080 
git config --global --unset http.proxy
```

## No colocar siepre las credenciales de github
```
git config --global credential.helper 'cache --timeout=864000'
```

## Conectar tu repositorio local con uno remoto
```
git remote add origin URL	// Conectar
git remote -v			// Ve los repositorios remotos
git remote remove origin	// Quita el repositorio remoto
```
## Comandos varios

`git clone url`				      Baja el proyecto de la nube <br>
`git status` 					      Ver el estado <br>
`git add .` 					      Añado todo cuando hago cambios <br>
`git commit -m "mensaje"` 	Sube local <br>
`git push` 					        Envía a online <br>
`git pull` 					        Baja de online <br>
`git log`						        Ve todos los commits <br>
`git log --pretty=oneline`	Ve todos los commits por linea solo con IDS <br>
`git log --pretty=format:"%h - %an, %ar : %s"` <br>
`git checkout ID_COMMIT`		Vuelve al estado del ID_COMMIT <br>
INVESTIGAR amend para cambiar el mensaje de los commit

## Ramas
`git branch nombre`			        Crea una nueva rama<br>
`git checkout nombreBranch`	    Cambio a esa rama<br>
`git checkout master`			      Vuelve al mas actual<br>
`git add .`					            Añadiendo antes de subir<br>
`git push origin nombreBranch`	Subiendo a GIT HUB<br>
`git branch -D NOMBRE_RAMA`		  Eliminar una rama<br>

### Mezclar rama master con una rama
```
git checkout master
git merge nombreRama
```
### Eliminar una rama
```
git branch -d nombreRama
```
### Muestra grafico
```
git log --oneline --graph --all
```

## Mostrar las ramas no fusionadas
```
git branch --no-merged
```

# Tags
Los tags no se suben con los push

`git tag -a v0.1 -m "Mensaje de versión"`			        se le asigna al último commit<br>
`git tag -a v0.1 -m "Mensaje de versión"	SHA_COMMIT`	Tag a un commit en específico<br>
`git push origin v0.1`
`git push origin --tags`					                    Sube todos los tags que hemos creado<br>


# Trabajo en equipo

Para cuando se trabaja en equipo, y existen cambios y hay que verificar si existe algun cambio
```
git fetch origin
git merge origin/master
git push origin/master
```

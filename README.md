# Práctica del curso de git, gitHub y Sourcetree

## Pedro Liébana Castellano

## **¿Qué comando utilizaste en el paso 11? ¿Por qué?**

    He utilizado el comando `git reset --hard HEAD~1`. Con *reset* movemos la rama de lugar, concretamente se mueve al commit padre, el cual se lo indicamos con *HEAD~1*. Por último, con *--hard* hacemos que se pierdan los cambios en el working copy.

## **¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**

    Para este paso he utilizado `git reflog` y después: `git reset --hard <id del commit>`  

    Con git reflog obtenemos el id del commit que se había creado y con `git reset --hard <id del commit>` movemos el puntureo HEAD al commit que habíamos creado para, de este modo, recuperar cambios en el working copy

## **El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**

    No produce ningún conflicto, pero tampoco ningún cambio. Entiendo que la rama styled ya contenía todos los cambios de la rama main, por este motivo no hay nada que absorber.

## **El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**

    Si, se producen conflictos cuando mergeamos htmlify y styled, ya que en ambas ramas se han modificado las mismas líneas.

## **El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**

    No se producen conflictos, ya que, aunque en styled se ha modificado el archivo git-nuestro.md y en main no hemos actualizado nada sobre este archivo, al absorber main a styled, se actualiza el archivo pero no se produce ningún conflicto.

## **¿Qué comando o comandos utilizaste en el paso 25?**

    Para ver el diagrama he hecho uso del comando `git log --graph`

## **El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**

    Sí podría serlo, además, si en el comando no hubiesemos indicado *--no-ff* sería fast forward por defecto. Puede serlo debido a que desde la rama title a la main, el grafo es lineal sin ninguna ramificación, hasta el commit donde se quiere hacer el merge.

## **¿Qué comando o comandos utilizaste en el paso 27?**

    Como primer comando he utilizado `git log` para identificar el id del commit. Posteriormente con `git reset <id commit>` el puntero HEAD y main regresan al commit anterior al merge sin que el se pierdan los cambios en el working copy.

## **¿Qué comando o comandos utilizaste en el paso 28?**

    He utilizado `git restore git-nuestro.md`, Con este comando descarto los cambios en el working copy que habían sido producidos por el merge.

## **¿Qué comando o comandos utilizaste en el paso 29?**

    Lo primero que debemos hacer es asegurarnos que no estamos situados en la rama que quiero eliminar, esto lo haremos ejecutando el comando `git branch`.
    Después eliminaremos de manera forzada la rama title con `git branch -D title`.

## **¿Qué comando o comandos utilizaste en el paso 30?**

    Utilicé primero `git reflog` para obtener el id del commit y después ejecutar `git reset --hard <id del commit>`, de esta manera rehacemos el merge.

## **¿Qué comando o comandos usaste en el paso 32?**

    Utilicé `git reflog` para saber el id del commit inicial. Despúes hice `git reset <id del commit inicial>` para deshacer todos los commits regresasndo al commit inicial pero sin tocar el working copy.

## **¿Qué comando o comandos usaste en el punto 33?**

    Lo primero que hay que hacer es un `git reflog` para obtener el id del commit donde se realizó el merge "no-ff" de title. Con este id ejecutamos `git reset <id del commit>`. Después con `nano git-nuestro.md` comprobé que todos los cambios han quedado reflejados.

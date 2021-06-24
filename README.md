
# Práctica del Curso Git

## Ejercicio 1

**1. ¿Qué comando utilizaste en el paso 11? ¿Por qué?**

	* El comando "git reset --hard HEAD~1"
	* Para retrasar el HEAD un paso por lo que deshariamos el último commit y ademas con --hard para perder los cambios del working copy 

**2. ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**

	* Usando git reflog veo el hash del commit al que quiero ir (antes de deshacer el coomit) con el identificador localizado hago el siguiente comando.
	* git reset --hard e9a7304 para volver al paso donde existía el commit que posteriormente había desecho en el paso anterior.
	* git restore para restaurar el working copy con el contenido del repositorio.

**3. El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**

	* No causó ningún conflicto, debido a que el commit de la rama "styled" es hijo del commit de la rama master que ya contiene los últimos cambios realizados sobre la rama master y no se poduce ningún cambio.

**4. El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**

	* Si produjo conflicto, debido a que el contenido del archivo en la rama "htmlify" es diferente al contenido del archivo en la rama "styled" en el primero existem las mismas lineas pero con caracteres tipo html que no estan en el archivo de la rama "styled" y git no sabe decidir por nosostros cual es el correcto, por lo que deberemos de corregir nosostros estos conflictos quedando los dos archivos con contenido idéntico.

**5. El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**

	* No me genera ningún conflicto debido a que en el paso 20 (el paso anterior) tuve que resolver los conflictos que se produjeron para ello tuve que editar el archivo "git-nuestro.md" de la rama "htmlify" quedandolo con contenido identico al mismo archivo de la rama "styled" una vez los dos archivos tienen su contenido idéntico (en este caso el de la rama "styled", habiendo modificado y guardado el archivo de la rama "htmlify") pasamos al staying area el archivo de la rama "htmlify" con "git add git-nuestro.md", hacemos un commit y procedemos a hacer el merge sin que nos de problemas. Este merge es un fast-foward 

**6. ¿Qué comando o comandos utilizaste en el paso 25?**

	* Inicialmente hice un "git log --graph" y luego hice un "git log --graph --decorate --pretty=oneline, para que me muestre el puntero y el resumen de cada commit.

**7. El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**

	* Si, ya que desde que se creo la rama "title" en la rama padre (master) no se hahecho ningún commit, por lo que los commit de la rama "title" se podrían haber añadido a la linea de tiempo de la rama "master" sin perjudicar los commit de la linea de tiempo de dicha rama.

**8. ¿Qué comando o comandos utilizaste en el paso 27?**

	* git reset HEAD~1 ya que al no tener el parámetro --hard mantiene los cambios en el working copy.

**9. ¿Qué comando o comandos utilizaste en el paso 28?**

	* git reflog paar saber hacia donde debo situarme
	* git checkout 4dd3ff

**10. ¿Qué comando o comandos utilizaste en el paso 29?**

	* git branch -D title

**11. ¿Qué comando o comandos utilizaste en el paso 30?**

	* git reflog para buscar el identificador del merge a rehacer
	* git checkout master para asegurarnos de estar en la rama "master"
	* git reset --hard 7b24f05  para restaurar el commit donde se realiza el merge

**12. ¿Qué comando o comandos usaste en el paso 32?**

	* git reflog
	* git reset cbcf95a

**13. ¿Qué comando o comandos usaste en el punto 33?** 

	* git reflog
	* git checkout 4dd3ffe  para ir al último commit de la rama title con los cambios del título
	* Debido a que aunque estoy en el lugar adecuado estoy en detached HEAD vuelvo a crear la rama "title" con git branch title. Luego de la misma forma sigo recuperando las ramas eliminadas "Styled" y "htmlify"
	* git checkout 7b24f05 y git branch styled
	* git checkout 47b9659 y git branch htmlify
=======

**1. ¿Qué comando utilizaste en el paso 11? ¿Por qué?**

        * El comando "git reset --hard HEAD~1"
        * Para retrasar el HEAD un paso por lo que deshariamos el último commit y ademas con --hard para perder los cambios del working copy

**2. ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**

        * Usando git reflog veo el hash del commit al que quiero ir (antes de deshacer el coomit) con el identificador localizado hago el siguiente comando.
        * git reset --hard e9a7304 para volver al paso donde existía el commit que posteriormente había desecho en el paso anterior.
        * git restore para restaurar el working copy con el contenido del repositorio.

**3. El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**

        * No causó ningún conflicto, debido a que el commit de la rama "styled" es hijo del commit de la rama master que ya contiene los últimos cambios realiza$

**4. El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**

        * Si produjo conflicto, debido a que el contenido del archivo en la rama "htmlify" es diferente al contenido del archivo en la rama "styled" en el prime$

**5. El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**

        * No me genera ningún conflicto debido a que en el paso 20 (el paso anterior) tuve que resolver los conflictos que se produjeron para ello tuve que edit$

**6. ¿Qué comando o comandos utilizaste en el paso 25?**

        * Inicialmente hice un "git log --graph" y luego hice un "git log --graph --decorate --pretty=oneline, para que me muestre el puntero y el resumen de ca$

**7. El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**
      * Si, ya que desde que se creo la rama "title" en la rama padre (master) no se hahecho ningún commit, por lo que los commit de la rama "title" se podría$

**8. ¿Qué comando o comandos utilizaste en el paso 27?**

        * git reset HEAD~1 ya que al no tener el parámetro --hard mantiene los cambios en el working copy.

**9. ¿Qué comando o comandos utilizaste en el paso 28?**

        * git reflog paar saber hacia donde debo situarme
        * git checkout 4dd3ff

**10. ¿Qué comando o comandos utilizaste en el paso 29?**

        * git branch -D title

**11. ¿Qué comando o comandos utilizaste en el paso 30?**

        * git reflog para buscar el identificador del merge a rehacer
        * git checkout master para asegurarnos de estar en la rama "master"
        * git reset --hard 7b24f05  para restaurar el commit donde se realiza el merge

**12. ¿Qué comando o comandos usaste en el paso 32?**

        * git reflog
        * git reset cbcf95a

**13. ¿Qué comando o comandos usaste en el punto 33?**

        * git reflog
        * git checkout 4dd3ffe  para ir al último commit de la rama title con los cambios del título
        * Debido a que aunque estoy en el lugar adecuado estoy en detached HEAD vuelvo a crear la rama "title" con git branch title. Luego de la misma forma sig$
        * git checkout 7b24f05 y git branch styled
        * git checkout 47b9659 y git branch htmlify
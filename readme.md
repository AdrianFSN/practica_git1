# Ejercicio 1 Git. Preguntas:
## ¿Qué comando utilizaste en el paso 11? ¿Por qué?
He utilizado git reset --hard HEAD~1.

Porque necesitaba deshacer los cambios tanto en el grafo como en el Working Copy. Además, podía retroceder desde la rama Styled a HEAD~1 sin problemas, porque esa rama no había avanzado más padres en la línea de commits.

## ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
He utilizado git reflog para identificar el commit al que quería volver.

He utilizado git reset (*id de dicho commit*) para llegar hasta él.

He empleado git status y git diff para ver los cambios que había perdido en el Working Copy de la rama styled.

He usado git restore para recuperar mis cambios.

## El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No me ha causado conflicto porque la rama styled tiene acceso a todos los padres de la rama main. El merge entre las ramas styled y main es un fast forward y en ese caso no se generan conflictos.

## El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Sí. Porque en este caso el merge es not fast forward y los cambios en el contenido del archivo git-nuestro se hacen desde dos ramas diferentes, en las mismas líneas y en el mismo fichero. La rama styled no tiene acceso al commit hecho sobre la rama htmlify.

## El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No ha causado ningún conflicto porque ha vuelto a ser un merge fast forward en el que la rama styled tenía acceso a todos los padres anteriores.

## ¿Qué comando o comandos utilizaste en el paso 25?
He utilizado git log --graph

## El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
Sí, porque la rama title tenía acceso al padre de la rama main.

## ¿Qué comando o comandos utilizaste en el paso 27?
He usado git reflog para identificar el id del paso anterior al commit del merge entre main y title.

He usado git reset (*id del log*) para volver al estado de la rama main en ese punto, sin afectar al Working Copy.

## ¿Qué comando o comandos utilizaste en el paso 28?
He usado git status para comprobar si había cambios pendientes en el archivo git-nuestro.

He usado git restore para descartar los cambios.

## ¿Qué comando o comandos utilizaste en el paso 29?
He empleado git branch -D (*nombre de la rama*).

## ¿Qué comando o comandos utilizaste en el paso 30?
He usado git reflog para encontrar el id del commit en el que consolidé la rama title original y sus cambios.

He usado git checkout (*id de dicho commit*) para colocar el puntero HEAD en esa posición.

He empleado git branch title para crear la nueva rama title en la posición de HEAD.

He utilizado git checkout title para que HEAD dejase de estar detached y apuntase a title, que ha asimilado los cambios asociados a la rama original que había sido borrada.

Una vez que he restaurado la rama title, he usado git checkout main para cambiar a main.

He empleado git merge title para repetir el merge anterior y comprobar que se podía hacer el merge fast forward.

## ¿Qué comando o comandos usaste en el paso 32?
He usado git log para encontrar el id del commit inicial.

He utilizado git reset --hard (*id del commit*) para devolverlo todo al commit inicial.

## ¿Qué comando o comandos usaste en el punto 33?
He usado un git reflog para encontrar el id del commit en el que puse el título al archivo git nuestro.

He usado un git reset (*id del commit*) para volver a ese punto.

He usado un git restore (*archivo*) para restaurar el archivo git nuestro.
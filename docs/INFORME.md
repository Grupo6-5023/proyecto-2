1. ¿Por qué el segundo push del apartado 2.2 fue rechazado? ¿Qué dos operaciones hace `git pull` por debajo?
    El segundo push falla porque main habia avanzado un commit más de lo que la versión contenía.
    Git fetch para descargar los commits que no se tienen en local y git merge para juntarlos con lo existente.

2. En vuestro historial, señalad un merge *fast-forward* y un *merge commit*. ¿Qué los diferencia?
    La primera PR del 2.4 sería un merge fast-forward porque la rama main no había recibido cambios desde la creación de esta rama.
    Las otras dos PR del mismo punto serían merge commit porque la PR anterior había alterado main.
    En fast forward no hay conflictos mientras que en merge commit te pide que elijas con que parte del codigo quedarte de la diferencia entre main y la rama nueva.

3. ¿Por qué rellenar filas distintas de la tabla no dio conflicto y cambiar `Última revisión` sí?
    Porque la edición de las filas era en partes separadas del codigo, mientras que en ultima revisión era todo sobre la misma linea de codigo.

4. Pegad el mensaje de error del push a `main` protegida y explicad qué regla lo ha bloqueado.
    [remote rejected] master -> master (protected branch hook declined)
    La regla Require a pull request before merging.

5. ¿Qué comando sacó `.env` del control de versiones sin borrarlo? ¿Por qué la contraseña sigue siendo un problema y qué haríais en un proyecto real? (Pista: la respuesta empieza por lo que hay que hacer con la contraseña, no con el historial.)
    git rm --cached .env
    Cambiar la contraseña, añadir .env a gitignore y limpiar el historial.

6. ¿Qué hace mejor GitHub Desktop que la terminal, y qué no puede hacer? ¿Con cuál habéis entendido mejor el conflicto?
    El hecho de tener una interfaz gráfica permite ver con facilidad lo que se hace y lo que se ha hecho, cambiar de ramas y hacer los commits, pulls y pushes de manera mas sencilla. También permite resolver los conflictos de manera mas visual.
    Algunas operaciones avanzadas como rebase, cherry-pick o limpiar el historial.
    Hemos entendido mejor el conflicto en Desktop.
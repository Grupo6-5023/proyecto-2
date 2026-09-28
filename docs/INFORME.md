1. ¿Por qué el segundo push del apartado 2.2 fue rechazado? ¿Qué dos operaciones hace `git pull` por debajo?
    El segundo push falla porque main habia avanzado un commit más de lo que la versión contenía.
    Git fetch para descargar los commits que no se tienen en local y git merge para juntarlos con lo existente.
2. En vuestro historial, señalad un merge *fast-forward* y un *merge commit*. ¿Qué los diferencia?
    La primera PR del 2.4 sería un merge fast-forward porque la rama main no había recibido cambios desde la creación de esta rama.
    Las otras dos PR del mismo punto serían merge commit porque la PR anterior había alterado main.
    En fast forward no hay conflictos mientras que en merge commit te pide que elijas con que parte del codigo quedarte de la diferencia entre main y la rama nueva.
3. ¿Por qué rellenar filas distintas de la tabla no dio conflicto y cambiar `Última revisión` sí?
    Porque la edición de las filas era en partes separadas del codigo, mientras que en ultima revisión era todo sobre la misma linea de codigo.
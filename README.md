# panda-sharks-attack
Cleaning data 

- 25722 rows 
- Analizing the rows:
Desde la fila 25722 hasta la 8701, todos los campos aparecen como "NaN" en todas las columnas.
En la fila 8701 todos los campos siguen como NaN, si embargo, en la columna "Case Number" empiezan a aparecer registros "0"
Desde 8701 hasta 6302 todos los cases number son 0 y el resto NaN

df.loc[:] analizamos el contenido de las filas
Esto se consigue con comandos `add` que especifican esos archivos y un commit para confirmar:
```
git add *.c
git add LICENSE
git commit -m "Initial commit"
```

Te devuelve una salida descriptiva: indica qué [[Rama]] has modificado, que checksum [[Hash SHA-1]] tiene el commit, cuántos archivos han cambiado y estadísticas sobre las líneas añadidas y eliminadas en el commit.

Si solo ejecutamos `git commit`, nos abrirá el editor de preferencia, ya sea el predeterminado del sistema (variable $EDITOR de la terminal) o el configurado por [[Estableciendo el editor de texto por defecto para Git]]. El mensaje de confirmación por defecto contiene la última salida del comando git status comentada y una línea vacía encima de ella.

Podemos añadir el texto de confirmación directo desde terminal con:
```
git commit -m "Mi comentario"
```

Si quieres ver explícitamente lo que modificaste, puedes ejecutar:
```
git commit -v
```

Si quieres saltarte el área de preparación, añade -a al comando git commit, lo que hará que Git prepare automáticamente todos los archivos rastreados antes de confirmarlos, ahorrando el paso git add.
```
git commit -a -m "Mis cambios"
```
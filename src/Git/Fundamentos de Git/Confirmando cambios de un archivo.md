Esto se consigue con comandos `add` que especifican esos archivos y un commit para confirmar:
```
git add *.c
git add LICENSE
git commit -m "Initial commit"
```

Si solo ejecutamos `git commit`, nos abrirá el editor de preferencia, ya sea el predeterminado del sistema (variable $EDITOR de la terminal) o el configurado por [[Estableciendo el editor de texto por defecto para Git]]. El mensaje de confirmación por defecto contiene la última salida del comando git status comentada y una línea vacía encima de ella.

Podemos añadir el texto de confirmación directo desde terminal con:
```
git commit -m "Mi comentario"
```
```

Si quieres ver explícitamente lo que modificaste, puedes:
```
git commit -v
```
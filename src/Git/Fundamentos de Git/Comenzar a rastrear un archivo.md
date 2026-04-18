Usa `git add`.
```
git add
```
Los archivos aparecen como "Changes to be committed" cuando ejecutas el comando para [[Determinar el estado de cada archivo]].

`git add` Puede recibir tanto una ruta de archivo como de un directorio. Si es de un directorio, añade todos los archivos de forma recursiva.

Puedes acortar la salida usando:
```
git status -s

O

git status --short
```

Los estados se representan como:
- `??` Para los archivos nuevos que no están rastreados 
- `A` para los archivos que están preparados 
- `M` para los archivos que están modificados 
El estado se muestra en dos columnas, en donde la columna de la izquierda indica el estado preparado del archivo y la columna de la derecha indica el estado sin preparar del mismo archivo.
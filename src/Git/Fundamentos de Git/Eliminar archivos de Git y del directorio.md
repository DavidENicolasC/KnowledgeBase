Usa `git rm`. Puedes pasarle  archivos, directorios y patrones glob.
```
git rm Archivo.extension
```
Si habías preparado cambios de ese archivo en tu [[Área de Preparación (Staging Area)]], tendrás que forzar su eliminación con la opción `-f`.

Si solo eliminas el archivo de tu [[Directorio de Trabajo (Working Directory)]], aparecerá dentro de `Changes not staged for commit`. Con `git rm`, preparas su eliminación.

Si quieres mantener el archivo en tu directorio de trabajo pero eliminarlo del área de preparación, utiliza la opción `--cached`.
```
git rm --cached
```
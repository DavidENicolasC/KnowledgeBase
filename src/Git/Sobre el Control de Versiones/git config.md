Te permite obtener y establecer variables de configuración que controlan el aspecto y funcionamiento de Git.

Éstas pueden almacenarse en tres sitios distintos:
- [[Archivo etc gitconfig]]
- [[Archivo gitconfig o config git config]]
- [[Archivo config en el directorio de Git del repositorio actual]]

Cada uno sobrescribe los valores del nivel anterior.

Puedes ver los valores configurados cuando [[Estableciendo el autor de los commits]] y [[Estableciendo el editor de texto por defecto para Git]] con `--list`.
```
git config --list
```

Pueden haber claves repetidas por los múltiples lugares donde puedes establecer la configuración. Los últimos valores serán los usados.

Puedes comprobar cada valor usado consultándolo, por ejemplo:
```
git config user.name
```
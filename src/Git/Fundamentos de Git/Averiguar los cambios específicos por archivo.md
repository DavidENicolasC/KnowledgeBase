Usa `git diff`.

Compara lo que tienes en tu [[Directorio de Git (Git Directory)]] con lo que está en el [[Área de Preparación (Staging Area)]].

Al llamar a git diff sin parámetros no verás los cambios desde tu última confirmación - sólo verás los cambios aún no preparados. Puede ser confuso, por que si lo ejecutas y preparaste todos los cambios de tu directorio de trabajo, no te devolverá ninguna salida.

Si quieres ver lo que has preparado y será incluido en la próxima confirmación, utiliza `git diff --staged`.

Si quieres ver lo que has preparado hasta ahora, usa `git diff --cached`.
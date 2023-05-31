# **replacer**
**replacer** es un pequeño script PHP pensado para reemplazar patrones construidos con expresiones regulares por cadenas, en múltiples ficheros.
## Requisitos:
Necesitas tener instalado en tu Linux el CLI de PHP.
## Instalación:
```
git clone https://github.com/richi-rm/replacer.git
cd replacer
./install.sh
```
install.sh instalará replacer en /usr/local/bin
## Ejemplos de uso:
Reemplazar 'a' por '*' en el fichero de texto file.txt:
```
replacer 'a' '*' file.txt
```
Reemplazar '<?' seguido de salto de línea por '<?php' seguido de salto de línea, en todos los ficheros PHP del directorio actual y sus subdirectorios:
```
find . -type f -name '*.php' -exec replacer "<\?\n" "<?php\n" {} \;
```
## Bugs y sugerencias:
Envía tus comentarios a: Ricardo Ruiz Martínez <richiruizmartinez@gmail.com>

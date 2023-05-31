# **replacer**
**replacer** es un pequeño script PHP pensado para reemplazar patrones construidos con expresiones regulares por cadenas, en múltiples ficheros. En concreto puedes usarlo para encontrar patrones multilínea en ficheros y sustituir las ocurrencias por una cadena. La motivación de hacer este script es porque usar sed o awk para encontrar patrones multilínea es difícil, este script te hace la vida más fácil.
## Requisitos:
# **replacer**
**replacer** es un pequeño script PHP pensado para reemplazar patrones construidos con expresiones regulares por cadenas, en múltiples ficheros.
## Requisitos:
- Necesitas tener instalado el CLI de PHP en tu Linux.
- Necesitas que tu usuario pueda ejecutar sudo.
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
Envía tus comentarios a Ricardo Ruiz Martínez <richiruizmartinez@gmail.com>
¡Gracias!

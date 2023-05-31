# **replacer**
**replacer** is a small PHP script designed to replace patterns built with regular expressions by strings, in multiple files. Specifically, you can use it to find multiline patterns in files and replace the occurrences with a string. The motivation of making this script is because using sed or awk to find multiline patterns is hard, this script makes your life easier.
## Requirements:
- You need to have the PHP CLI installed on your Linux.
- You need your user to be able to run sudo.
## Install:
```
git clone https://github.com/richi-rm/replacer.git
cd replacer
./install.sh
```
install.sh will install replacer in /usr/local/bin
## Examples:
Replace 'a' with '*' in the text file file.txt:
```
replacer 'a' '*' file.txt
```
Replace '<?' followed by newline by '<?php' followed by newline, in all PHP files in the current directory and its subdirectories:
```
find . -type f -name '*.php' -exec replacer "<\?\n" "<?php\n" {} \;
```
## Bugs and comments:
Send your comments to Ricardo Ruiz Martínez <richiruizmartinez@gmail.com>
Thank you!

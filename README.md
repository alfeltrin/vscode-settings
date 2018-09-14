# VSCode settings

## VSCode path:
/Users/alessandro/Library/Application Support/Code/User/

## PHP coding standard install

#### COMPOSER
Installazione ```curl -sS https://getcomposer.org/installer | php```

Creare o modificare il file **~/.bash_profile** (oppure se si usa zsh **~/.zshrc**) e aggiungere la riga seguente
```alias composer="php /usr/local/bin/composer.phar"```

#### PHPCS
Installazione dalla cartella home dell'utente ```composer global require "squizlabs/php_codesniffer=*"```

Aggiungere il percorso alla shell path:
```
cat << EOF >> ~/.bash_profile
export PATH="$PATH:~/.composer/vendor/bin"
EOF
```

Oppure se si usa zsh:
```
cat << EOF >> ~/.zshrc
export PATH="$PATH:~/.composer/vendor/bin"
EOF
```

Aggiungere il soft link ```ln -s ~/.composer/vendor/bin/phpcs /usr/local/bin/phpcs```

Installare estensione **phpcs**

#### PHP-CS-FIXER
Installazione ```composer global require friendsofphp/php-cs-fixer```

Aggiungere nelle impostazioni di VSCode ```"php-cs-fixer.executablePath": "~/.composer/vendor/bin/php-cs-fixer"```

Installare estensione **php-cs-fixer**

#### Standard utilizzato
PSR2

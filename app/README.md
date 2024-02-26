for phpmyadmin
 http://localhost:9001/
 Username : symfony
 Password:  symfony

for symfony project
 http://localhost:8080



Debug -  Symfony: command not found
Solution
Add the following line to your shell configuration file:

export PATH="$HOME/.symfony/bin:$PATH" 
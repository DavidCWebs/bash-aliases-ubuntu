# bash-aliases-ubuntu
Some handy aliases - add to `~/.bash_aliases` and require this in `~/.bashrc`.

~~~
# Apache
# ==============================================================================
alias restart-apache="sudo /etc/init.d/apache2 restart"
alias reload-apache="sudo /etc/init.d/apache2 force-reload"
alias docroot="cd /var/www/html; ll"

# SSH
# ==============================================================================
alias restart-ssh="sudo service ssh restart"
alias reload-ssh="sudo service ssh restart"

# Upgrades
# ==============================================================================
alias supdate="sudo apt-get update && sudo apt-get upgrade"

# Fail2Ban: note Jail names and add IP address
# See: https://www.fail2ban.org/wiki/index.php/Commands
# ==============================================================================
alias reload-fail2ban="fail2ban-client reload"
alias stop-fail2ban="fail2ban-client stop"
alias start-fail2ban="fail2ban-client start"
alias status-fail2ban="fail2ban-client status"
alias unban-home="sudo fail2ban-client set wordpress-soft unbanip X.X.X.X; fail2ban-client set wordpress-hard unbanip X.X.X.X"
~~~

apt
– package manager used to install, update, and remove software
– works with trusted repositories only

apt update
– refreshes the list of available packages
– does not install or change anything
– tells the system which versions exist

apt list --upgradable
– shows packages that have newer versions available
– informational only

apt upgrade
– upgrades already installed packages
– does not install new ones
– does not remove existing ones

apt install <package>
– installs a new package
– checks dependencies
– shows what will change before installing

tree package
– command-line tool
– installs a single command (tree)
– no service
– does not run in the background
– no logs

installing the tree package gives you
– binary file in /usr/bin/tree
– manual page (man tree)

apt remove <package>
– removes a package
– keeps configuration files

apt purge <package>
– removes a package and its configuration

apt autoremove
– removes unused dependencies
– used to keep the system clean

openssh-server package
– package that installs the SSH server
– different from the SSH client (ssh command)
– installs a service, configuration, and logging

difference between SSH client and server
– SSH client: you connect to other systems
– SSH server: others connect to your system

systemd
– main service manager
– knows which services exist
– starts, stops, and monitors them

systemctl
– command-line tool to control systemd
– does not see packages
– only sees registered services

service
– program that runs in the background
– has a status
– can be started, stopped, restarted
– writes logs

systemctl status <service>
– shows whether a service exists
– shows whether it is running
– displays recent logs

Active: active (running)
– service is running normally

Active: inactive (dead)
– service is not running, no error

Active: failed
– service failed to start or crashed

systemctl start <service>
– starts a service manually

systemctl stop <service>
– stops a service

systemctl restart <service>
– restarts a service
– commonly used after config changes

systemctl enable <service>
– enables automatic start on system boot

systemctl disable <service>
– disables automatic start on boot

enable vs start
– start: runs the service now
– enable: runs the service after reboot

socket activation
– systemd listens on a port
– service starts only when needed
– service may be inactive but still functional

journalctl
– central logging system
– stores system and service events

journalctl -u <service>
– shows logs for a specific service

journalctl -u <service> -n 20
– shows the last 20 log entries

journalctl -u <service> -f
– follows logs in real time

journalctl -u <service> --since today
– shows logs from today

journalctl -u <service> --since "1 hour ago"
– shows logs from a specific time range

systemctl tells you whether something is running
journalctl tells you why it is or is not running

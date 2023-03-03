## apt
```bash
# search
apt search <PACKAGE> # based on name / description / other
apt list | grep -i <package> # based on name

# install
apt install <PACKAGE>

# uninstall
apt remove <PACKAGE> #binaries
apt purge <PACKAGE> #binaries + configs (except in /home/)
apt purge --auto-remove <PACKAGE> #binaries + configs (except in /home/) + dependencies

# list installed
apt list --installed
apt list --installed | grep -i <PACKAGE>
dpkg -l
dpkg -l | grep -i <PACKAGE>

# update
apt list --upgradeable # list updateable
apt update
apt upgrade
apt upgrade <PACKAGE>
```

## pip
```bash
apt install python3-pip

# search
python3 -m pip search <PACKAGE>

# install
python3 -m pip install <PACKAGE>

# uninstall
python3 -m pip uninstall <PACKAGE>

# list installed
python3 -m pip list
python3 -m pip list | grep -i <PACKAGE>
python3 -m pip freeze
python3 -m pip freeze | grep -i <PACKAGE>

# update
python3 -m pip list --outdated # list updateable
python3 -m pip list --outdated --format=freeze | grep -v '^\-e' | awk -F'==' '{print$1}' | xargs -n1 pip install -U
python3 -m pip install -U <PACKAGE>
```

## pipx
```bash
apt install pipx
pipx ensurepath

# search (use pip)
python3 -m pip search <PACKAGE>

# install
pipx install <PACKAGE>

# uninstall
pipx uninstall <PACKAGE>

# list installed
pipx list
pipx list | grep -i <PACKAGE>

# update
pipx upgrade-all
pipx upgrade <PACKAGE>
```

## Deprecated
* pipsi
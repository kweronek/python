# Grundinstallation python
## Ubuntu
```
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.9
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.8 1
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.9 2
python --version
```
## Mac
### Grundsätzlich
```
brew install python
```

### optional
## Raspberry PI
tbd
## Windows
tbd


# IDEs
## pyCharm (empfohlen)
## Visual Studio Code (optional)
```linux
brew install visual-studio-code
```
## Textmate (informell)

# Pythonpakete
## Paket- und Environment-Manager
### Paketmanager pip (obligatorisch)
gehört zu Python, wird bei brew mitinstalliert by Unix:
```
sudo apt update
sudo apt install python3-pip
```
### Paket- und Environment-Manager pipenv
### Environment-Manager virtualenv/venv (obligatorisch)
```
pip install virtualenv
```
#### basic usage
```
cd project_folder
virtualenv myvenv
```
### Paket- und Environment-Manager pipenv
```
pip install --user pipenv
```
### Environment-Manager pyenv
```
brew install python pyenv
```

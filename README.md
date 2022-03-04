# Grundinstallation python
## Ubuntu (obligatorisch)
```
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.9
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.8 1
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.9 2
python --version
```
## Mac
```
brew install python
```
### optional
## Raspberry PI
tbd
## Windows
tbd
## Paket- und Environment-Manager
### Paketmanager pip (obligatorisch)
gehört zu Python, wird bei brew mitinstalliert by Unix:
```
sudo apt update
sudo apt install python3-pip
```
### Environment-Manager virtualenv/venv (obligatorisch)
```
pip install virtualenv
```
#### basic usage
```
cd project_folder
virtualenv myvenv
```
### Paket- und Environment-Manager pipenv (optional)
```
pip install --user pipenv
```
### Environment-Manager pyenv (optional)
```
brew install python pyenv
```

# IDEs
## pyCharm (empfohlen)
## Visual Studio Code (optional)
```linux
brew install visual-studio-code
```
## Textmate (informell)

# Pythonpakete

## Basics
### numpy
### random
### mathplotlib
### collections

## Data scaping
### csv
### beautyfulsoup4
### defusedxml
### json
### PyYAML

## Web
### requests
### django
### flask

## Data Science
### pandas
### statsmodels

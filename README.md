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
## Mac (optional)
```
brew install python
```
## Raspberry PI (optional)
https://allurcode.com/install-latest-version-of-python-on-raspberry-pi/

## Paket- und Environment-Manager
### Paketmanager pip (obligatorisch)
gehört zu Python, wird bei brew mitinstalliert by Unix:
```
sudo apt update
sudo apt install python3-pip
```
### Environment-Manager virtualenv/venv (obligatorisch)
Voraussetzung pip installiert.
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
https://www.jetbrains.com/help/pycharm/installation-guide.html

## Visual Studio Code (optional)
Auf Ubuntu:
sudo snap install --classic code

Auf MAC:
```linux
brew install visual-studio-code
```
andere:
https://code.visualstudio.com/

## Textmate (nur MAC, informell)
```
brew install --cask textmate
```

# Pythonpakete

## Basics
### time (empfohlen)
### numpy (empfohlen)
### random (bei Bedarf)

## Grafik
### mathplotlib (empfohlen)
### Bokeh (informell)

## Web
### django (obligatorisch)
### flask (bei Bedarf)

## Network
### socket
### socketserver
### requests (obligatorisch)
### http
### ssl
### grpc (obligatorisch)

## Data scraping
### defusedxml  (obligatorisch)
### json (obligatorisch)
### PyYAML (obligatorisch)
### csv (informell)
### html.parser (informell)
### beautyfulsoup4 (informell)

## Persistance
### sqlite3 

## Data Science
Voraussetzung: 
### pandas
### statsmodels
### SciPy
### skykit-learn
Voraussetzung: numpy, pandas, mathplotlib
### MlPy
Voraussetzung: numpy, pandas, mathplotlib
### NLTK
### theano
### Tensorflow
### PyTorch
### Keras
### LightGBM

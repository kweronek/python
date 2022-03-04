# Grundinstallation python
Dies ist ein Spickzettel für Python. Es wird auf Version 3 focussiert. Ist Version 2 erforderlich wird darauf hingewiesen.
Im Zweifelsfall wird eine Plattform-unabhängige Installationsvariant angegeben. Ggf. wird per link auf spezifische Varianten hingewiesen (Ausnahme brew).
Installationsangaben beziehen sich auf Ubuntu und MacOS.
Windows wird von hier nicht unterstütz, ist aber in den meisten Fällen möglich.

Empfehlung alias python=python3

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
Der Paketmanager pip gehört zu Python, wird bei brew python mitinstalliert, bei Linux comme-ci comme-ca.
```
python3 -m pip install --user --upgrade pip
```
In order to keep your environment consistent, it’s a good idea to “freeze” the current state of the environment packages. To do this, run:
```
pip freeze > requirements.txt
```
This will create a requirements.txt file, which contains a simple list of all the packages in the current environment, and their respective versions. You can see the list of installed packages without the requirements format using pip list. Later it will be easier for a different developer (or you, if you need to re-create the environment) to install the same packages using the same versions:
```
pip install -r requirements.txt
```
This can help ensure consistency across installations, across deployments, and across developers.

### Environment-Manager venv (obligatorisch)
Voraussetzung pip installiert. (Anm. für Pyhton2 verwende virtualenv)
```
python3.9 -m pip install --user virtualenv
pip install virtualenv
```
#### basic usage
To create a virtual environment, head to your project directory and run the following command.
```
python -m venv venv
```
Before using your virtual environment on your project, you need to activate it using
```
source venv/bin/activate
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

Auf openSuSe

Auf MAC:
```linux
brew install visual-studio-code
```
andere:
https://code.visualstudio.com/

# Pythonpakete
Die Packages der Python-Standard-Library findet man hier.
Fast alle anderen Packages finden sich hier. 
## Basics
### time (empfohlen)
Das Package time enthält Standardzeitfunktionen, jedoch keine Datums- und Echtzeitdaten.
### numpy (empfohlen)
Das Package numpy enthält im wesentlichen numerische Arrays.
### random (bei Bedarf)
Das Package random enthält diverse Funktionen zur Erzeugung von (Pseudo-)Zufallszahlen.

## Grafik
### mathplotlib (empfohlen)
### Bokeh (informell)

## Web
### django (obligatorisch)
Das Package [django](django/README.ms) ist für die Entwicklung von Frontends gut geeignet.
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

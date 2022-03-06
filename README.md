# Grundinstallation python
Dies ist ein Spickzettel für Python. Es wird auf Version 3 focussiert. Ist Version 2 erforderlich wird darauf hingewiesen.
Im Zweifelsfall wird eine Plattform-unabhängige Installationsvariant angegeben. Ggf. wird per link auf spezifische Varianten hingewiesen (Ausnahme brew).
Installationsangaben beziehen sich auf Ubuntu und MacOS.
Windows wird von hier nicht unterstützt, ist aber in den meisten Fällen möglich.

Empfehlung: ```alias pyt=python3

## Ubuntu (obligatorisch)
Ubuntu 20.04 LTS hat bereits vorinstalliert python 2.7.18 und pyton 3.8.10 .
Aktuell (3/2022) scheint 3.9.10 sinnvoll.
Der Paket-Manager pip3 ist auf Ubuntu 20.04 noch tricky zu installieren. Siehe:
https://cloudbytes.dev/snippets/upgrade-python-to-latest-version-on-ubuntu-linux
```
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.9
sudo apt install python3.10
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.8 4
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.9 5
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.10 3
python3 --version
```
Versionen umschalten mit:
```
sudo apt install python3.10
sudo update-alternative --config python3
````
## Mac (optional)
```
brew install python
```
## Raspberry PI (optional)
https://allurcode.com/install-latest-version-of-python-on-raspberry-pi/

# Paket- und Environment-Manager
## Paket-Manager pip (obligatorisch)
Der Paketmanager pip gehört zu Python, wird bei brew python mitinstalliert, bei Linux comme-ci comme-ca, ansonsten:
```
sudo apt install python3-pip
pip3 --version
```
### Installation von Paketen mit pip3
```
python3 -m <modulname> install pip3
```

Alle installierten Pakete anzeigen:
```
pip3 list
```


In order to keep your environment consistent, it’s a good idea to “freeze” the current state of the environment packages. To do this, run:
Aktuelle Konfiguration anzeigen und speichern:
```
pip3 freeze > requirements.txt
```
This will create a requirements.txt file, which contains a simple list of all the packages in the current environment, and their respective versions. You can see the list of installed packages without the requirements format using pip list. Later it will be easier for a different developer (or you, if you need to re-create the environment) to install the same packages using the same versions:
```
pip3 install -r requirements.txt
```
This can help ensure consistency across installations, across deployments, and across developers.

Zum deinstallieren:
```
pip3 -m <paketname> deinstall
```
## Environment-Manager venv/virtualenv (obligatorisch)
Voraussetzung pip installiert. (Anm. für Python2 verwende virtualenv)
```
python3 -m pip install --user virtualenv
pip3 install virtualenv
```
### Verwendung
To create a virtual environment, head to your project directory and run the following command.
```
python3 -m venv myvenv
```
Before using your virtual environment on your project, you need to activate it using
```
source myvenv/bin/activate
```
Zum Deaktivieren von virtuellen Environments:
```
source myvenv/bin/deactivate
```

## Paket- und Environment-Manager pipenv (optional)
```
pip3 install --user pipenv
```
## Environment-Manager pyenv (optional)
```
brew install python3 pyenv
```

# IDEs
## pyCharm (empfohlen)
https://www.jetbrains.com/help/pycharm/installation-guide.html

## Visual Studio Code (optional)
Auf Ubuntu:
```
sudo snap install --classic code

Auf MAC:
```linux
brew install visual-studio-code
```
andere:
https://code.visualstudio.com/

# Python-Pakete
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
Das Package [django](django/README.md) ist für die Entwicklung von Frontends gut geeignet.
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

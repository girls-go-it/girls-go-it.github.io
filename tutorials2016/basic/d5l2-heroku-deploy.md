---
layout: default
title: Heroku Deploy
category: basic
---

# Heroku Deployment

###### Cuvinte cheie:

* mediu de rulare (environment)
* rulare (running)
* configurare
* repository

## Ce este deployment?

Deployment este procesul ce include instalarea, configurarea, rularea si testarea unui produs software, ce are ca scop rularea propriu-zisa a produsului nou in mediul lui de rulare.

## Hosting

Serviciul de hosting este un serviciu care ruleaza servere in internet, ce ofera posibilitatea de a face serviciile lor accesibile in internet. Cel mai comun tip de hosting este *web hosting* care permite rularea website-urilor si accesul lor de catre utilizatori.

Sunt mai multe companii care ofera servicii de hosting, si mai multe tipuri de servicii de a face website-urile accesibile. De exemplu, sunt servicii care ofera doar spatiu de memorie pentru website, altele care ofera un server cu memorie, altele care ofera infrastructura care are ofera un mediu gata pentru deployment, direct, si cateva servicii de configurare. 

## Heroku Deployment

Heroku este un serviciu care ofera un mediu prestabilit, si este gratis pentru utilizatorii care au cel mult 5 aplicatii web. Pentru a folosi acest serviciu este nevoie de a te inregistra pe link-ul de 

[aici](https://www.heroku.com/).

Deasemenea, este nevoie de instalat un program care sa ruleze la noi in calculator. Astfel, vom descarca Heroku Toolbelt de pe acest 

[link](https://toolbelt.heroku.com/windows)

Dupa ce am descarcat fisierul executabil de pe website, il rulam si instalam ca pe un program obisnuit pe windows. Un exemplu de cum ar trebui sa arate este in imaginea urmatoare:

![Install Heroku Toolbelt](/images/www/install_toolbelt_heroku.png)

Dupa ce am instalat Heroku Toolbelt, cautam cmd in comanda start de la windows si alegem pe cea care spune "Command Line with Ruby"
Inainte de toate trebuie de instalat cateva pachete care ne vor ajuta sa facem deployment la aplicatie. In proiectul nostru scrim comenzile pe rand:

```sh
pip install gunicorn
pip install whitenoise
```

Dupa care scrim comanda:

```sh
heroku login
```

Trebuie sa ne apara urmatoarele afirmatii:

```sh
Enter your Heroku credentials.
Email:
```

Introducem email-ul cu care ne-am inregistrat pe website, mai intai. Apoi introducem parola cand apare cuvantul "password". E important de tras atentie la faptul ca nimic nu va fi afisat in linia de comanda in timp ce introduceti parola.

Iar acum vom lucra la procesul propriu-zis de deployment. Primul lucru inainte de a face deployment la proiect este de a crea un fisier `requirements.txt`, pe care serviciul heroku il va utiliza pentru a instala toate pachetele utilizate pentru rularea websiteului nostru cum ar fi Django, gunicorn si whitenoise in cazul nostru. Deci, fiind in directoria(mapa) proiectului nostru scrim comanda:

```sh
pip freeze > requirements.txt
```

Deasemenea, este nevoie de un fisier care va indica care versiune de python va fi folosita. La fel in directoria proiectului cream un fisier nou `runtime.txt` si introducem in felul urmator versiunea de python pe care e scris proiectul nostru.

```sh
python-3.5.1
```

## Procfile
Procfile este un fisier de tip text care, ca si celelalte, se afla in directoria principala a proiectului, ce defineste tipurile de procese si declara explicit ce comenzi trebuie executate pentru a rula aplicatia noastra pe server. Asadar cream un fisier "Procfile", si scrim in felul urmator:

```
web: gunicorn schoolproject.wsgi:application --log-file -
```


Deasemenea, mai avem de facut cateva configurari, pentru a face deploymentul fara erori. Astfel in fisierul "schoolproject/schoolproject/settings.py" adaugam urmatoarele linii de cod:

```python
PROJECT_ROOT = os.path.dirname(os.path.abspath(__file__))

STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles')
# Extra places for collectstatic to find static files.
STATICFILES_DIRS = (
    os.path.join(PROJECT_ROOT, 'static'),
)

STATICFILES_STORAGE = 'whitenoise.storage.CompressedManifestStaticFilesStorage'
```

Si in fisierul "schoolproject/schoolproject/wsgi.py" adaugam 2 linii de cod astfel incat fisierul sa arate astfel:

```python
import os

from django.core.wsgi import get_wsgi_application

os.environ.setdefault("DJANGO_SETTINGS_MODULE", "rtscheduler.settings")

from whitenoise.django import DjangoWhiteNoise

application = get_wsgi_application()
application = DjangoWhiteNoise(application)
```

Si mai este nevoie de a crea o directorie pentru a asigura utilizarea fisierelor statice asa ca imaginile, fisierele .css si .javascript.
Asadar, dupa exemplul de mai jos creati fisierele ca in imaginea urmatoare:

![Directoriu static in directoriu principal al proiectului](/images/www/static_creation_deploy.png)

Pentru a face posibil deployment-ul a mai multe versiuni, iterativ a websiteului este nevoie de utilizat un sistem care sa aiba grija de versionarea codului in mod corect. Cel mai raspandit sistem de versiune in prezent este GIT. De aceea deployment-ul pe platforma heroku este utilizat GIT ca forma de actualizare a aplicatiei web.

Structura aplicatie voastre trebuie sa arate in felul urmator:

![Structura aplicatiei](project_deploy.png)

Astfel pentru a initia repositoria scrim in linia de comanda:

```sh
git init
```

Cream un fisier `.gitignore` in directoria principala a proiectului si in el scrim:

```sh
venv
*.pyc
staticfiles
.env
```

Dupa care scrim urmatoarele comenzi:

```sh
git add .
git commit -m "Initial commit"
```

Dupa care mai scrim inca o data comanda `heroku login` si ne logam.

Iar acum vom crea aplicatia noastra pe heroku cu urmatoarea comanda:

```sh
heroku create
```

Dupa care trimitem informatia websiteului pe serverul platformei Heroku:

```sh
git push heroku master
```

Dupa ce ati scris `heroku create` a aparut un text ce arata in felul urmator:

```sh
Creating intense-falls-9163... done, stack is cedar
http://intense-falls-9163.herokuapp.com/ | git@heroku.com:intense-falls-9163.git
Git remote heroku added
```

Dupa cum vedeti denumirea aplicatiei in heroku este creata automat si nu coincide cu denumirea care vrem sa o punem noi. Din aceasta cauza este nevoie de a o schimba. 
Noi o vom schimba cu urmatoarele comenzi, analogic scriind numele aplicatiei noastre in loc de "myschoolproject" si cu numele dat de heroku in linia de comanda proprie in loc de "intense-falls-9163":

```sh
heroku apps:rename girlsgoit --app intense-falls-9163
```

Dupa tot acest proces veti putea sa accesati websiteul vostru la adresa:

```
http://denumiresite.heroku.com
```

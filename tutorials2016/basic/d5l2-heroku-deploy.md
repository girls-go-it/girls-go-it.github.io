---
layout: default
title: Heroku Deploy
category: basic
---

#Heroku Deployment

######Cuvinte cheie:

* mediu de rulare (environment)
* rulare (running)
* configurare

###Ce este deployment?

Deployment este procesul ce include instalare, configurarea, rularea si testarea unui produs software, ce are ca scop rularea propriu-zisa a produsului nou in mediul lui de rulare.

###Hosting

Serviciul de hosting este un serviciu care ruleaza servere in internet, ce ofera posibilitatea de a face serviciile lor accesibile in internet. Cel mai comun tip de hosting este *web hosting* care permite rularea website-urilor si accesul lor de catre utilizatori.

Sunt mai multe companii care ofera servicii de hosting, si mai multe tipuri de servicii de a face website-urile accesibile. De exemplu, sunt servicii care ofera doar spatiu de memorie pentru website, altele care ofera un server cu memorie, altele care ofera infrastructura care are ofera un mediu gata pentru deployment, direct, si cateva servicii de configurare. 

Heroku este un serviciu care ofera un mediu prestabilit, si este gratis pentru utilizatorii cu website. Pentru a folosi acest serviciu este nevoie de a te inregistra pe link-ul de [aici](https://www.heroku.com/).

Deasemenea, este nevoie de instalat un program care sa ruleze la noi in calculator. Astfel, vom downloada Heroku Toolbelt de pe acest [link](https://toolbelt.heroku.com/windows)

Dupa ce am descarcat fisierul executabil de pe website, il rulam si instalam ca pe un program obisnuit pe windows. Un exemplu de cum ar trebui sa arate este in imaginea urmatoare:
![Install Heroku Toolbelt](/images/www/install_toolbelt_heroku.png)

Dupa ce am instalat Heroku Toolbelt, cautam cmd in comanda start de la windows si alegem pe cea care spune "Command Line with Ruby"
Inainte de toate trebuie de instalat cateva pachete care ne vor ajuta sa facem deployment la aplicatie. Scrim comenzile pe rand:
```
pip install gunicorn
pip install whitenoise
```

Dupa care scrim comanda:
```heroku login```

Trebuie sa ne apara urmatoarele afirmatii:
```
Enter your Heroku credentials.
Email:
```
Introducem email-ul cu care ne-am inregistrat pe website, mai intai. Apoi introducem parola cand apare cuvantul "password". E important de tras atentie la faptul ca nimic nu va fi afisat in linia de comanda in timp ce introduceti parola.

Iar acum vom lucra la procesul propriu-zis de deployment. Primul lucru inainte de a face deployment la proiect este de a crea un fisier "`requirements.txt`", pe care, serviciul heroku il va utiliza pentru a instala toate pachetele utilizate pentru rularea websiteului nostru cum ar fi Django, gunicorn si whitenoise in cazul nostru. Deci, fiind in directoria(mapa) proiectului nostru scrim comanda:

```
pip freeze > requirements.txt
```

Deasemenea este nevoie de creare a unui fisier care va indica care versiune de python va fi folosita. La fel in directoria proiectului cream un fisier nou "`runtime.txt`" si introducem in felul urmator versiunea de python pe care e scris proiectul nostru.

```
python-3.5.1
```

####Procfile
Procfile este un fisier de tip text care, deasemenea, se afla in directoria principala a proiectului nostru, ce defineste tipurile de procese si declara explicit ce comenzi trebuie executate pentru a rula aplicatia noastra. Asadar cream un fisier "Procfile", si scrim in felul urmator:

```web: gunicorn schoolproject.wsgi:application --log-file -```


Deasemenea, mai avem de facut cateva configurari, pentru a face deploymentul fara erori. Astfel in fisierul "schoolproject/schoolproject/settings.py" adaugam urmatoarele linii de cod:
```
PROJECT_ROOT = os.path.dirname(os.path.abspath(__file__))

STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles')
# Extra places for collectstatic to find static files.
STATICFILES_DIRS = (
    os.path.join(PROJECT_ROOT, 'static'),
)

STATICFILES_STORAGE = 'whitenoise.storage.CompressedManifestStaticFilesStorage'
```

Si in fisierul "schoolproject/schoolproject/wsgi.py" adaugam 2 linii de cod astfel incat fisierul sa arate astfel:
```
import os

from django.core.wsgi import get_wsgi_application

os.environ.setdefault("DJANGO_SETTINGS_MODULE", "rtscheduler.settings")

from whitenoise.django import DjangoWhiteNoise

application = get_wsgi_application()
application = DjangoWhiteNoise(application)
```

Si mai este nevoie de a crea o directorie pentru a asigura utilizarea fisierelor statice asa ca imaginile si fisierele .css si .javascript.
Asadar, dupa exemplul de mai jos creati fisierele ca in imaginea urmatoare:

[Directoriu static in directoriu principal al proiectului](/images/www/static_creation_deploy.png)

Pentru a face posibil deployment-ul a mai multe versiuni, iterativ a websiteului este nevoie de utilizat un sistem care sa aiba grija de versionarea codului in mod corect. Cel mai raspandit sistem de versiune in prezent este GIT. De aceea deployment-ul pe platforma heroku este utilizat GIT ca forma de actualizare a aplicatiei web.

Astfel pentru a initia repositoria scrim in linia de comanda:
```git init```

Cream un fisier "`.gitignore`" in directoria principala a proiectului si in el scrim:
```
	venv
	*.pyc
	staticfiles
	.env
```

Dupa care scrim urmatoarele comenzi:
```
	git add .
	git commit -m "Initial commit"
```

Dupa care mai scrim inca o data comanda ```heroku login```.

Iar acum vom crea aplicatia noastra pe heroku cu urmatoarea comanda:
```heroku create```

Dupa care trimitem informatia websiteului pe serverul platformei Heroku:
```git push heroku master```

Dupa ce ati scris heroku create a aparut un text ce arata in felul urmator:
```
Creating intense-falls-9163... done, stack is cedar
http://intense-falls-9163.herokuapp.com/ | git@heroku.com:intense-falls-9163.git
Git remote heroku added
```

Denumirea aplicatiei in heroku este creata automat si nu coincide cu denumirea care vrem sa o punem noi. Din aceasta cauza este nevoie de a o schimba. 
Noi o vom schimba cu urmatoarele comenzi, analogic scriind numele aplicatiei noastre in loc de "myschoolproject" si cu numele dat de heroku in linia de comanda proprie in loc de "intense-falls-9163":

```
heroku apps:rename girlsgoit --app intense-falls-9163
```

Dupa tot acest proces veti putea sa accesati websiteul vostru la adresa:
```
http://denumiresite.heroku.com
```

---
layout: default
title: Django Intro
category: basic
---

## Setarea Mediului de Lucru

### 1. Instalarea Sublime Text
![Sublime Text](https://cdn.tutsplus.com/net/uploads/legacy/1140_st2plugins/200u.jpg)

&nbsp; &nbsp;  **Sublime Text** este un editor de cod util deoarece el ofera multe optiuni  ajutor programistului ca: auto-recunoastere de limbaj, evidentiere multi-colora a codului etc. 
&nbsp;  &nbsp;  Pentru ca sa il instalam, accesam linkul : [https://www.sublimetext.com/3](https://www.sublimetext.com/3) si alegem versiunea care coencide cu sistemul nostru de operare pentru descarcare.
&nbsp;  &nbsp; Dupa descarare il instalam in locatia dorita ca ori si ce alta programa 


### 2. Instalarea Python 
![Python](https://www.python.org/static/opengraph-icon-200x200.png)
&nbsp; &nbsp; **Python** este un limbaj de programare la baza caruia stau principiile ca codul scris sa fie unul lizibil si usor de invatat.

&nbsp; &nbsp; Pentru instalare accesam linkul: [https://www.python.org/downloads/]( https://www.python.org/downloads/) si alegem versiunea **3.5.2**(cea mai actuala). 
Dupa descarcare deschidem fisierul si il instalam, dar, inainte de a apasa **Install Now**, pe prima pagina a instalrii trebuie sa fim singuri ca am bifat **Add Path**

![instal](http://loadbalancerblog.com/sites/default/files/images/image003.jpg)

&nbsp; &nbsp; Apoi astemptam sa se finiseze instalarea. 


### 3. Instalarea Django 
![Django](http://seeklogo.com/images/D/django-logo-182231C1BB-seeklogo.com.gif)
&nbsp; &nbsp;**Django** este un framework scris in limbajul Python care ne ofera cu multa usurinta sa cream o aplicatie web de la 0 

Pentru a instala **Django**, apasam Start si in search scriem “**cmd**”, pentru a deschide Linia de Comanda.

![CMD](http://cdn.winability.com/info/delete-partition/start-menu-cmd.png)

&nbsp; &nbsp;**Linia de Comanda** este o unealta inca de pe timpurile cind nu existau interfete grafice, dar si in  ziua de astazi ea ne poate ajuta foarte mult.

![ComandLine](http://www.computerhope.com/issues/pictures/dos.jpg)

In linia de comanda scriem `pip install django` si asteptam ca instalarea sa se termine si la urma linia de comanda sa ne afiseze "**Succesfully Installed Django**"

![SuccesfulInstall](http://www.swegler.com/becky/blog/wp-content/uploads/2011/08/climsy_20110828_185611.jpg)


## Crearea Proiectului Django
&nbsp; &nbsp; Pe Desktop sau orice alt directoriu creati un folder cu denumirea dorita a  proiectului

![Folder](http://wishmesh.com/wp-content/uploads/2012/04/02-new-folder.jpg)

 Tinind butonul **shift** apasati **click dreapta** pe folderul creat. Veti vedea o optiune Open Command Line, selecati. 

![OpenCommandLine](http://i.stack.imgur.com/0DLsh.png)

Aceasta optiune va deschide Linia de Comanda cu calea spre folderul vostru, ca comenzile pe care le rulati sa ruleze din folderul care il folositi. 

Pentru a crea proiectul, rulam urmatoarea  comanda in Linia de Comanda: `django-admin.py startproject mysite .` , unde ultimul cuvint **mysite** este denumirea proiectului. 

Aceasta comanda automat va genera toate fisierele necesare noua ca sa lucram in continuare la proiectul nostru

Dupa rularea acestei comande, deschideti folderul in care lucrati, daca tot a decurs bine, folderul trebuie sa contina urmatoarele fisiere

![img](/images/django/img1.png) 


Pentru momemnt deschideti editorul **Sublime Text**. In coltul sting sus accesati tabul File, acolo veti gasi optiunea Open Folder

![FindFolder](http://rosebusch.net/jeff/Web_Testing/img/openFolderSublime.png)

Gasiti folderul care contine proiectul, evidentiati cu un click folderul si apasati Open. Important e doar sa evedentiati si sa nu faceti dublu click pe folder. 

![OpenFolder](/images/django/img2.png)

Dupa cum observati in stinga editorului sa deschis un tab unde este afisat continutul folderului care a fost selectat. Acesta ne ajuta mai usor sa ne orientam in fisierele noastre fara ca sa parasim editorul. 

![FileHeriarchy](/images/django/img3.png)

## Partea de applicatie 

Intoarcetiva la Linia de Comanda(fereastra cu fundal negru strasnica) si in ea introduceti urmatoarea commanda 

```sh
python manage.py startapp blog
``` 

**blog** este denumirea applicatiei, puteti sa o schimbati 

Acesta commanda va crea applicatie in proiectul dorit,  aici se vor contine toate fisierele care vor fi direct responsabile de site-ul care il creati(URL’uri, imagini, text etc)

In urma executarii acesteti comande , in folderul proiectului trebuie sa apara un nou folder

![File](/images/django/img4.png)
Fisierele cu denumirea **urls.py** sunt responsabile de de URL’urile din proiect si aplicatia care o creati. 

Haideti sa dechidem fisierul urls.py din folder-ul mysite in Sublime Text.  Vom vedea urmatorul cod:

```python
from django.conf.urls import url
from django.contrib import admin

urlpatterns = [
    url(r'^admin/', admin.site.urls),
]
```

Analizam urmatorul rind de cod  

```python
url(r'^admin/', admin.site.urls)
```

Acesta va analiza tot ce noi introducem in Browser si daca va gasi cuvintul cheie `admin` acesta va rederectiona spre URL-urile ale admin 

Adaugam  urmatorul rind de cod 

```python

from django.conf.urls import url
from django.contrib import admin
urlpatterns = [
    url(r'^admin/', admin.site.urls),
    url(r'',('blog.urls'))
]
```
  
Dar daca ne uitam in folderul **blog** sau mai general folderul applicatiei in proiect

![ProjectFolder](/images/django/img5.png) 

Observam ca fisierul **urls.py** lipseste din folderul applicatiei blog. Inseamna ca trebuie sa il adaugam

Apasam **Click Dreapta** pe folderul applicatiei, in cazul dat **blog** si dam click la ** New File**

Apoi mai jos dam denumirea fisierului **urls.py**. Asa am creat un fisier python. 
![URLS](/images/django/img6.png)

Deschidem fisierul **urls.py**  din folderul **mysite**, apasam **ctrl-A** si apoi **ctrl-C** pentru a copia continutul fisierului. In **urls.py** din folderul applicatiei(blog in cazul dat) apasti **ctrl-V** pentru a insera continutul in fisierul nou. Apoi **ctrl-S** pentru a salva fisierul.

Si incepem sa editam acest fisier pentru ca sa cream URL-lul a aplicatiei noastre 

Stergem 

```python
from django.contrib import admin
```

si adaugam in locul ei
 
```python
from . import views
```

Stergem  

```python
url(r'^admin/', admin.site.urls)
url(r'',('blog.urls'))
```


In locul lor adaugam  

```python
url(r'^denumirea_urlui', views.blog_page)
``` 

Dar totusi aplicatia noastra nu stie de nici o pagina cu denumirea **blog_page** in cazul dat. 

Observam ca inainte de **blog_page** avem **views** urmat de un punct. Prin asa metoda noi chemam o functie sau alte componente dintrun fisier, in cazul nostru **views**. 
 
Dechidem fisierul **views.py** din folderul applicatiei(blog), aici noi declaram orice pagina in felul urmator

```python
from django.shortcuts import render

# Create your views here.
```

Pentru moment noi dorim ca pagina noastra sa ne afiseze un text, pentru aceasta trebuie sa importam o nous librarire `HttpResponse`, pe ea o vom folosi pentru ca sa putem afisa textul.

```python
from django.shortcuts import render
from django.http import HttpResponse

def blog_page():
	return HttpResponse("You are Awesome")
```

salvam fisierul 

La final lansam serverul local. Ne intoarcem la linia de comanda si introducem urmatoarea comanda 

```sh
python manage.py runserver
```

Asigurativa ca linia de comanda este deschis din folderul proiectului.

pentru inceput introduceti 127.0.0.1:8000, in browser, apoi 127.0.0`.1:8000/url in cazul dat **blog**. Pagina trebuie sa afiseze stringul care lati introdus in views.py 

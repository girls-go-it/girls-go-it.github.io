---
layout: default
title: Django Project
category: basic
---

## Setarea Mediului de Lucru

### 1. Instalarea Sublime Text
![Sublime Text](https://cdn.tutsplus.com/net/uploads/legacy/1140_st2plugins/200u.jpg)

&nbsp; &nbsp;  ** Sublime Text** este un editor de cod util deoarece el ofera multe optiuni  ajutor programistului ca: auto-recunoastere de limbaj, evidentiere multi-colora a codului etc. 
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

![Folder](https://scontent-frt3-1.xx.fbcdn.net/v/t35.0-12/13662648_1351761801518250_1980309842_o.png?oh=2ebefbd79aadaa5fc5477d4ed8f4e42b&oe=579A9B8C)


Pentru momemnt deschideti editorul **Sublime Text**. In coltul sting sus accesati tabul File, acolo veti gasi optiunea Open Folder

![FindFolder](http://rosebusch.net/jeff/Web_Testing/img/openFolderSublime.png)

Gasiti folderul care contine proiectul, evidentiati cu un click folderul si apasati Open. Important e doar sa evedentiati si sa nu faceti dublu click pe folder. 

![OpenFolder](https://scontent-frt3-1.xx.fbcdn.net/v/t35.0-12/13833096_1351771711517259_1251096350_o.png?oh=5a9f67188acbbe1af73c2a8bc58aa259&oe=5799966F)

Dupa cum observati in stinga editorului sa deschis un tab unde este afisat continutul folderului care a fost selectat. Acesta ne ajuta mai usor sa ne orientam in fisierele noastre fara ca sa parasim editorul. 

![FileHeriarchy](https://scontent-frt3-1.xx.fbcdn.net/v/t35.0-12/13839755_1351777404850023_198335560_o.png?oh=9c1ba0f6c02e06fb8141fe9392e8d562&oe=579982AD)

## Partea de applicatie 

Intoarcetiva la Linia de Comanda(fereastra cu fundal negru strasnica) si in ea introduceti urmatoarea commanda 

`python manage.py startapp blog`, **blog** este denumirea applicatiei, puteti sa o schimbati 

Acesta commanda va crea applicatie in proiectul dorit,  aici se vor contine toate fisierele care vor fi direct responsabile de site-ul care il creati(URL’uri, imagini, text etc)

In urma executarii acesteti comande , in folderul proiectului trebuie sa apara un nou folder

![File](https://scontent-frt3-1.xx.fbcdn.net/v/t35.0-12/13839876_1351807928180304_769299373_o.png?oh=a52181e45bb5f8ce5f83024f72d7f058&oe=579A75BB)

Fisierele cu denumirea **urls.py** sunt responsabile de de URL’urile din proiect si aplicatia care o creati. 

Haideti sa dechidem fisierul urls.py din folder-ul mysite in Sublime Text.  Vom vedea urmatorul cod:

```python

from django.conf.urls import url
from django.contrib import admin

urlpatterns = [
    url(r'^admin/', admin.site.urls),

```

Analizam urmatorul rind de cod  

```python
	url(r'^admin/', admin.site.urls)

```
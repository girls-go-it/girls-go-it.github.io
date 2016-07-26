---
layout: default
title: How Web Works
category: basic
---



# Cum lucreaza acest internet?

Internetul e un lucru fascinant!
De fiecare data cand va conectati la o retea, prin cablu sau wifi, va conectati la o retea enorma (si cand zic enorma am in vedere miliarde!) de calculatoare.

Cum arata aceasta retea?.. cam asa:
![Cum arata internetul](http://www.myinsightmag.com/wp-content/uploads/2012/03/wired-610x250.gif)

Daca va mirati ca nu intelegeti nimic,  credeti-ne, nimeni nu intelege ;) Ba chiar expertii zic, ca daca oamenii ar studia cum lucreaza internetul, s-ar mira cum de el lucreaza in general!

In realitate asta-i o retea de calculatoare conectate intre ele si kilometri de cablu in jurul lumii. Puteti sa vizitati [Submarine Cable Map](http://submarinecablemap.com/) ca sa vedeti cat de complicat e. Iata un mic exeplu: 
![Internet map](http://tutorial.djangogirls.org/en/how_the_internet_works/images/internet_3.png) 



## Dar cum accesez o pagina internet?

In primul rand trebuie sa constientizam ca nu e posibil sa interconectam intre ele fiecare calculator, de aceea comunicarea se intampla prin intermediari, cam asa:
![Request path](/images/www/internet_2.png)


Comunicarea are loc intotdeauna dupa modelul Intrebare - Raspuns. Si anume, calculatorul vostru intreaba un alt calculator din internet ceva fisiere, si el le transmite inapoi ca raspuns:
![Communication](/images/www/get-response.png)

Acest "alt" calculator, asa numitul server, e la fel ca si calculatorul vostru, doar ca mai puternic - el doar trebuie sa suporte multe multe cereri!

Ca sa accesati serverul GOOGLE, spre exemplu, scrieti adresa `www.google.com` in bara de adrese din browser si obtineti bine cunoscuta pagina de cautare.

In spate se intampla multe lucruri interesante, dar mai intai haideti sa descurcam cateva detalii:

1. Calculatoarele se acceaseaza intre ele nu prin nume, ci prin o secventa de 4 numere separate prin punct, numita IP, un exemplu de IP ar fi: `212.0.195.168`

2. Numele (cum ar fi 'google.com') e la fel ca si numele care-l salvati la voi in telefon pentru fiecare numar al prietenilor, familie, etc. Si are doar rolul sa arate memorizabil pentru noi, oamenii, si sa faca legatura cu numarul de telefon sunat.

3. Reiese ca avem nevoie si de o "Carte de IP'uri" globala, care sa traduca un nume ca `google.com` intr-un ip ca `212.0.195.168` - aceasta carte globala se numeste DNS (Domain Name Server)

4. Noi putem apela o persoana atat dupa nume (cand e salvata), cat si dupa un numar direct de telefon. In acelasi mod putem accesa serverul google atat dupa numele 'google.com' cat si dupa ip'ul '212.0.195.168'. Recomand sa incercati `http://212.0.195.168` in browserul vostru ;)

## URL

Haideti sa luam un URL generic si sa-i analizam structura:

`https://example.com:8000/group/resource`

* `https://` - este protocolul comunicarii
* `example.com` - este numele resursei
* `8000` - este portul catre resursa
* `/group/resoure` - este calea catre pagina concreta a resursei

Protocolul - este doar un set de reguli, o intelegere cum sa comunice intre ele calculatoarele, tot asa cum avem un protocol de a ne saluta cand ne intalnim intre oameni.
⋅⋅⋅`https://` e varianta securizata a protocului `http://`, care la randul sau e un set de reguli de comunicare a textelor prin web

Numele resursei -  este acel nume dupa care un DNS gaseste IP'ul concret al serverului

Portul -  este doar un numar. Puteti sa-l interpretati ca numarul apartamentului intr-un bloc locativ. 
⋅⋅⋅ El permite mai multor aplicatii in paralel sa ruleze pe server si sa primeasca mesaje fara se incurce una pe alta (e.g. skype, torrent, web server, etc). Browserele implicit comunica pe portul `80`, dar noi intotdeauna putem "forta" portul comunicarii specificandu-l.

Calea catre pagina concreta -  e deja structura interna a paginilor in cadrul unei aplicatii. In aplicatia creata de noi, aceasta cale o vom defini in dependenta de cum vom dori sa fie apelate diferite pagini create de noi.

## Localhost

Calculatorul vostru personal tot poate actiona ca un web server, caci un web server e doar o aplicatie care ruleaza pe calculator.
Fiecare calculator are o adresa care inseamna "eu insumi":
![Request path](/images/www/laptop.png)

Portul `8000` e portul pe care va rula implicit Django, serverul care il vom porni noi.

Deci, pentru a apela la serverul care va rula la noi local, vom apela: `http://127.0.0.1:8000/` sau `http://localhost:8000/`

Dar ajunge atata vorba, cred ca ar fi timpul sa vedem ceva actiune!
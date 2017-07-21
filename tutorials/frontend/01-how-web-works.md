---
layout: default
title: How Web Works
category: basic
---



# Ce este internetul?

​​Posibil îți imaginezi că internetul este router-ul wifi de acasă, data centers gigante undeva prin lume, numerele care se rotesc printr-un tub.

![](/images/hww/the-internet-imagined.jpg)   


Ceea ce este, în principiu, adevărat dar, deasemenea, o mare parte a internetului arată cam așa:    
![](/images/hww/the-internet.jpg)   
​​O rețea masivă ce ne conectează pe întreaga planetă, a cărei suprafață e 71% apă. Ca consecință marea parte a internetului este sub apă, care lucrează prin cabluri de internet subacvatice.

![](/images/hww/cable.jpg)  
În mijlocul acestor cabluri se află niște fibre de sticlă extrem de mici, aproximativ de dimensiunea unui fir de păr. Acele fire minuscule sunt internetul. Modul în care lucrează este prin transmiterea fotografiilor, videoclipurilor, paginilor web ca impulsuri de lumină.    
Deci **lumină + sticlă = internet**.

La moment sunt mai mult de 250 de astfel de cabluri active și chiar au și o [hartă](http://submarine-cable-map-2015.telegeography.com/) intercativă.



## Deci cum accesez o pagină web?

Modul simplu:
- Deschizi un browser (Chrome, Firefox, Opera, Internet Explorer etc.).
- Scrii adresa, ex: `google.com`.
- Și navighezi cu plăcere.

Acum câteva procese care au loc de la deschiderea browserului până la utilizarea propriu-zisă a paginii web. Comunicarea între calculatorul vostru și cel care păstrează pagini web, imagini, video are loc prin modelul:    
- **cerere**
- **răspuns**

Aceste cereri și răspunsuri au un format foarte asemănător cu cele studiate la lecțiile de limbă română.

**Cerere**
![request](/images/hww/request.jpg)
- **User-Agent**: cine cere
- **Request URL/Remote Address**: de la cine cere / cui i se adresează
- **Reuest Method**: tipul cererii

**Răspuns**
![response](/images/hww/response.jpg)
- **content-type**: tipul conținutului care l-ai primit
- **date**: data și timpul când l-ai primit
- **status**: o serie de coduri care determină tipul răspunsului


Accesând o pagină web, comunicarea nu are loc direct între `client` (*calculatorul tău*) și `server` (*un calculator, data center care păstrează acele resurse*).
![network model](/images/hww/network.jpg)   
Cererea este transmisă printr-o rețea de servere, fiecare verificând dacă are resursele cerute. Dacă le are, se creează răspunsul și resursele sunt trimise înapoi către client, dacă nu - cererea este transmisă serverului *vecin* până când unul din aceștia are resursele cerute sau cererea nu ajunge la ultima destinație, cazul dat fiind serverul de la google.

Adresa resurselor cerute sau transmise este formată din o secvență de 4 numere separate prin punct numită **IP** address. Numerele singure nu ne oferă nouă (utilizatorilor) foartă multă informație despre ce pagină web reprezină, nemaivorbind cât de ridicol ar fi să fii impus să memorizezi zeci de serii de numere pentru a naviga pe internet. De aceea ele sunt utilizate doar de calculatoare, iar pentru utilizator, acestor numere li se atribue un nume informativ și ușor de memorizat.

Spre exemplu:
- IP-ului `172.217.22.78` îi este atribuit numele `google.com`
- IP-ului `185.60.218.35` îi este atribuit numele `facebook.com`

Toate aceste sunt intr-o *carte de numere* numită **Domain Name Server (DNS)**. Acesta are rolul de a transforma un nume de genul `google.com` în IP-ul acestuia `172.217.22.78` pentru a fi transmis mai departe până când resursele cerute sunt găsite.

## URL

Cunoaștem deja că URL-ul este adresa folosită pentru obținearea unei pagini web, imagini etc.
Acesta are și el câteva elemente care joacă un rol diferit în crearea unei cereri:   
`https://example.com:8000/group/resource`

* `https://` - protocolul comunicarii
* `example.com` - numele resursei
* `8000` - portul catre resursa
* `/group/resource` - este calea *locală* către o pagină sau resursă numită **path**

**Protocolul** - un set de reguli ce determină cum are loc transmiterea datelor între `client` și `server`.
**Numele resursei** - nume după care un DNS găsește IP-ul acelei resurse.

**Portul** - definește un *tunel* cu anumite restricții și posibilități destinate pentru un scop anume care va fi folosit de un oarecare tip de cerere. De exemplu:  
- Pentru obținearea unei pagine web se va folosi portul `80`.   
- Pentru a obține **Citatul zilei (Quote of the Day)** se va folosi portul `17`.

**Path** - structura internă a paginilor în cadrul unei aplicații. Elementele acesteia reprezintă nume de mape, fișiere sau pagină a unei aplicații.

## Localhost

E evident deja că pentru obținerea unei pagini web este necesar să fiți conectați la o rețea de internet. Ceea ce ar însemna că în timpul dezvoltării unei pagini web ar trebui de la început să păstrați acea pagină web pentru a o putea vizualiza în browser.

Din fericire acesta nu este cazul deoarece fiecare calculator poate funcționa ca un web server.
- este numit **Localhost**
- IP address: **127.0.0.1**

Și îl accesezi folosind URL-ul `http://localhost`.

Pentru a-l putea folosi trebuie să aveți instalat pe calculator una din programele care i-ar permite să funcționeze ca un web server. Unele din acestea fiind:
- [wamp](http://www.wampserver.com/en/)
- [mamp](https://www.mamp.info/en/)

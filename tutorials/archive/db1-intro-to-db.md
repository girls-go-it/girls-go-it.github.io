<!---
layout: default
title: Introducere in baze de date
--->

# Introducere in baza de date [[slides](http://slides.com/glebtocarenco/introducere-in-baze-de-date/live#/)]
In acest tutorial vei primi raspunsuri la sa inrebari ca:

- De ce avem nevoie de baza de date?
- Unde se folosesc bazele de date
- Din ce este compusă o bază de date?
- Ce este o schema a bazei de date, coloană, rînd, tabel?
- Vei afla cum se face legătura logică dintre infomația păstrată in baza de date.

## De ce avem nevoie de o bază de date?
Informatica este știința care se ocupă de prelucrearea, stocarea și procesarea datelor. Pentru aceasta este nevoie de un sistem care sa stocheze datele într-un mod structurat, care să aiba instrumentele necesare pentru a adauga date noi, cauta date într-un mod eficient. Cu acest scop au fost create bazele de date, ele ne permit într-un mod ușor sa obținem acces la informația necesară, inscrierea datelor noi și structurarea lor.


## Unde se folosesc bazele de date?
Raspunsul simplu ar fi peste tot :D, insă dacă privim atent la un web-site, aplicație desktop sau aplicație mobilă putem sa observam ca in spatele ei stă o bază de date care ne ajută sa pastrăm și să gasim ușor informația de care avem nevoie. Dacă vei continua calatoria in lumea magică IT vei avea de afacere mai mult sau mai puțin cu baze de date.


## Din ce este compusă o bază de date?

Ca să înțelegm mai bine cum sunt reprezentate datele in baza de date este nevoie vom incepe cu structura de bază a unei baze da date. Cea mai primitivă structură într-o bază de date este tabelul, cu ajutorul lui putem să reprezentăm intr-un mod comod, strucuturat și intuiiv datele de care avem nevoie in aplicație. Un tabel este compus compus din următoarele componente:
- Schema tabelului, care ne ajută să definim caracteristicele comune a datelor din programul nostru
- Rînduri, care contin mai multe însușiri in comun resprezintă o înregistrare in tabel
- Coloane, care sunt caracteristicele comune a entitatilor din tabel

Cu ajutorul acestor termeni putem să descriem orice entintate ce care avem nevoie în baza de date.
Acum hai să aplicam termenii însușiți anterior și să descrie un animal din Savanna Tweet. Datele care definesc un animal ar fi următoarele:
- numele
- numărul de picioare
- culoare blanei
- imaginea
- tip
- id (numărul de inscriere)

Toate aceste în comun reprezintă schema unui tabel sau descrierea entității din baza de date.

Coloanele din tabelul nostru ar fi: numele, tip, ...

Un rînd reprezinta o înregitrare pentru un animal particular.

### Cum sa indedificăm o inregistrare în un tabel?
Pentru acesta trebuie să gasim o caracteristica unica pentru animal. Un candidat perfect ar fi numarul de inscriere în tabel, deoarece el nu se repetă la nici un animal. În terminologia bazelor de date așa cîmp se numește cheie primară, cu ajutorul ei putem ușor sa gasim un animal in tabelul nostru.

### Cum se fac legături între tabele?
Acum hai sa adaugăm încă o entitate in baza noastră, spre exemplu postarea unui animal. Schema unei postări ar fi următoarea:
- id (număr de inscriere)
- id animal
- textul postării
- număr de likeuri

În acest exemplu apare ceva neobișnuit în comparație cu schema din tabelul precedent, este vorba despre coloana id animal. Anume ea face legatura dintre postare și animalul care a facut-o. Ea reprezintă cheia externă care defapt corespunde cu cheia primară a animalului.



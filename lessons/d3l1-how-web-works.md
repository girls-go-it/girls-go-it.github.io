<!-- ---
layout: default
title: How Web Works
--- -->


## How the Web Works 
----------


Scurt Istoric
-------------

		Browserele actuale pot nu numai să afișeze pagini web, ci oferă și interfețe cătrecelelalte servicii Internet, având astfel un efect integrator (pentru toate serviciile e suficient un singur browser). De aceea granițele dintre serviciul WWW și cTermenul World Wide Web, abreviat WWW sau și www, numit scurt și web, care în engleză înseamnă „pânza” (de păianjen); de multe ori este confundat cu rețea (net) și se pronunță /ˌwɝːld waɪd wɛb/ respectiv /wɛb/ (v. AFI), iar pe românește [ pron. ŭeb ] , este totalitatea siturilor / documentelor și informaților de tip hipertext legate între ele, care pot fi accesate prin rețeaua mondială de Internet (net = retea ). Documentele, care rezidează în diferite locații pe diverse calculatoare server, pot fi regăsite cu ajutorul unui identificator univoc numit URL. Hipertextul inclusiv imagini etc. este afișat cu un ajutorul unui program de navigare în web numit browser, care descarcă paginile web de pe un server web și le afișează pe un terminal „client” la utilizator.
		WWW este numai unul din numeroasele servicii și aplicații informatice disponibile în Internet. Alte servicii sunt de exemplu: afișarea de informații cu formă de text, imagini și sunete, poșta electronică e-mail, transferul de fișiere de date și informații FTP, chat, aplicații video și video on demand, servicii telefonie și telefonie cu imagine prin Internet de tip VoIP, posturi de radio și televiziune prin Internet, e-commerce, sondări de opinie, răspândirea știrilor prin metode RSS, toate genurile de grafică și muzică, lucrul pe un calculator de la distanță prin Internet, grupuri de discuții pe diverse teme, sisteme de jocuri interactive, distribuție de software ș.a.

		Celelalte servicii din Internet nu sunt întotdeauna clare.Webul a fost inventat în 1989 la Centrul European de Cercetări Nucleare (CERN) din Geneva, Elveția. Propunerea inițială de creare a unei colecții de documente având legături între ele [1] a fost făcută de Tim Berners-Lee în martie 1989. Propunerea a apărut în urma problemelor de comunicare pe care le întâmpinau echipele de cercetători ce foloseau centrul, chiar și folosind poșta electronică.

		Primul server web folosit de Tim Berners-Lee, acum la Microcosm, muzeu al CERN.Primul prototip al acestei colecții (mai întâi în format de text simplu) a apărut nu mult înainte de decembrie 1991, când s-a făcut prima lui demonstrație publică. Studiul a fost continuat prin apariția primei aplicații grafice Mosaic, în februarie 1993, realizată de cercetătorulMarc Andreessen de la centrul universitar National Center for Supercomputing Applications (NCSA) din orașul Urbana-Champaign din statul federal Illinois, SUA.
		În 1994 CERN și M.I.T. au format Consortiul World Wide Web, care are drept obiectiv dezvoltarea webului, standardizarea protocoalelor și încurajarea legăturilor dintre site-uri. Berners-Lee a devenit directorul acestui consorțiu. M.I.T. coordonează partea americană a consorțiului, iar partea europeană este coordonată de INRIA, centrul de cercetări francez.
		În 1995 Andreessen părăsește NCSA și înființează o nouă companie, Netscape Communications Corp., care se ocupă cu dezvoltarea de software pentru web.Apoi webul a evoluat până la ceea ce este astăzi, un serviciu multimedia integrativ, având ca suport fizic Internetul.Berners-Lee și echipa sa au realizat primele versiuni pentru patru componente cheie necesare serviciului web, și anume:

- protocolul de intercomunicație HTTP;
- limbajul de descriere a hipertextului HTML, pentru a putea fi afișat de browser;
- serverul de web;
- browserul.

		La baza funcționării webului stau 3 standarde, și anume:
	

 - (HTTP) - Hypertext Transfer Protocol, stiva de protocoale OSI prin
   care serverul web și browserul clientului (utilizatorului) comunică
   între ele;

		

 - (HTML) - Hypertext Markup Language, standard de definire și
   prezentare a paginilor web.

		

 - (URI) - Uniform Resource Identifier, sistem universal de identificare
   a resurselor din web, folosit pentru a identifica și regăsi paginile
   web; Următoarele stand

				World Wide Web Consortium (cunoscut și sub denumirea de W3C), care astăzi este condus de Berners-Lee, dezvoltă standardele HTML și CSS; alte standarde provin de la Internet Engineering Task Force (IETF), ECMA sau producători ca Sun Microsystems.Programul de navigare (browserul) cheamă pagina folosindu-se de URI și HTTP, o interpretează conform formatării paginii (hipertext) și o prezintă utilizatorului pe un monitor. Unul dintre principiile webului este modelul client-server, browserul fiind aplicația client, iar serverul HTTP (serverul web) fiind aplicația server. Pentru a putea interpreta și reda informațiile sub forma hipertextului, browserul apelează la standardul de limbaj HTML, definit încă de la începtul dezvoltării webului.
				În perioada 2004-2005 webul a cunoscut un salt calitativ cu privință la aplicațiile de mare răspândire pe glob, care e cunoscut sub numele simbolic Web 2.0.



Protocolul HTTP Hypertext Transfer Protocol (HTTP)
-----------------------------------------------------

		 Este metoda cea mai des utilizată pentru accesarea informațiilor în Internet care sunt păstrate pe servere World Wide Web (WWW). e un protocol de tip text, fiind protocolul "implicit" al WWW. Adică, dacă unURL nu conține partea de protocol, aceasta se consideră ca fiind http. HTTP presupune că pe calculatorul destinație rulează un program care înțelege protocolul. Fișierul trimis la destinație poate fi un document HTML (abreviație de la HyperText MarkupLanguage), un fișier grafic, de sunet, animație sau video, de asemenea un program executabil pe server-ul respectiv sau și un editor de text. După clasificarea după modelul de referință OSI, protocolul HTTP este un protocol de nivel aplicație. Realizarea și evoluția sa este coordonată de către World Wide Web Consortium (W3C).
		HTTP oferă o tehnică de comunicare prin care paginile web se pot transmite de la un computer aflat la distanță spre propriul computer. Dacă se apelează un link sau o adresă de web cum ar fi http://www.example.com, atunci se cere calculatorului host să afișeze o pagină web (index.html sau altele). În prima fază numele (adresa) www.example.com este convertit de protocolul DNS într-o adresă IP. Urmează transferul prin protocolul TCP pe portul standard 80 al serverului HTTP, ca răspuns la cererea HTTP-GET. Informații suplimentare ca de ex. indicații pentru browser, limba dorită ș.a. se pot adăuga în header-ul (antetul) pachetului HTTP. În urma cererii HTTP-GET urmează din partea serverului răspunsul cu datele cerute, ca de ex.: pagini în (X)HTML, cu fișiere atașate ca imagini, fișiere de stil (CSS), scripturi (Javascript), dar pot fi și pagini generate dinamic (SSI, JSP, PHP și ASP.NET). Dacă dintr-un anumit motiv informațiile nu pot fi transmise, atunci serverul trimite înapoi un mesaj de eroare. Modul exact de desfășurare a acestei acțiuni (cerere și răspuns) este stabilit în specificațiile HTTP.
		Deseori utilizatorul dorește să transmită informații speciale la website. Aici HTTP pune la dispozitie două posibilități:

 - Transferul datelor în combinație cu o cerere pentru o resursă
   (HTTP-metoda "GET")
 - Transferul datelor în combinație cu o cerere specială (HTTP-metoda
   "POST")

			Datele transferate vin deseori %-codate. La metoda GET se utilizează partea de cerere Uniform Resource Identifiers (URI) cu simbolul ?. Această metodă se utilizează pentru a transfera o listă de parametri, pe care partea opusă trebuie să o ia în considerare la prelucrarea cererii.Deseori această listă cuprinde perechi de valori separate prin semnul &, care sunt alcătuite din numele parametrului, semnul = și valoarea parametrului. Rareori se mai utilizează și semnul ; pentru separarea înregistrărilor listei [1]

IP (Internet Protocol)
----------------------

		 Este un protocol care asigură un serviciu de transmitere a datelor, fără conexiune permanentă. Acesta identifică fiecare interfață logică a echipamentelor conectate printr-un număr numit „adresă IP". Versiunea de standard folosită în majoritatea cazurilor este IPv4. În IPv4, standardul curent pentru comunicarea în Internet, adresa IP este reprezentată pe 32 de biți (de ex. 192.168.0.1). Alocarea adreselor IP nu este arbitrară; ea se face de către organizații însărcinate cu distribuirea de spații de adrese. De exemplu, RIPE este responsabilă cu gestiunea spațiului de adrese atribuit Europei.



Identificator uniform de resurse
--------------------------------

		 In original în engleză Uniform Resource Identifier, abreviat URI este o secvență alfanumerică univocă și universală a unei resurse de peInternet, cum ar fi un document sau un sit web. Deseori URI-ul unei resurse este identic cu URL-ul ei (localizator uniform de resurse), formă timpurie a identificatorului URI.

		Sintaxa URI
		conform RFC 1630:
				<schema>:<locatie>[?<interogarea>][#<fragmentul>]


		Exemplu:
	foo://example.com:8042/over/there?name=ferret#nose
			  \ /   \______________/\_________/ \_________/ \__/
		|           |             |           |        |
		schema    autoritatea      calea    interogare  fragment
		   |   ______________________|_
		  / \ /                        \
		

Sistem de nume de domeniu
-------------------------

		 Abreviat DNS, în engleză Domain Name System este un sistem distribuit de păstrare și interogare a unor date arbitrare într-o structură ierarhică. Cea mai cunoscută aplicație a DNS este gestionarea domeniilor în Internet.
		Caracteristicile sistemului de nume (DNS) sunt:

 - folosește o structură ierarhizată;
 - deleagă autoritatea pentru nume;
 - baza de date cu numele și adresele IP este distribuită.

			Fiecare implementare TCP/IP conține o rutină software (name resolver) specializată în interogarea serverului de nume (DNS) în vederea obținerii translatării nume/adresă IP sau invers.
			Există 2 tipuri de rezoluție de nume:

 - rezoluție recursivă (name resolverul cere serverului de nume să facă
   translatarea);



 - ezoluție iterativă (name resolverul cere serverului de nume să îi
   furnizeze adresa IP a unui server care poate face translatarea).

			Tipic, procesul de rezoluție a numelor se desfășoară astfel:
			Name resolverul primește de la o aplicație client TCP/IP un nume; acesta formulează o interogare primului server de nume din lista serverelor;
			Serverul de nume (DNS) determină daca este mandatat (autorizat) pentru domeniul respectiv (dacă există configurată o zonă DNS care conține numele respectiv);
		

 - Dacă este autorizat, transmite răspunsul clientului;

		

 - Dacă nu, transmite o interogare altui server de nume pentru un
   răspuns autorizat; obține răspunsul autorizat și transmite clientului
   un răspuns neautorizat; totodată stochează răspunsul local pentru a
   răspunde la alte cereri pentru același nume.

			Resolverul de nume transmite răspunsul aplicației utilizator și îl păstrează într-un cache pentru o anumită perioadă;
			Dacă name resolverul nu primește un răspuns într-un anumit timp, transmite cererea următorului server de nume din listă. Când lista este epuizată, va genera o eroare.
			

Protocolul DNS
--------------

		Redirectorul. La un calculator conectat la o rețea se pot executa atât aplicații care necesită numai resursele sistemului respectiv (programe de calcul tabelar, programe de procesare de texte etc.), cât și aplicații care accesează resursele rețelei (browsere de navigare în internet etc.). Nivelul aplicație este cel care permite accesul aplicațiilor la mediul de rețea.
		Într-o rețea LAN, redirectorul este protocolul care lucrează la nivelul sistemului de operare al calculatorului și permite să se facă distincție între cererile adresate unității centrale a calculatorului respectiv și cele adresate unui server. Redirectorul permite administratorului de rețea să atribuie nume logice resurselor aflate pe diverse unități, iar utilizatorul, pentru a accesa o anumită resursă, va utiliza numai acești identificatori, fără nici o referință la rețeaua respectivă. Astfel, redirectoarele extind componentele software locale. Astfel, este posibilă utilizarea în comun a resurselor logice și fizice ale rețelei, precum și integrarea aplicațiilor locale cu cele de rețea.
		Fiecare “site” de pe Internet are alocată o adresă IP. Folosirea de către utilizatorii obișnuiți a acestor adrese este dificilă și poate genera erori. Astfel, este necesar un protocol care să facă corespondența dintre numele diverselor componente de rețea și adresele lor IP. Această problemă este rezolvată de către protocolul DNS (Domain Names System).

		Domeniul este un grup de calculatoare care sunt asociate prin localizarea lor geografică sau prin tipul de activitate al organizației pe care o deservesc. Numele de domeniu este un șir de caractere și/sau numere, de obicei un nume sau prescurtarea unui nume.
		La începutul existenței Internetului, când numărul de calculatoare legate în rețea era relativ mic, a existat o tabelă realizată de organizația NIC (Network Information Center), care făcea corespondența dintre adresa IP și numele gazdei. Numele de gazde erau șiruri de caractere, fără a avea o organizare ierarhică. Aceste corespondențe erau introduse manual în tabelă și erau transmise tuturor administratorilor de rețele conectate la Internet.
		Ierarhia de domeniu. DNS implementează un spațiu ierarhizat de nume pentru obiectele din Internet. Spre deosebire de numele de fișiere (calea către acestea), care sunt prelucrate de la dreapta la stânga, fiind separate de slash-uri, numele DNS sunt prelucrate de la dreapta la stânga, separatorul fiind caracterul “.”. Asemănător ierarhiei de fișiere, ierarhia DNS poate fi văzută ca un arbore.
		Servere de nume Primul pas în organizarea acestor servere este partiționarea ierarhiei în zone. Fiecare zonă poate fi gândită ca fiind corespondentă la o anumită autoritate administrativă, responsabilă pentru acea porțiune a ierarhi

Hosting
-------

		În rețelele de calculatoare, localhost este un nume de host care înseamnă acest calculator și poate fi utilizat pentru accesarea propriilor servicii de rețea ale calculatorului prin interfața sa de loopback. Utilizarea interfeței de loopback evită placa de rețea. Mecanismul de loopback local poate fi util pentru testarea software-ului în timpul dezvoltării, independent de alte configurări ale rețelei. Spre exemplu, dacă un calculator a fost configurat să servească un site web, accesând http://localhost într-un browser local, ar putea afișa pagina de index.
		Pe majoritatea calculatoarelor, „localhost” se rezolvă în adresa ip 127.0.0.1, care este cea mai des utilizată adresă loopback IPv4 și către adresa loopback IPv6 ::1.[1] Numele „localhost” este un TLD rezervat, pus deoparte pentru a evita confuzia cu definiția îngustă a numelui de host.[2] Standardele IETF restricționează asignarea numelui în procedurile standard de înregistrare, cum ar fi „localhost.com” pentru domenii de nivel secundar (SLD).
		Găzduirea web (în engleză: [web hosting]) este un serviciu oferit atât companiilor cât și persoanelor particulare, care le permite acestora să își publice un sit web în Internet - să îl pună la dispoziție în web "vizitatorilor", online. Furnizorul acordă clientului spațiu de memorare pe un server conectat la Internet și de obicei aflat fizic într-un centru de calcul. Deseori furnizorul:

 - alocă fiecărui sit web găzduit și câte un nume de domeniu web unic.
 - pune la dispoziție clientului nu numai spațiul de stocare necesar
 - sitului, dar chiar un întreg server (virtual) inclusiv sistemul său
   de operare.

			Gazduirea web este de mai multe feluri :

 - Găzduirea partajata (în engleză: shared hosting)care presupune
   gazduirea mai multor siteuri pe un singur server

 - Găzduirea reseller (în engleză: reseller hosting) care presupune
   revanzarea pachetelor de gazduire ce sunt gazduite pe un singur
   server (găzduirea partajata)

 - Găzduirea reseller (în engleză: shared hosting) care presupune
   resurse dedicate (servere dedicate sau masini virtuale - VPS - pentru
   un singur site

			Site-urile web se pot clasifica după o mulțime de factori, dar principalul factor rămâne subiectul de activitate (sau conținutul) site-ului. Din punct de vedere tehnologic un site web poate fi alcătuit din orice tipuri de date și informații statice, camere de discuții, produse și servicii de vânzare, anunțuri, formulare de completat online, sunete digitalizate, clipuri video, imagini statice și animate, efecte speciale, meniuri dinamice și multe, multe altele. Vorbind la un nivel mai înalt, subiectul (tema) unui site web poate fi: un așa-numit blog, portal web, catalog web, magazin virtual, bancă, universitate virtuală, bibliotecă, enciclopedie virtuală, revistă web, ziar web și aproape orice altceva. Un exemplu de site web oarecum surprinzător este CouchSurfing, un sistem de mijlocire de locuințe particulare pentru găzduirea pe timpul concediului a călătorilor interesați de contacte cu noi persoane particulare și noi culturi.
			Dacă la început nu s-a pus accent prea mare pe latura estetică, în zilele de azi se acordă o importanță din ce în ce mai mare nu numai conținutului de informații al unui site web, dar și esteticii, dinamicii și atractivității lui.
			La ora actuală (2007) Internetul conține sute de milioane de pagini web, pe cele mai variate subiecte și limbi[necesită citare]. În octombrie 2006, Netcraft, o companie de monitorizare a Internetului care produce statistici despre Internet încă din anul 1995, a anunțat că în web există 101.435.235 site-uri, fiecare cu nume de domeniu propriu unic (față de 18.000 site-uri în august 1995).

			Principalele categorii de site-uri web după conținut

 - Conținutul de tip meme - meme-urile reprezintă imagini editate cu
   textul dorit

 - Conținut infografic - reprezentări grafice ale unor date
   (ex.graficele vânzărilor de pe ultima lună)

 - Conținut video - foarte util în cazul website-urilor ce oferă
   demonstrații,tutoriale,etc

 - Conținutul propriu-zis de tip text - textul este elementul cheie al
   unui site sau blog ce poate fi combinat cu succes împreună cu primei Trei tipuri de conținut

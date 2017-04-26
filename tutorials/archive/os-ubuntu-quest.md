---
layout: default
title: Ubuntu Quest
---

# Ubuntu Quest
## Ce este un sistem de operare?
Zi de zi ne folosim de calculatoare, telfeoane, televizoare. Acestea sunt un set de piese electronice legate între ele. Ceia ce ne permite interacțiunea cu aceste gadgeturi este un **program** care contrololează dispozitivul. Și odată ce acest **program** devine destul de complex noi îl putem numi sistem de operare.

Un exemplu bun ar fi **Android**. Acesta este un **sistem de operare** care ne permite să utilizăm majoritatea smartfonurilor. Un alt exemplu este **Windows**. Toți ați auzit de el și știeți ce face :smiley_cat:

<div class="custom-image"><img src="http://www.datalogics.com/images/windows-store.png" /></div>

## Ce este Ubuntu?
Ubuntu este și el un **sistem de operare** care ne permite să interacționăm cu calculatorul.

Avantajele utilizării acestuia sunt următoarele:

- Este fără plată
- Majoritatea programelor istalate la fel sunt fără plată (Dacă nu știai pentru a utiliza MicrosoftWord ai nevoie de fapt să îl cumpărați)
- Este mult mai comod de îl folosit din perspectiva unui programator (de ce vom afla în curând).
- ESTE FĂRĂ PLĂTĂ!!!!!!!!!

<div class="custom-image"><img src="https://design.ubuntu.com/wp-content/uploads/logo-ubuntu_cof-orange-hex.png" /></div>

## Cum interacționăm cu Ubuntu?
Modul primar de interacționare cu acest sistem de operare este similar cu Windows. Avem Interfața de unde lansăm diferite programe. Navigăm prin directorii pentru a accesa pozele, muzica și fișierele prefereate. Pentru a asculta un cântec facem un dublu click pe acesta, foarte similar cu ce oferă windows.

<div class="custom-image"><img src="http://2.bp.blogspot.com/-omfXnS75kuM/TjK-YxLqAZI/AAAAAAAACRQ/v3-g6RFsgEY/s1600/PCMan+file+manager+in+ubuntu+11.04.png" /></div>

O altă modalitate mai puțin tradițională este **terminalul**. Chiar dacă pare un pic criptică el ne oferă un avantaj enorm. Pentru a putea folosi **terminalul** este nevoie mai întâi de a înțelege un pic conceptul care stă în spatele lui. Aceasta vine cu un set de comenzi predefinite peste care le vom explora mai târziu.

<div class="custom-image"><img src="http://i.imgur.com/C1lE1NK.png"></div>

## Ce este un fișier?
Un fișier este un bloc de informație identificată după o denumire. De exemplu un cântec, sau o poză. Pentru un sistem de operare ele reprezintă una și același lucru, fișier. Însă sunt deja programe speciale care permit ascultarea cântecului, sau vizualizarea pozei. Un exemplu de **nume** a unui fișier arată în următorul fel `song352.mp3` . Textul până la punct reprezintă numele propriu zis, iar textul după punct reprezintă numele formatului fișierului (adică este poză, sau film, sau cântec, sau text). Aceasta nu este nimic altecva decât o convenție pentru ca utilizatorii să înțeleagă mai simplu ce reprezintă fișierul. Extensia simplu poate fi schimbată, însă aceasta nu va schimba formatul fișierului.

## Cum sunt structurate fișierele?
Dacă ai utilizat **Windows** probabil știi de **Discul C** și **Discul D**. Pe **Discul C** de obicei e instalat sistemul de operare propriuzis împreună cu setul de programe care le utilizeizi. Iar deja pe **Discult D** salvezi pozele, cântecele, filmele, și alte fișiere cu care lucrezi.

Situația în Ubuntu este similară. Aici nu sunt prezente **discuri** ca pe Windows. Analogic spus este doar un singur disc și el se numește **/**. Toate fișierele sunt structurate în directorii (în Windows se numesc folders). Și directoriul părinte este **/**. Aici se află întregul sistem de operare împreună cu fișierele personale.

<div class="custom-image"><img src="http://i.imgur.com/wnPkv62.png"></div>

Toate directoriile marcate cu roșu reprezintă sistemul de operare împreună cu programele instalate (analog cu **Discul C**). Accesul la acestea are loc printr-un mod mai special (vei vedea mai târziu cum). Restricționarea accesului direct la aceste fișiere este din motiv de securitate, și în caz că nu știi precis ce dorești să modifici **insistent recomand** să nu faci schimbări în aceste directorii.

Directoriile marcate cu albastru sunt la dispoziția ta pentru lucru. Aici vom lucra la poiectele noastre.


## Terminal
<div class="custom-image"><img src="http://media.giphy.com/media/mwOein9vVjBLO/giphy.gif"></div>

Terminalul este o programă ce permite interacțiunea cu sistemul de operare prin intermediul comenzilor textuale. Scrii ceva în el și primești un rezultat la ecran. Terminalul este folosit pentru un set divers de operații. Cel mai des pentru executarea programelor (ceia ce vom face cel mai des). Apoi pentru navigarea în directorii, crearea fișierelor, directoriilor, instalarea aplicațiilor și alte comenzi.

Pentru a porni fereastra de terminal apăsați combinația `CTR+ALT+T`.
în rezultat obțineți următoarea:

<div class="custom-image"><img src="http://i.imgur.com/gfT1j2A.png"></div>

Primul lucru care trebuie să înțelegi este că în momentul ce ai pornit terminalul tu te afli într-un directoriu (și întodeauna te vei afla într-un directoriu anumit). Mai mult decât atât tu te afli în `/home/sergiu/`. În loc de "sergiu" va fi numele utilizatorului vostru. Acest este așa numit **home directory**. Cum și am spus aici se află informația personală. Dacă nu mă crezi, introdu

```bash
$ pwd
```

și vei vedea unde te afli. Dolarul nu face parte din comandă, este doar un indicator că acum tapezi comenzi în terminal. Felicitări cu prima comandă tapată în terminal :tulip:. Iată rezultatul care eu l-am primit:

<div class="custom-image"><img src="http://i.imgur.com/dkksPAm.png"></div>

Dacă te uiți atent vei observa pe imagine că după execuția comenzii terminalul este gata pentru introducerea următoarei comenzi. Deci haideți să facem asta :smiling_imp:.

```bash
$ ls
```

Acum vedem directoriile și fișierele care se află în directoriul curent. La mine pe ecran este afișat următorul lucru:

<div class="custom-image"><img src="http://i.imgur.com/dQ7FLfV.png"></div>

Nu ai observat nimic dubios? Dacă te uiți atent la lista de directorii ai să observi că e aceiași lista din interfața oferită de Ubuntu.

<div class="custom-image"><img src="http://i.imgur.com/1UENgxh.png"></div>

#### Pro Tip
:alien:
Folosiți cât mai des TAB atunci când scrieti comenzi sau navigați prin directorii, pentru a putea folosi **autocomplete feature**

Superb :rose:. Acum aș dori să creez un directoriu în care să fac un experiment. Pentru aceasta rulez următoarea comandă:

```bash
$ mkdir experiment
```
Pentru a oferi complexitate comenzilor executate din terminal acestea au nevoie de parametri adiționali care urmează imediat după comandă. Comanda `mkdir` este folosită pentru crearea directoriilor. Dacă observi această comandă este următă cu cuvântul **experiment**. Aceasta nu este nimic altceva decât numele directoriului care doresc să îl creez, în același timp **experiment** este parametrul adițional transmis comenzii `mkdir`. Pentru a mă asigura că comanda a fost executată cu succes și că directoriul a fost creat execut încă odată următoarea comandă:

```bash
$ ls
```

<div class="custom-image"><img src="http://i.imgur.com/Qazq3yb.png"></div>

Vedem că comanda a fost executată cu success. Următoarea întrebare e cum de navigat în directoriul curent?. Mai bine spus cum de navigat în directorii în cadrul unui terminal? Aceasta se face destul de simplu cu ajutorul comenzii `cd`.

```bash
# /home/sergiu, home directory, este un directoriu des utilizat
# de aceasta se foloseste o scurtătură: ~
$ cd /home/sergiu # se va muta în home directory (în cazul meu /home/sergiu)
$ cd ~/ # același lucru ca și comanda precedentă
$ cd # același lucru ca și comanda precendentă
$ cd experiment # se va muta în /home/sergiu/experiment,
# pentru a reveni cu un nivel înapoi
$ cd ../
```

Recomand pentru început după fiecare rulare a comenzii `cd` să încerci să rulezi comanda `pwd` pentru a vedea în ce directoriu te afli. Bun după câteva experiențe hai să trecem la eperimentul nostru. Pentru a fi sigur că te afli în directoriul **experiment**, rulează următoarea comandă:

```bash
$ cd ~/experiment
```

Iar acum hai să creăm, redenumim fișiere. Pentru a crea un fișier cu numele "test.txt" rulează următoarea comandă:

```bash
$ touch test.txt
```

Pentru a te asigura că aceasta a avut loc cu success rulează din nou comanda

```bash
$ ls
```

Acum ar trebui să obții următorul rezultat la ecran:
<div class="custom-image"><img src="http://s29.postimg.org/khqemvcp3/Screenshot_2015_08_10_23_07_06.png"></div>

Ubuntu vine cu un set predefinit de aplicații dar deseori este nevoie de ceva mai mult. De asta a venit timpul de instalat cva alpicații noi. Pentru a înțelege cum are asta log am să încerc să fac o analogie. Probabil ai un telefon care folosește un sistem de operare IOS sau Android. De obicei când dorești să instalezi o aplicație nouă folosești deja o programă similară gen App Store pentru IOS, sau Play Store pentru Android. Pe aceiași filosofie lucreaza și Ubuntu. Ubuntu are o aplicație care te ajută ușor să instalezi aplicații și programe noi la tine pe calculator. Desigur ai nevoie de internet pentru asta. Ghici prin ce vom instala noi aplicații :smiley_cat:. Prin terminal desigur. Pentru a instala o aplicație nouă trebuie de folosit următoarea comandă:

```bash
$ sudo apt-get install numele_aplicatiei
# după asta urmează să introduci parola cu care te-ai logat în Ubuntu
# nu te mira dacă nu apar caractere pe ecrat, e făcut din motiv de securitate
# (să nu vadă vecinul câte caractere are parola ta)
```

Pentru că aplicațiile se instalează în directoriile sistemului de operare (mai ții minte directoriile roșii?), este nevoie de acces special pentru aceasta. Accesul special se face prin intermediul comenzii `sudo`.

Hai acum să instalăm prima aplicație care se numește **sl**

```bash
$ sudo apt-get install sl
```

Acum rulează noua aplicație

```bash
$ sl
```

Bucură-te de rezultat :smiley_cat:

Acum hai să instalăm ceva un pic mai practic. Ce zici de un mp3 player din terminal. Sună amuzant să pornești cântece din terminal nu? Programa se numește **mplayer**. Pentru a instala facem următoarea:

```bash
$ sudo apt-get install mplayer
```

Acum trebuie de testat aplicația noua aplicație. Pentru asta avem nevoie de un fișier mp3. Eu am pregătit unul pentru voi. Pentru a-l obține rulează următoarea comandă:

```bash
$ wget https://github.com/girls-go-it/random-files/raw/master/ubuntu-quest/help.mp3
```

După ce ai rulat din nou comanda `ls` pentru a te asigura că fișierul sa descărcat la tine în calculator, ar trebui să obții următorul rezultat la ecran.

<div class="custom-image"><img src="http://s28.postimg.org/mc8rxa5zw/Screenshot_2015_08_10_23_35_28.jpg"></div>

HEY!!! STOP!!! Dar de unde știi că fișierul care l-ai descărcat este un fișier audio? Ții minte spuneam ca extensia **.mp3** este doar o convenție? Chiar dacă fișierul se numește **help.mp3** acesta foarte simplu poate fi un virus sau altceva rău pentru calculatorul tău.

Primul pas pentru a te asigura că fișierul este întradevăr este să rulezi comanda:

```bash
$ file help.mp3
```

Această comandă afișează detalii despre tipul fișierului ignorând extensia acestuia. Ca rezultat ar trebui să obții următoarea:

<div class="custom-image"><img src="http://s14.postimg.org/706z87b00/Screenshot_2015_08_10_23_43_45.jpg"></div>

După ce ne-am asigurat că fișierul e întradevăr de formatul audio putem să încercăm să ascultăm cântecul.

```bash
$ mplayer help.mp3
```

Acum ar trebui să cânte "The Beatles" :D. Pentru a întrerupe programul apasă combinația `CTR+C`. Dar mai este o problemă. Mie îmi pare că numele fișierului nu este destul de descriptiv și vreau să redenumesc numele în așa fel ca să fie și numele trupei muzicale vizibile. Pentru aceasta rulăm următoarea comandă:

```bash
$ mv help.mp3 the_beatles_help.mp3
```

După rularea comenzii `ls` trebuie să obții următoarea

<div class="custom-image"><img src="http://s4.postimg.org/xdkoke7y5/Screenshot_2015_08_11_01_01_29.png"></div>

Dar cum rămâine cu fișierul care l-am creat anterior **test.txt**. Haideți să scriem niște text în el. De ce? pentru că așa se scriu programele (inclusiv acelea care le vom dezvolta în timpul evenimentului). Codul sursă al unei programe nu este nimic altceva decât text scris într-un fișier. Înainte de a scrie text în el este nevoie de un program care permite editarea acestuia. Pentru aceasta avem nevoie să instalăm **Sublime Text 3**. Aceast program îl vom folosi în continuare pentru scrierea aplicațiilor noastre. Pentru a instala programul facem următoarea:

```bash
$ sudo add-apt-repository ppa:webupd8team/sublime-text-3
$ sudo apt-get update
$ sudo apt-get install sublime-text-installer
```

Pentru a edita fișierul executăm următoarea:

```bash
$ subl test.txt
```

Acum putem scrie ce dorim în el. De exemplu eu am scris "Acesta este un simplu fisier textual", după care am salvat fișierul. Pentru a putea vizualiza conținutul unui fișier din terminal putem executa următoarea comandă:

```bash
$ cat test.txt
```

Și vei obține următoarea la ecran

<div class="custom-image"><img src="http://s8.postimg.org/uccpcfujp/Screenshot_2015_08_11_00_56_39.png"></div>

După cum vezi comanda `cat` pur și simplu afișează conținutul fișierului. Superb :tulib:, dar acum mi-am dat seama că nu mai am nevoie de acest fișier. Deci am nevoie să îl șterg. Pentru a șterge un fișierul în terminal rulez următoarea comandă:

```bash
$ rm test.txt
```

Și după rularea comenzii `ls` obervăm că fișierul nu mai este în directoriul curent.

<div class="custom-image"><img src="http://s23.postimg.org/6448w44nf/Screenshot_2015_08_11_01_06_38.png"></div>

Acum că experimentul a ajuns la un sfârșit am decis că nu mai am nevoie de directoriul curent și am decis să îl șterg. Pentru a sterge directoriul curent în primul rând am nevoie să îmi mut locația în altă parte, de exemplu în **home directory** și de acolo să șterg directoriul. În fine rulez următoarele comenzi:

```bash
$ cd
$ rm -r experiment
$ ls
```

Și în final am primit că directoriul **experiment** a fost șters din **home directory**.

<div class="custom-image"><img src="http://s22.postimg.org/6umeo3iip/Screenshot_2015_08_11_01_15_50.png"></div>

Și aici s-a terminat și sesiunea De **Ubuntu Quest**. Succes în continuare :bouquet:

## Exercițiu
Executați următoarele comenzi:

```
$ wget https://github.com/girls-go-it/random-files/raw/master/ubuntu-quest/file1
$ wget https://github.com/girls-go-it/random-files/raw/master/ubuntu-quest/file2
$ wget https://github.com/girls-go-it/random-files/raw/master/ubuntu-quest/file3
$ wget https://github.com/girls-go-it/random-files/raw/master/ubuntu-quest/file4
```

Încearcă să determini tipul de fișiere care le-ai downloadat și poate ce acțiuni poți face cu ele :kiss:
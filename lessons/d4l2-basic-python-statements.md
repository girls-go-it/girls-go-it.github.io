---
layout: default
title: Basic Python Statements
---

#Basic Python Statements

În decursul acestei sesiuni, veți afla ce înseamnă un limbaj de programare, de ce am ales să studiem **Python** și care este sintaxa acestuia. De asemenea, vă veți familiariza cu practica și logica de bază a scrierii unui program, făcând referință la unele situații cotidiene. În felul acesta, veți percepe mai ușor necesitatea programării în viața de zi cu zi.

####Ce este un limbaj de programare?
Un **limbaj de programare** este un mijloc de comunicare cu computerul. El reprezintă un set bine definit de expresii și reguli necesare pentru a formula instrucțiuni pe care ulterior computerul le va procesa. Limbajul de programare dă posibilitate programatorului să specifice în mod exact și amănunțit acțiunile pe care trebuie să le execute calculatorul, în ce ordine și cu ce date. Această specificare constă în scrierea programelor necesare.

####Ce este Python și de ce l-am ales pentru a-l studia?
Ce limbaje de programare cunoașteți? Probabil ați auzit de *HTML*, *CSS* sau *Pascal*. Da, ele toate sunt limbaje de programare. Ca și *Python*, de altfel.

Dacă există atât de multe limbaje de programare, de ce noi am ales să studiem anume *Python*? Deoarece *Python* este un limbaj de programare:

 - **modern** (mai modern decât *Pascal*);
 - **renumit**, fiind utilizat la ora actuală la o scară largă de către programatorii din toată lumea, crescându-și popularitatea tot mai mult;
 - **ușor de învățat**, deoarece există foarte multe comunități *Python* online cu membri activi, dispuși să vă ajute dacă aveți vreo problemă, comunități unde puteți accesa ghiduri, manuale, exerciții, proiecte, etc.

Cu ajutorul *Python*, puteți crea site-uri, aplicații web, jocuri și chiar motoare de căutare.


###**Sintaxa Python**

Pentru a scrie și executa toate exercițiile propuse mai jos, veți folosi editorul de text *Sublime Text*.

Deschideți *Sublime Text* și mergeți la bara de meniuri de sus. Selectați `File -> New File`. După ce vi s-a deschis un fișier nou, apăsați `Ctrl + s` pe tastatură. Salvați fișierul sub orice denumire doriți, dar neapărat cu extensia `.py`. Vă amintiți ce va povestit postetit Sergiu despre extensiile fișierelor? Eu o să-mi numesc fișierul `test.py`. Puteți face și voi la fel. Selectați mapa în care veți salva fișierul și apăsați `Save`. Acuma, sunteți gata să efectuați exercițiile propuse la această sesiune.

Pentru început, executați următoarea instrucțiune:

```python
print "Diana Jalba"
```

Pentru a face acest lucru, copiați textul de mai sus (dar cu numele vostru între ghilimele) și apăsați `Ctrl + b` pe tastatură. În partea de jos a editorului de text, trebuie să vă apară consola, unde vă veți vedea numele afișat.

Instrucțiunea ``` print ``` este simplă și foarte des utilizată, practic în orice program. Ea nu face altceva, decât să afișeze la ecran informația pe care i-o transmiteți (în cazul nostru, numele vostru).



####**Variabile**
Variabilele reprezintă un element important în programare. O **variabilă** reprezintă o valoare care se poate schimba de mai multe ori în timpul execuției unui program. Gândiți-vă la o variabilă ca la o cutie. Atunci când creați variabila, cutia este goală. Când îi atribuiți variabilei o valoare, e ca și cum ați pune în cutie un obiect, să zicem un pix. Peste o perioadă de timp, decideți să nu mai păstrați pixul în cutie, de aia puneți un creion în loc. Acest proces se numește *realocare de date*.

Așadar, o variabilă stochează o cantitate de informație sub un anumit nume. De exemplu, vârsta. Vârsta este un concept dinamic. Acum eu voi crea o variabilă cu numele ```varsta_mea``` și îi voi atribui vârsta mea:

```python
varsta_mea = 20
```
Acum, variabila ```varsta_mea``` conține valoarea 20. Dacă ulterior voi scrie un program specific, valoarea variabilei ```varsta_mea``` va crește periodic.

> **Notă:** Pentru ca să înțelegeți mai bine conceptul de variabilă, gândiți-vă la constante, adică la opusul variabilelor. O constantă este pur și simplu o valoare care este... constantă, cu alte cuvinte o valoare care nu se modifică, în acest sens, constantele sunt antonimul variabilelor, deoarece valoarea unei variabile se poate modifica pe durata execuției unui program. Constantele au o valoare fixă pe tot parcursul rulării. O constantă arhi-cunoscută este *PI* care are o valoare fixă și nu și-o poate schimba deloc în timpul execuției.

####**Tipuri de variabile**
În *Python*, ca și în oricare alt limbaj de programare, există mai multe tipuri de variabile. Astăzi, veți face cunoștință cu următoarele tipuri de variabile: ```int```, ```float```, ```bool```, ```string```.

Probabil vă întrebați: "La ce bun există mai multe tipuri de variabile?".
Pentru că în programare sunt necesare anumite convenții pentru a diferenția tipul de variabile cu care lucrăm.


 - ```int```

Primul tip de variabile se numește ```int```. ```int``` reprezintă aceeași mulțime *Z* din matematică, adică mulțimea numerelor întregi.


```python
my_int = 3
your_int = -4
```

- ```float```

```float``` este un alt tip de variabilă, care include în sine mulțimea numerelor fracționare din matematică, adică cifrele cu punct.


```python
my_float = 3.1
your_float = 4.5
```

- ```bool```

```Bool```-urile reprezintă un tip de variabile care pot avea doar două valori. Așa cum un întrerupător poate avea doar două stări: conectat sau deconectat, la fel și un bool poate fi doar ```True``` sau ```False```. Puteți utiliza variabile pentru a stoca ```bool```-urile:


```python
my_bool = True
your_bool = False
```

- ```string```

Cu tipul de date ```string``` noi deja am lucrat. Țineți minte când am executat instrucțiunea ```print "Numele Vostru"```? În această instrucțiune, ```"Numele Vostru"``` este scris în ghilimele. Toate variabilele care se scriu între ghilimele sunt de tip ```string```. Un ```string``` poate fi o literă, un cuvânt, o mulțime de cuvinte, chiar și cifre, spații sau simboluri atâta timp cât ele sunt scrise între ghilimele.


```python
my_string = "pix"
your_sring = "Tu ai 24 pixuri!"
```

###*Exercițiu:*
Creați o variabilă ```my_int``` și atribuiți-i o valoare de tip ```int```.
Creați o variabilă ```my_float``` și atribuiți-i o valoare de tip ```float```.
Creați o variabilă ``my_bool`` și atribuiți-i o valoare de tip ``bool``.
Creați o variabilă ``my_string`` și atribuiți-i o valoare de tip ``string``.

```python
age = 7
money = 1.23
is_happy = True
name = "Diana"
```

Să mergem mai departe.

Acum cunoașteți cum să folosiți variabilele pentru a stoca valori. Să zicem:

```python
my_int = 7
```
Puteți să schimbați valoarea acestei variabile, realocând-o:

```python
my_int = 3
```
Pentru a vedea dacă valoarea lui ``my_int`` s-a schimbat, afișați variabila:


```python
# daca scriem print my_int, consola ne va afisa valoarea 3, si nu 7

print my_int
```

###**Comentarii**
La exercițiul anterior, ați observat că am utilizat semnul ``#`` înaintea unei linii de cod. În această linie de cod eu am dat niște explicații a ceea ce fac eu în program. Semnul ``#`` semnifică începutul unui comentariu. Un **comentariu** este o linie de cod pe care *Python* o ignoră. Comentariile sunt utile doar pentru oameni pentru ca să înțeleagă ce fac unele bucăți mai mari și mai complicate de cod.

La ce bun s-au inventat comentariile? Comentariile fac programul vostru mai ușor de înțeles. Când vă uitați la codul pe care l-ați scris cu ceva timp în urmă sau alții doresc să colaboreze cu voi, ei pot citi comentariile și astfel percep foarte repede ce anume face programul vostru.

###*Exercițiu:*
Creați o variabilă și atribuiți-i o valoare de tip ``string``. Înainte de asta, adăugați un comentariu în care puteți scrie orice doriți. Nu uitați de semnul #.

```python
# acesta este un comentariu
oras = "Madrid"
```

###**Matematică**
De matematică nu scăpați nici în programare. Partea bună este că programarea vă ajută să faceți operațiile matematice simplu și rapid.  Putem să adunăm, scădem, înmulțim, împărțim și nu doar!
###*Exercițiu:*
Haideți să creăm patru variabile: ``suma``, ``diferenta``, ``inmultire`` și ``impartire`` și să le atribuim operațiile matematice corespunzătoare.

```python
suma = 25 + 25
diferenta = 108 - 7
inmultire = 4 * 5
impartire = 10 / 9
```
Pentru a vă convinge că rezultatele sunt corecte, scrieți, spre exemplu, ``print suma`` și vedeți rezultatul. Același exercițiu îl puteți face și asupra diferenței, înmulțirii și împărțirii. Apropo de împărțire. Care credeți că va fi rezultatul ``10 / 9``? Rezultatul va fi 1. De ce? Deoarece în acest caz, noi am împărțit două numere de tip ``int``, respectiv, rezultatul va fi tot de tip ``int``. Această împărțire ne va arăta de câte ori 9 se conține în 10 – o singură dată.

```python
print suma
print diferenta
print inmultire
print impartire
```
Dacă toate operațiile matematice pot fi efectuate la un simplu calculator, de ce să folosim *Python*? Pentru că putem combina operațiile matematice cu diferite tipuri de date (de exemplu ``bool``) și astfel se poate de creat programe utile.

Însă, să ne amintim că *Python* nu se rezumă doar la cele patru operații matematice de bază! Haideți să vedem cum scriem ridicarea la putere.


```python
opt = 2 ** 3
print opt
```
În acest exemplu, am creat o variabilă nouă pe care am numit-o ``opt`` și am setat-o ca fiind egală cu rezultatul a 2 la puterea 3 (2^3). Observați că am folosit două semne asteriks ``**``.

###*Exercițiu:*
Creați o variabilă ``suma_mea`` egală cu suma a două numere la dorința voastră și afișați variabila la ecran.

Creați o altă variabilă, numită ``distanta`` și folosiți ridicarea la putere pentru ca rezultatul să fie egal cu 100. (Încercați să ridicați 10 la puterea 2). Afișați rezultatul.

```python
# setam variabila suma_mea egala cu suma a doua numere
suma_mea = 5 + 3
print suma_mea
# setam variabila distanta egala cu 100 folosind ridicarea la putere
distanta = 10 ** 2
print distanta
```
###**Strings**
Să ne întoarcem un pic la ``string``-uri. ``String``-urile sunt cool. Și asta deoarece în *Python*, asupra lor se pot chema o mulțime de metode utile și interesante pentru a însuși mai bine programarea web. Așa după cum am mai menționat, un ``string`` poate conține litere, numere, simboluri și spații. Ele trebuie să fie scrise între ghilimele.


Să analizăm un exemplu:

```python
nume = "Mihai"
varsta = "21"
hobby = 'iubeste limbajul Python'
```
În acest exemplu, am creat o variabilă ``nume`` și i-am atribuit ``string``-ul ``"Mihai"``. De asemenea, am creat variabila ``varsta`` cu ``string``-ul ``"21"`` și ``hobby`` cu ``'iubeste limbajul Python'``. Observați că în ultimul exemplu, ``'iubeste limbajul Python'`` nu este scris între ghilimele duble. Aceasta nu este o problemă. *Python* acceptă și un asemenea fel de scriere a ``string``-urilor.

Dacă dorim să afișăm vârsta lui Mihai, vom scrie pur și simplu:

```python
print varsta
```

###**Accesarea după index**
Minunat! Acum, că v-ați reamintit ce înseamnă ``string``-urile, haideți să le analizăm mai detaliat. Trebuie să cunoașteți că toate caracterele dintr-un ``string`` sunt aranjate într-o ordine. Această ordine presupune ca fiecărui caracter din ``string`` să-i fie atribuit un număr. Acest număr este numit **index**. Să analizăm diagrama de mai jos:

<div class="custom-image-shadow"><img src="/images/d4l2-basic-python-statements/diagrama.png" /></div>

``String``-ul ``"Hello World"`` are 12 caractere, enumerate de la 0 la 11. Observați că și caracterului space (de după virgulă) îi este atribuit un index (indicele 5).

Prin urmare, dacă doriți să accesați caracterul ``"w"``din ``string``-ul ``"Hello World"``, trebuie pur și simplu să scrieți ``"Hello World"[7]`` (pentru că enumerarea începe tot timpul de la 0!).

Pentru a însuși această logică mai bine, vă aduc un exemplu simplu:

```python
p = "pix"[0]
e = "creion"[2]
```
În acest exemplu, am creat o variabilă nouă numită ``p`` și i-am atribuit "p" – caracterul de la index-ul zero al ``string``-ului ``"pix"``. Apoi, am creat o variabilă nouă, numită ``e``, căreia i-am atribuit caracterul cu index-ul 2 din ``string``-ul ``"creion"``. În Python, enumerarea începe de la zero, și nu de la unu.

###*Exercițiu:*
Atribuiți variabilei ``litera_patru`` a patra literă din ``string``-ul ``"prieten"``. Țineți minte că a patra literă nu se află la index-ul 5. Începeți să numărați indecșii de la zero.

```python
litera_patru = "prieten"[4]
print litera_patru
```
###**Concatenarea string-urilor**
Să mergem mai departe! Voi deja cunoașteți ``string``-urile! De asemenea, voi deja cunoașteți și operațiile aritmetice din *Python*! Zic să combinăm aceste două concepte!


Haideți să analizăm următoarea linie de cod:

```python
print "Python " + "este " + "dragut!"
```
Aceasta va afișa propoziția ``"Python este dragut!"``. Semnul ``+`` ‘unește’ toate aceste trei ``string``-uri într-un singur ``string``. Observați că sunt două spații în ghilimele: un spațiu după cuvântul ``Python`` și altul după cuvântul ``este``. Am scris aceste spații pentru ca cuvintele *(ca cuvintele… e cacofonie?)* să fie delimitate atunci când se va forma un singur ``string``, adică să se afișeze trei cuvinte, și nu unul întreg. Combinarea ``string``-urilor în felul dat și presupune **concatenarea**. Haideți acum să încercăm să concatenăm câteva ``string``-uri împreună!

###*Exercițiu:*
Afișați ``string``-urile concatenate ``"Programarea "``, ``"este "``, ``"simpla"``. Asigurați-vă că ați inclus spații după ``"Programarea "`` și ``"simpla "``.

```python
# afisam concatenarea a trei stringuri
print "Programarea " + "este " + "simpla"
```

###**Convertirea string-urilor**

Uneori, veți avea nevoie să combinați un ``string`` cu ceva care nu este ``string``. Pentru a face asta, trebuie să convertiți non-``string``-urile în ``string``-uri.



```python
print "Eu am " + str(6) + " pixuri!"
```
În acest caz, se va afișa: ``"Eu am 6 pixuri!"``.

Metoda ``str()`` convertește non-``string``-urile în ``string``-uri. În exemplul de mai sus, am convertit numărul ``6`` într-un ``string``, iar apoi am concatenat împreună toate ``string``-urile. Acum încercați și voi.
###*Exercițiu:*
Utilizați ``str()`` pentru a converti 3.14 într-un ``string``. Afișați rezultatul printr-o concatenare.

```python
# convertim pi in string
pi = 3.14
print "Valoarea lui pi este aproximativ " + str(pi)
```

###**Formatarea string-urilor**
Dacă vreți să afișați o variabilă cu un ``string``, să știți că există o metodă mai bună decât concatenarea.

```python
nume = "Mihai"
print "Salut, %s" % (nume)
```
Operatorul ``%`` scris după un ``string`` este folosit pentru a combina ``string``-urile cu variabilele. Operatorul ``%`` înlocuiește toate ``%s`` din ``string`` cu variabilele scrise după acesta.

Ce credeți că se va afișa în urma executării acestui program?

```python
string_1 = "Norvegia"
string_2 = "tara"
print "Haidem in %s. Este o %s frumoasa." % (string_1, string_2)
```
Cred că deja ați intuit că numărul operatorilor ``%`` dintr-un ``string`` trebuie să fie egal cu numărul variabilelor dintre paranteze.

```python
print "%s viitoare se va %s %s!" % ("Luna", "numi", "septembrie")
# se va afisa "Luna viitoare se va numi septembrie".
```

Sunteți foarte bravo dacă ați ajuns până aici! Deja ați învățat trei metode de creare a ``string``-urilor:

```python
'Iunie'
"Octombrie"
str(3)
```
De asemenea, ați învățat cum se afișează ``string``-urile:

```python
print "Vreau sa fiu programator"
```
Și, nu în ultimul rând, ați învățat și tehnici avansate de afișare:

```python
p = "Programare"
w = "Web"
print "%s %s" % (p, w)
```

###**Condiționalele și Control Flow**
La fel ca în viața reală, uneori codul nostru trebuie să fie capabil să ia decizii.

Până acum, tot ce am scris împreună în *Python* putea să urmeze doar un singur fir logic: fie că am adunat două numere sau fie că am afișat ceva. Codul nostru, însă, nu putea lua decizii de sine-stătător în privința a ce instrucțiuni să execute în dependență de o careva condiție. Conceptul de **Control Flow** oferă posibilitate programului de a alege ce să facă.

Pentru a intra în esența conceptului de Control Flow, trebuie să definim câteva noțiuni importante.

###**Comparatoarele**
În *Python* există șase comparatoare:

 - egal (``==``)
 - diferit (``!=``)
 - mai mic (``<``)
 - mai mic sau egal (``<=``)
 - mai mare (``>``)
 - mai mare sau egal (``>=``)

Atrageți atenția că ``==`` compară dacă două lucruri sunt egale, pe când ``=`` atribuie o valoare unei variabile.

###**Operațiile Boolean**

Operațiile ``boolean`` compară careva afirmații, rezultatul acestei comparații fiind o valoare ``boolean``. Există trei operații ``boolean``:

 - ``and``, care verifică dacă *ambele* afirmații sunt ``True``;
 - ``or``, care verifică dacă *cel puțin* o afirmație este ``True``;
 - ``not``, care este *opusul* afirmației.

În acest context, aflați că:

```python
 - True  and True  este True;
 - True  and False este False;
 - False and True  este False;
 - False and False este False;

 - True  or True  este True;
 - True  or False este True;
 - False or True  este True;
 - False or False este False;

 - Not True  este False;
 - Not False este True.
```


Să mergem mai departe.

Să zicem că avem următoarea expresie *Python*:  `1 < 2 and 2 < 3`.

Rezultatul acestei expresii va fi `True` sau `False`? Pentru a răspunde la această întrebare, să apelăm la tabelul de mai sus.

`1 < 2` este `True`. `2 < 3` este la fel `True`. `True and True` ce va fi? Corect! `True`!

Dar care vor fi rezultatele următoarelor expresii?
``1 < 2 and 2 > 3`` (*False*)
``1 < 2 or 2 > 3`` (*True*)
``1 > 2 or 2 > 3`` (*False*)
``not False`` (*True*)
``not 41 > 40`` (*False*)


Operațiile ``boolean`` nu sunt pur și simplu evaluate de la stânga la dreapta. La fel ca operațiile aritmetice, operațiile ``boolean`` au o ordine de execuție:

 - ``not`` este evaluat primul;
 - ``and`` este evaluat al doilea;
 - ``or`` este evaluat ultimul.

De exemplu, ``True or not False and False`` returnează ``True``. De ce?

``not`` este evaluat primul, astfel noi avem
``True or True and False``. Deoarece ``and``-ul e următorul evaluat, avem
``True or False``. Așa după cum am văzut mai sus, ``True or False`` este ``True``, astfel valoarea finală este ``True``!

###**Sintaxa condiționalelor**
If
``if`` (dacă) este cea mai simplă instrucțiune condițională. ``if``-ul execută o anumită bucată de cod dacă expresia pe care o verifică este ``True``.

Aici avem un exemplu de sintaxă:

```python
if 8 < 9:
    print "Opt este mai mic decat noua!"
```
În acest exemplu, ``8 < 9`` este expresia verificată de către ``if``. Această expresie este ``True``, de aceea *Python* va executa instrucțiunea ``print "Opt este mai mic decat noua!"``.

Observați cele *două puncte* la sfârșitul afirmației ``if``. Ele sunt **necesare** atunci când scrieți condiționale.

În cazul în care expresia verificată de către `if` nu ar fi `True`, dar `False`, instrucțiunea `print` nu s-ar mai fi executat. Pentru a vă convinge, haideți să schimbăm expresia `8 < 9` și s-o facem falsă.

```python
if 8 > 9:
    print "Opt este mai mic decat noua!"
```
În acest caz, consola din *Sublime Text* nu ne va afișa nimic.

Să ne întoarcem la exemplul nostru *corect*. Luați în considerare și faptul că a doua linie de cod, cea de după `if`, este scrisă cu câteva spații mai la dreapta, și mai exact cu 4 spații (sau cu un tab). Această linie de cod este **indentată**.

###**Indentarea**
Noțiunea de **indentare** este foarte importantă în programare, atunci când scrieți cod. În cazul în care scrieți cod în limbajul *Python*, această noțiune nu este doar importantă, dar este absolut **necesară**. Indentarea presupune plasarea codului pe linii, pentru scrierea corectă și cât mai clară a acestuia. Uneori, programatorii începători uită de indentare atunci când scriu cod și din acest motiv se confruntă cu erori la execuția programelor. De aceea, fiți atenți la acest capitol și **nu uitați de indentare**! <3

Dacă scriem expresia if încă o dată, dar cu a doua linie neindentată, adică așa:

```python
if 8 < 9:
print "Opt este mai mic decat noua!"
```
atunci vom primi un mesaj de eroare. În genere, un *mesaj de eroare* pe care-l primim este un indiciu a ceea ce noi n-am făcut corect în program.

Dar haideți să examinăm eroarea: ``"IndentationError: expected an indented block"``. Veți primi această eroare ori de câte ori veți uita de indentare sau indentarea va fi greșită.

Else
Instrucțiunea condițională ``else`` completează instrucțiunea condițională ``if``. O pereche ``if/else`` spune: *"Hey Python, dacă această expresie este adevărată, execută blocul de cod indentat de după if; în caz contrar, execută cealaltă bucată de cod indentat de după instrucțiunea else."*

Spre deosebire de ``if``, ``else`` nu depinde de o expresie (pe care ar trebui să o verifice). De exemplu:

```python
if 8 > 9:
    print "Opt nu este mai mare decat noua!"
else:
    print "Opt este mai mare decat noua!"
```
Luați în vedere **indentarea**!


Elif
``elif`` este prescurtarea lui "else if". ``elif``-ul spune: *"În caz contrar, dacă expresia următoare este adevărată, atunci fă asta!"*

```python
if 8 > 9:
    print "Opt nu este mai mare decat noua!"
elif 8 < 9:
    print "Opt este mai mare decat noua!"
else:
    print "Opt este mereu mai mic decat noua!"
```
În exemplul de mai sus, instrucțiunea condițională ``elif`` este executată doar în cazul în care instrucțiunea ``if`` originală este falsă.
Totuși, ce credeți că va afișa codul?


###**The Big If**
Ați făcut o muncă enormă! Dacă ați trecut ușor prin toată logica descrisă mai sus, să știți că ceea ce urmează nu e foarte complicat! Dar haideți să rezumăm ce am învățat în acest capitol:

*Comparatoarele!*

```python
3 < 4
5 >= 5
10 == 10
12 != 13
```
*Operațiile boolean!*

```python
True or False
(3 < 4) and (5 >= 5)
```
*Instrucțiunile condiționale!*

```python
if conditie_unu:
    print "Unu"
elif conditie_doi:
    print "Doi"
else:
    print "Trei"
```


###**Data și Timpul**
####**Librăria datetime**
De foarte multe ori, în programare, și mai ales în programarea web, e necesar de stabilit și de salvat data și ora exactă a unei informații. Gândiți-vă, spre exemplu, la *Facebook*. În *Facebook* e păstrată și chiar afișată data și ora exactă a fiecărei postări sau comentariu. În *Python*, putem păstra aceste informații, legate de timp, folosind librăria ``datetime``.
####**Obținerea de date și timp**
Pentru a obține data și ora curentă, putem folosi funcția numită ``datetime.now()``.

```python
from datetime import datetime
print datetime.now()
```
Prima linie de cod importă librăria ``datetime``, astfel încât s-o putem utiliza. A doua linie afișează data și ora curentă.

####**Extragerea informației**
Observați cum arată output-ul: ``2015-08-25 23:45:14.317454``. Cum veți proceda în cazul în care nu doriți să se afișeze întreaga dată și oră?

Simplu!

```python
from datetime import datetime
now = datetime.now()
current_year = now.year
current_month = now.month
current_day = now.day

print current_year
print current_month
print current_day
```
Primele două linii deja le înțelegeți. În linia a treia, am luat ``anul`` din variabila ``now`` și l-am stocat în ``current_year``. În liniile patru și cinci, am stocat ``luna`` și ``ziua`` din ``now``.


Să zicem că noi dorim să afișăm data de azi în formatul următor: *lună/ziuă/an*. Cum putem face asta? Aici ne vine în ajutor **substituția ``string``-urilor**!

```python
from datetime import datetime
new = datetime.now()

print '%s-%s-%s' % (new.year, new.month, new.day)
# se va afisa: 2015-8-17
```

Amintiți-vă că operatorul ``%`` va găsi toate scrierile ``%s`` din ``string`` și toate argumentele din paranteze. El le va afișa în ordinea corespunzătoare.
Vi s-a afișat data corect?

Sunteți bravo! Haideți să implementăm aceeași logică pentru ore, minute și secunde.

```python
from datetime import datetime
now = datetime.now()

print now.hour
print now.minute
print now.second
```

În exemplul de mai sus, noi am afișat ora, minuta și secunda curentă.

###*Exercițiu:*
Exact ca și în exercițiul anterior, afișați timpul curent în forma: *oră:minută:secundă*.

Schimbați ``string``-ul pe care-l veți afișa, astfel încât să aveți caracterul ``:`` între ``%s``.
Modificați luna, ziua și anul în ``now.hour``, ``now.minute`` și ``now.second``.

```python
from datetime import datetime
now = datetime.now()
print '%s:%s:%s' % (now.hour, now.minute, now.second)
```



##**Funcții**

Funcția este un concept important în programare (la fel ca și în matematică). Fiecare programator trebuie să poată să scrie funcții.

Funcția reprezintă un bloc de cod care cere un input, îl prelucrează, și-l returnează sub formă de output. Cu alte cuvinte, funcția cere de la noi careva parametri cu care face niște operații. În urma acestor operații efectuate asupra parametrilor, funcția ne returnează rezultatul dorit.

<div class="custom-image-shadow"><img src="/images/d4l2-basic-python-statements/functii-si-gaini.jpg" /></div>

###**Sintaxa funcțiilor**

Funcțiile sunt constituite din două componente.

Primul component este **header**-ul funcției, care include: cuvântul-cheie ``def``, **numele** funcției și **parametrii** pe care-i transmiteți funcției. Parametrii sunt opționali. Vedeți mai jos un exemplu de funcție fără parametri:

```python
# acesta este header-ul unei functii fara parametri
def hello_world():
```
Al doilea component este **corpul** funcției, care descrie, propriu-zis, ce face funcția voastră. Corpul funcției trebuie să fie **indentat**, la fel ca și în cazul instrucțiunilor condiționale. *(Vă amintiți de indentarea condiționalelor?)*

```python
print "Hello World!" # acesta este corpul functiei
```
Mai jos puteți vedea întreaga funcție, scrisă de la început până la sfârșit:

```python
def hello_world():
    print "Hello World!"
```
Pentru a **apela** funcția dată, se scrie numele ei, urmat de două paranteze ``( )``.

```python
hello_world()
```
###*Exercițiu:*
Creați o funcție numită ``felicitare``, care afișează ``string``-ul ``"La multi ani!"``, după care apelați funcția dată.

```python
def felicitare():
    print "La multi ani!"

felicitare()
```

####**Parametri**


```python
def calcul(n):
    patrat = n**2
    print str(n) + " la patrat este " + str(patrat)
    return patrat

calcul(10)
```

În exemplul de mai sus, ``n`` este **parametrul** funcției ``calcul``.


###*Exercițiu:*
Analizați funcția ``putere`` de mai jos. Ea cere doi parametri: o bază și un exponent. Primul parametru este ridicat la puterea parametrului al doilea. După cum vedeți, funcția nu este completă, de aceea adăugați de sine-stătător parametrii: ``baza`` și ``exponent``. Apoi, apelați funcția cu datele: ``2`` pentru bază și ``3`` pentru exponent.

```python
def putere(___, ___):  # adaugati aici parametrii
    rezultat = baza**exponent
    print "%s la puterea a %s este %s." % (baza, exponent, rezultat)

putere(__,__)
```
*Rezultatul vostru trebuie să arate așa:*

```python
def putere(baza, exponent):  # adaugati aici parametrii
    rezultat = baza**exponent
    print "%s la puterea a %s este %s." % (baza, exponent, rezultat)

putere(2, 3)
```
Vi s-a dat rezultatul corect? Sunt sigură că da!
###**Funcții apelând funcții**

Ați văzut deja funcții care pot afișa texte sau care pot face operații aritmetice, dar funcțiile pot fi mult mai puternice decât atât! De exemplu, o funcție poate apela o altă funcție:

```python
def func_one(n):
    return n * 5

def func_two(m):
    return func_one(m) + 7
```

###*Exercițiu:*
Să analizăm următoarele două funcții: ``o_afisare`` (care adună 1 la un număr pe care-l ia ca parametru) și ``merita_alta_afisare`` (care adună 2).

```python
def o_afisare(n):
    return n + 1

def merita_alta afisare(n):
    return n + 2
```
Schimbați corpul funcției ``merita_alta_afisare`` astfel încât ea să adune 2 la output-ul funcției ``o_afisare``:

```python
def o_afisare(n):
    return n + 1

def merita_alta_afisare(n):
    return o_afisare(n) + 2

```

####**Practice Makes Perfect**

###*Exercițiu:*
Definiți ``(def)`` o funcție numită ``cub`` care cere un parametru numit ``numar``. Nu uitați de paranteze și de două puncte!

Faceți ca funcția să returneze ``(return)`` cubul unui număr (adică un număr ridicat la puterea a treia).

Definiți a doua funcție, numită ``mai_mare``, care cere un parametru numit ``numar``.

Dacă ``(if)`` acel număr este mai mare decât 100, atunci ``mai_mare`` trebuie să apeleze funcția ``cub(numar)`` și să returneze rezultatul acesteia. În caz contrar, ``mai_mare`` trebuie să returneze ``False``.

Nu uitați că instrucțiunile condiționale ``if`` și ``else`` necesită ``:`` la sfârșitul liniei!

```python
def cub(numar):
    return numar ** 3

def mai_mare(numar):
    if numar > 100:
        return cub(numar)
    else:
        return False
```
###**Importarea modulelor**
Acum, să trecem la un capitol din *Python* extrem de interesant și, în același timp foarte important - importarea modulelor!

Ce înseamnă un modul?

De-a lungul timpului, programatorii s-au confruntat cu problema scrierii prea dese a unuia și aceluiași fragment cu cod, fapt care le cerea mult timp pierdut și prea multe linii de cod scrise. Pentru a-și ușura lucrul, programatorii s-au gândit să facă niște fișiere care, odată importate în program, le vor permite să scrie unele funcționalități mai simplu, mai repede și mai eficient.

Un **modul** este un fișier care conține multe definiții, inclusiv variabile și funcții, pe care le puteți folosi odată ce el, acest modul, a fost importat în programul vostru.

Înainte de a importa ceva, haideți să vedem ce știe *Python* implicit, adică fără de module. Vom lua exemplul funcției radical. Linia de mai jos trebuie să afișeze ``5``.

```python
print sqrt(25)
```
Hey, dar nu ni s-a afișat ``5``! Se pare că avem o eroare. Să analizăm mesajul:

```python
NameError: name 'sqrt' is not defined
```

*Python* ne-a spus: ``"NameError: name 'sqrt' is not defined."`` *Python* nu știe ce înseamnă extragerea rădăcinii… până când!

În *Python* există un modul, numit ``math`` (de la matematică), care include un număr mare de variabile și funcții utile, iar ``sqrt()`` este una dintre aceste funcții. Pentru a accesa ``math``, tot de ce avem nevoie este cuvântul-cheie ``import``.

```python
import modul
```
Acest fel de import de modul (ca cel de mai sus) se numește **import generic**.


###*Exercițiu:*
În acest exercițiu, trebuie să faceți două lucruri.

Primul lucru este să scrieți ``import math`` în prima linie de cod.

Al doilea lucru este să scrieți ``math.sqrt()`` cu argumentul ``25`` și să afișați rezultatul. În felul acesta îi veți spune lui *Python* nu doar să importe ``math``, dar și să extragă rădăcina dintr-un număr.

```python
import math
print math.sqrt(25)
```
####**Importarea funcțiilor**

Minunat! Acum *Python* știe cum să extragă rădăcina pătrată dintr-un număr!

Totuși, noi am avut nevoie, de fapt, doar de funcția ``sqrt``, iar să scrii mereu ``math.sqrt()`` poate deveni frustrant.

În *Python*, este posibil de importat doar unele din multiplele variabile sau funcții dintr-un anumit modul. Pentru asta, avem nevoie de cuvântul-cheie ``from``:

```python
from modul import functie
```
În acest fel, puteți scrie doar ``sqrt()`` pentru a obține rădăcina pătrată a unui număr. Nu mai aveți nevoie de ``math.sqrt()``!

Să mergem mai departe.

Haideți să importăm doar funcția ``sqrt`` din modulul ``math``. (Nu avem nevoie de ``()`` după ``sqrt``!)

```python
from math import sqrt
print sqrt(25)
```
####**Importurile universale**

Fain! Am găsit o modalitate corectă de a selecta variabile și funcții din modulul pe care-l vrem!

Iar dacă noi în continuare dorim să obținem absolut toate variabilele și funcțiile dintr-un modul, dar nu vrem să scriem permanent ``math.``, ce facem?

**Importul universal** vine cu o soluție! Sintaxa acestuia este:

```python
from modul import *
```

Haideți să utilizăm ``from modul import *`` pentru a importa tot din modulul ``math``.

```python
from math import *
print sqrt(25)
```

Totul e bine, dar...
Importurile universale pot să pară ok din exterior, dar ele nu sunt o idee bună dintr-un motiv foarte important: ele fac programul vostru plin de o groază de variabile și funcții inutile sau care vă pot crea probleme.

Să zicem că ați creați funcția voastră și ați numit-o ``sqrt``. Tot în același program, ați importat modulul ``math``. În acest caz, funcția voastră ``sqrt`` va fi în siguranță: veți avea funcția pe care ați creat-o – ``sqrt``, și funcția din modul – ``import.sqrt``. Însă, dacă ați fi scris ``from math import *``, v-ați fi confruntat cu o problemă: două funcții diferite, dar cu același nume. Iar dacă ați fi scris de mai multe ori în același program ``import *``, nu ați fi fost capabili să înțelegeți care variabilă sau care funcție din care modul vine.

Din aceste motive, cel mai bine este fie să utilizați ``import modul`` și apoi ``modul.nume``, fie pur și simplu să faceți ``import`` unor variabile și funcții specifice din diferite module.

###**Review: Funcții**


###*Exercițiu:*


Definiți (`def`) o funcție, numită `shut_down`, care cere un singur parametru `s`. Nu uitați de paranteze și de două puncte!

Dacă (`if`) funcția `shut_down` primește un `s` egal cu `"yes"`, ea trebuie să vă returneze `"Shutting down"`, iar dacă (`elif`) `s` este egal cu `"no"`, atunci funcția trebuie să vă returneze `"Shutdown aborted"`. În final, dacă `shut_down` nu primește nimic din cele spuse mai sus, atunci funcția trebuie să returneze `"Sorry"`.


```python
def shut_down(s):
  if s == "yes":
    return "Shutting down"
  elif s == "no":
     return "Shutdown aborted"
  else:
      return "Sorry"
```

###**Review: Module**
Să ne reamintim despre importarea modulelor (și, în mod special, ce este accesibil din modulul `math`).

###*Exercițiu:*
Imporați modulul `math` prin oricare metodă doriți voi. Apelați funcția `sqrt` al acestui modul cu argumentul `13689` și afișați valoarea.

```python
from math import sqrt
print sqrt(13689)
```

###**Liste și Dicționare**
####**Introducere în liste**

**Listele** reprezintă un alt tip de date din *Python*. Ele reprezintă o colecție de date. Aceste date pot fi de orice tip doriți.

Listele sunt constituite dintr-un nume și din itemii atribuiți.

Puteți atribui itemi unei liste printr-o expresie de forma:

```python
nume_lista = [item_1, item_2]
```
Observați că itemii sunt scriși între paranteze patrate. O listă poate fi și goală:

```python
lista_goala = []
```


Lista de mai jos,  `zoo_animale`, are trei itemi:

```python
zoo_animale = ["urs", "vulpe", "tigru"]
```
Adăugați un al patrulea item listei! Introduceți numele animalului vostru preferat (ca un `string`) după `"tigru"`, prin virgulă. Afișați rezultatul final.

```python
zoo_animale = ["urs", "vulpe", "tigru", "elefant"]
```
####**Accesarea după index**


Puteți accesa un item al listei după index-ul său. Un **index** e ca o adresă care identifică locul itemului în listă. Index-ul se scrie direct după numele listei, în paranteze patrate, cam așa: `nume_lista[index]`.


Indecșii listei încep cu 0, nu cu 1! (Da, da, la fel ca și la `string`-uri). Puteți să accesați primul element al unei liste în felul următor: `nume_lista[0]`. Al doilea item îl accesați așa: `nume_lista[1]`. Programatorii iubesc să numere de la zero.


###*Exercițiu:*

Creați o listă, numită `numere,` cu itemii `5`, `6`, `7` și `8`. Din rând nou, afișați rezultatul adunării itemilor doi și patru din listă.

```python
numere = [5, 6, 7, 8]
print numere[1] + numere[3]
```
####**New Neighbors**


Știți deja cum se accesează un item al listei. (După index).

```python
zoo_animale = ["urs", "vulpe", "tigru", "elefant"]
print zoo_animale[0]
# se va afisa "urs"
```
Buuuuuun.

Într-o listă, de asemenea, se pot realoca itemi:

```python
zoo_animale = ["urs", "vulpe", "tigru", "elefant"]
zoo_animale[2] = "girafa"
print zoo_animale
# se va afisa ["urs", "vulpe", "girafa", "elefant"]
```

###*Exercițiu:*

Scrieți codul prin care veți înlocui itemul cu valoarea `"elefant"` cu oricare alt animal doriți voi. Afișați lista finală.

```python
zoo_animale = ["urs", "vulpe", "girafa", "elefant"]
zoo_animale[3] = "zebra"
print zoo_animale
# se va afisa ["urs", "vulpe", "girafa", "zebra"]
```

####**Late Arrivals**

O listă nu e obligată să aibă lungime fixă. Puteți adăuga itemi într-o listă oricând vreți voi!

```python
litere = ['a', 'b', 'c']
litere.append('d')
print litere
```
În exemplul de mai sus, de la început, am creat o listă numită `litere`.

Apoi, am adăugat `string`-ul `"d"` la sfârșitul listei.

În final, s-a afișat `['a', 'b', 'c', 'd']`.

###*Exercițiu:*
Mai jos, aveți o listă goală, numită `bagaj`.

```python
bagaj = []
```
Adăugați în lista dată trei obiecte (ochelari de soare, spre exemplu). Folosiți metoda `append()`. Afișați lista finală.

```python
bagaj = []
bagaj.append("ochelari de soare")
bagaj.append("palarie")
bagaj.append("costum de baie")
print bagaj
```
####**List Slicing**
Uneori, veți avea nevoie să accesați doar o porțiune a listei.

Să executăm codul de mai jos!

```python
litere = ['a', 'b', 'c', 'd', 'e']
slice = litere[1:3]
print slice
print litere
```

 În exemplul de mai sus, de la început am creat o listă nouă, numită `litere`.

Apoi, am luat o secvență din `litere` și am stocat-o în `slice`.

În rezultat, instrucțiunea `litere[1:3]` a afișat rezultatul `['b', 'c']`. E de înțeles de ce s-a afișat itemul `"b"` cu indicele `1`. Dar de ce itemul `"d"`, cu indicele `3`, nu s-a afișat? Deoarece acest mod de "feliere a listelor" se stopează cu un index înainte de cel scris în instrucțiune.

În final, am afișat `['a', 'b', 'c', 'd', 'e']`, pentru a arăta că nu am modificat nimic din lista inițială.


Mai jos aveți o listă, numită `culori`, care conține 4 itemi.

```python
culori = [ 'negru', 'rosu', 'albastru', 'verde' ]
```

Această listă fi sortată în ordine alfabetică. Asta nu e complicat! Priviți aici:

```python
culori.sort()
# se va afisa ['albastru', 'galben', 'negru', 'rosu', 'verde']
```
Metoda `.sort()` a aranjat `string`-urile în ordine alfabetică în mai puțin de o secundă!


####**Remove a Few Things**

Uneori, avem nevoie să ștergem ceva din listă.

```python
beatles = [ "john", "paul", "george", "ringo", "stuart" ]
beatles.remove("stuart")
print beatles
# se va afisa ["john", "paul", "george", "ringo"]
```

În exemplul de mai sus, am creat o listă cu 5 `string`-uri.

Apoi, am eliminat primul item din `beatles` care coincide cu `string`-ul `"stuart"`.

În final, am afișat lista pentru a ne asigura că `"stuart"` într-adevăr a fost eliminat.

###*Exercițiu:*
Creați o listă nouă, numită `rechizite`. Lista trebuie să aibă minim 5 itemi. Ulterior, eliminați un item la dorința voastră și afișați rezultatul!

```python
rechizite = ['pix', 'creion', 'radiera', 'rigla', 'compas']
rechizite.remove('radiera')
print rechizite
```

###**Dicționare**

Un **dicționar** este asemănător cu o listă, doar că în cazul dicționarelor puteți să accesați valorile prin intermediul unei chei, și nu prin intermediul unui index. O **cheie** poate fi un `string` sau un număr. Dicționarele se scriu între acolade, în felul următor:

```python
dictionar = {'cheie1' : 1, 'cheie2' : 2, 'cheie3' : 3}
```
Mai sus avem exemplul unui dicționar cu trei perechi *cheie-valoare*. Cheia `cheie1` are valoarea `1`, `cheie2` - valoarea `2` ș.a.m.d.

Dicționarele sunt utile pentru asemenea lucruri, ca: lista numerelor de telefoane (având perechile *nume - număr*), pagini de logare (având perechile *adresa de e-mail - nume de utilizator*) și nu doar!

Mai jos, vă prezint un exemplu de dicționar, care stochează informația pentru perechile *e-mail - parolă*.

```python
d = { 'alexandru@gmail.com' : 2345,
      'olga@yahoo.com' : 6789,
      'daniela@mail.md' : 1234 }
print d
```

Accesarea unei valori din dicționar după o cheie e aceeași cum am accesa valorile din liste după indecși:

```python
print d['alexandru@gmail.com']
```


####**New Entries**

La fel ca listele, dicționarele sunt "flexibile".  Aceasta înseamnă că ele pot fi schimbate după ce au fost create. Un avantaj al acestui fapt este ceea că putem adăuga în dicționarele deja create noi perechi *cheie-valoare*, în felul următor:

```python
nume_dict[cheie_noua] = valoare_noua
```
O pereche goală de acolade este un dicționar gol, la fel cum o pereche goală de `[]` este o listă goală.

###*Exercițiu:*

Haideți să creăm un dicționar nou, numit `meniu`.

```python
meniu = {}
```
Acum să adăugăm în acest dicționar o pereche *cheie-valoare*:

```python
meniu['Supa cu ciuperci'] = 40.00
```
În final, să afișăm prețul supei cu ciuperci:

```python
print meniu['Supa cu ciuperci']
```

###*Exercițiu:*
Adăugați, la meniul de mai sus, cel puțin trei feluri de bucate și indicați-le prețul. Vă puteți orienta după exercițiul de mai sus!

```python
meniu = {}
meniu['Pizza cu broccoli']   = 60.00
meniu['Cartofi prajiti']     = 35.00
meniu['Inghetata cu zmeura'] = 29.00
print meniu
```

####**Changing Your Mind**

Deoarece dicționarele sunt flexibile, ele pot fi modificate în diverse moduri. Itemii pot fi eliminați dintr-un dicționar cu comanda `del`:

```python
del nume_dict[nume_cheie]
```
Codul de mai sus va șterge din dicționar cheia `nume_cheie` și valoarea asociată acesteia.

O valoare nouă poate fi asociată unei chei prin atribuire:

```python
nume_dict[cheie] = valoare_noua
```

Mai jos, aveți creat un dicționar cu animalele de la Grădina Zoologică și un exemplu de cum se elimină unul din itemi.

```python
# cheie - nume_animal : valoare - locatia
zoo_animale = { 'Maimuta' : 'Africa',
                'Tigru' : 'Asia',
                'Cangur' : 'Australia',
                'Unicorn' : 'Wonderland' }

# stergem 'Unicorn'. (Unicornii sunt excesiv de scumpi.)
del zoo_animale['Unicorn']

print zoo_animale
```

Eliminați și maimuța din acest dicționar. Apoi, atribuiți-i altă locație tigrului. În final, afișați dicționarul!

```python
del zoo_animale["Maimuta"]
zoo_animale["Tigru"] = "America de Sud"
print zoo_animale
```

####**It's Dangerous to Go Alone!**

Să rezumăm un pic dicționarele:

```python
my_dict = {
    "day": [ "s", "u", "n", "d", "a", "y" ],
    "cash": -4483,
    "mood": "tired"
}
print my_dict["day"][0]
```
În exemplul de mai sus, am creat un dicționar care conține diferite tipuri de valori.

Cheia `"day"` are o listă, cheia `"cash"` are un `int` și cheia `"mood"` are un `string`.

În final, am afișat litera `"s"`. Când accesăm o valoare într-un dicționar de genul `my_dict["day"]`, avem acces direct la valoare. Astfel, putem accesa itemul de la index-ul `'0'` din listă stocat de cheia `"day"`.

###*Exercițiu:*

Analizați sevența de cod de mai jos:

```python
liceu = {
    'elevi' : 500,
    'olimpici' : ['matematica', 'informatica', 'geografie'], # am atribuit o lista la cheia 'olimpici'
    'premii' : ['sport', 'teatru', 'dans', 'pictura']
}

# sortam lista cu cheia 'olimpici'
liceu['olimpici'].sort()

# adaugam o cheie noua 'cursuri' si ii atribuim o lista
liceu['cursuri'] = ['programare', 'antreprenoriat', 'engleza']

print liceu

```
Adăugați o nouă cheie la dicționarul `liceu`, numită `'fesivitati'`.
Valoarea cheiei `'festivitati'` trebuie să fie o listă ce va conține: `'halloween'`, `'revelion'` și  `'ultimul sunet'`.

Prin `.sort()`, sortați itemii listei `premii`. Apoi, eliminați din această listă, prin `.remove()`, itemul stocat sub cheia `'teatru'`.

Adăugați `50` la numărul stocat sub cheia `"elevi"`.


```python
liceu["festivitati"] = ["halloween", "revelion", "ultimul sunet"]
liceu['premii'].sort()
liceu["premii"].remove("teatru")
liceu['elevi'] = liceu['elevi'] + 50

print liceu
```

###**Function Recap**


```python
number = 5

def my_function(x):
    return x * 3

print my_function(number)
```
Ce va afișa funcția de mai sus? Corect, `15`!

####**More than one parameter**
Acest exercițiu o să ne ajute să recapitulăm cum se utilizează mai mult de un parametru într-o funcție.

###*Exercițiu:*

Definiți două variabile, `m` și `n`, cu următoarele valori stocate în ele: `5` și, respectiv, `13`.

Definiți o funcție, numită `add_function` care cere 2 parametri: `x` și `y` și îi adună împreună.

În final, afișați rezultatul apelării funcției `add_function` cu parametrii `m` și `n`.

```python
m = 5
n = 13

def add_function(x, y):
    return x + y


print add_function(m, n)
```

####**Strings in functions**
Acest exercițiu o să vă reamintească cum se utilizează `string`-urile în funcții.

###*Exercițiu:*

Creați o variabilă `n` cu `string`-ul `"Hello"` stocat în ea.

Scrieți o funcție, numită `string_function` care cere un parametru de tip `string` `(s)` și returnează acest parametru concatenat cu cuvântul `'world'`. Folosiți un spațiu înainte de cuvântul `"world"`!

În final, afișați rezultatul apelării funcției `string_function` cu parametrul `n`.


```python
n = "Hello"

def string_function(s):
    return s + " world"


print string_function(n)
```

###**Introduction to Using Functions With Lists**

####**Passing a list to a function**
O listă se transmite unei funcții la fel cum un parametru simplu se transmite unei funcții.

```python
def list_function(x):
    return x

n = [3, 5, 7]
print list_function(n)
```

####**Using an element from a list in a function**
Atunci când transmitem o listă unei funcții, noi stocăm în funcție această listă drept parametru (la fel ca și în cazul `string`-urilor sau numerelor!)

```python
def first_item(items):
    print items[0]

numbers = [2, 7, 9]
first_item(numbers)
```
În exemplul de mai sus, am definit o funcție numită `first_item`. Ea are un singur argument, numit `items`.

În interiorul funcției, am afișat itemul stocat la index-ul zero.
Apoi, am creat o listă numită `numbers`.

La final, am apelat funcția `first_item` cu `numbers` ca parametru, care afișează `2`.

####**Modifying an element of a list in a function**
A schimba un element în lista unei funcții este aceeași dacă pur și simplu modificăm un element într-o listă din afara funcției.

```python
def double_first(n):
    n[0] = n[0] * 2

numbers = [1, 2, 3, 4]
double_first(numbers)
print numbers
```
Am creat o listă numită `numbers`.

Am utilizat funcția `double_first` pentru a modifica această listă.

La final, am afișat `[2, 2, 3, 4]`.

Apoi, am transmis o listă funcției și am modificat lista dată, așa ca în funcția `double_first` de mai sus, și la final am modificat lista originală.

####**List manipulation in functions**
Puteți, de asemenea, să adăugați sau să ștergeți itemi din lista unei funcții la fel ca și cum ați manipula cu lista în afara funcției.

```python
my_list = [1, 2, 3]
my_list.append(4)
print my_list
# prints [1, 2, 3, 4]
```
Exemplul de mai sus ne reamintește cum se adaugă un item într-o listă.

##**Loops**
####**For your health**
Cea mai bună metodă de a *itera* în *Python* este `for loop`. Dar ce înseamnă să iterezi?

Când un proces sau o secvență de program este executată multiplu, adică repetată, atunci această secvență se numește **iterată**. `For loop` reprezintă o metodă de iterare, care repetă aceeași bucată de cod pentru a determina mai multe valori ale acelorași variabile.

Să analizăm exemplul următor:

```python
for i in range(10):
    print i
```
`range` este o funcție care primește un parametru `n` și returnează o listă de la `0` la `n-1`.

Această sintaxă ne spune următoarele: *"pentru fiecare număr `i` din range de la `0` la `10`, afișează `i`"*.

Observați că instrucțiunea iterativă `for`, la fel ca și instrucțiunea condițională `if` (sau `elif`, `else`), necesită două puncte la sfârșit de linie, respectiv necesită ca și codul ce urmează să fie identat.

Mai observați că, deși argumentul transmis funcției `range()` este `10`, consola ne-a afișat numerele de la 0 până la 9. Dacă doriți să se afișeze la consolă inclusiv numărul `10`, atunci trebuie să transmiteți argumentul `11` funcției `range()`.


Acum, haideți să creăm un loop care va putea să adauge ceva într-o listă.


```python
numbers = []

for i in range(3):
    numbers.append(i)

print numbers
```

Rezultat: `[0, 1, 2]`.


####**For your lists**
Cel mai utilizat `for` din *Python* este `for`-ul folosit pentru a itera prin liste.

```python
numbers  = [7, 9, 12, 54, 99]

print "This list contains: "

for num in numbers:
    print num
```

În exemplul de mai sus, la fiecare iterație, variabila `num` va fi următoarea valoare din lista `numbers`. Astfel, prima dată, `num` va fi `7`, a doua oară - va fi `9`, apoi `12`, `54`, `99`, iar după asta iterația se va termina, deoarece nu mai există valori în listă.

###*Exercițiu:*

Tot pentru  lista `numbers`, scrieți un alt loop, care va itera prin ea și va afișa fiecare element al listei ridicat la patrat, fiecare din rând nou.

```python
numbers  = [7, 9, 12, 54, 99]

# Add your loop below!
for num in numbers:
    num = num ** 2
    print num
```

###**Looping over a dictionary**
Probabil vă întrebați: *"Cum e posibil de iterat prin dicționare? Trebuie de folosit cheia sau valoarea?"*

Răspunsul este: **folosim cheia ca să obținem valoarea**.

```python
d = {'x': 9, 'y': 10, 'z': 20}
for key in d:
    if d[key] == 10:
        print "This dictionary has the value 10!"
```
În acest exemplu, de la început am creat un dicționar cu numele `d`. El are `string`-uri în rol de chei și numere în rol de valori.

Apoi, am iterat prin dicționar, de fiecare dată stocând cheile în `key`.

Ulterior, am verificat dacă valoarea unei chei din dicționar este egală cu `10`.

La final, am afișat: `This dictionary has the value 10!`



În secvența de cod de mai jos, am creat un dicționar `d`. Am folosit instrucțiunea iterativă `for` pentru a afișa fiecare cheie din dicționar, urmată de valoarea atribuită acestei chei.

```python
d = {'a': 'apple', 'b': 'berry', 'c': 'cherry'}

for key in d:
    print key, d[key]
```

##**Lucru în echipă cu mentorii**

 1. **Exercițiul 1**
 Scrieți o funcție care va afișa rădăcinile următoarei ecuații de gradul 2: `123 * x**2 - 232 * x + 1 = 0`.

 2.  **Exercițiul 2**
Scrabble este un joc în care participanții câștigă puncte scriind cuvinte. Cuvintele sunt evaluate prin adunarea punctajului fiecărei litere.

  Mai jos aveți dicționarul tuturor literelor din alfabet cu punctajul corespunzător lor.

```python
score = {"a": 1, "c": 3, "b": 3, "e": 1, "d": 2, "g": 2,
         "f": 4, "i": 1, "h": 4, "k": 5, "j": 8, "m": 3,
         "l": 1, "o": 1, "n": 1, "q": 10, "p": 3, "s": 1,
         "r": 1, "u": 1, "t": 1, "w": 4, "v": 4, "y": 4,
         "x": 8, "z": 10}
 ```


  De exemplu, cuvântul `"helix"` va acumula 15 puncte deoarece suma literelor din acest cuvânt este: 4 + 1 + 1 + 1 + 8.


  Definiți o funcție care primește un cuvânt (evident de tip `string`) și returnează punctajul echivalent al sumei literelor acestui cuvânt.





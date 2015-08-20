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


- `int` <br>
Primul tip de variabile se numește `int`. `int` reprezintă aceeași mulțime *Z* din matematică, adică mulțimea numerelor întregi. 


```python
my_int = 3
your_int = -4
```

- `float` <br>
`float` este un alt tip de variabilă, care include în sine mulțimea numerelor fracționare din matematică, adică cifrele cu punct. 


```python
my_float = 3.1
your_float = 4.5
```

- `bool` <br>
`Bool`-urile reprezintă un tip de variabile care pot avea doar două valori. Așa cum un întrerupător poate avea doar două stări: conectat sau deconectat, la fel și un bool poate fi doar `True` sau `False`. Puteți utiliza variabile pentru a stoca `bool`-urile:


```python
my_bool = True
your_bool = False
```

- `string` <br>
Cu tipul de date `string` noi deja am lucrat. Țineți minte când am executat instrucțiunea `print "Numele Vostru"`? În această instrucțiune, `"Numele Vostru"` este scris în ghilimele. Toate variabilele care se scriu între ghilimele sunt de tip `string`. Un `string` poate fi o literă, un cuvânt, o mulțime de cuvinte, chiar și cifre, spații sau simboluri atâta timp cât ele sunt scrise între ghilimele.


```python
my_string = "pix"
your_sring = "Tu ai 24 pixuri!"
```

###*Live coding:*
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
###*Live coding:*
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

###*Live coding:*
Creați o variabilă și atribuiți-i o valoare de tip ``string``. Înainte de asta, adăugați un comentariu în care puteți scrie orice doriți. Nu uitați de semnul #.


```python
# acesta este un comentariu
oras = "Madrid"
```

###**Matematică**
De matematică nu scăpați nici în programare. Partea bună este că programarea vă ajută să faceți operațiile matematice simplu și rapid.  Putem să adunăm, scădem, înmulțim, împărțim și nu doar!
###*Live coding:*
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


###*Live coding:*

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

###*Live coding:*

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

<div class="custom-image-shadow"><img src="/images//d4l2-basic-python-statements/diagrama.png" /></div>

``String``-ul ``"Hello World"`` are 13 caractere, enumerate de la 0 la 12. Observați că și caracterului space (de după virgulă) îi este atribuit un index (indicele 6).

Prin urmare, dacă doriți să accesați caracterul ``"w"``din ``string``-ul ``"Hello World"``, trebuie pur și simplu să scrieți ``"Hello World"[8]`` (pentru că enumerarea începe tot timpul de la 0!).

Pentru a însuși această logică mai bine, vă aduc un exemplu simplu:

```python
p = "pix"[0]
e = "creion"[2]
```
În acest exemplu, am creat o variabilă nouă numită ``p`` și i-am atribuit "p" – caracterul de la index-ul zero al ``string``-ului ``"pix"``. Apoi, am creat o variabilă nouă, numită ``e``, căreia i-am atribuit caracterul cu index-ul 2 din ``string``-ul ``"creion"``. În Python, enumerarea începe de la zero, și nu de la unu.

###*Live coding:*
Atribuiți variabilei ``litera_patru`` a patra literă din ``string``-ul ``"prieten"``. Țineți minte că a patra literă nu se află la index-ul 5. Începeți să numărați indecșii de la zero.

```python
litera_patru = "prieten"[4]
print litera_patru
```
###**Concatenarea string-urilor**
Să mergem mai departe! Voi deja cunoașteți ``string``-urile! De asemenea, voi deja cunoașteți și operațiile aritmetice din *Python*! Zic să combinăm aceste două concepte! 

###*Live coding:*
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

###*Live coding:*


```python
print "Eu am " + str(6) + " pixuri!"
```
În acest caz, se va afișa: ``"Eu am 6 pixuri!"``.

Metoda ``str()`` convertește non-``string``-urile în ``string``-uri. În exemplul de mai sus, am convertit numărul ``6`` într-un ``string``, iar apoi am concatenat împreună toate ``string``-urile. Acum încercați și voi.
###*Live coding:*
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

###*Live coding:*
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


###*Live coding:*

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
Noțiunea de **indentare** este foarte importantă în programare, atunci când scrieți cod. În cazul în care scrieți cod în limbajul *Python*, această noțiune nu este doar importantă, dar este absolut **necesară**. Indentarea presupune plasarea codului pe linii, pentru scrierea corectă și cât mai clară a acestuia. Uneori, programatorii începători uită de indentare atunci când scriu cod și din acest motiv se confruntă cu erori la execuția programelor. De aceea, fiți atenți la acest capitol și **nu uitați de indentare**! :heart:

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



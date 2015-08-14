---
layout: default
title: Basic Python Statements
---

#Basic Python Statements

În decursul acestei sesiuni, veți afla ce înseamnă un limbaj de programare, de ce am ales să studiem **Python** și care este sintaxa acestuia. De asemenea, vă veți familiariza cu practica și logica de bază a scrierii unui program, făcând referință la unele situații cotidiene. În felul acesta, veți percepe mai ușor necesitatea programării în viața de zi cu zi.

####Ce este un limbaj de programare?
Un **limbaj de programare** este un mijloc de comunicare cu computerul. El reprezintă un set bine definit de expresii și reguli necesare pentru a formula instrucțiuni pe care ulterior computerul le va procesa. Limbajul de programare dă posibilitate programatorului să specifice în mod exact și amănunțit acțiunile pe care trebuie să le execute calculatorul, în ce ordine și cu ce date. Această specificare constă în scrierea programelor necesare.

####Ce este Python și de ce am l-am ales pentru a-l studia?
Ce limbaje de programare cunoașteți? Probabil ați auzit de *HTML*, *CSS* sau *Pascal*. Da, ele toate sunt limbaje de programare. Ca și *Python*, de altfel.

Dacă există atât de multe limbaje de programare, de ce noi am ales să studiem anume *Python*? Deoarece *Python* este un limbaj de programare:

 - **modern**;
 - **renumit**, fiind utilizat la ora actuală la o scară largă de către programatorii din toată lumea, crescându-și popularitatea tot mai mult;
 - **simplu**, întrucât se pune accentul pe curățenia și simplitatea codului, iar sintaxa sa le permite dezvoltatorilor să exprime unele idei programatice într-o manieră mai clară și mai concisă decât în alte limbaje de programare (de exemplu *Pascal*).

Cu ajutorul *Python*, puteți crea aplicații web, jocuri și chiar motoare de căutare.

> **Notă:** Există foarte multe site-uri și aplicații web sau mobile scrise în *Python* pe care sigur le cunoașteți și chiar le utilizați zilnic: *Google*, *YouTube*, *Facebook*, *Pinterest*, *Instagram*, *DropBox* ș.a.

###**Sintaxa Python**

Pentru a scrie și executa toate exercițiile propuse mai jos, veți folosi editorul de text *Sublime Text*.

Deschideți *Sublime Text* și mergeți la bara de meniuri de sus. Selectați `File -> New File`. După ce vi s-a deschis un fișier nou, apăsați `Ctrl + s` pe tastatură. Salvați fișierul sub orice denumire doriți, dar neapărat cu extensia `.py`. Vă amintiți ce va povestit postetit Sergiu despre extensiile fișierelor? Eu o să-mi numesc fișierul `test.py`. Puteți face și voi la fel. Selectați mapa în care veți salva fișierul și apăsați `Save`. Acuma, sunteți gata să efectuați exercițiile propuse la această sesiune.

Pentru început, executați următoarea instrucțiune:

```python
print "Numele Vostru"
```

Pentru a face acest lucru, copiați textul de mai sus (dar cu numele vostru între ghilimele) și apăsați `Ctrl + b` pe tastatură. În partea de jos a editorului de text, trebuie să vă apară consola, unde vă veți vedea numele afișat.

Instrucțiunea ``` print ``` este simplă și foarte des utilizată, practic în orice program. Ea nu face altceva, decât să afișeze la ecran informația pe care i-o transmiteți.

####**Variabile și constante**
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

###*Exercițiu:*
Creați o variabilă ```my_int``` și atribuiți-i o valoare de tip ```int```.
Creați o variabilă ```my_float``` și atribuiți-i o valoare de tip ```float```.
Creați o variabilă ``my_bool`` și atribuiți-i o valoare de tip ``bool``.
Creați o variabilă ``my_string`` și atribuiți-i o valoare de tip ``string``.

```python
my_int = 7
my_float = 1.23
my_bool = True
my_string = "lalala"
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
print my_int
```

###*Live coding:*
Creați o variabilă cu orice nume doriți voi și atribuiți-i valoarea 7. După asta, schimbați valoarea variabilei voastre de la 7 la 3. În final, cu ajutorul instrucțiunii ``print``, afișați valoarea variabilei.

```python
# cream my_int cu valoarea 7
my_int = 7
# schimbam valoarea my_int
my_int = 3
# daca scriem print my_int, ce credeti ca va afisa consola?
print my_int
```
###**Comentarii**
La exercițiul anterior, ați observat că am utilizat semnul ``#`` înaintea unor linii de cod. În aceste linii de cod eu am dat niște explicații a ceea ce fac eu în program. Semnul ``#`` semnifică începutul unui comentariu. Un **comentariu** este o linie de cod pe care *Python* nu încercă s-o execute. Comentariile sunt utile doar pentru oameni.

La ce bun s-au inventat comentariile? Comentariile fac programul vostru mai ușor de înțeles. Când vă uitați la codul pe care l-ați scris cu ceva timp în urmă sau alții doresc să colaboreze cu voi, ei pot citi comentariile și astfel percep foarte repede ce anume face programul vostru.

###*Exercițiu:*
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
Să ne întoarcem un pic la ``string``-uri. ``String``-urile sunt cool. Și asta deoarece în *Python*, asupra lor se pot chema o mulțime de metode utile și interesante pentru a însuși mai bine programarea web. Așa după cum am mai menționat, un ``string`` poate conține litere, numere, simboluri și spații. Ele trebuie să fie scrise între ghilimele. Să analizăm un exemplu:

```python
nume = "Mihai"
varsta = "21"
mancare = 'piept de pui'
```
În acest exemplu, am creat o variabilă ``nume`` și i-am atribuit ``string``-ul ``"Mihai"``. De asemenea, am creat variabila ``varsta`` cu ``string``-ul ``"21"`` și ``mancare`` cu ``'piept de pui'``. Observați că în ultimul exemplu, ``'piept de pui'`` nu este scris între ghilimele duble. Aceasta nu este o problemă. *Python* acceptă și un asemenea fel de scriere a ``string``-urilor.
###*Exercițiu:*
Ce ziceți să căpătăm un pic de practică în lucrul cu ``string``-urile? Setați următoarele variabile la valorile corespunzătoare lor:
Setați ``disciplina`` la ``"Informatica"``.
Setați ``profesor`` la ``"profesorul vostru de informatica"``.
Setați ``coleg`` la ``"colegul vostru de banca de la informatica"``.

```python
# scriem variabilele cu valorile corespunzatoare lor mai jos
disciplina = "Informatica"
profesor = "Veronica"
coleg = "Corina"
# afisam mai jos valorile variabilelor create
print disciplina
print profesor
print coleg
```
###**Accesarea după indice**
Minunat! Acum, că v-ați reamintit ce înseamnă ``string``-urile, haideți să le analizăm mai detaliat. Trebuie să cunoașteți că toate caracterele dintr-un ``string`` sunt aranjate într-o ordine. Această ordine presupune ca fiecărui caracter din ``string`` să-i fie atribuit un număr. Acest număr este numit **indice**. Să analizați diagrama de mai jos:

*diagrama*

``String``-ul ``"Hello, world!"`` are 13 caractere, enumerate de la 0 la 12. Observați că și caracterului space (de după virgulă) îi este atribuit un indice (indicele 6).

Prin urmare, dacă doriți să accesați caracterul ``"w"``din ``"string``-ul ``"Hello, world!"``, trebuie pur și simplu să scrieți ``"Hello, world!"[8]`` (pentru că enumerarea începe tot timpul de la 0!).

Pentru a însuși această logică mai bine, vă aduc un exemplu simplu:

```python
p = "pix"[0]
e = "creion"[2]
```
În acest exemplu, am creat o variabilă nouă numită ``p`` și i-am atribuit "p" – caracterul de la indicele zero al ``string``-ului ``"pix"``. Apoi, am creat o variabilă nouă, numită ``e``, căreia i-am atribuit caracterul cu indicele 2 din ``string``-ul ``"creion"``. În Python, enumerarea începe de la zero, și nu de la unu.
###*Exercițiu:*
Atribuiți variabilei ``litera_patru`` a patra literă din ``string``-ul ``"prieten"``. Țineți minte că a patra literă nu se află la indicele 5. Începeți să numărați indicii de la zero.

```python
litera_patru = "prieten"[4]
print litera_patru
```
###**Concatenarea string-urilor**
Să mergem mai departe! Voi deja cunoașteți ``string``-urile! De asemenea, voi deja cunoașteți și operațiile aritmetice din *Python*! Zic să combinăm aceste două concepte! Haideți să analizăm următoarea linie de cod:

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
# convertim 3.14 in string
print "Valoarea lui pi este aproximativ " + str(3.14)
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
###**Indentarea**
Noțiunea de **indentare** este foarte importantă în programare, atunci când scrieți cod. În cazul în care scrieți cod în limbajul *Python*, această noțiune nu este doar importantă, dar este absolut **necesară**. Indentarea presupune plasarea codului pe linii, pentru scrierea corectă și cât mai clară a acestuia. De multe ori, programatorii începători uită de indentare atunci când scriu cod și din acest motiv se confruntă cu erori la execuția programelor. De aceea, fiți atenți la acest capitol și **nu uitați de indentare**! <3

Să analizăm următoarea secvență de cod *Python*. Această sintaxă nu o să vă fie cunoscută, dar pentru moment asta nu e important.

```python
def colectiv():
colegi = 45
return colegi
print colectiv()
```
Copiați această secvență de cod și executați-o. Ea trebuie să vă returneze la ecran ``"45"``.

Oh, dar de ce nu ni se afișează ``"45"``? Se pare că *Python* ne spune că avem o greșeală.

Da, așa este. Ceea ce vedeți la ecran se numește *mesaj de eroare*. În general, orice mesaj de eroare pe care-l primim este un indiciu a ceea ce noi n-am făcut corect în program.

Dar haideți să examinăm eroarea: ``"IndentationError: expected an indented block"``. Veți primi această eroare ori de câte ori veți uita de indentare sau indentarea va fi greșită.

Această situație este, însă, rezolvabilă! Haideți să reparăm bucata de cod de mai sus, pentru ca atunci când o veți executa, să nu mai aveți mesaje de eroare. Indentați linia a doua de cod (înainte de cuvântul ``colegi``) cu patru spații sau cu un tab. Faceți exact același lucru și la linia a treia de cod (înainte de cuvântul ``return``).

```python
def colectiv():
    colegi = 45
    return colegi
print colectiv()
```
Voila! În sfârșit putem vedea acel ``"45"``!

###**Condiționalele și Control Flow**
La fel ca în viața reală, uneori codul nostru trebuie să fie capabil să ia decizii.

Până acum, toate programele pe care le-am scris împreună în *Python* puteau să urmeze doar un singur fir logic: fie că am adunat două numere sau fie că am afișat ceva. Programele noastre, însă, nu puteau lua decizii de sine-stătător în privința a ce instrucțiuni să execute în dependență de o careva condiție. Conceptul de **Control Flow** oferă posibilitate programului de a alege ce să facă.

Aici avem un program micuț. Chiar dacă acum acest program vi se pare complicat, în doar câțiva pași veți fi capabili să-l înțelegeți. Vă propun doar să treceți prin el cu vederea:

```python
def olimpiada():
    print "Vrei sa mergi la olimpiada de geografie sau la cea de chimie?"
    raspuns = raw_input("Alege geografia sau chimia apoi apasa 'Enter'.").lower()
    if raspuns == "geografia" or raspuns == "g":
        print "Este o alegere foarte buna!"
    elif raspuns == "chimie" or raspuns == "c":
        print "Hmm, esti sigur ca stii bine tabelul periodic?"
    else:
        print "Nu ai ales nici geografia, nici chimia. Mai incearca odata."
        olimpiada()

olimpiada()
```

Pentru a înțelege programul de mai sus, ar fi bine să-l ‘depănăm’ pas cu pas. Inițial, trebuie să începem prin a înțelege cum are loc compararea în *Python*.
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
 - True and True este True;
 - True and False este False;
 - False and True este False;
 - False and False este False;

 - True or True este True;
 - True or False este True;
 - False or True este True;
 - False or False este False;

 - Not True este False;
 - Not False este True.
```


###*Exercițiu:*
Creați variabila ``bool_1``. Atribuiți-i valoarea ``boolean`` egală cu rezultatul expresiei: ```1 < 2 and 2 < 3```.

```python
bool_1 = True
```
Creați variabila ``bool_2``. Atribuiți-i valoarea ``boolean`` egală cu rezultatul expresiei: ``1 < 2 and 2 > 3``.

```python
bool_2 = False
```
Creați variabila ``bool_3``. Atribuiți-i valoarea ``boolean`` egală cu rezultatul expresiei: ``1 < 2 or 2 > 3``.

```python
bool_3 = True
```
Creați variabila ``bool_4``. Atribuiți-i valoarea ``boolean`` egală cu rezultatul expresiei: ``1 > 2 or 2 > 3``.

```python
bool_4 = False
```
Creați variabila ``bool_5``. Atribuiți-i valoarea ``boolean`` egală cu rezultatul expresiei: ``not False``.

```python
bool_5 = True
```
Creați variabila ``bool_6``. Atribuiți-i valoarea ``boolean`` egală cu rezultatul expresiei: ``not 41 > 40``.

```python
bool_6 = False
```
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

Luați în considerare *indentarea*. De asemenea, observați cele *două puncte* la sfârșitul afirmației ``if``. Aceste două componente sunt **necesare** atunci când scrieți condiționale.

Else
Instrucțiunea condițională ``else`` completează instrucțiunea condițională ``if``. O pereche ``if/else`` spune: *"Hey Python, dacă această expresie este adevărată, execută blocul de cod indentat de după if; în caz contrar, execută cealaltă bucată de cod indentat de după instrucțiunea else."*

Spre deosebire de ``if``, ``else`` nu depinde de o expresie (pe care ar trebui să o verifice). De exemplu:

```python
if 8 > 9:
    print "Rosu"
else:
    print "Galben"
```
Luați în vedere **indentarea**!

Elif
``elif`` este prescurtarea lui "else if". ``elif``-ul spune: *"În caz contrar, dacă expresia următoare este adevărată, atunci fă asta!"*

```python
if 8 > 9:
    print "Rosu"
elif 8 < 9:
    print "Galben"
else:
    print "Albastru"
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
if conditie_unu():
    print "Unu"
elif conditie_doi():
    print "Doi"
else:
    print "Trei"
```
###*Exercițiu:*
Scrieți o secvență de cod care trebuie să includă neapărat: ``if``, ``elif``, și ``else``. De asemenea, codul vostru trebuie să conțină cel puțin un ``and``, ``or`` sau ``not`` și cel puțin un comparator (``==``, ``!=``, ``<``, ``<=``, ``>``, ``>=``). Nu uitați să scrieți ``:`` după afirmația ``if``!

```python
    if  8 < 9:
        return True
    elif 9 < 10 and 10 < 11:
        return "lalala"
    else:
        return "lololo"
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
###*Exercițiu:*
Creați o variabilă numită ``acum`` și stocați în ea rezultatul funcției ``datetime.now()``. Apoi, afișați valoarea lui ``acum``. Nu uitați de ``import``!

```python
from datetime import datetime
acum = datetime.now()
print acum
```
####**Extragerea informației**
Observați cum arată output-ul: ``2015-08-25 23:45:14.317454``. Cum veți proceda în cazul în care nu doriți să se afișeze întreaga dată și oră?

Simplu!
```Pythom
from datetime import datetime
acum = datetime.now()
anul_curent = acum.year
luna_curenta = acum.month
ziua_curenta = acum.day
```
Primele două linii deja le înțelegeți. În linia a treia, am luat ``anul`` din variabila ``acum`` și l-am stocat în ``anul_curent``. În liniile patru și cinci, am stocat ``luna`` și ``ziua`` din ``acum``.

###*Live coding:*
Să zicem că noi dorim să afișăm data de azi în formatul următor: *lună/ziuă/an*. Cum putem face asta? Aici ne vine în ajutor **substituția ``string``-urilor**!

```python
from datetime import datetime
acum = datetime.now()

print '%s-%s-%s' % (acum.year, acum.month, acum.day)
# se va afisa: 2015-08-19
```

Amintiți-vă că operatorul ``%`` va găsi toate scrierile ``%s`` din ``string`` și toate argumentele din paranteze. El le va afișa în ordinea corespunzătoare.
Vi s-a afișat data corect?

###*Exercițiu:*
Afișați data curentă în formatul: *zi/lună/an*. Pentru asta trebuie doar să înlocuiți simbolurile ``–`` cu ``/``  și să schimbați ordinea a ``now.month``, ``now.day`` și ``now.year``.

```python
from datetime import datetime
acum = datetime.now()
print '%s/%s/%s' % (acum.day, acum.month, acum.year)
```

Sunteți bravo! Haideți să implementăm aceeași logică pentru ore, minute și secunde.

```python
from datetime import datetime
acum = datetime.now()

print acum.hour
print acum.minute
print acum.second
```

În exemplul de mai sus, noi am afișat ora, minuta și secunda curentă.

###*Exercițiu:*
Exact ca și în exercițiul anterior, afișați timpul curent în forma: *oră:minută:secundă*.

Schimbați ``string``-ul pe care-l veți afișa, astfel încât să aveți caracterul ``:`` între ``%s``.
Modificați luna, ziua și anul în ``acum.hour``, ``acum.minute`` și ``acum.second``.

```python
from datetime import datetime
acum = datetime.now()
print '%s:%s:%s' % (acum.hour, acum.minute, acum.second)
```

###**Marea provocare!**
Ați reușit să afișați data și timpul în mod separat și într-o formă foarte drăguță! Bravo! Haideți acum să le combinăm!

```python
from datetime import datetime
acum = datetime.now()

print '%s/%s/%s' % (acum.month, acum.day, acum.year)
print '%s:%s:%s' % (acum.hour, acum.minute, acum.second)
```
În exemplul de mai sus, se va afișa data. Apoi, dintr-o linie nouă, se va afișa timpul.

Haideți să le afișăm pe toate pe aceeași linie într-o singură instrucțiune ``print``!

###*Exercițiu:*
Afișați data și timpul împreună în forma: *lună/zi/an oră:minută:secundă*.

Pentru a face asta:

- importați librăria ``datetime``;
- creați o variabilă numită ``acum`` și atribuiți-I funcția ``datetime.now()``;
- afișați data și timpul după cum vi s-a cerut mai sus. Nu uitați de: ``%s``, ``%``, ``/``, ``-`` și de ordinea variabilelor din paranteze.

```python
from datetime import datetime
acum = datetime.now()

print '%s/%s/%s %s:%s:%s' % (acum.month, acum.day, acum.year, acum.hour, acum.minute, acum.second)
```

**Concluzie:**
În acest capitol voi ați învățat două lucruri: ce înseamnă librăria ``datetime`` și cum are loc importarea de librării!

##**Funcții**
De multe ori, voi, ca viitori programatori, vă veți întâlni cu situația în care veți fi nevoiți să reutilizați o anumită secvență de program, dar deja cu alte valori. Pentru a nu scrie de fiecare dată codul din nou, este mult mai simplu să definiți o **funcție**, care poate fi reutilizată oricând.

Funcția este un concept important în programare (la fel ca și în matematică). Fiecare programator trebuie să poată să scrie funcții.
###**Sintaxa funcțiilor**

Funcțiile sunt constituite din două componente.

Primul component este **header**-ul funcției, care include: cuvântul-cheie ``def``, **numele** funcției și **parametrii** pe care-i transmiteți funcției. Parametrii sunt opționali. Vedeți mai jos un exemplu de funcție fără parametri:

```python
def hello_world(): # acesta este header-ul unei functii fara parametri
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

```python
def calcul(n):
    patrat = n**2
    print str(n) + " la patrat este " + str(patrat)
    return patrat

calcul(10)
```
####**Parametri și Argumente**

În exemplul de mai sus, ``n`` este **parametrul** funcției ``calcul``. ``10`` este **argumentul** transmis.

> **Notă:** Unei funcții îi puteți transmite atâția parametri, de câți aveți nevoie. Când apelați funcția, ar fi bine să-i transmiteți tot atâtea argumente, câți parametri ați definit.

###*Exercițiu:*
Analizați funcția ``putere`` de mai jos. Ea cere doi parametri: o bază și un exponent. Primul parametru este ridicat la puterea parametrului al doilea. După cum vedeți, funcția nu este completă, de aceea adăugați de sine-stătător parametrii: ``baza`` și ``exponent``. Apoi, apelați funcția cu argumentele: ``2`` pentru bază și ``3`` pentru exponent.

```python
def putere(___, ___):  # adaugati aici parametrii
    rezultat = baza**exponent
    print "%s la puterea a %s este %s." % (baza, exponent, rezultat)

putere(__,__)  # adaugati aici argumentele
```
*Rezultatul vostru trebuie să arate așa:*

```python
def putere(baza, exponent):  # adaugati aici parametrii
    rezultat = baza**exponent
    print "%s la puterea a %s este %s." % (baza, exponent, rezultat)

putere(2, 3)  # adaugati aici argumentele
```
Vi s-a dat rezultatul corect? Sunt sigură că da!
###**Funcții apelând funcții**

###*Live coding:*
Ați văzut deja funcții care pot afișa texte sau care pot face operații aritmetice, dar funcțiile pot fi mult mai puternice decât atât! De exemplu, o funcție poate apela o altă funcție:

```python
def func_one(n):
    return n * 5

def func_two(m):
    return func_one(m) + 7
```

###*Exercițiu:*
Să analizăm următoarele două funcții: ``o_afisare`` (care adună 1 la un număr pe care-l ia ca argument) și ``merita_alta_afisare`` (care adună 2).

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

Definiți a doua funcție, numită ``mai_mare``, care cere un argument numit ``numar``.

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

Un **modul** este un fișier care conține multe definiții, inclusiv variabile și funcții, pe care le puteți folosi odată ce el, acest modul, a fost importat în programul vostru.
###*Live coding:*
Înainte de a importa ceva, haideți să vedem ce știe *Python* implicit, adică fără de importuri. Vom lua exemplul funcției radical. Linia de mai jos trebuie să afișeze ``5``.

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
Acest fel de import de module (ca cel de mai sus) se numește **import generic**.
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
###*Live coding:*
Haideți să importăm doar funcția ``sqrt`` din modulul ``math``. (Nu avem nevoie de ``()`` după ``sqrt``!)

```python
from math import sqrt
```
####**Importurile universale**

Fain! Am găsit o modalitate corectă de a selecta variabile și funcții din modulul pe care-l vrem!

Iar dacă noi în continuare dorim să obținem toate variabilele și funcțiile dintr-un modul, dar nu vrem să scriem permanent ``math.``, ce facem?

**Importul universal** vine cu o soluție! Sintaxa acestuia este:

```python
from module import *
```
###*Live coding:*
Haideți să utilizăm ``from modul import *`` pentru a importa tot din modulul ``math``.

```python
from math import *
```
Totul e bine, dar...
Importurile universale pot să pară ok din exterior, dar ele nu sunt o idee bună dintr-un motiv foarte important: ele fac programul vostru plin de o groază de variabile și funcții inutile sau care vă pot crea probleme.

Să zicem că ați creați funcția voastră și ați numit-o ``sqrt``. Tot în același program, ați importat modulul ``math``. În acest caz, funcția voastră ``sqrt`` va fi în siguranță: veți avea funcția pe care ați creat-o – ``sqrt``, și funcția din modul – ``import.sqrt``. Însă, dacă ați fi scris ``from math import *``, v-ați fi confruntat cu o problemă: două funcții diferite, dar cu același nume. Iar dacă ați fi scris de mai multe ori în același program ``import *``, nu ați fi fost capabili să înțelegeți care variabilă sau care funcție din care modul vine.

Din aceste motive, cel mai bine este fie să utilizați fie ``import modul`` și apoi ``modul.nume``, fie pur și simplu să faceți ``import`` unor variabile și funcții specifice din diferite module.

###**Review: Funcții**
Okay! Să revizuim funcțiile!

```python
def dialog(mesaj):
    return mesaj

if fericit():
    dialog("Sunt fericit!")
elif trist():
    dialog("Sunt trist.")
else:
    dialog("Nu stiu ce simt...")
```
Exemplul de mai sus este scris pentru a vă reaminti de funcții și pentru a vă servi drept referință.
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

**Listele** reprezintă un alt tip de date din *Python*. În liste puteți stoca date de orice tip sub numele unei singure variabile.

Listele sunt constituite dintr-un nume și din itemii atribuiți.

Puteți atribui itemi unei liste printr-o expresie de forma:

```python
nume_lista = [item_1, item_2]
```
Observați că itemii sunt scriși între paranteze patrate. O listă poate fi și goală:

```python
lista_goala = [].
```
###*Exercițiu:*

Lista de mai jos,  `zoo_animale`, are trei itemi:

```python
zoo_animale = ["urs", "vulpe", "tigru"]
```
Adăugați un al patrulea item listei! Introduceți numele animalului vostru preferat (ca un `string`) după `"tigru"`, prin virgulă.

```python
zoo_animale = ["urs", "vulpe", "tigru", "elefant"]
```
####**Accesarea după indice**


Puteți accesa un item al listei după indicele său. Un **indiciu** e ca o adresă care identifică locul itemului în listă. Indicele se scrie direct după numele listei, în paranteze patrate, cam așa: `nume_lista[indiciu]`.

Indicii listei încep cu 0, nu cu 1! (Da, da, la fel ca și la `string`-uri). Puteți să accesați primul element al unei liste în felul următor: `nume_lista[0]`. Al doilea item îl accesați așa: `nume_lista[1]`. Programatorii iubesc să numere de la zero.


###*Exercițiu:*

Creați o listă, numită `numere,` cu itemii `5`, `6`, `7` și `8`. Din rând nou, afișați rezultatul adunării itemilor doi și patru din listă.

```python
numere = [5, 6, 7, 8]
print numere[1] + numere[3]
```
####**New Neighbors**
Știți deja cum se accesează un item al listei. (După indice).

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

###*Live coding:*
Să executăm codul de mai jos!

```python
litere = ['a', 'b', 'c', 'd', 'e']
slice = litere[1:3]
print slice
print litere
```

 În exemplul de mai sus, de la început am creat o listă nouă, numită `litere`.

Apoi, am luat o secvență din `litere` și am stocat-o în `slice`.

În rezultat, instrucțiunea `litere[1:3]` a afișat rezultatul `['b', 'c']`. E de înțeles de ce s-a afișat itemul `"b"` cu indicele `1`. Dar de ce itemul `"d"`, cu indicele `3`, nu s-a afișat? Deoarece acest mod de "feliere a listelor" se stopează cu un indice înainte de cel scris în instrucțiune.

În final, am afișat `['a', 'b', 'c', 'd', 'e']`, pentru a arăta că nu am modificat nimic din lista inițială.

###**Slicing Lists and Strings**
Puteți "felia" `string`-urile exact ca și listele! De fapt, `string`-urile se pot interpreta ca niște liste de caractere: fiecare caracter este un item din listă, care începe cu indicele 0.

Dacă secvența vostră de listă pe care vreți s-o afișați include primul sau ultimul item din listă, indicele pentru acest item nu trebuie inclus:

```python
print lista_mea[:2]
# afiseaza primii doi itemi ai listei lista_mea
print lista_mea[3:]
# afiseaza itemii de la al patrulea pana la ultimul
```

###*Live coding:*
Logica pe care am descris-o mai sus poate fi aplicată și asupra `string`-urilor, așa cum am mai menționat.

În continuare, voi afișa, de 3 ori, doar caracterele care reprezintă un animal din `string`-ul `zoo`:


```python
zoo = "urslupcerb"

print zoo[:3]
print zoo[3:6]
print zoo[6:]
```

####**Maintaining Order**
Uneori, avem nevoia să căutăm un item într-o listă.

```python
pasari = ["papagal", "flamingo", "colibri"]
print pasari.index("flamingo")
```
Inițial, am creat o listă numită `pasari` cu trei `string`-uri. Apoi, am afișat primul indiciu care conține `string`-ul `"flamingo"`. Rezultatul este `1`.

De asemenea, noi putem insera itemi într-o listă.

```python
pasari.insert(1, "paun")
print pasari
```
Am inserat `"paun"` la indicele `1`, ceea ce va mișca totul de la 1 spre dreapta.
În final, am afișat `["papagal", "paun", "flamingo", "colibri"]`

###*Exercițiu:*
Mai jos aveți o listă, numită `culori`, care conține 4 itemi.

```python
culori = [ 'negru', 'rosu', 'albastru', 'verde' ]
```

Folosiți funcția `.index(item)` pentru a găsi indicele culorii verde. Atribuiți acest rezultat unei variabile numite `verde_index`. Apoi, inserați prin `.insert(index, item)` `string`-ul `"galben"` la indicele `verde_index`.

```python
culori = [ 'negru', 'rosu', 'albastru', 'verde' ]

verde_index = culori.index("verde")
culori.insert(verde_index, "galben")
print culori
```

O listă poate fi și sortată după ordinea alfabetică. Asta nu e complicat! Priviți aici:

```python
culori.sort()
# se va afisa ['albastru', 'galben', 'negru', 'rosu', 'verde']
```
Metoda `.sort()` a aranjat `string`-urile în ordine alfabetică în mai puțin de o secundă!


####**Remove a Few Things**

Uneori, avem nevoie să ștergem ceva și dintr-o listă.

```python
beatles = [ "john", "paul", "george", "ringo", "stuart" ]
beatles.remove("stuart")
print beatles
# se va afisa ["john", "paul", "george", "ringo"]
```

În exemplul de mai sus, am creat o listă cu 5 `string`-uri.

Apoi, am eliminat primul item din `beatles` care coincide cu `string`-ul `"stuart"`. Țineți minte că `.remove(item)` nu returnează nimic.

În final, am afișat lista pentru a ne asigura că `"stuart"` într-adevăr a fost eliminat.

###*Exercițiu:*
Creați o listă nouă, numită `rechizite`. Lista trebuie să aibă minim 5 itemi. Ulterior, eliminați un item la dorința voastră și afișați rezultatul!

```python
rechizite = ['pix', 'creion', 'radiera', 'rigla', 'compas']
rechizite.remove('radiera')
print rechizite
```

###**Dicționare**

Un **dicționar** este asemănător cu o listă, doar că în cazul dicționarelor puteți să accesați valorile prin intermediul unei chei, și nu prin intermediul unui indice. O **cheie** poate fi un `string` sau un număr. Dicționarele se scriu între acolade, în felul următor:

```python
dictionar = {'cheie1' : 1, 'cheie2' : 2, 'cheie3' : 3}
```
Mai sus avem exemplul unui dicționar cu trei perechi *cheie-valoare*. Cheia `cheie1` are valoarea `1`, `cheie2` - valoarea `2` ș.a.m.d.

Dicționarele sunt utile pentru asemenea lucruri, ca: lista numerelor de telefoane (având perechile *nume - număr*), pagini de logare (având perechile *adresa de e-mail - nume de utilizator*) și nu doar!

###*Live coding:*
Mai jos, vă prezint un exemplu de dicționar, care stochează informația pentru perechile *e-mail - parolă*.

```python
d = { 'alexandru@gmail.com' : 2345,
    'olga@yahoo.com' : 6789,
    'daniela@mail.md' : 0123 }
```

Accesarea unei valori din dicționar după o cheie e aceeași cum am accesa valorile din liste după indici:

```python
print d['alexandru@gmail.com']
```
###*Exercițiu:*
Din dicționarul de mai sus, accesați valoarea perechii a doua și a treia (după cheie). Pentru aceasta, de la început, copiați dicționarul `d` în Sublime Text. Afișați rezultatele.

```python
d = { 'alexandru@gmail.com' : 2345,
    'olga@yahoo.com' : 6789,
    'daniela@mail.md' : 0123 }

print d['olga@yahoo.com']
print d['daniela@mail.md']
```

####**New Entries**

La fel ca listele, dicționarele sunt "flexibile".  Aceasta înseamnă că ele pot fi schimbate după ce au fost create. Un avantaj al acestui fapt este ceea că putem adăuga în dicționarele deja create noi perechi *cheie-valoare*, în felul următor:

```python
nume_dict[cheie_noua] = valoare_noua
```
O pereche goală de acolade este un dicționar gol, la fel cum o pereche goală de `[]` este o listă goală.

###*Live coding:*

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
meniu['Pizza cu broccoli']   = 60.00
meniu['Cartofi prajiti']     = 35.00
meniu['Inghetata cu zmeura'] = 29.00
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
###*Exercițiu:*
Mai jos, aveți creat un dicționar cu animalele de la Grădina Zoologică și un exemplu de cum se elimină unul din itemi.

```python
# cheie - nume_animal : valoare - locatia
zoo_animale = { 'Maimuta' : 'Africa',
        'Tigru' : 'Asia',
        'Cangur' : 'Australia',
        'Unicorn' : 'Wonderland' }

# stergem 'Unicorn'. (Unicornii sunt excesiv de scumpi.)
del zoo_animale['Unicorn']
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
    "ziua": [ "d", "u", "m", "i", "n", "i", "c", "a" ],
    "cash": -4483,
    "stare": "obosit"
}
print my_dict["ziua"][0]
```
În exemplul de mai sus, am creat un dicționar care conține diferite tipuri de valori.

Cheia `"ziua"` are o listă, cheia `"cash"` are un `int` și cheia `"stare"` are un `string`.

În final, am afișat litera `"d"`. Când accesăm o valoare într-un dicționar de genul `my_dict["ziua"]`, avem acces direct la valoare. Astfel, putem accesa itemul de la indicele `'0'` din listă stocat de cheia `"ziua"`.

###*Exercițiu:*

Analizați sevența de cod de mai jos:

```python
liceu = {
    'elevi' : 500,
    'olimpici' : ['matematica', 'informatica', 'geografie'], # am atribuit o lista la cheia 'olimpici'
    'premii' : ['sport', 'teatru', 'dans', 'pictura']
}

# adaugam o cheie noua 'cursuri' si ii atrinuim o lista
liceu['cursuri'] = ['programare', 'antreprenoriat', 'engleza']

# sortam lista cu cheia 'olimpici'
liceu['olimpici'].sort()
```
Adăugați o nouă cheie la dicționarul `liceu`, numită `'fesivitati'`.
Valoarea sub cheia `'festivitati'` trebuie să fie o listă ce va conține: `'halloween'`, `'revelion'` și  `'ultimul sunet'`.

Prin `.sort()`, sortați itemii listei `premii`. Apoi, eliminați din această listă, prin `.remove()`, itemul stocat sub cheia `'teatru'`.

Adăugați `50` la numărul stocat sub cheia `"elevi"`.


```python
liceu["festivitati"] = ["halloween", "revelion", "ultimul sunet"]
liceu['premii'].sort()
liceu["premii"].remove("teatru")
liceu['elevi'] = liceu['elevi'] + 50
```
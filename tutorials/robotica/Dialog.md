# Dialog - QiChat 

#### Link-uri de care avem nevoie:
- [Cum creez boxe de Dialog](https://github.com/girls-go-it/girls-go-it.github.io/blob/master/tutorials/robotica/Dialog_box_how_to_create.md)
- [Sintaxa Dialog](http://doc.aldebaran.com/2-1/naoqi/audio/dialog/aldialog_syntax_overview.html)
- [Sintaxa completă](http://doc.aldebaran.com/2-1/naoqi/audio/dialog/dialog-syntax_full.html)


#### Resurse în limba engleză:
- [Website oficial](http://doc.aldebaran.com/2-1/naoqi/audio/dialog/dialog.html)
- [How to create Dialog boxes](http://doc.aldebaran.com/2-1/software/choregraphe/tutos/dialog_topic.html)
- [QiDialog CheatSheet](http://doc.aldebaran.com/2-1/naoqi/audio/dialog/aldialog_syntax_cheat_sheet.html)
- [Dialog Syntax](http://doc.aldebaran.com/2-1/naoqi/audio/dialog/aldialog_syntax_overview.html)
- [Full Syntax Dialog](http://doc.aldebaran.com/2-1/naoqi/audio/dialog/dialog-syntax_full.html)

#### Lista de animații:
[http://doc.aldebaran.com/2-1/naoqi/audio/alanimatedspeech_advanced.html#animated-speech-list-behaviors-nao](http://doc.aldebaran.com/2-1/naoqi/audio/alanimatedspeech_advanced.html#animated-speech-list-behaviors-nao)

# Exemple discutate:
## Reguli, alegere [], optional {} , ^rand
```
topic: ~robots()
language: enu

u:(hello) hello

u:(hello) [hi hello "good morning"]

u:(what do you like?) I like {^rand[chocolate vanilla red]} icecream

```

## Variabile
```
topic: ~robots()
language: enu

concept:(name) [Diana Ana Ileana]

u:(My name is _~name and I like
 _ music) Hello $1 you like $2 $myname=$1
u:($myname, how are you?) good
```
## Proposal 
```
topic: ~robots()
language: enu

proposal: What do you like?
proposal: proposal2
proposal: proposal3

u:(what do you like?) ^nextproposal 
^firstproposal ^sameproposal

```

## Proposal cu taguri
```
topic: ~robots()
language: enu

proposal: %tag1 How do you feel?
proposal: %tag2 Do you like the weather?
proposal: %tag3 Do you like the sun?
			

u:(speak) ^goto(tag1)
u:(good) ^goto(tag2)
u:(understand) ^goto(tag1)
```




# Teorie

## Topic 
Un Topic este o tema, o idee principală despre care vrem să vorbim cu robotul.
Tehnic vorbind, un Topic este un script(fișier) care conține o regulă (Rule), despre care vorbim mai târziu.
Antetul său conține obligatoriu numele și limba Topic-ului.

Sintaxă:
```
topic: ~introduction ()
language: enu
```

Exemplu:
```
topic: ~introduction ()
language: enu

u:(hello) hello human, pleased to meet you
```
Pentru a crea primul topic, vezi Creating Dialog boxes.
Alte referințe:  name,  language

## Rule (Regulă)

O regulă asociază un Human input (ce spune omul) cu un Robot ouptut (ce raspunde robotul) corespunzător.
Delimitatorii (Delimiters), Caracterele speciale (Special characters) și Funcțiie si proprietățile regulilor( Rule functions and properties) dau posibilitatea de a crea reguli puternice, care conțin într-o linie mai multe cazuri.

Există 3 tipuri de reguli: 

![tipuri de reguli](https://raw.githubusercontent.com/girls-go-it/girls-go-it.github.io/master/tutorials/robotica/img/rules.png)



## Human input (ce spune omul)
Human input (ce spune omul) este o parte a User rule sau User subrule delimitată de paranteze, care conține mesajul ce va fi recunoscut de către robot.
Cand un Human input se potrivește, adică mesajul este recunoscut, o Regulă (Rule) este acționată (triggered).
Cand o regula este acționată, se întâmplă următoarele:
- Robot output se execută (spus și/sau făcut).
- Focusul este setat pe Tema(Topicul) ce conține regulile.

## Robot output (ce spune robotul)
Este o parte a User rule, User subrule, sau Proposal, ce conține ce va spune sau face robotul cand regula este acționată. 

## Concept
Conceptul este o listă de cuvinte și/sau fraze care se referă la o idee.

Exemple:

```
- o listă de țări
- o listă de nume
- sinonimele unui cuvânt
```

Conceptele pot fi utilizate atât la Human input, cât și la Robot output.
Exista 2 tipuri de concepte:
![concept types](https://github.com/girls-go-it/girls-go-it.github.io/blob/master/tutorials/robotica/img/concept_types.png?raw=true)


Exemple:

```
concept:(want) ^rand {"i'd * like" "i want {"a lot"}"}
dynamic:want
python:
setConcept("want","enu", ["i'd like" "i want" "i want a lot"]
```

Sintaxă:

- Pentru a declara un concept static:

```
concept:(name) [word1 word2 "word3 word4"]
```

unde:

- word1 și word2 sunt cuvinte izolate
- “word3 word4” este o frază, adică un grup de câteva cuvinte
- name este numele conceptului static

Exemplu:

```
topic: ~introduction ()
language:enu

concept:(greetings) ^rand[hi hello "hey there"]

concept:(icecream) [strawberry chocolate] icecream
concept:(desert) [cookies ~icecream]

u:(~greetings) ~greetings
u:(do you have _~dessert) yes, I have $1
u:(I want to eat something) do you want ~desert?
```

Execuție:
```
> hey there
hello
> do you have strawberry icecream?
yes, I have strawberry icecream
> I want to eat something
do you want cookies?
> I want to eat something
do you want chocolate icecream?
```




- Pentru a declara un concept dinamic:
```
dynamic:name
```
Notă: un concept dinamic poate conține doar o listă de cuvinte sau fraze într-un singur Choice (alegere), notată cu [ ].
Exemple:
```
concept:(want) ^rand {"i'd * like" "i want {"a lot"}"}
dynamic:want
```

Referințe: Choice: [ ], Optional part: { }, Funcții (^rand , ^first ), Variable: $, Conditions: == > <> <

## Activat/dezactivat
Topics si Rules trebuie să fie activate pentru a fi nu fi ignorate de către Dialog engine (Motorul de dialog). 
Este posibil sa activezi sau dezactivezi doar o parte din ele, pentru a crea un context conversațional și/sau să reduci numărul de reguli administrate (managed) în memorie.
- Activarea unui Topic
In Choregraphe, un Topic se activează sau dezactivează când Dialog topic box este încărcat(loaded) și descărcat (unloaded)
Într-un script, poți de asemenea să folosești:
```
- ALDialogProxy::activateTopic()
- ALDialogProxy::deactivateTopic()
```

### Activarea unei reguli
- Toate Regulile unui Topic dezactivat sunt dezactivate.
- Toate Regulile unui Topic activat sunt activate, cu excepția situațiilor în care:
   * este un User subrule și nu este atașată de ultima regula activată
   * este un Proposal deja executat
   * conține o eticheta(tag) dezactivată
   * conține funcția ^private, iar Topic nu are Focusul.

## Focus
Mai multe Topicuri pot fi activate simultan, dar numai unul poate avea Focus.
Focusul este dat Topicului care conține ultima regula activata. Cu excepția situației în care Topicul conține proprietatea ^noStay.
Daca în diferite topicuri sunt reguli similare, atunci prioritate are Topicul ce are Focus.
Daca nici un topic nu are focus, atunci alegerea este random(aleatorie).
În unele cazuri, Dialog engine poate decide singur să dea Focusul unei Reguli și să spună primul ei Proposal. 
Funcția ^noPick face ca această selecție automată să nu se întâmple.
Funcții și proprietăți importante:
- ^noPick ,
- ^noStay ,
- ^resetOnFocus ,
- ^fallback .

## Recover section (Secțiunea de restabilire)
Regulile plasate după secțiunea de restabilire au o prioritate mai mică.
Sintaxă:
```
recover:
```
Exemplu:

```
topic: ~topic1()
language: frf

u:(alien) I am not an alien, I am a humanoid robot

recover:
u:(hello) hello human
```

Execuție:
```
> hello alien
I am not an alien, I am a humanoid robot
```

### Prioritatea regulilor
![Cheat Sheet](https://raw.githubusercontent.com/girls-go-it/girls-go-it.github.io/master/tutorials/robotica/img/prioritatea_regulilor.png)


## Refolosirea Human input
Este posibil să salvezi o parte din Human input(ce spune omul) pentru a o folosi in răspunsul robotului (Robot output).
Referințe:  Input storing: _ 


## Variabile și evenimente
ALDialog folosește ALMemory pentru a stoca și recupera datele.
Orice date stocate pot fi văzute ca variabile sau evenimente.
Referințe: variable , event 
 
## Skin 
Un Skin este o meta regulă, ce definește transformările care vor fi aplicate pe Robot outputs deja definite.
Un Skin poate fi plasat în orice Topic și este activat când un Robot output se potrivește.
Referințe: Transformation rules
 
# Anexe:
### Rezumat:
![Cheat Sheet](https://raw.githubusercontent.com/girls-go-it/girls-go-it.github.io/master/tutorials/robotica/img/cheat_sheet_dialog.png)

### Lista de limbi în care poate vorbi Nao:
![tipuri de reguli](https://raw.githubusercontent.com/girls-go-it/girls-go-it.github.io/master/tutorials/robotica/img/supported_languages.png)

### Resurse utile:
#### Website oficial:
[http://doc.aldebaran.com/2-1/naoqi/audio/dialog/dialog.html](http://doc.aldebaran.com/2-1/naoqi/audio/dialog/dialog.html)
#### Sintaxa:
[http://doc.aldebaran.com/2-1/naoqi/audio/dialog/dialog-syntax_full.html](http://doc.aldebaran.com/2-1/naoqi/audio/dialog/dialog-syntax_full.html)
#### QiDialog CheatSheet:
[http://doc.aldebaran.com/2-1/naoqi/audio/dialog/aldialog_syntax_cheat_sheet.html](http://doc.aldebaran.com/2-1/naoqi/audio/dialog/aldialog_syntax_cheat_sheet.html)
[http://doc.aldebaran.com/2-1/naoqi/audio/dialog/aldialog_syntax_overview.html](http://doc.aldebaran.com/2-1/naoqi/audio/dialog/aldialog_syntax_overview.html)
#### Limbi disponibile:
[http://doc.aldebaran.com/2-1/family/robots/languages.html#dialog-supported-languages](http://doc.aldebaran.com/2-1/family/robots/languages.html#dialog-supported-languages)
#### Tutorial YouTube:
[https://youtu.be/vyEGRs3pnQE](https://youtu.be/vyEGRs3pnQE)



# Exerciții practice:
1.Creează un program ce folosește Dialog și poate avea o discuție despre tipuri de mâncare
2.Transformă-l pe Frank într-o persoană foarte amabilă care lucrează la serviciul clientelă pentru un operator de telefonie.
El poate răspunde la următoarele întrebări:
- Câți bani am în cont?
- Care este numărul meu de telefon?
- La ce ora a fost ultimul apel?
*Nivel de dificultate:
1. Folosește valori prestabilile de la început(de ex. u:(întrebare):3, 4.5, 203)
2. Folosește delimitatorul choice și random să aleagă dintr-o listă de răspunsuri
3. Folosește boxele random int si random float*

3.Creează un program ce folosește Dialog, astfel încît să poți întreba roboțica ce este Choregraphe și despre ce boxe ați învățat până acum.




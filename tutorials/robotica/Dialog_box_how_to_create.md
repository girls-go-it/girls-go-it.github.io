# Cum creez un Dialog box 
Pentru tutorialul în engleză, accesează
[English tutorial](http://doc.aldebaran.com/2-1/software/choregraphe/tutos/dialog_topic.html)

## 1-Hello World

1.Pornește Choregraphe

2.Gasește boxa **Set Language** din **Audio -> Voice**

Intră în setări și setează limba - English

![](http://doc.aldebaran.com/2-1/_images/helloworld_cho_dlg_00.png)


3.Fă click de dreapta pe suprafața de lucru și alege, din meniul deschis **Create a new Box > Dialog....** 

![](http://doc.aldebaran.com/2-1/_images/helloworld_cho_dlg_01.png)

4.Apasă pe butonul **Add new topic**, apoi scrie numele topicului **fară spații**, de exemplu HelloWorld.
Apasă pe butonul **Add**, apoi pe butonul **OK**.

![](http://doc.aldebaran.com/2-1/_images/helloworld_cho_dlg_02.png)

5. Creează legături ca în imaginea de mai jos:

![](http://doc.aldebaran.com/2-1/_images/helloworld_cho_dlg_05.png)

6. În stânga, în fereastra **Project content**, găsește fișierul HelloWorld_enu.top și deschide-l.
*Notă: Dacă nu vezi fereastra Project content, deschide de sus din bara de meniu, View -> Project content și vei vedea în partea stângă Project content*

Se va deschide editorul care arată așa:

![](http://doc.aldebaran.com/2-1/_images/helloworld_cho_dlg_06.png)

7. Scrie aceste reguli:
```
u:(Hello) Hello, young lady

u:(Good morning) Let's start a wonderful day
```

![](http://doc.aldebaran.com/2-1/_images/helloworld_cho_dlg_07.png)


### Testarea pe un robot virtual(simulare)
1.Fii sigură că ești conectată la robot

2.Apasă butonul Play ![](http://doc.aldebaran.com/2-1/_images/beginning_play_button.png)



3.În panelul Dialog, scrie “Hello” și apasă Enter.

Poți vedea rezultatul în panelul Dialog sau în Robot view.

![](http://doc.aldebaran.com/2-1/_images/dialog_tuto2.png)



## Testarea pe un robot real
	
1.Fii sigur că ești conectat la robot.
Dacă nu știi cum să te conectezi la robot, vezi (http://doc.aldebaran.com/2-1/software/choregraphe/connection_widget.html#chore-howto-connect)

2.Apasă butonul Play(rulează programul)

3.Așteaptă până auzi semnalul “bip” care indică faptul că robotul te ascultă.

4.Spune “Hello”.
Robotul răspunde: “hello young lady”.

Poți vedea răspunsul și în Dialog panel și Robot view.




## “Hi”, “Hello”.. într-o singură regulă
1. Pentru a face prima regulă un pic mai complexă, schimbă scriptul așa:

```
u:([hi hello wassup]) hello young lady
u:(["tell me" "give me"] your name) of course, my name is NAO
```

![](http://doc.aldebaran.com/2-1/_images/dialog_tuto3.png)



## Conectarea QiChat cu animații
1. Adaugă aceste reguli noi:

```
u:(["can you" please] sit down {now}) ok i sit down $sit=1
u:(["can you" please] stand up {now}) ok i stand up $standup=1
```


2. Adaugă 2 ieșiri la boxa Hello world:

- una care se numește "sit"
- una care se numește "standup"

![](http://doc.aldebaran.com/2-1/_images/dialog_tuto4.png)


Pentru mai multe detalii cum să adaugi sau să ștergi intrări, ieșori sau parametri într-o boxă, vezi http://doc.aldebaran.com/2-1/software/choregraphe/objects/box_optional_components.html#choregraphe-howto-add-remove-box-in-out-param

3. Adaugă 2 boxe Flow Control > Time > Wait și conectează-le la ieșirile pe care le-ai creat

4. Adaugă și conectează 2 boxe Motion > Sit Down și Motion > Stand Up

![](http://doc.aldebaran.com/2-1/_images/dialog_tuto5.png)


## Schimbarea topicurilor. 

1.Creează un proiect nou.
Adaugă o boxă **Audio > Voice > Set Language**.

Creează 2 topicuri:

```
topic: ~Food()
language: enu

u:(let's talk about food) OK, guess what I like

u:^private(do you like fish) yes and sea food too
u:^private(do you like meat) no, I don't
```


```
topic: ~Sport()
language: enu

u:(let's talk about sport) OK, guess what sport I like

u:^private(do you like tennis) no, I can't play tennis
u:^private(do you like yoga) yes, would you like to do yoga with me?
```

Creează legăturile așa:
![](http://doc.aldebaran.com/2-1/_images/dialog_tuto6.png)

Testează programul.

Pentru a trece de la un topic la altul și să-i dai focusul, folosește una dintre regulile:
În exemplul nostru, “Let’s talk about food” sau “Let’s talk about sport”.

Atunci când un topic (food sau sport) are focusul, se întâmplă următoarele:
- toate **user rules private** ale **acestui topic** sunt **activate**
- toate **user rules private** ale **altor topice** sunt **dezactivate**

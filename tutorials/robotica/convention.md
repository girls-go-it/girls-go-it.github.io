# Convenția GirlsGoIT Robotics Choregraphe

## Reguli generale
- toate **conceptele** și **proposalurile** se scriu la **începutul programului**
- toate **denumirile** de concepte, taguri, etc. pot să fie formate din **maxim 3 cuvinte**, dar este preferabil să fie **doar un cuvânt**, dacă este posibil.
- dacă o denumire este formată din **2 sau 3 cuvinte**, trebuie să fie în formatul **cuvantCuvantCuvant**, de exemplu *poeziiDespreArta*, *GirlsGoTech* etc.

Exemplu: (Atrageți atenția că toate **proposalurile și conceptele** sunt la **începutul programului**)
```
topic: ~robots()
language: enu

proposal: Do you like arts? 
proposal: Which type of art do you like the most?
concept:(arts) [music painting sculpture]

u:(hi) hello. ^nextProposal
u:(yes) ^nextProposal
u:(i like ~arts)
```
- 
## Denumirea topicurilor
Topicurile se vor numi sugestiv, de exemplu, Istorie, Geografie, Artă, începând cu litera Mare și celelalte litere mici

## Denumirea conceptelor
Conceptele se vor scrie cu litere litere mici, cu excepția conceptelor care sunt formate din 2 sau 3 cuvinte.
Conceptele pot fi formate din **maxim 3 cuvinte**, ideal 1 sau 2.
Exemple:
```
- concept:(nume) [Diana Ana Ileana]
- concept:(cantec) lalala
- concept:(dansPopular) [sarba hora batuata]
- concept:(poezieVasileAlexandri) pastel
```

## Regulile
Regulile se scriu cat mai clar.
Cuvintele spuse de om trebuie să fie **în mod ideal maxim 3**, nu este de dorit, dar se poate 4, si doar în cazuri extrem de critice 5 cuvinte. Mai mult de 5 cuvinte consideră că din start nu se vor recunoaște.

## Subregulile
Subregulile se scriu **pe nivele** și se lasă spațiu înainte de regulile de pe nivelurile de mai jos, ca în exemplu:
![http://doc.aldebaran.com/2-1/_images/dialog_scope.png](http://doc.aldebaran.com/2-1/_images/dialog_scope.png)

## Proposal-urile și tagurile
Tagurile se numesc clar, sugestiv (**NU le numim tag1, tag2, etc**)
Exemple:
```
proposal: %questionBanana Do you like bananas?
proposal: %rightAnswer Yes, that's right
proposal: %wrongAnswer No, that's wrong
```

## Variabilele
Variabilele se numesc **sugestiv, clar, pe înțelesul tuturor**. Se aplică regula generală, ori scriem un cuvânt, ori o denumire formată din maxim 3 cuvinte, în formatul cuvantCuvantCuvant.
Exemple:
```
- nume
- numePrenume
- poezie
```

---
layout: default
title: Bootstrap Intro
category: basic
---

# Bootstrap [[slides-1](http://www.slideshare.net/mihaiiachimovschi/girls-go-it-day-6-training-1-bootstrap)] [[slides-2](http://www.slideshare.net/mihaiiachimovschi/girls-go-it-day-6-training-2-bootstrap-integration)]

[Bootstrap](getbootstrap.com) sau Twitter Bootstrap Framework este un conglomerat de intstrumente și șabloane stilizate ce au ca scop ușurarea și facilitarea dezvoltării aplicațiilor web.

Inițial, a fost un proiect intern în cadrul Twitter Inc., ca ulterior să devină Open-Source și accesibil pentru toți. După ce sursele au fost deschise și publicate pe GitHub, proiectului i s-au alăturat un număr foarte mare de voluntari ce au contribuit și au dezvoltat proiectul până la ziua de azi.

Începând cu versiunea 3.0, Bootstrap a adoptat un standard mobile-first, ce permite crearea interfețelor responsive. Interfețele responsive își au ca scop furnizarea aplicațiilor web pe diferite platforme cum ar fi telefoanele mobile, tabletele, laptop-uri și alte dispozitive.

## Starting point
Pentru început, zic să inițiem un fișier în care vom experimenta bootstrap-ul. Eu sper că deja te-ai obișnuit cu terminalul și cu editorul de text. Dacă încă nu te simți confortabil utilizând terminalul sau alte instrumente și ai careva neclarități - **întreabă**! La această etapă comunicarea este foarte importantă, iar eu și colegii mei suntem gata să-ți oferim suport suplimentar. :wink:

Deci, te rog să deschizi terminalul, să mergi în directoria în care lucrezi și să rulezi următoarea comandă:

```
$ subl bootstrap.html
```

În editorul tău preferat (încă nu te-ai îndrăgostit de sublime text?), inserează următorul text. El va fi scheletul experimentelor noastre.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Bootstraping...</title>
</head>
<body>
<div style="width: 800px; margin: 10px auto 0;">

</div>
</body>
</html>
```

Adaugă o salutare în `body`, inserează acest text:

```html
<h1>Welcome to Bootstrap-Savannah!</h1>
<h2>Lions are cute!</h2>
```

Vezi rezultatul în navigatorul tău web preferat:

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/clean-page.png" />
</div>

Implicit, navigatorul tău stilizează elementele HTML fundamentale. Hai să-i dăm o aromă de bootstrap!

Stai! Nu trebuie să downloadezi nimic! Vom încărca stilurile bootsreap de pe CDN-ul oficial. Ah, nu ți-am povestit ce-i aia **CDN**. CDN este **C**ontent **D**elivery **N**etwork, sau **C**ontent **D**istribution **N**etwork. Sună complicat? În practică nu e, cel puțin din perspectivă de utilizator. CDN este un sistem distribuit care servește fișiere statice. Pe lângă simplitatea de utilizare, CDN-urile mai au și alte avantaje, ele însă nu sunt în scopul acestui tutorial.

Adăugăm legătura spre stilurile bootstrap, undeva în interiorul tag-ului head:

```html
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">
```

Adăugăm și librăria javascript pentru bootstrap. Nu ne trebuie la moment, dar vom avea nevoie în viitor de ea. Așa cum Bootstrap se bazează pe jQuery, includem ambele surse din CDN.

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.4/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
```

Surprinzător! Ceva s-a schimbat. Poți observa că textul a căpătat automat altă nuanță de culoare, altă dimensiune și alt font.

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/clean-bootstrap.png" />
</div>

Te întrebi probabil de ce s-a întâmplat asta. bootstrap.css a făcut-o. Ca prim scop, acele stil-uri au resetat toate stilurile predefinite de navigatorul tău și și-a impus standardele asupra elementelor de bază. Totuși, Bootstrap nu-și impune stilizarea asupra butoanelor, tabelelor, input-urilor (căsuțe de introducere a textului) și altele. Stilizarea se face explicit, specificând clasele necesare pentru elementele alese. Știm că explicit e mai bine decât implicit pentru că ni se oferă libertatea de a lua decizii mai multe.

## Stilizarea lucrurilor obișnuite

Acum că avem un schelet funcțional, haideți să încercăm să stilizăm elemente obișnuite cu ajutorul la bootstrap.

### Tabele
Că tot suntem la începutul sesiunii, vom da startul experimentelor cu chestii mai plictisitoare, și anume - tabele. Deseori în aplicațiile tale vei avea nevoie să afișezi fie careva statistici fie alte date organizate sub formă de tabel. Fără ele, poate fi într-adevăr dificil. Hai să încercăm un tabelaș cu oarecare 5 animale din savană:

```html
    <table>
        <thead>
            <tr>
                <th>#</th>
                <th>Name</th>
                <th>Genus</th>
                <th>Family</th>
                <th>Order</th>
                <th>Class</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>1.</td>
                <td>Giraffe</td>
                <td>Giraffa</td>
                <td>Giraffidae</td>
                <td>Artiodactyla</td>
                <td>Mammalia</td>
            </tr>
            <tr>
                <td>2.</td>
                <td>Zebra</td>
                <td>Equus</td>
                <td>Equidae</td>
                <td>Perissodactyla</td>
                <td>Mammalia</td>
            </tr>
            <tr>
                <td>3.</td>
                <td>Ostrich</td>
                <td>Struthio</td>
                <td>Struthionidae</td>
                <td>Struthioniformes</td>
                <td>Aves</td>
            </tr>
            <tr>
                <td>4.</td>
                <td>Grasshopper</td>
                <td>-</td>
                <td>Caelifera</td>
                <td>Orthoptera</td>
                <td>Insecta</td>
            </tr>
            <tr>
                <td>5.</td>
                <td>Cheetah</td>
                <td>Acinonyx</td>
                <td>Felidae</td>
                <td>Carnivora</td>
                <td>Mammalia</td>
            </tr>
        </tbody>
    </table>
```

Rezultatul e un tabel simplu, stilizat cumva de către navigatorul tău web. Ar putea cam așa:

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/clean-table.png" />
</div>

Nu e rău! Însă hai să beneficiem de oporunitățile oferite de bootstrap. Adăugăm tabelului clasa `table` și explorăm clasele `table-hover`, `table-bordered` și `table-striped`.

În combinația `table table-striped`, tabelul tău va arăta cam așa:

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/bootstrap-table-striped.png" />
</div>

Bravo! :rose: Te-ai descurcat de minune. Sper că te-am intrigat și vrei să explorăm împreună în continuare bootstrap-ul.

### Forme și butoane

Mereu, atunci când utilizatorul va trebui să introducă ceva date în aplicațiile tale vei avea nevoie de forme. În cadrul formelor vei avea diverse tipuri de câmpuri ca de exemplu câmpuri de introducere a textului, checkbox (elemente de bifare), radio button (la fel ca și checkbox doar că având posibilitatea de a selecta un unic item dintr-un grup), butoane și altele.

Să zicem că avem nevoie de o interfață de căutare a animalelor după numele lor. Deasemenea putem salva rezultatele căutării pentru utilizare ulterioară. Vom avea nevoie deci de un text input, un checkbox și un buton. Hai să vedem cum o facem:

```html
    <form action="#">
        <div>
            <label for="animal-name">Animal name</label>
            <input type="text" id="animal-name">
        </div>
        <div>
            <label>
                <input type="checkbox"> Save this search for later
            </label>
        </div>
        <div>
            <button type="submit">Search</button>
        </div>
    </form>
```

Să vedem rezultatul:

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/clean-search-form.png" />
</div>


Am obținut rezultatul dorit. Acum hai s-o stilizăm utilizând bootstrap.

Adăugăm clasa `form-group` la grupul cu text box, clasa `checkbox` grupului cu checkbox și clasele `btn btn-default` butonului de căutare. Căsuței de introducere a textului îi dăm clasa `form-control`. Acum avem formă stilizată standard cu bootstrap. Iată cum s-a schimbat codul pentru formă:

```html
    <form action="#">
        <div class="form-group">
            <label for="animal-name">Animal name</label>
            <input type="text" id="animal-name" class="form-control">
        </div>
        <div class="checkbox">
            <label>
                <input type="checkbox"> Save this search for later
            </label>
        </div>
        <div class="form-group">
            <button type="submit" class="btn btn-success">Search</button>
        </div>
    </form>
```

Și iată cum arată vizual:

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/bootstrap-form.png" />
</div>

Perfect! Acum, dacă dorim ca forma să fie aliniată orizontal într-un rând, trebuie să punem forma într-un `div` cu clasa `form-inline`. Superb! Cu un efort minim, elementele stau frumos aliniate, perfect pentru interfața noastră de căutare. :+1:

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/bootstrap-inline-form.png" />
</div>

Haideți acum să experimentăm cu stilul butonului. Colorarea în culorile predefinite se face prin clasele: `btn-primary`, `btn-success`, `btn-info`, `btn-warning`, `btn-danger` și `btn-link`. Desigur, puteți stiliza suplimentar scriind definind noi clase în CSS și aplicându-le în locurile necesare.

La fel ca și culorile, dimensiunile butoanelor pot fi definite prin clasele bootstrap: `btn-lg`, `btn-sm` și `btn-xs`.

De asemenea putem experimenta și cu starea input-urilor, bootstrap-ul se descurcă și cu aceste detalii. Haideți să experimentăm cu atributele `disabled` and `readonly`.

### Glyphicons
Glyphicons este un set cu 254 de iconițe incorporate într-un font cu același nume. Dat fiind că e un font, beneficiem de grafică vector pentru iconițe, deci putem să le scalăm la orice dimensiune fără a pierde din calitate.

NB: Grafica vectorială se deosebește de cea simplă numită raster sau bitmap prin faptul că imaginile sunt construite utilizând primitivele grafice cum ar fi punctul, linia, linii bezier și altele. Imaginile raster folosesc pixelii ca unitate primitivă, deci de exemplu o imagine de 16x16 pixeli nu poate fi scalată fără pierderea calității, chiar și cu tehnici avansate de interpolare.

La fel ca și celelalte componente, iconițele sunt disponibile prin intermediul claselor specifice. Pentru a plasa o iconiță pe un element este necesară plasarea claselor: `glyphicon` și `glyphicon-<nume_iconiță>`. Dimensiunea iconiței e dependentă de parametrul CSS `font-size` pentru acel element.

Acum că am învățat care e treaba cu iconițele și cum se folosesc, haideți să plasăm o pictogramă relevantă pe butonul de căutare din exemplul precedent. Pentru aceasta, tot ce trebuie să facem e să adăugăm un element nou în interiorul tag-ului `<button></button>` cu clasele discutate mai sus. Pentru acest exemplu este nevoie de `glyphicon glyphicon-search`:

```html
    <span class="glyphicon glyphicon-search" aria-hidden="true"></span>
```

Iată și rezultatul mult așteptat:

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/components-glyphicons.png" />
</div>

Perfect! A fost simplu, nu? :stuck_out_tongue_winking_eye:

### Dropdowns
Acum că și butonașul de căutare arată destul de intuitiv, trebuie să adăugăm un element în care am putea seta un filtru după modul de nutriție. Simplu, putem să creăm un select box:

```html
    <div class="form-group">
        <select name="nutrition">
            <option value="0">Carnivore</option>
            <option value="1">Herbivore</option>
            <option value="2">Omnivore</option>
        </select>
    </div>
```

Hm... Nu arată prea bine:

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/components-selectbox.png" />
</div>

We can do better than that! :innocent:

Un prim lucru ce poate fi făcut este adăugarea clasei `form-control` elementului `<select>`. Arată ceva mai bine, nu?

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/components-selectbox-formcontrol.png" />
</div>

Însă nu e perfect. Și lista deschisă arată diferit pe diferite sisteme. Probabil există vre-un mecanism prin care e posibilă crearea unui element universal care să arate bine și la fel pe toate sistemele. Haideți să analizăm împreună **button dropdowns** din Bootstrap.

Dați să rescriem codul de mai sus utilizând button dropdowns din bootstrap:

```html
    <div class="btn-group">
        <button type="button" class="btn btn-default dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
            Carnivore <span class="caret"></span>
        </button>
        <ul class="dropdown-menu">
            <li><a href="#">Carnivore</a></li>
            <li><a href="#">Herbivore</a></li>
            <li><a href="#">Omnivore</a></li>
        </ul>
    </div>

```

Să vedem... Acum atât butonul cât și lista de selecție arată bine, într-o manieră consistentă cu interfața bootstrap:

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/components-button-dropdown.png" />
</div>

Perfect! Vezi că ți-a ieșit bine? Hai să mergem mai departe să explorăm și alte detalii ale bootstrap-ului.

### Bară de navigare (navbar)
Ne-am propus ca în partea de sus a paginii să avem un meniu orizontal ce ne va ajuta să navigăm mai ușor aplicația noastră. Reieșind din documentația bootstrap, o să facem un navbar simplificat:

```html
    <nav class="navbar navbar-default">
        <div class="container-fluid">
            <div class="collapse navbar-collapse">
                <ul class="nav navbar-nav">
                    <li class="active"><a href="#">Home</a></li>
                    <li><a href="#">Catalog</a></li>
                    <li><a href="#">Messages</a></li>
                    <li><a href="#">Encyclopedia</a></li>
                </ul>

                <ul class="nav navbar-nav navbar-right">
                    <li><a href="#">Profile</a></li>
                    <li><a href="#">Logout</a></li>
                </ul>
            </div>
        </div>
    </nav>
```

Avem și un rezultat bun pe față. Twitter bootstrap chiar ne scutește de multe eforturi!

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/components-navbar.png" />
</div>

### Badges
"Badges" este termenul dat de bootstrap unor elemente speciale. Ele sunt niște etichete care au ca scop să ne arate careva numere sub formă de contoare. Acum am putea să adăugăm un element ce va denota numărul de mesaje necitite, în bara de navigare. În cazul dat soluția este extrem de simplă. Adăugăm secvența următoare de cod în itemul cu **Messages**:

```html
<span class="badge">21</span>
```

Și, din nou, avem un rezultat drăguț, obținut cu un foarte mic efort:

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/components-badge.png" />
</div>

## Fin
Cam atât de pe meleagurile componentelor Twitter bootstrap. Ca o provocare, zic să experimentezi cu elementele, stilurile, iconițele și alte detalii bootstrap. Îți pun la dispoziție documentația:

- [Getting Started](http://getbootstrap.com/getting-started/)
- [CSS](http://getbootstrap.com/css/)
- [Components](http://getbootstrap.com/components/)


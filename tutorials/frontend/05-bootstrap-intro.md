---
layout: default
title: Bootstrap Intro
category: basic
---

# Bootstrap

[Bootstrap](getbootstrap.com) sau Twitter Bootstrap Framework este un conglomerat de intstrumente și șabloane stilizate ce au ca scop ușurarea și facilitarea dezvoltării aplicațiilor web.

Inițial, a fost un proiect intern în cadrul Twitter Inc., ca ulterior să devină Open-Source și accesibil pentru toți. După ce sursele au fost deschise și publicate pe GitHub, proiectului i s-au alăturat un număr foarte mare de voluntari ce au contribuit și au dezvoltat proiectul până la ziua de azi.

Începând cu versiunea 3.0, Bootstrap a adoptat un standard mobile-first, ce permite crearea interfețelor responsive. Interfețele responsive își au ca scop furnizarea aplicațiilor web pe diferite platforme cum ar fi telefoanele mobile, tabletele, laptop-uri și alte dispozitive.

## Starting point
Pentru început, zic să inițiem un fișier în care vom experimenta bootstrap-ul. Eu sper că deja te-ai obișnuit cu terminalul și cu editorul de text. Dacă încă nu te simți confortabil utilizând terminalul sau alte instrumente și ai careva neclarități - **întreabă**! La această etapă comunicarea este foarte importantă, iar eu și colegii mei suntem gata să-ți oferim suport suplimentar. :wink:

În editorul tău preferat (încă nu te-ai îndrăgostit de sublime text?), inserează următorul text. El va fi scheletul experimentelor noastre.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Bootstraping...</title>
</head>
<body>

</body>
</html>
```

Adaugă o salutare în `body`, inserează acest text:

```html
<h1>Feel the power of Bootstrap.</h1>
<h2>Now YOU rule the world of web!</h2>
```

Vezi rezultatul în navigatorul web preferat:

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/1.png" />
</div>

Implicit, navigatorul tău stilizează elementele HTML fundamentale. Hai să-i dăm o aromă de bootstrap!

Stai! Nu trebuie să downloadezi nimic! Vom încărca stilurile bootstrap de pe CDN-ul oficial. Ah, nu ți-am povestit ce-i aia **CDN**. CDN este **C**ontent **D**elivery **N**etwork, sau **C**ontent **D**istribution **N**etwork. Sună complicat? În practică nu e, cel puțin din perspectivă de utilizator. CDN este un sistem distribuit care servește fișiere statice. Pe lângă simplitatea de utilizare, CDN-urile mai au și alte avantaje, ele însă nu sunt în scopul acestui tutorial.

Adăugăm legătura spre stilurile bootstrap, undeva în interiorul tag-ului head:

```html
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">
```

Adăugăm și librăria JavaScript pentru bootstrap. Nu ne trebuie la moment, dar vom avea nevoie în viitor de ea. Așa cum Bootstrap se bazează pe jQuery, includem ambele surse din CDN.

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.4/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
```

Surprinzător! Ceva s-a schimbat. Poți observa că textul a căpătat automat altă nuanță de culoare, altă dimensiune și alt font.

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/2.png" />
</div>

Te întrebi probabil de ce s-a întâmplat asta. bootstrap.css a făcut-o. Ca prim scop, acele stil-uri au resetat toate stilurile predefinite de navigatorul tău și și-a impus standardele asupra elementelor de bază. Totuși, Bootstrap nu-și impune stilizarea asupra butoanelor, tabelelor, input-urilor (căsuțe de introducere a textului) și altele. Stilizarea se face explicit, specificând clasele necesare pentru elementele alese. Știm că explicit e mai bine decât implicit pentru că ni se oferă mai mult control.

Acum că avem un schelet funcțional, haideți să încercăm să stilizăm elemente obișnuite cu ajutorul la bootstrap.

### Navbar
Navbar-ul este componentul cel mai des întâlnit pe paginile web. De obicei navbar-ul este amplasat împreună cu logo-ul, deci urmează un exemplu cum prezentăm un logo și un navbar pe pagina noastră utilizînd clasele Bootstrap.

```html
<nav class="navbar navbar-inverse navbar-fixed-top" role="navigation">
  <div class="container">
    <div class="navbar-header">
      <a class="navbar-brand" href="index.html">Your Logo Text Goes Here</a>
    </div>
    <div class="collapse navbar-collapse">
      <ul class="nav navbar-nav navbar-right">
        <li>
          <a href="#">First Menu Item</a>
        </li>
        <li>
          <a href="#">Second Menu Item</a>
        </li>
        <li>
          <a href="#">Third Menu Item</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
    
```

Rezultatul e un Navbar simpatic care l-am obținut în mai puțin de un minut. Isn't that fantastic?

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/3.png" />
</div>

### Slider

Nimic nu face mai sexy un site de cât niște imagini mari și frumoase într-un slider. Utilizînd codul ce urmează vă veți convinge că lucrurile stau foarte simplu.

```html
<header id="myCarousel" class="carousel slide" data-ride="carousel">
  <div class="carousel-inner">
    <div class="item active">
      <img src="http://unsplash.it/1900/800/?image=151" alt="Slide">
      <div class="carousel-caption">
        <h2>Quibusdam illum, suscipit labore. Voluptas minima, magni.</h2>
      </div>
    </div>
    <div class="item">
      <img src="http://unsplash.it/1900/800/?image=152" alt="Slide">
      <div class="carousel-caption">
        <h2>Soluta distinctio suscipit ab sapiente quo molestias.</h2>
      </div>
    </div>
    <div class="item">
      <img src="http://unsplash.it/1900/800/?image=153" alt="Slide">
      <div class="carousel-caption">
        <h2>Facere praesentium quo asperiores. Omnis, itaque, quo.</h2>
      </div>
    </div>
  </div>
  <a class="left carousel-control" href="#myCarousel" data-slide="prev">
    <span class="icon-prev"></span>
  </a>
  <a class="right carousel-control" href="#myCarousel" data-slide="next">
    <span class="icon-next"></span>
  </a>
</header>
```

Să vedem rezultatul:

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/4.png" />
</div>



### Responsive Layout

Pentru a defini o listă de știri pe pagină avem nevoie de câteva coloane. Paginile web au moștenit această tehnică de la ziare. Implicit Bootstrap folosește sistemul de 12 coloane. O reprezentare grafică vedeți mai jos.

<div class="custom-image-shadow">
    <img src="/images/d6l1-bootstrap/5.png" />
</div>

Următorul pas ar fi calcularea dimensiunilor coloanelor. Le calculăm folosind formula 12/x, unde x este numărul de coloane care dorim să-l obținem. De exemplu dacă dorim să afișăm conținutul în 3 coloane împărțim 12/3 și obținem dimensiunea coloanelor egală cu 4. Folosind rezultatele obținute și markup-ul de mai jos afișăm noutățile.

```html
<div class="container">
  <div class="row">
    <div class="col-md-4">
      <div class="panel panel-default">
        <img src="http://unsplash.it/800/600?image=101" class="img-thumbnail" alt="">
        <div class="panel-body">
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Itaque, optio corporis quae nulla aspernatur in alias at numquam rerum ea excepturi expedita tenetur assumenda voluptatibus eveniet incidunt dicta nostrum quod?</p>
          <a href="#" class="btn btn-success">Mai mult <i class="glyphicon glyphicon-menu-right"></i></a>
        </div>
      </div>
    </div>
    <div class="col-md-4">
      <div class="panel panel-default">
        <img src="http://unsplash.it/800/600?image=102" class="img-thumbnail" alt="">
        <div class="panel-body">
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Itaque, optio corporis quae nulla aspernatur in alias at numquam rerum ea excepturi expedita tenetur assumenda voluptatibus eveniet incidunt dicta nostrum quod?</p>
          <a href="#" class="btn btn-success">Mai mult <i class="glyphicon glyphicon-menu-right"></i></a>
        </div>
      </div>
    </div>
    <div class="col-md-4">
      <div class="panel panel-default">
        <img src="http://unsplash.it/800/600?image=103" class="img-thumbnail" alt="">
        <div class="panel-body">
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Itaque, optio corporis quae nulla aspernatur in alias at numquam rerum ea excepturi expedita tenetur assumenda voluptatibus eveniet incidunt dicta nostrum quod?</p>
          <a href="#" class="btn btn-success">Mai mult <i class="glyphicon glyphicon-menu-right"></i></a>
        </div>
      </div>
    </div>
  </div>
</div>
```

## Fin
Cam atât de pe meleagurile componentelor Twitter bootstrap. Ca o provocare, zic să experimentezi cu elementele, stilurile, iconițele și alte detalii bootstrap. Îți pun la dispoziție documentația:

- [Getting Started](http://getbootstrap.com/getting-started/)
- [CSS](http://getbootstrap.com/css/)
- [Components](http://getbootstrap.com/components/)


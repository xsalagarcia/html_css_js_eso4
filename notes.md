<!-- TOC -->
* [Presentació](#presentació)
* [Configuració de l'entorn](#configuració-de-lentorn)
  * [Recomanable: Visual Studio Code al propi ordinador](#recomanable-visual-studio-code-al-propi-ordinador)
  * [Menys recomanable: Visual Studio Code online](#menys-recomanable-visual-studio-code-online)
  * [Podeu utilitzar PyCharm per crear un fitxer HTML](#podeu-utilitzar-pycharm-per-crear-un-fitxer-html)
  * [Similar a PyCharm, tenim un IDE dedicat a la programació](#similar-a-pycharm-tenim-un-ide-dedicat-a-la-programació)
* [Creació d'una pàgina web a partir d'HTML bàsic](#creació-duna-pàgina-web-a-partir-dhtml-bàsic)
  * [Fonaments bàsics sobre HTML](#fonaments-bàsics-sobre-html)
  * [Posem contingut a la web](#posem-contingut-a-la-web)
  * [Ara tu](#ara-tu)
* [Els atributs de les etiquetes](#els-atributs-de-les-etiquetes)
* [Els salts de línia i els espais en blanc i altres caràcters especials.](#els-salts-de-línia-i-els-espais-en-blanc-i-altres-caràcters-especials)
* [CSS](#css)
  * [Selectors CSS dins l'etiqueta `<style>`](#selectors-css-dins-letiqueta-style)
  * [CSS en línia](#css-en-línia)
  * [La lògica de les propietats CSS](#la-lògica-de-les-propietats-css)
  * [Propietats rellevants](#propietats-rellevants)
* [JavaScript](#javascript)
  * [Exemple](#exemple)
<!-- TOC -->

# Presentació

**Hyper Text Markup Language (HTML)** és un llenguatge, però no de programació, sinó de marques. A través de marques o etiquetes es descriu com s'organitza un document.

Combinant etiquetes i text podem definir:
- Contingut.
- Quin tipus d'informació conté el document.
- Com s'ha de visualitzar el document.

Un fitxer HTML té extensió .html (o .htm).

Existeixen altres llenguatges de marques, similars a l'HTML que s'utilitzen per emmagatzemar el contingut de documents de text (word, writer)
o per comunicar-se entre aplicacions o serveis en xarxa.

Actualment, HTML ha evolucionat a la *versió 5*.

Habitualment, un servidor a la xarxa conté o genera documents HTML. Els serveix quan el nostre navegador ho sol·licita, per exemple al demanar una pàgina web.

# Configuració de l'entorn

## Recomanable: Visual Studio Code al propi ordinador

1. Descarregar Visual Studio Code: Seguir les instruccions per cada plataforma.
2. Instal·lar l'extensió `Live Preview` de *Microsoft*: **Vigileu que estigui firmada per Microsoft**: Aquesta extensió permetrà visualitzar el document web al mateix editor
de forma dinàmica.

## Menys recomanable: Visual Studio Code online

Es pot utilitzar l'editor Visual Studio Code sense instal·lar-lo, a través del navegador. A l'adreça https://vscode.dev/, però té algunes limitacions. Compte a l'hora de crear i desar fitxers.

## Podeu utilitzar PyCharm per crear un fitxer HTML

Simplement, crear un nou fitxer i donar-li extensió HTML. Ressalta la sintaxi html i té alguna funcionalitat específica.

## Similar a PyCharm, tenim un IDE dedicat a la programació web: Webstorm

[WebStorm](https://www.jetbrains.com/webstorm/)

## Utilitzar un editor bàsic com el bloc de notes

I obrir els documents html amb el vostre navegador.

# Creació d'una pàgina web a partir d'HTML bàsic

- Obrir i crear una nova carpeta: File -> Open folder: Crear una nova carpeta, que podem anomenar `web01`
- Botó secundari sobre l'explorador i seleccionar opció de crear un nou fitxer, anomenar-lo `berenguer.html`. És important l'extensió (`.html`).
- Editar aquest fitxer: Escriure `!` i prémer `Enter`.

Si fins aquí s'han seguit els passos correctes apareix el següent codi, escrit de forma automàtica:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

## Fonaments bàsics sobre HTML

HTML no és un llenguatge de programació, sinó que simplement defineix l'estructura i el contingut d'una pàgina web. Per això s'utilitzen etiquetes que organitzen el contingut. **Cada etiqueta representa un element de la pàgina web**.

Una estructura bàsica d'una etiqueta és com segueix:

```html
<etiqueta atribut="valor">Contingut</etiqueta>
```
Aquesta estructura pot variar, però en general, fixem-nos que `<nom_etiqueta>` defineix l'**obertura** de l'etiqueta i pot contenir atributs de forma opcional. `</nom_etiqueta>` és el **tancament** de l'etiqueta. Entre l'obertura i el tancament hi ha contingut. El contingut pot ser text, així com altres etiquetes. Quan el contingut són altres etiquetes es defineix una **jerarquía**.

Sobre l'estructura inicial que se'ns ha creat, comentem-la:


```html
<!--Aquesta primera línia indica al navegador que això és un document HTML-->
<!DOCTYPE html> 

<!--Aquesta segona és una etiqueta, és única per tot el document i conté la resta del document HTML.
Té habitualment un atribut, lang, que indica l'idioma del document web. En aquest cas anglès.-->
<html lang="en"> 

<!--Aquesta etiqueta <head> conté altres etiquetes dins que donen informació més per al navegador que 
no per l'usuari-->
<head> 
    <!--Una etiqueta que indica el conjunt de caràcters que s'utilitzen-->
    <meta charset="UTF-8"> 
    
    <!--Indica al navegador com visualitzar la web-->
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
    
    <!--El títol de la web-->
    <title>Document</title>
</head>

<!--Dins aquesta etiqueta, hi posarem el contingut, el cos del document: Text, imatges...-->
<body>
    
</body><!--Indica al navegador com visualitzar la web-->

<!--Fixa't que estem tancant la etiqueta <html>-->
</html>
```

> Un dels millors portals web per saber què fa cada etiqueta i com fer-la servir correctament és [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements).

## Posem contingut a la web

Aquest seria un petit exemple d'una pàgina web, molt senzill.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>El meu nom és Berenguer</h1>
    <p>Sóc un <strong>gat</strong> de color taronja, però no m'hauries de confondre amb Garfield. Potser som parents, però
        jo tinc els meus propis dibuixos animats i cómics. Algunes coses que hauries de saber són:
    </p>
    <ul>
        <li>M'argada dormir</li>
        <li>M'agrada menjar</li>
        <li>M'agrada el peix</li>
        <li>Freqüento els cubells d'escombraries</li>
    </ul>
    <img src="https://www.enfocamp.es/newsletter/img/boletin/gato-isidoro.jpg" alt="">

    <p>En el seu dia, vaig arribar a ser cèlebre.
        <a href="https://en.wikipedia.org/wiki/Heathcliff:_The_Movie">Fins i tot em van fer una pel·lícula.</a></p>
</body>
</html>
```

També pots, des del sistema d'arxius, fer doble click al fitxer i esperar que s'obri amb el navegador per defecte del teu ordinador.

## Ara tu

Hem vist i com crear una web. Crea un document html que et presenti: Qui ets, aficions, ...

- Crea un nou fitxer amb l'extensió `.html`
- Utilitza la instrucció `<!DOCTYPE html>` per deixar clar que es tracta d'un document html.
- Obre una etiqueta `<html>` (Recorda que s'ha de tancar, `</html>`).
- Obre una etiqueta `<head>` (Recorda que s'ha de tancar).
    - Dins l'etiqueta `<head>` posa el títol de la pàgina web amb l'etiqueta `<title>`.
- Obre una etiqueta `<body>` (Recorda que l'has de tancar). Dins l'etiqueta `<body>` posa el contingut de la pàgina web. Pots utilitzar:
    - `<h1>` per escriure un títol (encapçalament). Recorda que l'has de tancar. De fet, pots utilitzar fins a 6 nivells diferents de títol: `<h1>`, `<h2>`, ..., `<h6>`.
    - `<p>` per escriure un paràgraf.
    - `<b>` o `<strong>` per posar text en negreta, `<i>` o `<em>` possiblement tindràs cursiva. `<u>` per subratllar. Tot i això, pot ser que el teu navegador necessiti alguna cosa més per canviar l'estil del text. Ja ho veurem.
    - Utilitza `<ul>` o `<ol>` per crear una llista sense ordre o amb ordre respectivament.
        - Utilitza `<li>` Per cada ítem de la llista.
    - Si tens ganes d'utilitzar més elements, pots investigar: `<sub>`, `<sup>`, `<details>` + `<summary>`, `<small>`, `<hr>`, `<br>`


# Els atributs de les etiquetes

Quan parlàvem de fonaments, hem presentat aquesta estructura per les etiquetes HTML:


```html
<etiqueta atribut="valor">Contingut</etiqueta>
```

Els atributs són valors que configuren els elements que es creen amb les etiquetes o poden ajustar-ne el seu comportament.

Alguns exemples:

```html
<img src="https://picsum.photos/200" alt="Una imatge qualsevol">
```

Amb `src` s'indica on es troba la imatge que cal mostrar. Amb `alt` s'indica un text alternatiu per si no es pot mostrar l'imatge (o per als lectors de web per a invidents).

```html
<a href="https://www.google.com/" target="_blank">Ves a google</a>`
```

Amb `href` índiques la direcció del _link_. Amb `target` s'estableix com es comportarà el navegador en fer click al _link_ (El valor pot ser `_self`, `_blank`, `_parent`, `_top`, `_unfencedTop`).

```html
<video src="https://download.blender.org/peach/bigbuckbunny_movies/BigBuckBunny_320x180.mp4" controls width="400"></video>
```
L'atribut `src` indica on es troba el fitxer per reproduir. L'atribut `controls` no té cap valor associat, però si està present indica que es mostren els controls per reproduir. L'atribut `width` indica l'amplada el video a visualitzar.

```html
<h1 id="titol_principal">El títol principal</h1>
```
`id` és un atribut que s'utilitza per crear un identificador únic per un determinat element.

# Els salts de línia i els espais en blanc i altres caràcters especials.

Quan s'interpreta HTML no es tenen en compte els salts de línia del codi. Per canviar de línia, o bé s'utilitza un paràgraf `<p>`nou (o altres elements que es disposen en bloc (`<ul>`, `<li>`...)),
o bé, dins un paràgraf, si es vol fer un salt de línia intencionat pots utilitzar l'element `<br />`. **`<br />` és una de les poques etiquetes que no s'ha de tancar, donat que mai hi haurà contingut dins.**

Amb els espais en blanc és similar. Si entre dues paraules hi ha diversos espais en blanc, el navegador, en condicions normals, només en mostrarà un. Per afegir diversos espais en blanc s'utilitza el caràcter especial `&nbsp;`.

Altres [caràcters especials i emojis](https://www.w3schools.com/charsets/ref_emoji_intro.asp) es poden també mostrar de forma similar als caràcters en blanc:

```html
<p>
    Aquest matí<br />
    he vist un dofí &#x1F42C;<br />
    tocant el violí.<br />
</p>
<p>
    El tocava molt bé<br />
    Però era de paper.<br />
</p>
</p>
    XSG&nbsp;&nbsp;&nbsp;&nbsp;1983
</p>
```

Pràctica, crea una pàgina web que parli de la teva cançó o música preferida.

# CSS

El [Cascade Style Sheet (CSS)](https://developer.mozilla.org/es/docs/Web/CSS) és el llenguatge d'estils (no de programació). Fins ara hem deixat a càrrec del navegador la decisió de com mostrar cada element del document HTML. Sense CSS, totes les pàgines web tindrien el mateix format i aparença.

Per això es diu que l'HTML representa l'*esquelet* i el CSS la *pell*.

El CSS pot anar a un fitxer a part, amb extensió `.css`, referenciat amb l'etiqueta `<link>`, dins una etiqueta `<style>`, normalment formant part de `<head>` o bé *en línia* a través de l'atribut `style` a cada etiqueta.

Per simplicitat veurem els dos últims casos: etiqueta `<style>` i atribut `style`. Normalment s'utilitzen fitxers `.css`.

## Selectors CSS dins l'etiqueta `<style>`

És el mateix format que quan s'utilitza un fitxer `.css`.

```html
<style>
    h1 {  /* Selecciona una etiqueta*/
        font-family: sans-serif;
        color: red;
    }
    .bold { /*Selecciona una classe. L'atribut class defineix la classe, vàries etiquetes poden ser de la mateixa classe.*/
        font: font-weight: bold;
    }
    #titol_principal {  /*Selecciona un identificador. L'atribut id defineix l'identificador, l'identificador és únic per una sola etiqueta.*/
        font-family: sans-serif;
        background-color: lightcoral;
    }
    p, ul{ /*Selecciona dos etiquetes*/
        font-size: 1em;
    }
    p b { /*Selecciona les etiquetes b que es troben dins les etiquetes p*/
        font-weight: bold;
    }
</style>
```

Fixa't:
```css
selector {
    propietat: valor;
    propietat: valor; 
}
```

A través del selector indiquem quin element o elements volem afectar. Les claus `{}` contenen totes
les propietats i valors que volem establir. Cada propietat i valor se separa amb `;`.

## CSS en línia

```html
<p style="font-family: sans-serif; text-align:justify;">
    Aquí un paràgraf justificat
</p>
```
Fixa't, amb el CSS en línia, s'aplica per un mateix element, i es defineix tot dins l'atribut `style`, amb els diferents `atribut: valor` separats per `;`.

El CSS en línia sobreescriu el que s'hagi definit prèviament dins un fitxer o una etiqueta `style`.

## La lògica de les propietats CSS

- `background-...`: Coses sobre el fons.
- `font-...` coses sobre el tipus de lletra.
- `padding-...` Coses sobre el marge interior.
- `margin-...` Coses sobre el marge exterior.

## Propietats rellevants

CSS és simple d'utilitzar però extens i complicat en opcions. Aquí veurem pautes bàsiques per canviar petits detalls de la web, però tots els efectes especials (animacions, ombres i altres degradats) i algunes interaccions molt treballades estan fetes amb CSS.

- `background-color`
- `font-family`
- `font-size`
- `text-align`
- `text-decoration`
- `width`
- `max-width`
- `height`
- `display`
- `position`
- `padding`
- `margin`
...

## Alinear elements amb flexbox

El mètode [Flexbox](https://developer.mozilla.org/es/docs/Learn_web_development/Core/CSS_layout/Flexbox) és una de les formes senzilles d'alinear elements per aconseguir files i columnes i poder maquetar els elements de la web. N'hi ha d'altres però aquest és potent i relativament senzill.

Habitualment, es selecciona un elemnet contenidor i se'l defineix com un contenidor tipus *flex*. Els eelements que conté passen a comportar-se com a elements *flex*. Aquest contenidor se li poden donar altres propietats.

### Propietats del contenidor flex

Aquestes en són les principals:

- `display`: flex; → Tots els elements del contenidor (directes) passaran a comportar-se com a elements flex. El contingut s'estableix d'acord amb el model flexbox.
- `flex-flow:` row|column  wrap|nowrap ; Resumeix altres 2 instruccions `flex-direction`: Si serà en l'eix x (per defecte, row, eix principal, x, útil per fer columnes) o en l'eix y(column, eix principal y). `flex-wrap` si rebassarà  (nowrap) o no (wrap, força el canvi de línia o columna si no hi caben) al arribar a final (envoltar o no). Eix principial serà x (y secundari y) si és column, i eix principal serà y (i secundari x) si son row. 
- `justify-content`: flex-start|flex-end|center|space-around|space-evenly|space-between; podem configurar com els elements estan disposats a l'eix primari: alineats a l'inici, alineats al final, centrats, justificats amb espai a inici i final, igual però amb menys als extrems. o justificats arribant als extrems. Respectivament. Està alineat amb el que definim a flex-flow (columna o fila).
- `align-items`: permet configurar com els elements estan disposats a l'eix secundari.(controla la alineació vertical si hem especificat `flex-flow: row;`). Els valors poden ser els mateixos que els de justify-content, a més de stretch. Si posem stretch ens estirarà els continguts fins als extrems (a no ser que hi haguem especificat alçada o amplada).
- `align-content`: intervé només quan tenim wrap, i hi ha un salt de línia en l'eix principal. P.ex. quan eix principal és x i tenim dues files; llavors defineix com es comporta la següent fila (eix principal x) o columna (eix principal y).

### propietats dels elements continguts dins un contenidor flex

Aquestes en són les principals:
`flex-grow`: Com es distribueix espai sobrant que hi pugui haver a la fila(en cas de eix principal x). [0, infinit]. Els números són en proporció de la resta de continguts. P.ex. si tots els elements continguts tinguessin valor 1, tots utilitzarien la resta d'espai disponible a parts iguals. Si varis elements tinguessin 1 i un tingués 0.5, el de 0.5 seria la meitat. Hi hem estat jugant amb exemple 13. El valor per defecte és 0 per tots els continguts, de manera que quan especifiquem un flex-grow diferent a 0 a qualsevol altre element, el element on no hem especificat això
`flex-shrink`: com es comprimeix l'espai en cas que no hi hagi espai suficient a la fila (en cas de eix principal x) en cas que tinguem nowrap. [0, infinit]. Funciona com el flex-grow, però especifica el comportament dels elements quan es redueixen per intentar cabre a la mateixa lína i no sobrepassar el contenidor. Valor per defecte és 1.
`flex-basis`: Equivalent al width (el substitueix). És l'ample inicial que li volem donar a la caixa. En px, %...

# JavaScript

Si hem dit que HTML era l'esquelet i CSS la pell, [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) podria ser el cervell.

JavaScript és un llenguatge de programació que l'interpreta el navegador. Ens permet afegir certa lògica a les pàgines web.

JavaScript va ser creat per afegir petites parts de lògica a un document web, permetent canvis al document i interaccions complexes amb l'usuari. Aquest llenguatge ha evolucionat, i s'utilitza també, tant per fer aplicacions d'escriptori com serveis web.

Nosaltres veurem algun exemple de com pot utilitzar-se en un document web.

El codi JavaScript pot inserir-se de manera similar a com es fa amb el CSS:
- En un fitxer a part (habitualment amb l'extensió `.js`). Dins l'etiqueta <head> s'introdueix una etiqueta `<script>`:
```html
<head>
    <script src="path/to/the/file.js" defer></script>
</head>
```
- Dins un element `<script>`. Normalment, es situarà just abans de tancar l'etiqueta `<body>`:
```html
<body>
    <!--Més codi HTML-->
    <script>
        window.alert("Hola mami");
    </script>
</body>
```
- Dins una etiqueta html, per controlar esdeveniments. Com ara `onclick`:
```html
<body>
    <h1 onmouseover="this.style.color='orange'" onmouseout="this.style.color='black'">Passa el punter per aquí</h1>
</body>
```

## Exemple

Aquí un exemple on el navegador, en carregar el document web, obté dades d'un servei extern, i davant d'un esdeveniment concret, realitza un càlcul per mostrar una dada, modificant el contingut del document:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Async/Await Exchange Rate</title>
</head>
<body>
    <!-- Alguns elements html -->
    <p>Taxa de conversió actual (USD a EUR): <span id="rate">Carregant...</span></p>
    <p><input type="number" value="0" style="text-align: right;" id="dollars"> $ equival a <span id="euros">0 </span>€</p>

    <!--El codi JavaScript-->
    <script>
        /* Recuperem els elements que interessen del document.*/
        const rateSpan = document.getElementById("rate");
        const dollarsInput = document.getElementById("dollars");
        const eurosSpan = document.getElementById("euros");
        /* Declarem una variable que desarà el valor que ens interessa.*/
        let rate = 0;

        /*Una funció que demana i obté dades, en aquest cas per convertir un factor de conversió que pot ser diferent cada dia*/
        function getExchangeRate() {
            fetch("https://api.frankfurter.app/latest?from=USD&to=EUR")
                .then(response => response.json())
                .then(data => {
                    rate = data.rates.EUR;
                    rateSpan.innerText = rate;
                })
                .catch(error => {
                    rateSpan.innerText = "Error obtenint dades";
                })
        }

        /* Cridem la funció.*/
        getExchangeRate();

        /* Programem un event.*/
        dollarsInput.onchange = (event => {
            eurosSpan.innerText = (dollarsInput.value * rate).toFixed(2);
            console.log(event.srcElement.value);
        });
            
    </script>
</body>
</html>
```

Com pots veure, JavaScript es fa servir tant per enviar i rebre dades, com per modificar elements de la pàgina web de forma dinàmica.
# JavaScriptin Johdanto
Tervetuloa JavaScriptin maailmaan! Tämä luku esittelee JavaScript-ohjelmointikielen perusteet, sen käyttökohteet ja miten voit aloittaa koodauksen. Käymme läpi JavaScriptin historiaa, käyttötarkoituksia ja ensimmäisiä ohjelmointikokeiluja.

<br>

## Mikä on JavaScript?

JavaScript (JS) on yksi maailman suosituimmista ohjelmointikielistä, ja se toimii lähes jokaisella verkkosivulla. Se on dynaaminen ja monipuolinen kieli, joka mahdollistaa verkkosivujen toiminnallisuuden, kuten:

✅ Interaktiiviset elementit (napit, valikot, animaatiot)  
✅ Lomakkeiden validointi (esimerkiksi sähköpostiosoitteen tarkistus)  
✅ Datan käsittely ja tallennus  
✅ Verkkosovellukset ja pelit  

<br>

## JavaScriptin rooli web-kehityksessä


JavaScript on yksi kolmesta keskeisestä teknologiasta web-kehityksessä:

HTML (HyperText Markup Language) – Verkkosivun rakenne  
CSS (Cascading Style Sheets) – Sivun ulkoasu ja tyylit  
JavaScript – Toiminnallisuus ja interaktiivisuus  

Yhdessä nämä kolme muodostavat perinteisen verkkosivun perustan.

<br>

## JavaScriptin historia

JavaScript kehitettiin vuonna 1995 Netscape-yhtiössä Brendan Eichin toimesta. Se suunniteltiin alun perin verkkosivujen skriptauskieleksi, mutta nykyään sitä käytetään laajasti eri ympäristöissä, kuten palvelinpuolella (Node.js) ja mobiilisovelluksissa (React Native).

  ---
<br>

# JavaScriptin suorittaminen
JavaScriptiä voidaan ajaa eri ympäristöissä. Yleisimpiä tapoja suorittaa JavaScript-koodia ovat:

Selainkonsoli – JavaScriptin ajaminen suoraan selaimessa  
HTML-tiedoston <script>-elementti – JavaScript koodataan suoraan verkkosivulle  
Ulkoinen JavaScript-tiedosto (.js) – Koodi tallennetaan erilliseen tiedostoon ja liitetään verkkosivuun  
Node.js-palvelinympäristö – JavaScriptiä voidaan käyttää myös verkkopalvelinten ohjelmointiin  



## JavaScriptin ajaminen selainkonsolissa
JavaScriptiä voidaan suorittaa suoraan verkkoselaimen kehittäjätyökaluissa. Voit avata konsolin seuraavasti:

Paina F12 tai Ctrl + Shift + J

Kirjoita konsoliin seuraava komento ja paina Enter:

```js
console.log("Hei maailma!");
```
Tämän komennon pitäisi tulostaa "Hei maailma!" selaimen konsoliin.



## JavaScriptin lisääminen HTML-tiedostoon

Voit lisätä JavaScriptin verkkosivulle HTML-tiedostossa käyttäen <script>-elementtiä:

```html
<!DOCTYPE html>
<html lang="fi">
<head>
    <meta charset="UTF-8">
    <title>Ensimmäinen JavaScript</title>
</head>
<body>
    <h1>Tervetuloa JavaScriptiin!</h1>
    <script>
        alert("JavaScript toimii!");
    </script>
</body>
</html>
```

Kun sivu avataan selaimessa, JavaScript näyttää ponnahdusikkunan, jossa lukee "JavaScript toimii!".



## Ulkoinen JavaScript-tiedosto (.js)

On suositeltavaa kirjoittaa JavaScript erilliseen tiedostoon, jolloin koodi on helpompi ylläpitää ja uudelleenkäyttää. Ulkoinen tiedosto voidaan määrittää HTML:n <script>-elementissä

📄 HTML-tiedosto (index.html):
```html
<!DOCTYPE html>
<html lang="fi">
<head>
    <meta charset="UTF-8">
    <title>JavaScript-tiedosto</title>
    <script src="script.js"></script>  
</head>
<body>
    <h1>JavaScript ladattu ulkoisesta tiedostosta</h1>
</body>
</html>
```
📄 JavaScript-tiedosto (script.js):

```js
console.log("JavaScript ladattu erillisestä tiedostosta!");
```
Nyt selain suorittaa script.js-tiedoston komennot HTML-sivun latautuessa.

---



# JavaScriptin ensimmäiset komennot
Seuraavaksi opimme ensimmäisiä komentoja, joilla voimme tulostaa tietoa ja tehdä yksinkertaisia vuorovaikutuksia käyttäjän kanssa.



### console.log() – Tulostaminen konsoliin  
console.log()-komennolla voimme tulostaa viestejä konsoliin:

```js
console.log("Tämä on ensimmäinen JavaScript-komentoni!");
```



### alert() – Ponnahdusikkunan näyttäminen  
alert() näyttää yksinkertaisen ilmoitusikkunan:

```js
alert("Tämä on JavaScriptin alert!");
```



### prompt() – Käyttäjän syötteen kysyminen  
prompt() kysyy käyttäjältä tietoa ja tallentaa sen muuttujaan:

```js
let nimi = prompt("Mikä on nimesi?");
console.log("Hei, " + nimi + "!");
```



### confirm() – Käyttäjän valinnan varmistaminen  
confirm() näyttää ponnahdusikkunan, jossa käyttäjä voi valita OK tai Peruuta:

```js
let vastaus = confirm("Haluatko jatkaa?");
console.log("Käyttäjän vastaus: " + vastaus);
```

<br>

# Muuttujat ja tietotyypit

Kun alamme kirjoittaa JavaScript-koodia, meidän täytyy pystyä tallentamaan ja käsittelemään tietoa. Tässä luvussa opimme, kuinka JavaScript käsittelee muuttujia ja millaisia tietotyyppejä kielessä on.

  
## Mitä ovat muuttujat (variables)?

Muuttuja on säiliö, johon voidaan tallentaa tietoa. Kun ohjelma suoritetaan, se voi tallentaa tietoa muuttujaan ja käyttää sitä myöhemmin.

JavaScriptissä muuttujia voidaan luoda kolmella eri avainsanalla:

var (vanhentunut, mutta edelleen käytössä)  
let (suositeltu tapa muuttujien luomiseen)  
const (vakio, jonka arvoa ei voi muuttaa)  

### Esimerkki muuttujan luomisesta:

```js
let nimi = "Anna";
console.log(nimi); // Tulostaa: Anna
```

### Esimerkki muuttujan arvon muuttamisesta:

```js
let ikä = 25;
ikä = 26;
console.log(ikä); // Tulostaa: 26
```

###Vakion (const) käyttö:

```js
const syntymavuosi = 1995;
console.log(syntymavuosi); // Tulostaa: 1995
```
> [!Caution]
> Koska const-muuttujia ei voi muuttaa, seuraava rivi aiheuttaisi virheen:
``` js
syntymavuosi = 2000; // Tämä ei ole sallittua!
```

Jos haluat tietää tarkemmin näiden muuttujien eroista voit lukea lisää [täältä]([url](https://www.freecodecamp.org/news/var-let-and-const-whats-the-difference/))


## Tietotyypit JavaScriptissä

JavaScript tukee useita eri tietotyyppejä, jotka voidaan jakaa kahteen pääryhmään:

Perustietotyypit (Primitive types)  
Oliopohjaiset tietotyypit (Reference types)  

### Perustietotyypit

Perustietotyypit ovat yksinkertaisia arvoja, joita ei voi jakaa pienempiin osiin.

### string – Merkkijonot
 
#### Mikä on merkkijono?

Merkkijono (string) on tekstimuotoinen tieto, joka on kirjoitettu lainausmerkkeihin:

```js
let teksti1 = "Tämä on merkkijono";
let teksti2 = 'Myös tämä on merkkijono';
let teksti3 = `Tämäkin on merkkijono`;
```

Voimme käyttää joko yksinkertaisia ('), kaksoislainausmerkkejä ("), tai takakysymysmerkkejä ( `, template literals).

#### Merkkijonojen yhdistäminen (concatenation)
```js
let etunimi = "Anna";
let sukunimi = "Virtanen";

let kokoNimi = etunimi + " " + sukunimi;
console.log(kokoNimi); // "Anna Virtanen"
```

#### Template literals (${} sisällä backtick-merkeillä)
```js
let ika = 25;
let tervehdys = `Hei, olen ${etunimi} ja olen ${ika} vuotta vanha.`;
console.log(tervehdys);
```

#### Merkkijonojen muokkaaminen

JavaScript tarjoaa useita funktioita merkkijonojen käsittelyyn:


```js
let lause = "JavaScript on hauskaa!";
console.log(lause.length); // Pituus: 22
console.log(lause.toUpperCase()); // "JAVASCRIPT ON HAUSKAA!"
console.log(lause.toLowerCase()); // "javascript on hauskaa!"
console.log(lause.replace("hauskaa", "mahtavaa")); // "JavaScript on mahtavaa!"
console.log(lause.includes("Java")); // true
```

### number – Numerot
JavaScriptissä on vain yksi numerotyyppi, joka sisältää sekä kokonaisluvut että desimaalit:

```js
let kokonaisluku = 42;
let desimaaliluku = 3.14;
```

#### Laskutoimitukset numeroilla

Voimme käyttää JavaScriptin matemaattisia operaattoreita:

```js
let a = 10;
let b = 3;

console.log(a + b); // 13
console.log(a - b); // 7
console.log(a * b); // 30
console.log(a / b); // 3.3333...
console.log(a % b); // 1 (jakojäännös)
console.log(a ** b); // 1000 (10^3)
```

#### Numerot merkkijonoina ja niiden muuntaminen

Joskus numerot ovat merkkijonoina ja ne täytyy muuntaa:

```js
let tekstiNumero = "42";
let oikeaNumero = Number(tekstiNumero);

console.log(oikeaNumero + 1); // 43
console.log(typeof oikeaNumero); // "number"
```

Vastaavasti voimme muuntaa numeron merkkijonoksi:

```
let numero = 25;
let tekstina = String(numero);
console.log(tekstina); // "25"
console.log(typeof tekstina); // "string"
```

### boolean – Totuusarvot

Boolean-arvot voivat olla vain kaksi mahdollista vaihtoehtoa:  
✅ true (tosi)   
❌ false (epätosi)  

```js
let onAikuinen = true;
let sataa = false;
```
#### Boolean-arvojen käyttäminen if-lauseessa

```js
let ikä = 18;

if (ikä >= 18) {
    console.log("Olet täysi-ikäinen.");
} else {
    console.log("Olet alaikäinen.");
}
````

#### Boolean-arvon luominen vertaamalla

```js
let x = 10;
let y = 5;

console.log(x > y); // true
console.log(x < y); // false
console.log(x === 10); // true
console.log(y !== 10); // true
```

### undefined – Määrittelemätön arvo

Jos muuttujaa ei ole annettu arvoa, sen arvo on undefined:

```js
let tuntematon;
console.log(tuntematon); // undefined
```

undefined voi myös syntyä, jos yritämme käyttää muuttujaa, jota ei ole olemassa:

```js
console.log(eiOleOlemassa); // Virhe: eiOleOlemassa is not defined
```

### null – Tyhjä arvo

null tarkoittaa tarkoituksella asetettua tyhjää arvoa:

```js
let tieto = null;
console.log(tieto); // null
```

Toisin kuin undefined, null tarkoittaa, että arvo on tyhjennetty tietoisesti.



## Oliopohjaiset tietotyypit


JavaScriptissä on perustietotyyppien lisäksi myös oliopohjaisia tietotyyppejä (reference types). Oliopohjaiset tietotyypit säilyttävät viitteen arvoihinsa eivätkä itse arvoa, toisin kuin perustietotyypit. Tämä tarkoittaa, että jos kopioimme olion, molemmat muuttujat viittaavat samaan muistipaikkaan.

Tärkeimmät oliopohjaiset tietotyypit ovat:

Oliot (object)  
Taulukot (array)  
Funktiot (function)  
Päivämäärät (Date)  
Kartta (Map) ja joukko (Set) 


### Mitä ovat oliot (objects)?

Olio (object) on avain-arvopareja sisältävä tietorakenne. Se muistuttaa taulukkoa, mutta tiedot tallennetaan nimettyihin avaimiin eikä indeksinumeroihin.

#### Olion luominen
Olio voidaan luoda kahdella tavalla:

Olion määrittely käyttämällä {}-merkintää (objektiliteraali):

```js
let henkilo = {
    etunimi: "Anna",
    sukunimi: "Virtanen",
    ika: 25,
    onOpiskelija: true
};

console.log(henkilo); // Tulostaa koko olion
console.log(henkilo.etunimi); // "Anna"
console.log(henkilo["sukunimi"]); // "Virtanen"
```

Olion luominen new Object()-syntaksilla (harvemmin käytetty tapa):

```js
let auto = new Object();
auto.merkki = "Toyota";
auto.malli = "Corolla";
auto.vuosi = 2020;

console.log(auto.merkki); // "Toyota"
```

#### Olion arvojen muuttaminen

Voimme muuttaa olion ominaisuuksia näin:

```js
henkilo.ika = 26;
console.log(henkilo.ika); // 26
```

Tai voimme lisätä uusia ominaisuuksia:

```js
henkilo.kaupunki = "Helsinki";
console.log(henkilo.kaupunki); // "Helsinki"
```

#### Olion sisällä olevat funktiot (methods)
Olion sisälle voidaan lisätä funktioita (funktioista lisää alempana):

```js
let koira = {
    nimi: "Rekku",
    rotu: "Labradori",
    hauku: function () {
        console.log("Hau hau!");
    }
};

koira.hauku(); // "Hau hau!"
```

### Taulukot (arrays)

JavaScriptin taulukot (arrays) ovat kokoelmia, jotka voivat sisältää useita arvoja.

#### Taulukon luominen

```js
let hedelmat = ["omena", "banaani", "päärynä"];
console.log(hedelmat[0]); // "omena"
console.log(hedelmat.length); // 3
```

#### Taulukon muokkaaminen

```js
hedelmat.push("appelsiini"); // Lisää uuden arvon loppuun
console.log(hedelmat); // ["omena", "banaani", "päärynä", "appelsiini"]

hedelmat.pop(); // Poistaa viimeisen alkion
console.log(hedelmat); // ["omena", "banaani", "päärynä"]
```

```
hedelmat.unshift("mango"); // Lisää alkuun
console.log(hedelmat); // ["mango", "omena", "banaani", "päärynä"]

hedelmat.shift(); // Poistaa ensimmäisen alkion
console.log(hedelmat); // ["omena", "banaani", "päärynä"]
```

#### Taulukon läpikäynti (forEach)

Taulukon läpikäynnistä sekä yleisesti loopeista lisää alempana.
```js
hedelmat.forEach(function(hedelma) {
    console.log(hedelma);
});
```

### Funktiot (functions)
Funktiot ovat olioita, joita voidaan käyttää uudelleenkäytettävinä koodilohkoina.

```js
function tervehdys(nimi) {
    return `Hei, ${nimi}!`;
}

function yhteenlasku(x, y) {
    let summa = x + y;
    return summa
}

console.log(tervehdys("Anna")); // "Hei, Anna!"
console.log()
```

Voimme myös tallentaa funktiot muuttujaan:

```js
let tervehdys = function(nimi) {
    return `Hei, ${nimi}!`;
};

console.log(tervehdys("Matti"));
```

### Päivämäärät (Date)

JavaScriptin Date-olio mahdollistaa päivämäärien ja aikojen käsittelyn.

```js
let nyt = new Date();
console.log(nyt); // Tulostaa nykyisen päivämäärän ja ajan
```

Voimme myös asettaa tietyn päivämäärän:

```js
let joulu = new Date(2024, 11, 24);
console.log(joulu);
```


### Mikä on Kartta - Map?
Map on avain-arvoparien kokoelma, jossa avain voi olla mitä tahansa – ei vain merkkijonoja kuten object-olioissa.  
Map säilyttää avainten järjestyksen, toisin kuin object, jossa avainten järjestys voi muuttua.  
Map on optimoitu dynaamiseen tietojen käsittelyyn, joten se voi olla nopeampi kuin object suurilla tietomäärillä.  

```js
let kartta = new Map();
kartta.set("nimi", "Anna");
kartta.set("ikä", 25);

console.log(kartta.get("nimi")); // "Anna"
```
### Set – Uniikkien arvojen kokoelma

Set on kuin array, mutta ei salli samoja arvoja useaan kertaan.
```js
let joukko = new Set([1, 2, 3, 3, 4]);
console.log(joukko); // {1, 2, 3, 4}
```




## Säännöt muuttujien nimeämiselle

✅ Sallitut muuttujanimet:

```js
let etunimi = "Anna"; 
let _salasana = "salainen";
let $raha = 100;
```

❌ Virheelliset muuttujanimet:

```js
let 2nro = 10;  // Ei voi alkaa numerolla
let nimi sukunimi = "Anna Virtanen"; // Ei voi sisältää välilyöntejä
let let = "varattu"; // Ei voi käyttää varattuja avainsanoja
```

### CamelCase-nimeämistyyli
Yleisesti JavaScriptissä käytetään camelCase-tyyliä muuttujien ja funktioiden nimissä:

```js
let omaNimi = "Anna";
let ensimmainenKerta = true;

function helloWorld(){
    console.log("Hello World!")
}
```

### Tyyppimuunnokset
JavaScriptissä muuttujan tietotyyppi voi muuttua dynaamisesti.

📌 Automaattinen tyyppimuunnos:
```js
let numero = "5" + 2; // Merkkijonon ja numeron yhdistäminen
console.log(numero); // Tulostaa: "52"
```

📌 Pakotettu tyyppimuunnos:

```js
let luku = "10";
let oikeaLuku = Number(luku);
console.log(oikeaLuku); // Tulostaa: 10 (lukuna)
```
<br>

---

# Ehtolauseet

Ehtolauseet ovat yksi ohjelmoinnin peruspilareista. Niiden avulla voimme tehdä päätöksiä ohjelmassamme – eli suorittaa tiettyä koodia vain, jos jokin ehto täyttyy.

## If-lause (perusehto)
if-lauseella voidaan suorittaa koodia vain, jos ehto on tosi (true).

Syntaksi:
```js
if (ehto) {
    // Tämä koodi suoritetaan vain, jos ehto on tosi
}
```
Esimerkki:

```js
let ikä = 18;

if (ikä >= 18) {
    console.log("Olet täysi-ikäinen!");
}
// "Olet täysi-ikäinen!"
```
Jos ikä olisi esimerkiksi 17, lauseen sisällä oleva console.log() ei suoritettaisi.


## If...else -lause (muutoin tapaus)
else-lohkolla voidaan määritellä, mitä tapahtuu, jos ehto ei täyty.

Syntaksi:
```js
if (ehto) {
    // Suoritetaan, jos ehto on tosi
} else {
    // Suoritetaan, jos ehto on epätosi (false)
}
```

Esimerkki:

```js
let ikä = 16;

if (ikä >= 18) {
    console.log("Olet täysi-ikäinen!");
} else {
    console.log("Et ole vielä täysi-ikäinen.");
}
// "Et ole vielä täysi-ikäinen."
```
## If...else if...else -lause (useita ehtoja)

Jos haluamme tarkistaa useita erilaisia ehtoja, voimme käyttää else if -rakennetta.

Syntaksi:
```js
if (ehto1) {
    // Suoritetaan, jos ehto1 on tosi
} else if (ehto2) {
    // Suoritetaan, jos ehto1 on epätosi mutta ehto2 on tosi
} else {
    // Suoritetaan, jos mikään ehto ei ollut tosi
}
```
Esimerkki:
```js
let pisteet = 75;

if (pisteet >= 90) {
    console.log("Arvosana: 5");
} else if (pisteet >= 75) {
    console.log("Arvosana: 4");
} else if (pisteet >= 60) {
    console.log("Arvosana: 3");
} else {
    console.log("Hylätty");
}
// "Arvosana: 4"
```
else if -rakennetta voi olla niin monta kuin halutaan, mutta koodi suorittaa vain ensimmäisen toden lauseen.

## Switch-lause (vaihtoehtojen tarkistus)
switch on toinen tapa käsitellä useita mahdollisia arvoja. Se on erityisen hyödyllinen, kun vertaillaan muuttujan arvoa useisiin ennalta määriteltyihin vaihtoehtoihin.

Syntaksi:

```js
switch (arvo) {
    case vaihtoehto1:
        // Suorita tämä koodi
        break;
    case vaihtoehto2:
        // Suorita tämä koodi
        break;
    default:
        // Suorita tämä koodi, jos mikään vaihtoehto ei täsmää
}
```

Esimerkki:

```js
let viikonpäivä = 3;

switch (viikonpäivä) {
    case 1:
        console.log("Maanantai");
        break;
    case 2:
        console.log("Tiistai");
        break;
    case 3:
        console.log("Keskiviikko");
        break;
    case 4:
        console.log("Torstai");
        break;
    case 5:
        console.log("Perjantai");
        break;
    default:
        console.log("Viikonloppu!");
}
// "Keskiviikko"
```
break-lauseen avulla estetään koodin jatkuminen seuraaviin case-kohtiin.

## Ternary Operator (Lyhyt ehtolause ? :)
Ternäärinen operaattori on lyhyempi tapa kirjoittaa yksinkertainen if...else-lause.

Syntaksi:
```js
ehto ? josTosi : josEpätosi;
```

Esimerkki:

```js
let ikä = 20;
let viesti = ikä >= 18 ? "Saat äänestää" : "Et saa äänestää";
console.log(viesti);
// "Saat äänestää"
```

## Loogiset operaattorit ehtolauseissa

Ehtolauseissa käytetään usein loogisia operaattoreita, joilla voidaan yhdistää ehtoja:


&& (AND) Molempien ehtojen on oltava tosi  
|| (OR) Jomman kumman ehdon on oltava tosi  
! (NOT) Kääntää arvon toisin päin  

Esimerkki AND (&&)

```js
let ikä = 20;
let jäsen = true;

if (ikä >= 18 && jäsen) {
    console.log("Pääset jäsenalueelle!");
} else {
    console.log("Et voi liittyä.");
}
// "Pääset jäsenalueelle!"
```

Esimerkki OR (||)
```js
let opiskelija = true;
let eläkeläinen = false;

if (opiskelija || eläkeläinen) {
    console.log("Saat alennuksen!");
} else {
    console.log("Et saa alennusta.");
}
// "Saat alennuksen!"
```

Esimerkki NOT (!)
```js
let onKirjautunut = false;

if (!onKirjautunut) {
    console.log("Ole hyvä ja kirjaudu sisään.");
}
// "Ole hyvä ja kirjaudu sisään."
```

---

# Silmukat (Loops)
Silmukat ovat ohjelmoinnin tärkeimpiä rakenteita. Niiden avulla voimme toistaa tiettyä koodia useita kertoja ilman, että meidän täytyy kirjoittaa sitä manuaalisesti uudelleen.

## for-silmukka (tietty määrä toistoja)
for-silmukka on yksi yleisimmistä silmukoista. Se sopii erityisesti, kun tiedämme etukäteen kuinka monta kertaa silmukan tulisi toistua.

Syntaksi:
```js
for (aloitus; ehto; päivitys) {
    // Suoritetaan jokaisella kierroksella
}
```
aloitus: Määrittää muuttujan, joka toimii laskurina  
ehto: Silmukka jatkuu niin kauan kuin ehto on tosi  
päivitys: Päivittää laskurin jokaisen kierroksen jälkeen  

Esimerkki:

```js
for (let i = 0; i < 5; i++) {
    console.log("Kierros:", i);
}
// Tulostaa: 
// Kierros: 0
// Kierros: 1
// Kierros: 2
// Kierros: 3
// Kierros: 4
```

## while-silmukka (toistetaan, kunnes ehto muuttuu epätodeksi)  
while-silmukka toistaa koodia niin kauan kuin annettu ehto on tosi.

Syntaksi:
```js
while (ehto) {
    // Suoritetaan niin kauan kuin ehto on tosi
}
```

Esimerkki:
```js
let numero = 0;

while (numero < 5) {
    console.log("Numero:", numero);
    numero++;
}
```
Tässä silmukka jatkaa toistoa, kunnes numero muuttuja saavuttaa arvon 5.


## do...while-silmukka (vähintään yksi suoritus)  
do...while-silmukka toimii kuten while, mutta se suoritetaan ainakin kerran, vaikka ehto ei olisikaan alun perin tosi.

Syntaksi:

```js
do {
    // Suoritetaan vähintään kerran
} while (ehto);
```

Esimerkki:

```js
let luku = 10;

do {
    console.log("Luku:", luku);
    luku++;
} while (luku < 5);
```
Vaikka luku on aluksi jo 10, silmukka suoritetaan kerran, koska ehto tarkistetaan vasta ensimmäisen suorituksen jälkeen.

## for...in-silmukka (oliot ja avaimet)  
for...in-silmukkaa käytetään olioiden (objects) avainten (keys) läpikäyntiin.

Syntaksi:

```
for (let avain in olio) {
    // Suoritetaan jokaiselle avaimelle
}
```

Esimerkki:

```js
let opiskelija = {
    nimi: "Matti",
    ikä: 22,
    koulu: "Aalto-yliopisto"
};

for (let avain in opiskelija) {
    console.log(avain + ": " + opiskelija[avain]);
}
// Tulostaa:
// nimi: Matti
// ikä: 22
// koulu: Aalto-yliopisto
```
> [!Caution]
> Huom! Älä käytä for...in-silmukkaa taulukoiden (array) läpikäyntiin, koska se saattaa palauttaa myös perittyjä ominaisuuksia.


## for...of-silmukka (iteraattorit, kuten taulukot)  
for...of on tarkoitettu iteraattorien (arrays, maps, sets) läpikäyntiin.

Syntaksi:

```js
for (let arvo of kokoelma) {
    // Suoritetaan jokaiselle arvolle
}
```

Esimerkki taulukolla (array)

```js
let nimet = ["Anna", "Matti", "Laura"];

for (let nimi of nimet) {
    console.log(nimi);
}
// Tulostaa:
// Anna
// Matti
// Laura
```

Esimerkki Map-olion kanssa

```js
let kurssit = new Map([
    ["Matematiikka", "Prof. Virtanen"],
    ["Fysiikka", "Dr. Korhonen"]
]);

for (let [aine, opettaja] of kurssit) {
    console.log(`${aine} - ${opettaja}`);
}
// Matematiikka - Prof. Virtanen
// Fysiikka - Dr. Korhonen
```

## Silmukoiden hallinta (break ja continue)

### break – keskeyttää silmukan  
break-lauseella voidaan lopettaa silmukka ennenaikaisesti.

```js
for (let i = 0; i < 10; i++) {
    if (i === 5) {
        break; // Silmukka päättyy, kun i on 5
    }
    console.log(i);
}
// Tulostaa: 0, 1, 2, 3, 4
```

### continue – hyppää yli yhden kierroksen   
continue ohittaa nykyisen silmukkakierroksen ja jatkaa seuraavaan.

```js
for (let i = 0; i < 5; i++) {
    if (i === 2) {
        continue; // Ohittaa kierroksen, kun i on 2
    }
    console.log(i);
}
// Tulostaa: 0, 1, 3, 4
```

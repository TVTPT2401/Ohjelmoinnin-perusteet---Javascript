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

3.2 string – Merkkijonot
3.2.1 Mikä on merkkijono?
Merkkijono (string) on tekstimuotoinen tieto, joka on kirjoitettu lainausmerkkeihin:

js
Copy
Edit
let teksti1 = "Tämä on merkkijono";
let teksti2 = 'Myös tämä on merkkijono';
let teksti3 = `Tämäkin on merkkijono`;
Voimme käyttää joko yksinkertaisia ('), kaksoislainausmerkkejä ("), tai takakysymysmerkkejä ( `, template literals).

3.2.2 Merkkijonojen yhdistäminen (concatenation)
js
Copy
Edit
let etunimi = "Anna";
let sukunimi = "Virtanen";

let kokoNimi = etunimi + " " + sukunimi;
console.log(kokoNimi); // "Anna Virtanen"
3.2.3 Template literals (${} sisällä backtick-merkeillä)
js
Copy
Edit
let ika = 25;
let tervehdys = `Hei, olen ${etunimi} ja olen ${ika} vuotta vanha.`;
console.log(tervehdys);
3.2.4 Merkkijonojen muokkaaminen
JavaScript tarjoaa useita funktioita merkkijonojen käsittelyyn:

js
Copy
Edit
let lause = "JavaScript on hauskaa!";
console.log(lause.length); // Pituus: 22
console.log(lause.toUpperCase()); // "JAVASCRIPT ON HAUSKAA!"
console.log(lause.toLowerCase()); // "javascript on hauskaa!"
console.log(lause.replace("hauskaa", "mahtavaa")); // "JavaScript on mahtavaa!"
console.log(lause.includes("Java")); // true
3.3 number – Numerot
JavaScriptissä on vain yksi numerotyyppi, joka sisältää sekä kokonaisluvut että desimaalit:

js
Copy
Edit
let kokonaisluku = 42;
let desimaaliluku = 3.14;
3.3.1 Laskutoimitukset numeroilla
Voimme käyttää JavaScriptin matemaattisia operaattoreita:

js
Copy
Edit
let a = 10;
let b = 3;

console.log(a + b); // 13
console.log(a - b); // 7
console.log(a * b); // 30
console.log(a / b); // 3.3333...
console.log(a % b); // 1 (jakojäännös)
console.log(a ** b); // 1000 (10^3)
3.3.2 Numerot merkkijonoina ja niiden muuntaminen
Joskus numerot ovat merkkijonoina ja ne täytyy muuntaa:

js
Copy
Edit
let tekstiNumero = "42";
let oikeaNumero = Number(tekstiNumero);

console.log(oikeaNumero + 1); // 43
console.log(typeof oikeaNumero); // "number"
Vastaavasti voimme muuntaa numeron merkkijonoksi:

js
Copy
Edit
let numero = 25;
let tekstina = String(numero);
console.log(tekstina); // "25"
console.log(typeof tekstina); // "string"
3.4 boolean – Totuusarvot
Boolean-arvot voivat olla vain kaksi mahdollista vaihtoehtoa:
✅ true (tosi)
❌ false (epätosi)

js
Copy
Edit
let onAikuinen = true;
let sataa = false;
3.4.1 Boolean-arvojen käyttäminen if-lauseessa
js
Copy
Edit
let ikä = 18;

if (ikä >= 18) {
    console.log("Olet täysi-ikäinen.");
} else {
    console.log("Olet alaikäinen.");
}
3.4.2 Boolean-arvon luominen vertaamalla
js
Copy
Edit
let x = 10;
let y = 5;

console.log(x > y); // true
console.log(x < y); // false
console.log(x === 10); // true
console.log(y !== 10); // true
3.5 undefined – Määrittelemätön arvo
Jos muuttujaa ei ole annettu arvoa, sen arvo on undefined:

js
Copy
Edit
let tuntematon;
console.log(tuntematon); // undefined
undefined voi myös syntyä, jos yritämme käyttää muuttujaa, jota ei ole olemassa:

js
Copy
Edit
console.log(eiOleOlemassa); // Virhe: eiOleOlemassa is not defined
3.6 null – Tyhjä arvo
null tarkoittaa tarkoituksella asetettua tyhjää arvoa:

js
Copy
Edit
let tieto = null;
console.log(tieto); // null
Toisin kuin undefined, null tarkoittaa, että arvo on tyhjennetty tietoisesti.









string	Merkkijono (teksti)	"Hei maailma!"
number	Luku (kokonaisluvut ja desimaalit)	42, 3.14
boolean	Totuusarvo (true tai false)	true, false
undefined	Muuttuja, jolle ei ole annettu arvoa	let x;
null	Tyhjä arvo	let y = null;
📌 Esimerkkejä perustietotyypeistä:

js
Copy
Edit
let teksti = "Tämä on merkkijono";
let numero = 2024;
let totuus = true;
let eiMaaritetty;
let tyhjaArvo = null;

console.log(teksti, numero, totuus, eiMaaritetty, tyhjaArvo);
2.2.2 Oliopohjaiset tietotyypit
Oliopohjaiset tietotyypit sisältävät tietoa rakenteellisessa muodossa. Näitä ovat esimerkiksi taulukot (arrays) ja oliot (objects).

Tietotyyppi	Kuvaus	Esimerkki
object	Monimutkaisempi tietorakenne, jossa on avain-arvopareja	{ nimi: "Anna", ikä: 25 }
array	Lista arvoja, joita voidaan käsitellä yhdessä	["omena", "banaani", "päärynä"]
📌 Esimerkkejä oliopohjaisista tietotyypeistä:

js
Copy
Edit
// Objekti (tietorakenne, jossa on avain-arvopareja)
let henkilo = {
    nimi: "Anna",
    ika: 25
};
console.log(henkilo.nimi); // Tulostaa: Anna

// Taulukko (lista arvoja)
let hedelmat = ["omena", "banaani", "päärynä"];
console.log(hedelmat[0]); // Tulostaa: omena
2.3 Muuttujien käyttö ja muuttujanimien säännöt
JavaScriptissä muuttujien nimet voivat sisältää kirjaimia, numeroita, alaviivoja (_) ja dollarimerkkejä ($).

2.3.1 Säännöt muuttujien nimeämiselle
✅ Sallitut muuttujanimet:

js
Copy
Edit
let etunimi = "Anna"; 
let _salasana = "salainen";
let $raha = 100;
❌ Virheelliset muuttujanimet:

js
Copy
Edit
let 2nro = 10;  // Ei voi alkaa numerolla
let nimi sukunimi = "Anna Virtanen"; // Ei voi sisältää välilyöntejä
let let = "varattu"; // Ei voi käyttää varattuja avainsanoja
2.3.2 CamelCase-nimeämistyyli
Yleisesti JavaScriptissä käytetään camelCase-tyyliä muuttujien nimissä:

js
Copy
Edit
let omaNimi = "Anna";
let ensimmainenKerta = true;
2.4 Tyyppimuunnokset
JavaScriptissä muuttujan tietotyyppi voi muuttua dynaamisesti.

📌 Automaattinen tyyppimuunnos:

js
Copy
Edit
let numero = "5" + 2; // Merkkijonon ja numeron yhdistäminen
console.log(numero); // Tulostaa: "52"
📌 Pakotettu tyyppimuunnos:

js
Copy
Edit
let luku = "10";
let oikeaLuku = Number(luku);
console.log(oikeaLuku); // Tulostaa: 10 (lukuna)

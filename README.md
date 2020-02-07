# js-bootcamp

## Notities JS bootcamp:


### 1. Browser & client
De browser voert JS uit, je hebt dus een browser nodig.
De browser is hier dus de client. Bestanden staan op een server. (Server met back-end)
Front-End: Client, JS
Back-End: Server, JS, met Node.js zodat je het zonder browser kunt uitvoeren


### 2. ECMAscript
Overkoepelende naam van alle JS versies.
Afkorting: ES, wij gaan werken met ES6, en ze zijn backwards compatible.


### 3. Values & Types
In totaal zijn er 7 datatypes (string, boolean, null, number, undefined enz).
null en undefined zijn aparte datatypes, vaak bij errors.
JS corrigeert vaak strings en nummers, zoals var cijfer = '4'-3;.
var wordt vervangen door let en const.
var: creëert eigen scope, handig voor functies??
const: consistent, kan je niet overwriten maar wel gebruiken. Als je een waarde sws niet gaat veranderen.
let: scope is blob-scope, dus als je het moet oproepen moet het in dezelfde scope staan.
Wanneer je "14"+1 doet word er "141" gereturnd, let hier op. (inplicit type coercion, type = hetzelfde)
Je kan wel 1+number(14) doen, dan is het 15. (explicit type coercion, type = verschillend)
Null: deze waarde geef je iets wanneer de waarde nog niet bekend is, is zelf in te voeren.
Undef.: wanneer er geen waarde is gegeven aan een variebele, maar wel wordt opgeroepen.


### 4. Functions
function sum(a, b) {
	return a + b;
}
console.log(sum(1, 3));
//4
Invoken, apply en calling is het aanroepen van een functie.
Functies altijd laten zien in de console met console.log.
Argumenten geef je mee wanneer je de functie aanroept.
Parameters define je wanneer je een functie aanmaakt.
Conditional: If, else if , else. Wanneer iets, dan...
==: gebruiken wanneer iets hetzelfde moet zijn, ===: wanneer het ook hetzelfde datatype moet zijn.


### 5. Loops
for (var index = 0; index < 10; index++){
	console.log(index);
}
//er komt in de console 1 tot 9
Code in het blok wordt telkens opnieuw uitgevoerd wanneer de condities nog geldig zijn.
In het voorbeeld word dus eerst 0 gelogd, en dan is 0<10 dus word 1 gelogd, enz.


### 6. Flow
Creation/compile phase: Alle functies en var worden gelezen en opgeslagen in geheugen. Van boven naar beneden.
Runtime phase: Lezen van functies en var wanneer deze worden opgeroepen.


### 7. Object
var object = {
	[key]: value,
	[key]: 'value'
}
Objecten kun je meerdere keys met waardes geven, let wel op de komma tussen de keys.
Objecten worden vaak gebruikt om je code op te schonen en overzichtelijker te maken.
object.[key]: Het aanroepen van 1 key in het object doe je met een punt.


### 8. Array
var array = ["data", 14, true, "meer data];
Wanneer je een array oproept moet je uitkijken, want hij ziet het namelijk als een string.
Met array.length kun je achterhalen hoeveel items er in een array zitten.
Het tellen van een array begint vanaf 0! Het eerste item is dus item nummer 0.
console.log(typeof []); = het type van een array is een object.
array.push({object: "data"}); Dit voegt een nieuw object toe aan een array. Met .push, word toegevoegd als laatste.


### 9. Higher order function
array.forEach(function(student) {
	console.log(student);
})
//er word alle info van studenten weergeven
Dus een functie met daarin een functie is een higher order function.
In dit voorbeeld word er gebruik gemaakt van een method (forEach), methods zijn ook functions.
Methods: map/filter/reduce. Deze gaan over een array en returnen iets. Oproepen: array.map(function(){functie})
Map: returnd array met specifiek datatype. return student.name; //je krijgt: ["naam1", "naam2", "naam3"]
Filter: returnd array van wat true is, dus het hele object.     //je krijgt: [{name:"piet", age: 15}]
Reduce: returnd array van wat jij zelf wilt.
array.map(function(a){		//gebruik .map over een array, en voert voor elk element de functie uit.
	return a.name;		//return de naam van elk object.					
)}				//sluit de functie af.							
times.reduce(function(fastestTime, currentTime) {	//array van tijden, daarover gaat een functie die ze vergelijkt.
	if (fastestTime > currentTime.time){		//if die snelste tijd met huidige vergelijkt
		return currentTime.time			//returnt de huidige tijd als snelste tijd
	} else {					//else aanroepen voor als de tijd niet beter is
		return fastestTime			//als de tijd niet sneller is word de oude gereturnd
	}
}, infinity)						//tijd begint heel hoog zodat mensen lager kunnen (beginwaarde)


### 10. Scopes
Een globale variabele kan overal vandaan opgeroepen worden. Dus vanuit alle scopes.
Local variabelen zijn binnen hun eigen scope. Dus alles wat in een functie staat is daarbuiten niet te zien.
If is een block scope, een var kun je wel roepen van buiten een if statement. Let en Const is niet te roepen.
Vanuit een function kan je niet een var roepen.


### 11. Hoisting
Dit is een javaScript ding, en word niet in andere talen gebruikt. Hier doen we later wss weinig mee.
Variabelen en functies horen aan de bovenkant van je code, behalve als je gaat hoisten.
Wanneer je hoist roep je een functie als eerst aan, waardoor deze altijd beschikbaar is.
Je globaliseert de variabele, ookal maak je de var pas ergens beneden aan.
Hoisting is niet handig en niet echt toe te passen, behalve in speciale gevallen. Blijf er zoveel mogelijk bij weg.


### Xx. handig
"henk".includes("h"); = true, dus henk bevat een h. 
String("henk").length; = 4, dus er zitten 4 karakters in henk.
In een array kun je makkelijk objecten zetten, je kan ook makkelijk over een array loopen. (automatisering)
! = is not, dus met een ! kun je statements omdraaien.

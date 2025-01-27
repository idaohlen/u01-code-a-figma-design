# Individuell uppgift - Portfoliosida utifrån designskiss

[Uppgiften live på Netlify](https://idaohlen-u01.netlify.app)

## Sammanfattning av projekt

Jag har byggt en responsiv mobile first portfolio-sida efter en förutbestämd design med HTML och CSS som består utav flera undersidor.

Den huvudsakliga layouten på sidan är strukturerad med hjälp av flexbox, och jag har försökt att följa BEM-strukturen när jag satt namn på mina CSS-klasser, vilket varit ganska klurigt att komma på bra beskrivande namn till ibland. Jag har lagt till några mindre transitions här och där så att sidan ska kännas lite mer levande.

I base.css har jag lagt mina resets och definierat CSS variabler. Jag valde att dela upp variablerna i en sektion för sidans “palett”, och sedan definierat variabler för alla element som använder sig av färgerna i paletten så att jag har kunnat hitta allt på ett ställe istället för att scrolla fram och tillbaka i min CSS-kod varje gång jag behövt att ändra färger.

Sidan har en brytpunkt för mobil/desktop vid 896 pixlar, precis innan navigationen i headern bryter rader. Att lägga till en brytpunkt för tablet-bredd hade inte varit helt fel då sidan inte ser helt optimal ut vid den storleken, men den är fortfarande funktionell. Jag har satt en maxbredd för sidan på 1000 pixlar så att den ska se okej ut på större skärmar.

Jag implementerade först dark-mode genom att basera temat efter användarens systeminställningar, men bytte sedan ut detta mot en CSS-only lösning med en checkbox input. Jag fick strukturera om min HTML-kod för att kunna komma åt färgerna på alla element som jag ville ändra. Den “riktiga” checkboxen ligger direkt i `<body>` som en sibling till en wrapper som innehåller hela sidans innehåll, medans checkboxen man faktiskt klickar på är ett `<label>` element kopplat till checkboxen som ligger inuti sidans header. Detta gav togglen en inte helt optimal placering ur ett tillgänglighetsperspektiv när man t.ex. navigerar med hjälp av tangentbordet, så jag lade till några extra CSS selektorer för att highlighta `<label>` elementet när det är fokus på checkboxen.

Dark-mode knappen hör nog inte hemma inuti en `<nav>` tagg, men den lades till i efterhand när jag redan gjort HTML strukturen, så det skulle jag nog velat göra om.

Överlag är jag ganska nöjd med projektet, och slutresultatet är hyfsat likt referensen. Strukturen på listorna på “About” sidan skulle kanske kunna förbättras med en gridlayout så att det ser exakt ut som Figma-mallen.

## Teoretiska frågor

HTML är ett markup-språk som används för att strukturera innehållet på hemsidor, och har sedan år 2000 varit den internationella standarden för alla hemsidor på webben. Webbläsaren läser av och gör om HTML-kod till visuella element som text, länkar, bilder, listor och knappar. HTML är en fundamental del inom frontend då det lägger grunden för allt innehåll som ska visas på en hemsida. Utan HTML-dokument och kod finns det helt enkelt ingen hemsida för en besökare att titta på.

Byggstenarna i HTML kallas för taggar, och i och med HTML5 som släpptes 2014 introducerades det ett flertal taggar med ren semantisk innebörd för att göra HTML-kod dels mer överskådlig och lättförståelig för de som skriver och läser koden, men också dels för att förenkla för tillgänglighetsverktyg att kunna avgöra vad olika sektioner på en hemsida innehåller och förmedla detta till den som använder verktyget. Semantisk HTML är också viktigt för SEO, då det hjälper sökmotorsrobotar identifiera innehållet på sidan för att bättre avgöra vilka sökord som är relevanta. Så att skriva semantisk HTML innebär alltså att man använder sig av semantiska taggar så som `<header>`, `<footer>`, `<aside>` etc. för att beskriva innehåll i så stor utsträckning som möjligt och att göra detta på ett korrekt sätt.

CSS är ett stylingspråk som används för styra utseendet av HTML-element. Webbläsare har inbygga förutbestämda utseenden för alla HTML-element/taggar så att en hemsida ska kunna vara mestadels begriplig ifall CSS-stilmallarna inte laddar ordentligt.

CSS har en mycket viktigt roll inom frontend då det används till att ge hemsidor unika utseenden och designer. I och med den ökade populariteten av att använda färdigbyggda CSS-frameworks behöver en frontendutvecklare inte spendera lika mycket tid på att koda i CSS, men grunderna är fortfarande viktiga att kunna för att justera stilar när behövs och för att kunna manipulera en sidan utseende genom JavaScript, vilket kräver kunskap om vilka CSS properties man har att tillgå. Hur mycket manuell CSS en frontendutvecklare skriver kan alltså variera mycket beroende på hur de väljer att arbeta och vilka verktyg de vill använda sig av. För vissa lösningar funkar det bra att använda sig av frameworks som Bootstrap, Bulma eller Tailwind, medan för andra krävs det att man bygger stillmallar helt från grunden. Oftast krävs en sund mix av båda för att bygga hemsidor med bra kvalitet och på et tidseffektivt sätt.

***

## Använda resurser

### Ikoner

CSS-ikoner genererade med hjälp av [Iconify](https://iconify.design/). Ikonerna finns definierade i ```css/icons.css```. Vissa ikoner har sina brand colors, medans vissa använder current color.

För att använda en ikon, använd ett tomt ```i```-element med ikonens klass:
```
<i class="icon icon-[namn på ikon]"></i>
```

### CSS-lösningar

- https://cssgradient.io/blog/css-gradient-text/
- https://codyhouse.co/nuggets/css-gradient-borders
- https://alexandersandberg.com/articles/creating-a-website-theme-switcher-with-css-only/


### Bilder

- Ida Öhlén (profilbild)
- [publicdomainpictures.net](https://www.publicdomainpictures.net/en/)

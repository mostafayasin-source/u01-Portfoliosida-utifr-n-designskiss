# Portfolio utifrån designskiss

Det här projektet är en responsiv portfoliosida som jag har byggt från grunden med HTML och CSS utifrån en färdig designskiss i Figma. Webbplatsen innehåller sidorna Home, About, Technologies, Projects och Contact.

## Länkar

- GitHub-repository: <https://github.com/mostafayasin-source/u01-Portfoliosida-utifr-n-designskiss>
- Publicerad webbplats: **Lägg till länken här efter publicering**

## Reflektion

### Från skiss till kod

Jag började med att studera designskissen och dela upp den i återkommande delar, till exempel header, navigation, huvudinnehåll, projektkort och footer. Jag valde att arbeta mobile first. Det gjorde att grundstilarna först anpassades till en smal skärm och att desktoplayouten sedan lades till med en media query.

En svårighet var att översätta skissens proportioner till en flexibel webblayout. I början använde jag `width: calc(600 / 1600 * 100%)` på sidans container. Det gjorde bredden onödigt komplicerad och kunde ge olika eller för smala resultat. Jag ändrade därför containern till `width: 100%` tillsammans med `max-width: 1600px`. Då använder sidan hela skärmbredden på mobilen men kan fortfarande begränsas på större skärmar.

En annan utmaning var den responsiva headern och hero-sektionen. På mobilen ligger innehållet i kolumn, medan navigationen och hero-innehållet blir horisontella på större skärmar. Jag valde brytpunkten `900px` eftersom innehållet behöver tillräckligt med plats för logotyp, navigationslänkar och sociala ikoner. Brytpunkten valdes alltså utifrån innehållet, inte utifrån en särskild telefonmodell.

### Semantisk HTML

Jag använde semantiska element som `header`, `nav`, `main`, `section`, `article` och `footer`. Projektkorten och posterna för arbetslivserfarenhet är `article` eftersom de fungerar som självständiga delar. Varje sida har ett tydligt `h1`, och underrubriker använder `h2` och `h3` i en logisk ordning. Jag använde `div` när jag behövde en neutral behållare för layout och inget mer specifikt semantiskt element passade.

### Layout och responsiv design

Jag använde Flexbox i bland annat headern, hero-sektionen, arbetslivserfarenheten och länkarna i projektkorten. Grid används för teknologierna, verktygen och projektkorten. Grid-layouterna använder `auto-fit` och `minmax()` så att antalet kolumner kan anpassas efter det tillgängliga utrymmet.

Webbplatsen är byggd mobile first. Vid minst `900px` ändras headern från en vertikal till en horisontell layout, menyikonen döljs och hero-sektionen placerar texten och bilden bredvid varandra. Jag använde också relativa storlekar, `max-width` och flexibla mellanrum för att minska risken för horisontell scroll.

### Tillgänglighet

Jag har använt korrekta rubriknivåer, semantiska landmärken och `alt`-texter på bilder. Menyknappen har `type="button"` och ett `aria-label` som beskriver dess framtida funktion. Menyn ska göras interaktiv med JavaScript i nästa uppgift, så jag har inte lagt till en låtsasfunktion i den här HTML- och CSS-versionen.

Jag lade till `:focus-visible` för länkar och knappar och testade navigationen med Tab-tangenten. Fokusmarkeringen syns tydligt utan att vara beroende av muspekaren. Jag ändrade också telefonlänkens `href` till ett format utan mellanslag så att `tel:`-länken fungerar bättre.

Det som återstår före den slutliga inlämningen är att validera alla HTML-sidor med W3C Validator och testa sidan i Chrome, Firefox och Safari. Eventuella fel från dessa tester ska rättas och resultatet dokumenteras här.

### Användbarhet och UI

Jag behöll samma navigation på alla sidor så att användaren känner igen sig. Kontaktuppgifterna är klickbara via `mailto:` och `tel:`. Google Fonts används för typsnittet Poppins, och återkommande färger och typsnitt sparas som CSS-variabler i `:root`. Det gör designen mer konsekvent och enklare att ändra.

### Styrkor och förbättringar

Projektets styrkor är den semantiska strukturen, mobile-first-arbetssättet, återanvändningen av CSS-variabler samt användningen av både Flexbox och Grid. Jag har också arbetat med små, tydliga Git-commits i stället för att spara allt i en enda commit.

Med mer tid skulle jag ersätta återstående platshållarlänkar med riktiga projekt- och sociala länkar, finjustera avstånd och typografi ännu närmare Figma-skissen och genomföra fler tester i olika skärmstorlekar. Menyknappen ska få riktig funktionalitet i nästa uppgift när JavaScript introduceras.

### AI-verktyg

Jag använde Codex som stöd för att granska min HTML och CSS, förstå varför vissa problem uppstod och få förslag på mindre förbättringar. Ett exempel var förklaringen av varför containerns första breddberäkning inte var lämplig och hur en mobile-first breakpoint kan väljas utifrån innehållet. Jag skrev och ändrade koden själv, testade varje steg i webbläsaren och anpassade förslagen till projektet. Jag använde också Git efter varje logisk förbättring så att ändringarna blev tydliga i historiken.

## Återstående slutkontroll

- [ ] Lägg in länken till den publicerade webbplatsen.
- [ ] Validera samtliga HTML-sidor med 0 fel.
- [ ] Testa i Chrome, Firefox och Safari.
- [ ] Kontrollera tangentbordsnavigation och synlig fokusmarkering en sista gång.
